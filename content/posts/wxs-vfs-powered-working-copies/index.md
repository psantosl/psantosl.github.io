---
title: "wxs: VFS-powered working copies"
date: 2026-02-14
draft: false
_build:
  list: never
---
<link rel="stylesheet" type="text/css" href="https://unpkg.com/asciinema-player@3.9.0/dist/bundle/asciinema-player.css" />

Working PoC of a virtual filesystem that manages version control workspaces.

`wxs create` gets the tree (directory structure + metadata) so the workspace is browsable immediately. File content is fetched on demand when read, while a background prefetch warms the cache.

<div id="demo"></div>

Duplicating a workspace is near-instant. All workspaces share content through a content-addressable store with copy-on-write — only files you actually modify take extra disk.

This matters for agents: each task gets its own isolated workspace without multiplying storage.

<div id="demo2"></div>

4 workspaces of VS Code (9,304 files each), 27 MB total instead of 555 MB:

```console
$ wxs list
NAME      STATUS   BRANCH  FILES      SIZE  PRIVATE  PATH                      REPO
vscode00  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode00  https://github.com/microsoft/vscode.git
vscode01  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode01  https://github.com/microsoft/vscode.git
vscode02  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode02  https://github.com/microsoft/vscode.git
vscode03  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode03  https://github.com/microsoft/vscode.git

CAS: 27.8 MB on disk for 4 workspaces (555.7 MB without dedup, 95% saved)
```

Each workspace is a real filesystem mount. Standard git commands work inside it — no wrapping, no special workflow. `git status` runs in 35ms thanks to the built-in fsmonitor daemon watching the VFS.

```console
$ wxs info vscode00
vscode00
  Mount:    /home/pablo/wxs/vscode00 (mounted)
  Repo:     https://github.com/microsoft/vscode.git
  Branch:   main
  Commit:   d057f3f567de
  Files:    9304 (138.9 MB)
  CAS:      27.8 MB on disk, 138.0 MB decompressed (shared by 4 workspaces)

Git Repository
  Path:     ~/.wxs/repos/58f0899a002beabc (54.1 MB)
  Clone:    shallow (depth=1)
  Branches: 1
  Objects:  1 pack (25.9 MB)
  Remote:   yes
```

Workspaces track both version-controlled files and private files (build output, temp files). Git is the first backend but the VFS core is SCM-agnostic — the same architecture can support any version control system that provides a tree and blob fetching.

## What's next

The PoC proves the core: VFS-backed workspaces with shared content and copy-on-write. Here's where it goes from here.

**Automatic snapshots.** The VFS sees every write. That means it can snapshot workspace state at any point — before a build, before an agent run, on a timer. Rollback becomes trivial. Branch from any snapshot to explore alternatives.

**Cache servers.** Content-addressable storage makes caching straightforward. A local or regional cache server can warm up blobs ahead of time, making workspace creation near-instant even for massive repos.

**Auditing.** The VFS layer intercepts every file operation. That's a full audit trail for free — what was read, what was written, when, by which agent or process. Useful for compliance, debugging agent behavior, or understanding how a codebase is actually used.

**Cloud sync with snapshots.** Sync workspace state to the cloud, snapshots included. Pause work on one machine, resume on another. For agents, this means migrating a task mid-execution without losing filesystem state.

**Workspace templates.** Define content that isn't in version control but should be present in every workspace — test files, large assets from external storage, game art. Templates make workspaces reproducible without polluting the repo.

**Quick workspace sharing between machines.** Because workspaces are just metadata plus a content-addressable store, transferring a workspace between computers means syncing a small manifest and letting the target machine fetch only the blobs it doesn't already have. Moves a multi-GB workspace in seconds.

**Universal VCS layer.** A common interaction model for all version controls, making it much easier to switch or adapt. Also provide massive scale for teams with large monorepos without having to develop the infra themselves (like many big players had to do).

**A new filesystem standard for development**. The same FS semantics can be available for macOS, Linux and Windows.

<script src="https://unpkg.com/asciinema-player@3.9.0/dist/bundle/asciinema-player.min.js"></script>
<script>
  AsciinemaPlayer.create('00-create-first-wk.cast', document.getElementById('demo'), {
    fit: 'width'
  });
  AsciinemaPlayer.create('01-copy-wks.cast', document.getElementById('demo2'), {
    fit: 'width'
  });
</script>
