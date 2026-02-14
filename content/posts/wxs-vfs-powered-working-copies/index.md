---
title: "wxs: vfs powered working copies"
date: 2026-02-14
draft: false
_build:
  list: never
---
<link rel="stylesheet" type="text/css" href="https://unpkg.com/asciinema-player@3.9.0/dist/bundle/asciinema-player.css" />

This is a virtual file system to handle version control working copies (workspaces).

Creating the workspace takes no time because it just does a fast clone and gets the blobs later.

But users and agents can immediately access the workspace because while the prefetch finishes, blobs can also be downloaded on demand.

<div id="demo"></div>

Duplicating workspaces (to work on multiple branches, something key for agents) is blazing fast, as you can see in the following video.

This is because there is an underlying cache for all workspaces, so they all share the same data. Users (and agents) see multiple directories, but they all share the same data (with copy on write to diverge).

<div id="demo2"></div>

Check the wxs list command:

```console
$ wxs list                                                                                
NAME      STATUS   BRANCH  FILES      SIZE  PRIVATE  PATH                      REPO                                    
vscode00  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode00  https://github.com/microsoft/vscode.git 
vscode01  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode01  https://github.com/microsoft/vscode.git 
vscode02  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode02  https://github.com/microsoft/vscode.git 
vscode03  mounted  main     9304  138.9 MB        -  /home/pablo/wxs/vscode03  https://github.com/microsoft/vscode.git 
                                                                                                                       
CAS: 27.8 MB on disk for 4 workspaces (555.7 MB without dedup, 95% saved) 
```

4 workspaces mounted in no time, but they all use just 27 MB instead of 555 MB.

This is the extended info for one of the virtual workspaces:

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

Each workspace can track version controlled files and also private files (build output, temporary files, etc)


<script src="https://unpkg.com/asciinema-player@3.9.0/dist/bundle/asciinema-player.min.js"></script>
<script>
  AsciinemaPlayer.create('00-create-first-wk.cast', document.getElementById('demo'), {
    fit: 'width'
  });
  AsciinemaPlayer.create('01-copy-wks.cast', document.getElementById('demo2'), {
    fit: 'width'
  });
</script>
