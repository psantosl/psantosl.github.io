---
title: "Plastic SCM vs Git"
date: 2018-03-15
draft: false
---

> *This post was originally published on [Medium](https://medium.com/@psluaces/plasticscm-vs-git-c17934fad7ed).*

(Este blogpost está disponible en Español [aquí](https://medium.com/@psluaces/plasticscmvsgit-e226ff50c01)).

There is a question I can’t seem to avoid every time I go to a meetup or attend a conference: how is Plastic different than Git? Sometimes is asked out of mere curiosity, other times it is a statement of “how dare you compete against the dominant version control software made by Torvalds himself?”

Sometimes, it seems like someone is offended by seeing a small group compete against “THE” dominant system that it is now supported by multinational companies like Atlassian, Microsoft, GitHub, and GitLab, among others.

Well, that’s what I’m going to explain right now; what makes Plastic different than Git? What makes +2500 developers companies go for Plastic? What prompts small game studios, big ones, insurance, health care, aerospace and automotive companies choose Plastic? Did they all go crazy?

![](./1.png)

Us versus the rest of the Empire

### Real branches

The first difference revolves around the concept of branches. Plastic branches are changeset containers (commits in Git jargon). Git branches are just pointers to a given commit.

What does this mean? It means that Plastic branches match what you have in your head; a line of work full of checkins. A changeset, as we call it, can’t be in more than one branch; it belongs to a branch. It can’t be easier.

Meanwhile, in Git you must adapt yourself thinking in pointers. And, very often it is not easy to figure out where a commit was created. In fact, it is not even important in the Git-way-of-thinking. You might say, ok, who cares! But, wouldn’t you like to see heritage and immediately understand per task where lines were touched without having to rely on commit messages? This is what Plastic-style branches are all about; a mapping of one-to-many branches in a changeset. For example:

![](./2.png)

Git vs Plastic branches

Additionally, deleting branches is very common in the Git world, simply because they blur the entire picture. Deleting branches is very uncommon in Plastic. To be honest, many teams delete branches in Git because most GUIs crash immediately if you try to open a repo with more than 2k branches. (The CLI can cope with that, though). So, if you stick to a branch per task, as we recommend you do with Plastic, you can have repos with 10k, 20k or more branches… and this is not a problem at all in Plastic; it is \*your\* history.

As I said earlier, in Plastic you always know where a changeset was created, while in Git, is almost impossible to tell:

![](./3.png)

Does this really matter? Well, the difference is all about full traceability and ease of use. Every single Git instructor I have ever spoken to has told me that he must figure out how to make students think in terms of pointers and not branches as they used to. All this is much more intuitive in Plastic. Branches as you expect. That’s all.

### Work centralized

You can have your local repos in Plastic and work distributed, as you do in Git. But, you can also work in Subversion-style: a local working copy and direct checkin to the server, without intermediate push/pull. You can’t do that in Git. By design, you need a local repo.

How important is this flexibility? Having a local repo is incredibly useful for many, they love it, but it is a nightmare for others. It is “checkin and done” versus “checkin and then push”.

Generally speaking, artists in videogame studios prefer to work centralized. They expect the version control to do its job and not get in their way. When we refer to artists, we mean everyone that is not a programmer in a game studio: game designers, animators, 3D artists, and so on.

Interestingly, we also find many coders who use blazing fast networks and then simply prefer to work centralized. Plastic is not like SVN. It is super-strong with branches and merges, [even stronger than Git](https://www.plasticscm.com/mergemachine/index.html). Thus, working centralized doesn’t remove the branching powers. Just remember that for many, Git is all about branching/merging, and working distributed is almost a price to pay.

### Plastic doesn’t cringe with huge repos

We have customers with +5TB repos. You simply can’t do that with Git. Ok, a few days ago we were in #gitmerge 2018 with some GitHub/Lab developers and they said, “Repos shouldn’t be that big. If they are it is because there are too many files that shouldn’t be there”. Well, if you are on a game project, automotive design project and many others, you do deal with big graphic, document, and video files. You could tell your customer “go put your code in Git and binaries in… Dropbox!?” but, to be honest, many won’t be happy with that. They want a system to solve problems, not to create more.

In Plastic, you can simply checkin big files and you’re done. It doesn’t break. It doesn’t slow down. It doesn’t require workarounds like Large File Storage. (Something many users complain about.) **Plastic is designed to handle everything you throw at it and work. No drama.**

This allows us to work with lots of different game studios. They can be big ones with +300 artists like at Telltale, or small indie groups but with large projects.

The same size friendliness applies to our Cloud solution; GitHub kindly asks you to remove your repo as soon as it grows over 2GB. **The average repo in Plastic Cloud is +50GB**.

### Version directories and moves

This is another big difference based in the underlying design and it is rather easy to explain. If you go and rename a directory in Git containing 1000 files, you get 1000 file moves. If you do the same in Plastic, you get a directory renamed. It is easier to understand. I mean, seriously, the Git solution is painful. It is a headache more than the solution you would expect from your version control.

We do pay a price: versioning directories complicates our implementation. But, it allows us to precisely track moves and renames, which will repeatedly save your life during complex diffs and merges.

### Visualization and GUIs included

I often take visualization and GUIs for granted. We have been working on them for so long that I tend to forget how important they are.

When you install Plastic, you get a very complete graphical user interface. It is super-visual. I’m not going to add screenshots here, but you can go to our [gallery and check some out](https://www.plasticscm.com/gallery.html). Also, one of the [key visualization features is our Branch Explorer](https://www.plasticscm.com/branch-explorer/index.html) which turns repo visualization from a nightmare to something very natural and easy.

At the end of the day, it is a huge amount of work for our team to take care of the full stack. We work on the server, on the command line, we develop the GUIs, third-party integrations, everything. But, the result means consistency. Much more than what many Git tools do, since they tend to be just command line wrappers. I mean, some even say “error, merge detected” before processing a merge. It is intimidating, isn’t it?

In Plastic, we also [include merge tools](https://www.plasticscm.com/features/xmerge.html) (with code move detection, something rather unique), so you don’t have to rely on unified diff or install Kdiff3. It also includes side-by-side diff, something not included by many Git GUIs even 12 years after Git was first released.

And we top off the package with unique features like “[semantic version control](https://www.plasticscm.com/features/semantic-version-control.html)”.

### And Plastic speaks the Git language

Every Plastic client can push/pull to a Git server. Every Plastic server can act as a Git server and handle push/pull from Git clients. (Who think they are talking to a regular Git daemon). It is [all covered here](https://www.plasticscm.com/features/plasticscm-for-git-users.html).

Git interoperability gives great flexibility for teams moving to Plastic from Git, or where they need interaction with other teams still on Git.

### Wrapping up

As I told you at the beginning, the question “how does Plastic compares to Git” is something I’m asked very frequently, so hopefully I wrote a good answer :)

It can be summarized as:

· Branches are easier to understand,  
· Merges are even more powerful,  
· Big repos and big files,  
· Visualization.

So, if you are a Plastic fan, I hope now you have a good weapon to defend yourself with from the attack of the next git-stormtrooper ;-)
