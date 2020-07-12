# Why I hate most of WoW private servers

*Written by Francesco Borzi' aka Shin*

Why there are still so many bugs in WoW private servers, despite they have been around for so many years?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

No, this is not the usual copyright lecture about Blizzard, etc ...
I just want to explain why I hate most of [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft) private servers.

## Introduction

I was fascinated by WoW emulation since the beginning, when I was 14 years old and I entered for the first time in these special realms where, at that time, everything was full of bugs, but you could play without paying anything. Being totally broke, I had no other alternative.

At 15 I began to wonder how private servers really worked and how their existence was technically possible. Did someone steal the code from [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment)? I had no idea, back then I was young and totally ignorant on the subject. But I started messing around and, with the help of a friend older than me (Fabio), I finally managed to install a WoW server on my own PC.

At that time I still had no idea how many satisfactions I would have had and how many things I would have learned thanks to this magical world.

It may seem strange, but this world fascinates me a lot even now, as an adult. It fascinated me so much that I also dedicated my degree thesis in Computer Science.

But still: **I hate most private servers and I really want to explain why.**

## Technicalities

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

In order to explain my point of view you need a small technical parenthesis concerning the functioning of WoW, which I will try to put in simple words.

### How the original World of Warcraft works

At the software level, there are two programs that are the main actors of this game:

- the **CLIENT APPLICATION**: the "World of Warcraft" program that each player installs on their computer in order to access the game.

- the **SERVER APPLICATION**: it's the program that runs on server machines

