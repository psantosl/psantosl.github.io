---
title: "I've tracked 44,000 rows of my life since 2014"
date: 2026-02-13
draft: false
---

I think most people can't tell you what they did last Tuesday. I'm afraid I can tell you what I did on most Tuesdays since June 3rd, 2014. Every hour, every project, every break, every meeting, every late-night rabbit hole.

I have about 44,000 rows in a spreadsheet where each one is a block of time — when it started, when it ended, what I was doing (categories: work, personal, code, meeting), and a short note. Over eleven years and mostly no gaps.

I realize I haven't talked about this habit often. When I did, I guess my friends thought I was crazy. And they are probably right: I know *exactly* how crazy — 44,000 rows of crazy.

Here's what I think those rows taught me.

## The spreadsheet started with a nagging feeling

Back in 2014, I was running a software company (Plastic SCM, a version control system — later acquired by Unity Technologies).

I was a big fan of software estimation back in the day, so I wanted to have a full database of project estimations and their actual times, so we could compare. Then, as soon as you have data, you can say 'this new project will take as much as this other one' and you have quite accurate numbers to create a range for best case, worst case, and most likely case (all about this in the great book ["Software Estimation: Demystifying the Black Art"](https://books.google.es/books?id=U5VCAwAAQBAJ&printsec=frontcover&redir_esc=y#v=onepage&q&f=false).

But I had this persistent feeling that I wasn't accomplishing enough. And the 'number of hours per task' were not enough telling me what I could improve. I suspected interruptions were eating me alive, or maybe it was lack of focus, but I couldn't prove it. So on June 3rd, I opened a spreadsheet and started logging: start time, end time, what I was doing, and a short note.

I wanted to move away from just sensations and into real data.

The data was shocking. I'd think "I worked on that feature almost all day, at least six hours" — only to look at the data and find 3.5 hours, split into several chunks. The interruptions were real, and now I could see them, but also I spotted meetings, planning, and many 'other' unnamed things that could take a good chunk of the day.

So, the actual 'worked hours' in the issue tracker we used to trace everything started to go down in my case, more adjusted to reality. Much later some of the core team members started to do the same, all private for themselves except the actual real hours they'd log in the system, so we started to have quite accurate data.

Besides 'worked hours for real' I started making decisions and changes: too much time on meetings, too little time in marketing, less time coding than I actually expected... and adjusted accordingly.

## Going personal
I started logging just work but soon I began adding personal notes, sometimes thoughts. It's easy when you're in front of the computer. Harder when you're not — and I don't pretend every minute is tracked. But I kept going. The beautiful thing is that sometimes you have clear notes of a meeting (that for whatever reason you didn't track elsewhere), decisions made, when you went to that place with the family that nobody really remembers exactly, etc.

I didn't add thoughts initially, but it is probably one of the most rewarding things to keep, because then you go back in time, and remember exactly how you were feeling, which is (like in a normal diary) quite therapeutic. You took that decision because of something, and 4 years later you just remember the good things, not the bad ones ... and that note makes you understand why you did what you did.

Over a decade later, I have a dataset about my own life that most researchers would envy :-P

## What 44,000 rows actually looks like

Each row has five fields:

- **Start time**
- **End time**
- **Type** (work, personal, health, learning, etc.)
- **Subtype** (the specific project or activity)
- **Notes** (what I actually did)

That's it. No mood scores, habit checkboxes, or gamification. Just: what did I do, and for how long?

Probably the simplicity was the point. Anything more complicated and I would've quit in month three.

## The things I learned

### A bit of data helps you steer your day

When I was spending too much time in meetings of course I had the feeling that the day wasn't productive, but when you see the numbers, you 'game it' a bit to try to reduce that and focus on what is more relevant the next day.

At one point down the road, I think it was 2017, after years of SCRUM, me and some key team members were spending too much time in 'planning'. There were reasons for that and by the way we were probably doing SCRUM wrong, but this metric (together with reducing 'cycle time', my favorite) helped us look for alternatives and we [landed into full Kanban](/posts/from-scrum-to-kanban-how-we-delivered-tasks-twice-as-fast/) a few months later.

Not magic, btw, but it helps seeing the picture.

### You don't spend time as you think

This was the very first lesson. I shared it before, I'd finish a day thinking "I spent at least six hours on that feature." The rows said 3.5, split across several chunks with meetings and interruptions in between.

It happens every time. In my most productive periods, I average about 6 hours of real, focused work per day. If you asked me to guess without the data, I'd have said 8-9 hours easy. Days with 8h of real work on tasks meant many more hours than that 'at work'.

By the way, as a team we never tracked 'presence time' but 'real time' and it also helped us correctly budget iterations. We knew more than 6h 'focus time' was impossible, and we shielded the team (no crazy meetings mid morning or mid afternoon) to achieve that. When we moved to Kanban that changed a bit because we stopped 'estimating sprints' but some core ideas persisted.

### Fewer entries = better day

The rows make it visible: the best days are the ones with the fewest entries. Fewer entries means bigger chunks of uninterrupted work. Days where I bounced between four different things have lots of short entries and fewer total productive hours. Days where I did one or two things have a few long blocks and way more output.

My most productive weeks are monotonous. One big project, deep focus, long blocks. My least productive weeks look "busy" — lots of variety, lots of switching. The row count tells you which kind of day it was before you even read the notes.

### The data shows you what running a company actually looks like

In 2018, I was CTO of Plastic SCM, but as a founder you just jump into whatever is needed. If you'd asked me what I spent most of my time on, I'd have said "marketing and product." The data told a different story.

Here's my actual work breakdown for that year — every category, measured to the minute:

| Category | Hours | % of work time |
|---|---|---|
| Marketing | 290h | 15.4% |
| Planning | 172h | 9.1% |
| Dev tasks | 148h | 7.9% |
| Support | 134h | 7.1% |
| Analysis | 126h | 6.7% |
| Dev meetings | 108h | 5.7% |
| Documentation | 90h | 4.8% |
| Unproductive | 81h | 4.3% |
| Product | 69h | 3.7% |
| Travel | 62h | 3.3% |
| Training | 62h | 3.3% |
| Email | 60h | 3.2% |
| HR | 51h | 2.7% |
| Everything else | ~230h | ~12% |

Marketing was the single biggest category — and it was only 15% of my time. The thing I considered *the* key activity barely got a sixth of my hours. Meanwhile, I spent 81 hours on things I classified as "unproductive," 60 hours on email, and 51 hours on HR. Running a company is death by a thousand small tasks, and you don't see it until you measure it.

This data changed how I structured my weeks. It's one thing to feel scattered. It's another to see exactly how scattered you are, in a table with percentages.

### The data survives career changes — and gets more useful

Unity acquired Plastic SCM in 2020. I stayed till early 2023. Then I shifted to consulting and advising — by end of 2023 I'd taken on a startup advisory role, then another in 2024, and eventually got hired by a big game developer studio to help with their version control setup.

For the past two years, I've juggled three clients plus side projects. And I can tell you exactly how much time each client got. How many hours on reports vs. meetings. Which weeks a client dominated and which ones got neglected.

When your career changes shape, the data adapts with you. The same rows that told me I was spending 15% of my founder time on marketing now tell me whether I'm giving each client what they're paying for.

### The diary is the unexpected gift

I started tracking time to understand where it went. The diary came free, quite naturally.

Because every row has a note — even a short one — I accidentally created a searchable record of my life. I can look up any day and remember what I was working on, what I was struggling with, what I was excited about. I started just with work-related stuff, but a few months later I was taking personal notes too, even about things like outdoor activities, holidays and such.

A spreadsheet isn't a journal but 44,000 annotated moments, stacked one on top of another, turns out to be something real close.

---

## Why I built it into a product

For over a decade, my "app" was a spreadsheet — first Excel on Windows, then Excel on macOS (I switched to Mac in 2021 to dogfood my own version control system), and eventually Google Sheets. It worked but it wasn't really enjoyable. I squeezed stats out of pivot tables, which got the job done but wasn't exactly elegant. No way to print a yearly diary. No way to spot patterns without manually wrangling pivots every time I had a question.

So I built [rows.life](https://rows.life) — the tool I wished I'd had from day one. It's a time tracker that's also a journal. You log rows (just like my spreadsheet), and it turns them into statistics, insights, and a printable diary.

It has zero-knowledge encryption (your notes are encrypted in your browser before they leave your device), full data export (your data is yours), and the analytics I spent years wishing my spreadsheet could do.

I'm not going to pretend that everyone needs this. Most people don't want to log every hour. That's fine. But if you're reading this and thinking "I already do something like that" or "I've always wanted to try" — this is for you.

---

## The real takeaway

Over a decade of data taught me that time is the one resource we're all terrible at estimating. We overcount our work. We undercount our rest. We don't notice the patterns that shape our years.

You don't need 44,000 rows to start noticing. You just need a few weeks of honest tracking.

The spreadsheet won't judge you. It'll just show you the truth. And the truth, it turns out, is more interesting than you'd expect.

---

## Bonus: maybe I was always going to end up here

If I'm honest, this didn't really start in 2014. My first computer was an Amstrad PCW 8256, and one of the first things I built on it was a program to track my bicycle rides. Distance, time, routes — a kind of Strava, except it was 1990-something, there was no internet, no GPS, no automatic syncing. Just me, typing data into a machine after every ride. I even sold a few copies through a magazine ad.

Around the same time, I remember watching Doogie Howser type his diary into his computer at the end of every episode. That image stuck with me — the idea that you could close each day by recording what it meant. Doogie was [basically blogging before blogs existed](https://doogiehowser.fandom.com/wiki/Personal_Journal_of_Doogie_Howser,_M.D.).

I later spent my career building version control systems — tools that track every change in source code. Looking back, there's a thread: version control tracks changes in code, rows.life tracks changes in life. I've apparently always needed to measure things. Maybe it's just how my brain works.

---

*[rows.life](https://rows.life) — Track your time. Remember your life.*
