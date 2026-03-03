I'm an occasional track day driver and rider. I'm not any good at it, but I enjoy track days. I've done a bunch over the last few years, specially with motorbikes. And, of course, same as I don't feel good doing mountain bike without tracking it to Strava, no track day goes without all possible telemetry recorded somewhere.

And the 'somewhere' was the problem. There's a bunch of dedicated hardware devices and apps (called lap timers) out there. I've used an AIM Mychron5S for years now, and also apps like the fenomenal Harry's Laptimer and lately I switched to RaceChrono since I prefer it while on track. I also purchased the fantastic Racebox Mini, a 25hz GPS you can plug to your phone to get really accuarate data.

The problem is that each lives in its own world, and it is far from easy to simply have a place to record all your laps... compare with others... and try to figure out how to get better without actually enrolling in a master's degree. And that's why I started creating... laps.racing with the help of some friends.

## How many laps have you done this year?
Not that it is life changing, but it is always great to know how much actual time you put on track after all the money spent in the vehicle, equipment, track day fees and more. Here goes mine for 2025.

[link to 00-totals.png]

These kind of stats are straightforward once you upload all your data, from different devices, to a single place that can read them and crunch some calculations.

While I still have to upload a few more, so far my totals ever seem to be 1784 laps, totalling a bit less than 3600 km. I need more track time.

## Listing your track days and sessions
Pretty basic too, but so good to just have it a single place:

[insert 01-my-dashboard.png]

And from there you can go and see the details of the track day.

All the sessions, and then all the laps for each session.

## Details of a session
It is still quite far from complete but this is where things start to get interesting. We just implemented the typical analysis where you see the speed over distance, which is like the view every analysis tool has.

[insert  02-session-details.png]

So far nothing crazy, except that is very, very easy to simply add laps from other sessions, probably a bit easier than in other tools I used.

## Analysis magic - finding improvement opportunities
Figuring out how to get a bit faster, when you're just an amateur, is not that easy. You can spend a fortune in coaches (and they are worth it), but at some point maybe it helps you understanding the data.

And the problem is that the data is quite counter intuitive if you're not a race engineer.

The first thing I wanted to figure out when comparing two laps was 'where I'm losing time?'. Yes, comparing the charts is 'easy' but truly understanding where most time is lost is not. That's why we came up with this analysis:

[insert 03]

Looking at the two charts that overlap doesn't give you exactly where are the zones of the track where you're losing more time between two laps. But this very simple calculation actually finds these zones, which lets you focus on that. And very often it is not 'just corner faster'. Most of the time (for amateurs) time is lost just braking or not accelerating fast enough. Easy to fix, hard to spot.

## Curve by curve analysis
This is my favorite so far, and it is somehow a comsequence of the previous: what if you split the track corner by corner, straight by straight, and you calculate how much time you lose or win on each?

Here we go. Visuals are still work in progress, but the info is quite valuable already.

[insert 04 here]

It helps you a lot focus on where the biggest problems are, which as an aficionado is really much harder than you might think (unless you're a gifted rider/driver in which case you're probably at another level, but still).

## Perfect lap calculation
Typically 'perfect lap' just combines the best sectors. You divide the track in 4 sectors and take the best. It makes a lot of sense, but we wanted to push harder and figure out what really perfect would be. What if you split the lap in a ton of small sections?

[insert 05]

This is what you see in this visualization. Of course it might not be very realistic, but it gives you info of where each section of 'best' comes from, so you can understand if this is something you can improve or if it is impossible (like if you made your best ever top speed but ran out of the track... which makes a great 'ideal lap' but hard to repeat).

## What's coming
I still don't know. I'm certainly using it but I don't know yet how it is going to evolve. We have tons of ideas for even better analysis (or at least more understandable for mere humans) and then track personal records, compare with others, and maybe become some sort of place where you can just share your performance with a coach and get better service instead of them just learning about what you say before the session without actual data.

