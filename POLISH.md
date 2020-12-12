# Dlaczego nienawidzę większośći prywatnych serwerów WoW

*Napisane przez Francesco Borzi' aka Shin*

Dlaczego jest wciąż tak wiele bugów, błędów w prywatnych serwerach WoWa, mimo że istnieją od tak wielu lat?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Nie martw się, nie jest kolejna, typowa pogadanka o prawach autorskich Blizzard.
Chcę po prostu wyjaśnić dlaczego nienawidzę większości prywatnych serwerów [World of Warcraft](https://pl.wikipedia.org/wiki/World_of_Warcraft).

## Wprowadzenie

Byłem zafascynowany emulacją WoWa odkąd miałem 14 lat. Pamiętam, gdy dołączyłem po raz pierwszy do jednego z tych "specjalnych realmów", było mnóstwo bugów, ale przynajmniej mogłem grać za darmo. Wiesz, nie miałem wtedy złamanego grosza, więc nie miałem żadnej alternatywy. 

Mając 15 lat zacząłem się zastanawiać w jaki sposób prywatne serwery działają i mogą istnieć, szczególnie z technicznego punktu widzenia. Czy ktoś może ukradł kod od [Blizzard](https://pl.wikipedia.org/wiki/Blizzard_Entertainment)? Nie mialem pojęcia - byłem młody i niedoświadczony! Mimo to, zacząłem próbować i z pomocą mojego starego przyjaciela (Fabio), udało mi się zainstalować serwer WoWa na moim własnym komputerze.

W tamtym czasie nie byłem w stanie sobie wyobrazić ile satysfakcji będę miał i ilu rzeczy będę mógł nauczyć się dzięki temu magicznemu światu.

Może to zabrzmieć dziwnie, ale ten świat fascynuje mnie również teraz, gdy jestem dorosły. Do tego stopnia, że poświęciłem mu [pracę magisterską z Informatyki](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![praca-magisterska-z-emulacji-wow](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Niemniej, wciąz: **Nienawidzę większości prywatnych serwerów i bardzo chcę wytłumaczyć dlaczego.**

## Kilka pojęć technicznych

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

In order to make you understand my point of view, I need to dwell on a small technical parenthesis about WoW working processes, which I will try to put in simple words.

### Jak działa oryginalny World of Warcraft

Na poziomie oprogramowania - są dwa programy, które pełnią kluczowe funkcje:

- **APLIKACJA KLIENCKA** - czyli program "World of Warcraft", który jest zainstalowany przez każdego gracza na jego komputerze, aby umożliwić dostęp do gry;

- **APLIKACJA SERWEROWA**: czyli program który jest uruchamiany na serwerach.

Cały proces jest bardzo prosty: wszyscy Klienci (gracze) podłączają się do serwera by wchodzić w interakcje między sobą. Klient gry wie jak adres serwera, bo jest on przechowywany w sławnym już pliku "**realmlist.wtf**"  (dlatego właśnie musisz edytować ten plik aby podłączyć się do innego serwera).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Jak działają serwery prywatne WoWa

Gdy grasz na serwerach prywatnych, zasada jest dokładnie taka sama. Różnica jest w oprogramowaniu z którego korzystasz

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**KLIENT**. Każdy ma dostęp do oryginalnego klienta World of Warcraft. Możesz go łatwo zdobyć kupując go lub pobierać z internetu. Jest to ten sam program, z którego byś korzysta(ł/a) chcąc grać na oficjalnym serwerze. Rzecz jasna, różne serwery prywatne mają różne wersje klienta, ale zawsze odnoszą się do oryginalnego klienta gry. Musisz jedynie dokonać małej zmiany w pliku "realmlist.wtf" przez zmianę adresu oryginalnego serwera na adres serwera prywatnego. Tyle.

**SERWER**. Tutaj sprawa ma się całkowicie inaczej. Nikt z poza Blizzarda nie ma dostępu do oryginalnego oprogramowania, na którym działają oficjalne serwery World of Warcraft. Więc te aplikacje są całkowicie inne niż oryginalna.

### Inżynieria wsteczna

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Każde oprogramowanie, które uruchamia prywatny serwer, powstało poprzez "inżynierię wsteczną" czyli technikę, która w prostych słowach oznacza - "Próboję napisać program, który imituje zachowanie innego programu, ale bez patrzenia na oryginalny kod."

Pytanie jest następujące: kto zaimplementował to oprogramowanie i kiedy to się stało?


#### Dygresja odnośnie praw autorskich

*Cały materiał chroniony prawem autorskim (obrazy, dźwięki, modele 3D, loga itd.) znajduje się wewnątrz aplikacji klienckiej. Aplikacja serwerowa zawiera tylko liczby i tekst. Wobec tego, jest w pełni legalnym użycie go w celach edukacyjnych.*

## Aplikacje serwerowe nieoficjalnych serwerów WoW

Kto tworzy oprogramowanie serwerowe (potocznie nazywane emulatorem) dzięki któremu można uruchomić prywatny serwer WoW? I jak oni to zrobili?



### Złożoność

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Nie musisz być ekspertem aby zrozumieć, że napisanie aplikacji serwerowej dla MMORPG o tak dużym zasięgu jak World of Warcraft, nie jest dziecięcą igraszką.

Blizzard jest dużą firmą z tysiącami pracowników. Napisanie programu, który imituje działanie ich aplikacji serwerowej zdecydowanie nie jest trywialne i wykonalne dla pojedyńczej osoby (lub małej grupy programistów).

Nie jest to tylko kwestia zlożoności. Pomyślmy o każdej bardzo trywialnej, ale powtarzalnej czynnności - jak dodanie każdego NPC do świata, uwzględniając każdy jeden przedmiot, który może z nich paść z procentowym prawdopodobieństwem jego uzyskania itd. Straszna praca. Nie wspominając w ogóle o wszystkich złożonych zadaniach, któ©e wymagają godzin studiowania i testowania - takich jak mechanika czarów, mechanika przeciwników itd.

Po krótce... nawet najlepszy programista na świecie nie byłby w stanie zrobić całej tej pracy samodzielnie.

Wciąż - serwery prywatne istnieją i oprogramowanie do ich uruchomienia również. Niektóre serwery prywatne są teraz w stanie zaoferować jakość rozgrywki nie odbiegającą wiele od oryginału (tutaj odwołuję się głównie do starych dodatków).

Jak jest to możliwe?

### MaNGOS i otwartoźródłowy model rozwoju oprogramowania

> Jeśli ty masz jabłko i ja mam jabłko, i wymienimy się tymi jabłkami, to wtedy ty i ja wciąż będziemy mieli po jednym jabłku. Ale jeśli ty masz pomysł i ja mam pomysł, i wymienimy się tymi pomysłami, to wtedy obaj będziemy mieli dwa pomysły. (George Bernard Shaw)

Upraszczając: program otwartoźródłowy to taki, którego kod jest publiczny.

W kontekście serwerów prywatnych, otwarte źródła pełnią kluczową rolę.

Niektórzy gracze-weterani mogą pamiętać, że niegdyś jakość gry na prywatnych serwerach pozostawiala wiele do życzenia. Prawie nic nie działało. Na przykład: jeśli grałeś roguem w stealth mogłeś zostać stargetowany przez każdą osobę, któ©a wpisała `/target Twojeimie`. Zgadnij, którą klasę wybrałem dla mojej pierwszej postaci...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Prawdziwą rewolucją okazał się [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), czyli open-sourceowy projekt powstały w 2005, którego celem było stworzenie serwera (aplikacji) World of Warcraft.
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
