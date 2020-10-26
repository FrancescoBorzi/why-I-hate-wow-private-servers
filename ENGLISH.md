# Why I hate most of WoW private servers

*Written by Francesco Borzi' aka Shin*

Why are there still so many bugs in WoW private servers, although they have been around for so many years?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Don't worry, this is not the usual copyright lecture about Blizzard.
I just want to explain why I hate most of the [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft) private servers.

## Introduction

I’ve been fascinated by WoW emulation since I was 14. I remember that the first time I joined one of these “special realms”, there were a lot of bugs, but you could play for free at least. You know, I didn’t have a red cent at that time, so I had no alternative. 

At 15 I began wondering how private servers actually worked and could exist, especially from a technical perspective. Did someone steal the code from [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment) maybe? I had no idea  – I was so young and inexperienced at that time! Despite that, I started messing around and, with the help of an old friend of mine (Fabio), I finally managed to install a WoW server on my own PC.

Back then I couldn’t even imagine the amount of satisfaction I would have got and how many things I would have learned thanks to this magical world.

It may sound weird, but this world still fascinates me now, as an adult, at the point that I dedicated an entire [Master’s Degree thesis in Computer Science to this topic](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

But still: **I hate most of the private servers and I really want to explain why.**

## Few technical terms

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

In order to make you understand my point of view, I need to dwell on a small technical parenthesis about WoW working processes, which I will try to put in simple words.

### How the original World of Warcraft works

At the software level, there are two programs that could be considered as the main actors of this game:

- the **CLIENT APPLICATION** - which is the actual "World of Warcraft" program installed by every player on their computer in order to access the game;

- the **SERVER APPLICATION**: which is the program that runs on the server machines.

The process is very simple: all Clients (players) connect to a Server in order to interact with each other. The client knows the server address, as it is stored in the famous "**realmlist.wtf**" file (that's why you have to modify this file in order to switch to another server).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### How WoW private servers work

When playing on private servers, the principle  is exactly the same. The difference lies in the software you use.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**. Everyone has access to the original World of Warcraft client. You can easily get it by buying it or downloading it online. This program is exactly the one that you would use to play on the official server. Obviously different private servers have different client versions, but they always refer to the original client. You just need to make a small change to the "realmlist.wtf" file, replacing the address of the retail server address with the one of a private server. That's it.

**SERVER**. This is completely different. Nobody outside Blizzard has access to the original software that runs the official World of Warcraft servers. So these applications are completely different from the original one.

### Reverse engineering

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Every software that runs private servers have been created through the "reverse engineering" technique, which, in simple words, means "I try to write a program that imitates the behaviour of another program, without looking at the original code".

The question now is: who implemented this software and when did it happen?


#### Digression about the copyright

*The entire copyrighted material (images, sounds, 3D models, logos, etc ...) is located inside the client application.
The server application contains only numbers and texts. Therefore, it is absolutely legal if you use it for educational purposes.*

## Unofficial WoW server applications

Who creates the software applications that run WoW's private servers (commonly called "emulators")? And how did they do it?



### Complexity

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

You don't need to be an expert to understand that writing a server application for an MMORPG with such a big scope like World of Warcraft is certainly not child's play.

Blizzard is a big company with thousands of employees. Writing a program that "imitates" the operation of their server application is certainly not trivial or feasible for a single individual (or a small group of programmers).

And it's not just a matter of complexity. Let's think of very trivial but repetitive tasks, like adding every single NPC into the world, including every single item of their loot with its own percentage of chance, etc.. . A terrific job basically. Not to mention all the very complex tasks that require hours of study and testing, such as spell mechanics, boss mechanics, etc.

In short .... not even the best programmer in the world could be able to do all this work on her/his own.

Yet there are private servers, and the software that makes them run. And some private servers are now able to offer a game quality that is not far from the original one (here I refer mainly to the old expansions).

How is that possible?

### MaNGOS and the open source development model

> If you have an apple and I have an apple and we exchange these apples then you and I will still each have one apple. But if you have an idea and I have an idea and we exchange these ideas, then each of us will have two ideas. (George Bernard Shaw)

Just to make it simple: an open source program is a program whose code is public.

In the context of private servers, the open source plays a fundamental role.

Some veteran gamers may remember that once the game quality on private servers was really bad. Almost nothing worked.
For example, if you were a rogue in stealth you could be targeted by anyone who wrote `/target Yourname`. Guess which class I chose for my first character ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

The real revolution was [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), an open source project created in 2005, whose purpose was to provide a server application for World of Warcraft.
The great news of MaNGOS, as well as its strength, was the fact that as an open source application, its code was completely public, and any user from all over the world could study it and offer their own contribution (both in terms of adding or fixing game mechanics, but also in terms of reporting bugs).

Only in this way, thanks to the contribution of many volunteers of different nationalities, it was possible to develop a server application capable of emulating World of Warcraft with a higher game quality.

In 2009 another important project was born [TrinityCore](https://www.trinitycore.org/), based on MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

To date, the overwhelming majority of private servers run on MaNGOS/TrinityCore-based applications.

Over the years, [different projects](http://mangosrumors.org/best-wow-emulator-2020/) were born, and they were based on the MaNGOS/TrinityCore code, which mainly vary according to the supported WoW version.
For example [AzerothCore](https://www.azerothcore.org/) for 3.3.5, [OregonCore](https://github.com/OregonCore) for 2.4.3, [SkyFire](https://www.projectskyfire.org/) for 5.4.8, [CMaNGOS](https://cmangos.net/) for Classic/TBC/WOTLK, and many others ... All of them based on MaNGOS and/or TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Recap

So the private servers have reached such a quality only thanks to the many contributors who have implemented more and more game features over the years (from 2005 to today).

Today any experienced PC user can easily install a WoW server, without even being a programmer.

## Open source vs private servers

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hypothetical scenario

Suppose that Alice and Bob have a private server each, and let's assume they are on the same version of the game.
Both Alice and Bob want to release a new content to their players, which has been closed so far because the bosses `A`,` B`, `C` and` D` are quite buggy.

- Alice is a very good developer and can fix both bosses `A` and` B`
- Bob is still a beginner and only fixes the boss `C`

### In an ideal world

Alice and Bob work together and exchange their fixes. As a result, both of their servers will have perfectly fixed bosses `A`,` B` and `C`.
In addition, Alice and Bob will join forces in order to work on `D` as well.

As a result, the players on both servers are very happy because they play a completely fixed content.

### In the real world

Alice and Bob are rivals and so they wage war against each other. In Alice's server, only bosses `A` and` B` work. While in Bob's server only `C` works.
Some players move from Bob's server to Alice's one. Bob's server closes after a while. Some of Alice's server players stop playing because they get tired of always doing only `A` and` B` because `C` and` D` don't work.

As a result, the players on both servers are less happy than in the previous scenario. Alice made more money through player donations than Bob did.

### The license of the WoW emulators

Actually, the MaNGOS/TrinityCore code (and their derivated projects) is released under the [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

In simple words, this license says the following: use the code to do whatever you want, without paying anything, as long as any modification to the original code is also released under the same license.
Basically, the license of these projects requires those who use them to publish any changes to the public.

Of course, most private servers use this license as **toilet paper**. Otherwise, there should be no private server that is "better fixed" than others.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## The lies about the private servers

Here it is a list of lies that the administrators of many WoW private servers keep telling to their players:


### "We wrote this core"

Fake news. It doesn't matter how many changes "you" made. However, you started with a MaNGOS-based project.

Maybe you've made some improvements, but most of the code is still MaNGOS/TrinityCore's.

Maybe you are really good and you have rewritten most of the code over the years. Still, you started from MaNGOS. Without it, on day 1 you wouldn't even have got the login feature working.

### "We have fixed X"

In the vast majority of cases, none of them has really fixed anything.
They have just downloaded the fixes coming from the open source community and applied them to their core.
Still they take all credits.

### "We (really) fixed X"

Some private servers really fix stuff on their own. They often have dedicated development teams that are paid with the money coming from players' donations.

Most of them do not share these fixes with the development community.

Well, the community that gave (for free) the software you are using to run your server is asking you to share them, but you still keep it private. So I hate you anyway.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## The "justifications" of private servers


### "I keep them private to make my server a special place, better than the others"

Alright champ. Try to think about this: if ALL the developers did like you, neither you nor your private server would exist.

Why? Simply because neither MaNGOS (nor TrinityCore, AzerothCore, etc ...) would exist.
These projects exist thanks to developers who, unlike you, shared their code.

If all devs kept their code private, we would have no decent WoW emulator and you just couldn't open your private server, because there wouldn't be any software available.


### "If I shared my fixes, the competition would steal them"

There is nothing to "steal". They can't "steal" that code because it doesn't "belong" to you. No, not even if you really wrote it.

The open source philosophy is clear: you can use that code for free, provided that any modification of it MUST be made public.

Oh don't you agree? Alright. Then don't use any open source code and write your own WoW emulator from scratch.

## How this affects players

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

I totally understand that this whole story about ethics and licenses matters very little to the average World of Warcraft player.
Players just want to play on a stable and well-fixed server, they don't care much whether this server collaborates with open source or not.

But... try for a moment to see it from another perspective.

Developers of the open source projects (MaNGOS, TrinityCore, AzerothCore, etc ...) basically don't care much about what private servers do.
Of course, as a developer it pisses you off to see some random server administrator taking credits for your work, but in the end it doesn't change your life.
Many open source developers just do it for fun and educational purposes.

Actually, if ALL private servers collaborated with open source, the players’ lives would change completely!
You know, in that case, every server would provide a much better game experience for any expansion. The example of Alice and Bob mentioned before can be applied to this case as well.

However, the reality is just that: there are many private servers around the world, each of them always works on the same things, racing to do them sooner and better.
If they collaborated with each other instead, they would avoid doing unnecessary work and would have more time and workforce. So they would surely be able to achieve much more.

*Note: the quality (and competition between) private servers should not be (only) about of fixing, but also about other factors such as its administrators’ skills in managing it. The quality of the community also plays a fundamental role, just as it happens in Blizzard servers (which are all equal from a technical perspective).*

If a private server closes, and its developers have not shared their work, that work will be lost forever.

## Exposing lies

### Official authors list

The most interesting thing is that all the MaNGOS-based projects are completely public, so it is possible to accurately verify who contributed to them.

As a result, all the contributors list of these projects are absolutely public and ANYONE can verify who actually fixed what.

For example:

- Official list of MaNGOS contributors: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Official list of TrinityCore contributors https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Official list of AzerothCore contributors https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: you can find the author of this article in all these lists

### Official commits list

Any open source project (generally hosted on GitHub) has the list of commits realised by the different developers. For each commit, both the author and the date are there.

It is very easy to verify this information, just open the official repository of any emulator. Google for example "TrinityCore github" or "AzerothCore github" and just have a look.

You will see who-does-really-what. You will see all the lines of code, their authors, other devs’ comments, etc. You will see everything. No more lies!


## What can I do as a player?

My advice is you play/support private servers that collaborate with open source, in spite of the type of expansion and emulator they use.

Or, at least, avoid those servers that peddle other people's work on their own, removing the credits from the original authors.


### Learn more about free software

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Thanks

Special thanks to *Laura Bartiromo*
