---
title: "Version control second coming"
date: 2026-09-01
draft: false
build:
  list: never
  render: always
  publishResources: true
sitemap:
  disable: true
---

While we all stopped coding manually around December 2025, something else was cooking: the biggest revolution in version control since 2005\.  
Two big pushes happening simultaneously: the need to handle a much higher commit pace due to agents, and a sudden urge to replace GitHub.  
I’m going to reflect about these two forces plus what we can probably expect in the near future from version control as it both adapts and supports new ways of developing software.  
Having spent my career in version control, what I can share is that I haven’t seen a more exciting moment since 2005, when distributed version controls landed.

# The fall of the giants

If only 2 years ago somebody said GitHub would be no longer relevant soon, nobody would believe them. GitHub was the undisputed leader in repository hosting, and it also shaped the way developers thought about version control. Having spent too much time as a competitor (more about that later) I suffered that: if something was different than what people understood it was ‘the way GitHub does things’ it was probably wrong.  
GitHub is still gigantic in both repos and minds, and its impact in the world of software development and collaboration in general has been enormous, and most likely it will continue to be.  
But if you have been around long enough, you probably remember there was a time when nobody would bet against SourceForge, and only a couple of years later, with the rise of GitHub, it became largely irrelevant.  
Are we living now in the same transition moment? GitHub has done too many great things over the years, so I hope it remains, but there is obviously an earthquake going on.

# My life in version control

If you’re reading this chances are you know I co-founded Plastic SCM, the version control that is not Git, back in 2005\. It was all about performance and gigantic repos, and it was acquired by Unity in 2020\.  
The first version control I used, though, was Visual Source Safe, in my first official job after university, back in 2000\. Known as VSS it has been one of the most blamed version controls ever, but perspective taught me that it had some pretty good things too: extremely simple, and very easy to share files among projects, something probably yet not resolved.  
A few months later I had the chance to put my hands on Clearcase, by then acquired by IBM, when I joined Sony in Belgium to develop digital televisions. I was shocked at first, but Clearcase blew my mind. It had incredibly good branching and merging, virtual filesystems, and it was extremely flexible. I used it mostly from a Sun workstation, and I was lucky not to touch its “simplified” version back then (which in my opinion helped to kill it, since it shaved most of its power).  
Clearcase was extremely expensive, my memory tells me something around 5k/year per user for an enterprise setup.  
The version control bug bit me hard. Wouldn’t it be amazing to have something as powerful as Clearcase but more affordable so small companies could use it too? Then I learned Subversion and CVS, and even Perforce (which is still THE solution for many large game dev teams and chip makers).  
We started Plastic SCM in summer of 2005 after more than one year trying to create a business plan pitching potential investors.  
After that, I saw a good number of version controls come and go: Accurev was a fantastic solution we competed against many times, and it is now largely gone. Team Foundation Server from Microsoft, Jazz from IBM (trying to replace Clearcase), Serena, and many others that are hard to hear from anymore.

# 2005 was the last big explosion

Circa 2025 there was a race to win the versioning of the Linux Kernel. Bitkeeper had to be replaced (it is a story on its own) and Mercurial, Darcs, and a few others wanted to win that crown. To be honest, my dream when I was trying to get Plastic SCM started was also to version the Linux kernel. In my head it looked fantastic, little I knew a commercial product would never be even remotely considered for that. But only if you are naïve enough you would start a new version control, I guess.  
As I remember it, Git was announced the very same week we got our first ever angel investor signed, in early summer of 2005\. The fact that Linus Torvalds himself was creating such a system made me think the road ahead was going to be harder than I had anticipated.  
Git was a revolution, and a little bit later, around 2008, GitHub brought it to the masses and the rest is history.  
It was incredible to see the new systems coming around that time, Git and Mercurial being probably the two most heavily adopted.

# The second explosion