The mechanism is very simple: all Clients (players) connect to a Server in order to interact with each other. The client knows the address of the server because it has stored it in the famous "**realmlist.wtf**" file (that's why to change the server you have to modify this file).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### How WoW private servers work

When playing on private servers, the mechanism is exactly the same. The difference lies in the used software.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**. Everyone has access to the original World of Warcraft client. you can easily get it by buying it or downloading it from the internet. This program is exactly the same that would be used to play on the official server. Obviously different private servers have different client versions, but they are always versions of the original client. You just need to make a small change to the "realmlist.wtf" file, replacing the address of the retail server address with the address of a private server, and you're done.

**SERVER**. This is completely different. Nobody outside Blizzard has access to the original software that runs the official World of Warcraft servers. So these applications are completely different from the original one.

### Reverse engineering

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

All the software that runs the private servers have been created with the "reverse engineering" technique. Which in simple terms it means "I try to write a program that imitates the behaviour of another program, without being able to access the original code".

The question now is who and when did they implement this software.


#### Parenthesis about the copyright

*All copyrighted material (images, sounds, 3D models, logos, etc ...) is located inside the client application.
The server application contains only numeric and textual values. Therefore, if used for educational purposes, it is perfectly legal.*

## Unofficial WoW server applications

Who creates the software applications that run WoW's private servers (commonly called "emulators")? And how did they do it?



### Complexity

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

You don't need to be an expert to understand that writing a server application for an MMORPG with such a big scope like World of Warcraft is certainly not child's play.

Blizzard is a large company with thousands of employees. Writing a program that "mimics" the operation of their server application is certainly not trivial or feasible by a single individual (or a small group of programmers).

And it's not just a matter of complexity. Think also of very trivial but repetitive tasks, like adding every single NPC in the world, including every single item of its loot with its own percentage of chance, etc .. A huge job in short. Not to mention very complex tasks that require hours of study and testing, such as spell mechanics, boss mechanics, etc.

In short .... not even the best programmer in the world would be able to do all this work alone.

Yet there are private servers, and the software that makes them run. And some private servers are now able to offer a game quality not far from the original one (here I refer mainly to the old expansions).

How was this possible?

### MaNGOS and the open source development model

> If you have an apple, and I have an apple, and we exchange them, then you and I always have one apple each. But if you have an idea, and I have an idea, and we exchange them, then we both have two ideas. (George Bernard Shaw)

Just to make it simple: an open source program is a program whose code is public.

In the context of private servers, open source plays a fundamental role.

Some veteran gamers will remember that once on private servers the quality of the game was really bad. Almost nothing worked.
For example, if you were a rogue in stealth you could be targeted by anyone who wrote `/target Yourname`. Guess what class was my first character ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

The real revolution was [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), an open source project created in 2005, whose purpose was to provide a server application for World of Warcraft.
The big news of MaNGOS, which was also its strong point, was the fact that being an open source application, its code was made completely public, and any user from anywhere in the world could study it and offer its own contribution (both in terms of adding or fixing game mechanics, but also in terms of reporting bugs).

Only in this way, thanks to the contributions of many volunteers of different nationalities, it was possible to develop a server application capable of emulating World of Warcraft ensuring a quality of a certain level.

In 2009 [TrinityCore](https://www.trinitycore.org/) was born, based on MaNGOS, which is another historically very important project.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

As today, the vast majority of private servers run on MaNGOS/TrinityCore-based applications.

Over the years, [different projects](http://mangosrumors.org/best-wow-emulator-2020/) were born, based on the MaNGOS/TrinityCore code, which mainly vary according to the supported WoW version.
For example [AzerothCore](https://www.azerothcore.org/) for 3.3.5, [OregonCore](https://github.com/OregonCore) for 2.4.3, [SkyFire](https://www.projectskyfire.org/) for 5.4.3, [CMaNGOS](https://cmangos.net/) for Classic/TBC/WOTLK, and many others ... all based on MaNGOS and/or TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Recap

So the private servers we have reached the quality we enjoy today only thanks to the many contributors who over the years (from 2005 to today) have implemented more and more game features.

Today any experienced PC user can easily install a WoW server, without even being a programmer.

## Open source vs private servers

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hypothetical scenario

Suppose that Alice and Bob have a private server each, and let's assume they are on the same version of the game.
Both Alice and Bob want to release a new content to their players, which has so far been closed because the bosses `A`,` B`, `C` and` D` are quite buggy.

- Alice is a very good developer and can fix both bosses `A` and` B`
- Bob is still a beginner and only fixes the boss `C`

### In an ideal world

Alice and Bob work together and exchange their fixes. As a result, both of their servers will have perfectly fixed bosses `A`,` B` and `C`.
In addition, Alice and Bob will join forces in order to work on `D` as well.

As a result, the players on both servers are very happy because they play with completely fixed content.

### In the real world

Alice and Bob are rivals and therefore wage war against each other. In Alice's server, only bosses `A` and` B` work. While in Bob's only `C` works.
Some players move from Bob's server to Alice's. Bob's server closes after a while. Some of Alice's server players stop playing because they get tired of always doing `A` and` B` because `C` and` D` don't work.

As a result, the players on both servers are less happy than in the previous scenario. Alice made more money through player donations than Bob did.

### The license of the WoW emulators

Actually, the MaNGOS/TrinityCore code (and derivative projects) is released under the [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

In simple words, this license says the following: use the code to do whatever you want, without paying anything, as long as any modification to the original code is also released under the same license.
Practically the licese of these projects would require those who use them to publish any changes to the core.

Of course, most private servers use this license as **toilet paper**. Otherwise, there should be no private server that is "better fixed" than others.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## The lies of private servers

Here a collection of lies that the administrator of private servers keep telling to their players:


### "We wrote this core"

Fake news. It doesn't matter how many changes "you" have made. However, you started with a MaNGOS-based project.

Maybe you've made some improvements, but most of the code is still MaNGOS/TrinityCore's.

Maybe you are really good and over time you have rewritten most of the code.
Still, you started from MaNGOS. Without it, on day 1 you didn't even have the login feature working.



### "We have fixed X"

In the vast majority of cases, none of them has really fixed anything.
Simply they have updated their core, downloading the fixes coming from the open source community.
Still they take all credits.

### "We (really) fixed X"

Some private servers really fix stuff on their own. They often have dedicated development teams that are paid using the money coming players' donations.

Most of them do not share these fixes with the development community.

Well, the GPL license of the software you are using to run your server is telling you to share them, but you still keep it private. So I hate you anyway.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## The "justifications" of private servers


### "I keep them private to make my server a special place, better than the others"

Alright champ. Try to think about this: if ALL the developers did like you, neither you nor your private server would exist.

Why? Simply because neither MaNGOS (nor TrinityCore, AzerothCore, etc ...) would exist.
These projects exist thanks to developers who, unlike you, shared their code.

At that point we were still without decent WoW emulators and you just couldn't open your private server. Because there wouldn't be any software available.


### "If I shared my fixes, the competition would steal them"

There is nothing to "steal". They can't "steal" that code because it doesn't "belong" to you. No, not even if you really wrote it.

The MaNGOS GPL license is clear: you can use that code for free, provided that any modification of it MUST be made public.

Oh you don't agree? Very well. Then don't use GPL licensed code and write your own WoW emulator from scratch.

## How this affect players

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

I realize that this whole story that talks about ethics and licenses matters very little to the average World of Warcraft player.
Players just want to play on a stable and well-fixed server, they don't care much whether this server collaborates with open source or not.

But... try for a moment to see it from another perspective.

Developers of the open source project (MaNGOS, TrinityCore, AzerothCore, etc ...) basically care very little about what private servers do.
Sure, as a developer it pisses you off to see some random server administrator taking credits for your work, but in the end it doesn't change your life.

Those that would really have different lives, if ALL private servers collaborated with open source, would be the players.

Oh yes, because if this were the case, ALL private servers would have a game quality far superior to what we enjoy today. In all expansions.

See for example the case of Alice and Bob before. That is a very simplified example, just to explain the concept.

However, the reality is just that: there are many private servers around the world, each of them always works on the same things, racing to do them sooner and better.
If they collaborated with each other instead, they would avoid doing unnecessary work and would have more time and workforce. So they would surely be able to achieve much more.

Parenthesis: the quality (and competitions between) private servers should not be measured (only) in terms of fixes, but on factors such as the skill of its administration in maintaining it. The quality of the community also plays a fundamental role, just as it happens in blizzard servers (which from the technical perspective are all the same).

If a private server closes, and its developers have not shared their work, that work is lost forever.

## Denying lies

### Official authors list

The most interesting thing is that all the MaNGOS-based projects are completely public, so it is possible to accurately verify who contributed to them.

As a result, all the contributors list of these projects are absolutely public and ANYONE can verify who actually fixed what.

For example:

- Official list of MaNGOS contributors: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Official list of TrinityCore contributors https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Official list of AzerothCore contributors https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: you can find the author of this article in all these lists

### Official commits list

Any open source project (generally hosted on GitHub) has the list of commits made by the develoers. For each commit, both the author and the date are there.

It is very easy to verify this information, just open the official repository of any emulator. Google for example "TrinityCore github" or "AzerothCore github" and take a look.

You will see who-does-really-what. You will see all the lines of code, their authors, the comments of the other devs, etc ... etc ... You will see everything. No more lies.


## What can I do as a player?

My advice is to play/support private servers that collaborate with open source. Regardless of which expansion and emulator they use.

Or, at least, avoid those servers that peddle other people's work on their own, removing the credits from the original authors.


### Learn more about free software

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software