By the end of 2025 I had the luck to talk with some different teams developing new version control solutions. With some of them I already had contact for a long time, and others were new to me, but the thing I started to perceive is that obviously something was going on.  
Nobody dared to challenge GitHub supremacy, but now startups here and there were trying to create “the next GitHub”.  
I’m sure I’ll forget some very relevant initiative, but here go the key ones I was more excited about.

## Entire

Everybody was shocked when the former CEO of GitHub announced a gigantic seed round for his new venture, a new version control system solution based on Git.  
They have released *provenance tracking* to basically know what code which agent created and which prompt, which I believe is going to be a must in how we handle version control, and also a number of performance improvements (like super fast clones thanks to distributed replicas worldwide). 

## Pierre

Visiting their website is an experience by itself (not sure how long this will last) because it is quite different to anything else. Pierre has released better diffs and better trees, open source, so anybody can empower their code UIs with them, but then focused on code.starage, their Git forge for the agentic reality.  
GitHub hit a wall in terms of performance when dealing with an incredibly high increase of commits, PRs, and traffic in general, and code.storage positioned itself as the solution for all platforms using repositories underneath, at AI scale.  
In recent posts in X they unveiled how Lovable and other massive AI solutions rely on their system to handle repositories.  
It is, definitely, one of the most promising Git based solutions out there.

## Origin

It was the last I heard about, but when I did I really realized something big was happening in the industry. Cursor (now SpaceXAI) working on their own Git forge too? Amazing.  
Origin is also a full Git forge, with a full solution for pull requests, repo hosting, etc, and has focused on performance and reliability so far, but like all the other Git platforms, this is just the start of a quite exciting trip.  
My friend and colleague Vmg posted an incredible writing about origin internals ([https://cursor.com/blog/git-at-any-scale](https://cursor.com/blog/git-at-any-scale)) that spiked an ‘WAL S3’ discussion on X for a few weeks. People like Scott Chacon and Tobias Lütke implemented their own versions in the next few days, inspired by Vmg’s post.  
Disclaimer: I joined the Origin team a few months ago to work full time again on version control internals, this time instead of racing against Git, I’m trying to make it as fast as I can.

## GitButler

Scott Chacon’s new version control venture has been around for a few years already, but they are now positioned as “version control for your agents”, which elaborates more in the same trend, although with a different approach.  
So far GitButler is not *a new forge* but focused more on the client side, with radically different user experience concepts, a focus on performance.  
Stacked branches (we all need them in my opinion), better rebasing and as I mentioned, innovative ideas they explored like ‘virtual branches’ makes them part of the cutting edge in Git evolution.

## East River Source Control \- [https://ersc.io](https://ersc.io)

The first ones in my list that are not creating something around Git… but around Jujutsu.   
I had the chance to talk a few times with the version control team at Google (and I always enjoy every minute of the conversation, they are so next level, specially in something I love which is super gigantic monorepos) and they put me in touch with this team, who is bringing Jujutsu to the market.  
Jujutsu was started at Google by Martin von Zweigbergk (who I also have the privilege to be in touch with) as a successor to Git. It brings innovative ideas like stacked branches, and goes beyond that versioning even unsolved conflicts in the repo, which opens up new previously impossible opportunities.  
Rearranging commits, reapplying changes (pure stacking) becomes a totally different experience.  
Jujutsu can work on top of Git, but internally at Google they use a different backend, and ersc tries to bring that idea to the market. You lose part of Jujutsu’s extra power when you push to GitHub, and a native backend would change that.  
I expect a lot of evolution coming from the Jujutsu land, not sure if native or transplanted to Git or other version controls.

## Diversion

I’ve been collaborating with Diversion for over three years now as an advisor. They have been around for a few years now and they are also not based on Git. At first they reminded me a lot of my old days at Plastic SCM, fighting Gits here and there with a totally different stack.  
Their approach is quite different, though, and I think this is what makes them so relevant in this ‘version control revolution’: they have been born in a post-decentralized world. I was in love with the fact of pushing/pulling to remote repos, and in fact in version 2 or 3 of Plastic (around 2008\) we made it “distributed”, so Plastic was able to work fully centralized (SVN style) and fully distributed, combining both modes in the same repo when needed. I was in love with this flexibility.  
But distributed, as amazing as it is, was born in a different world. Now you always have a decent internet connection, even when on a plane. What is the point of committing locally then pushing?  
I focused on large repositories like Diversion does, and found it was a key differentiator for game developers. Game dev teams handle repos of \> 1TB, with millions of files. At that size, having local clones is simply a no go.  
Even more, the fact of ‘commit then push’ was a drag in many professional environments, so many people just wanted to commit to central, period.  
This is what Diversion excels on, but it can’t be seen as a “back to the days of Subversion” because it comes with much better performance, full cloud deployment, excellent branching and merging (the things on Git that really distilled) and more.  
Diversion introduces cloud-first workspaces, fully versioned on the server side, which opens up new ways of collaboration and, while different, reminds me a lot of things that Jujutsu can do.

## Oxen.ai

It is a bit harder to realize now on their site that they do version control for large AI datasets. I first contacted them while I was collaborating with Activision in version control (of course) because if they are able to deal with gigantic datasets, game scenarios wouldn’t be such an issue.  
I had the chance to meet their founders in person and I really liked the team and their *familiar* architecture, which resonated with me (lots of super fast low level operations to make the system fast).  
Oxen is not in the same *forge race* as the others, but they are a good example of the fact that the market is evolving more than it did in the previous two decades.

## Lore\!

To build on the excitement, even Unreal released their open source version control, Lore, with an eye on the large monorepos/gaming industry. It is a complete full stack, not based on Git, which makes it very different and exciting. It shares an underlying DAG (directed acyclic graph) like Git, improvements to deal with big binaries, optimized data transfer based on modern algorithms to patch only what changes and avoid unnecessary downloads… and while it looks centralized to me, it seems it can also work disconnected.

# What to expect in the coming future

I described part of it when I covered Diversion, because I really think some of the challenges teams will face will be large monorepos receiving commits at a super high pace.  
When Microsoft tried to land Git in the Office team, they first developed a virtual filesystem (which is the type of solution I truly love) to fight the distributed nature of Git, which was a shortcoming in large repositories. When file counts are in the many millions, Git normal layout doesn’t help. They dropped the vfs and “git scalar” was born, now helping big repos everywhere.

## A solution for (super) large monorepos

I’m not sure if the many Git forges will evolve in this direction, but big monorepos receiving tons of contributions per second will certainly be one of the areas of future version control.  
Maybe we’ll see an evolved Git cover this (different from what it is today if the foundation can’t be adapted), or maybe a totally different stack (Diversion, Lore, Oxen?).

## The fall of distributed

My bet is that distributed with push/pull instead of simply commit will be limited by repo sizes, so after some threshold (maybe repos \>300 GB and 1 million files) the industry will need to look at solutions that have existed in version controls not based on Git. I believe that probably we’ll see (AI can do this smoothly) custom forks of Git addressing some of this, and probably the “Git” in 2-3 years will be radically different to the one that we see today, unless the industry is brave enough to adopt a radically different paradigm.

## Super fast commit speed

Right now committing to main on Git forges requires some serialization, so there is a limit in the speed of those commits. Google broke this barrier with their internal Piper solution (which backs Jujutsu) years ago, and I think we’ll see solutions revisiting this idea.

## Virtual files systems everywhere

This is definitely more a dream than a prediction, because I love the idea of working with a fully virtual file system that hydrates the files I need from the monorepo on demand, allows me to have unlimited copies of my repo locally with virtually zero cost (copy on write) and greatly improves usability and overall experience. I first saw that 25 years ago in Clearcase (the Xerox Park of version control to me) and developed a version of that for Plastic, and I saw it is used by the industry giants and many large game developers.  
There are some barriers for this to happen, though: first is macOS, which makes it virtually impossible to develop fast virtual file systems (I’ve done experiments on Linux and Windows with extraordinary performance, but no way on macOS). Second that maybe agents hide the underlying complexity that much that we no longer care… but speed and disk size would still matter.
