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
Wspaniałą wiadomością o MaNGOS, poza jego siłą, był fakt że był on aplikacją otwartoźródłową. Jego kod był całkowicie publiczny i każdy użytkownik na świecie mógł przestudiować go i zaoferować swój wkład (zarówno w kontekście dodawania lub naprawy mechanik, ale także przy raportowaniu bugów).


Jedynie w ten sposób, dzięki udziałowi wielu wolontariuszy z różnych krajów, było możliwe stworzenie aplikacji serwerowej, która będzie w stanie emulować World of Warcraft zapewniając wyższą jakość rozgrywki.

W 2009 roku powstał inny, bazujący na MaNGOS, emulator - [TrinityCore](https://www.trinitycore.org/).

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Do dziś dnia, znaczna większość prywatnych serwerów korzysta z oprogramowania bazującego na MaNGOS/TrinityCore.

Przez lata powstawały [różne projekty](http://mangosrumors.org/best-wow-emulator-2020/) i bazowały one na kodzie MaNGOS/TrinityCore, różniąc się głównie wspieraną wersją WoW. 
Na przkład [AzerothCore](https://www.azerothcore.org/) dla 3.3.5, [OregonCore](https://github.com/OregonCore) dla 2.4.3, [SkyFire](https://www.projectskyfire.org/) dla 5.4.8, [CMaNGOS](https://cmangos.net/) dla Classic/TBC/WOTLK, oraz wiele innych... Bazujących na MaNGOS i/lub TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Podsumowanie

Prywatne serwery osiągnęły obecną jakość jedynie dzięki udziałowi wielu współautorom (contributors), którzy na przestrzeni lat (od 2005 do dzisiaj) zaimplementowali coraz więcej funkcjonalności.

Dzisiaj, każdy doświadczony użytkownik komputera, nie będący programistą może z łatwością zainstalować serwer WoW.

## Open source vs serwery prywatne

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hipotetyczny scenariusz

Załóżmy, że zarówno Alice i Bob mają swój prywatny serwer WoW. Załóżmy również, że korzystają z tej samej wersji gry.
Zarówno Alice, jak i Bob chcą wypuścić nową zawartość (content) dla swoich graczy, która dotychczas była niedostępna bo bossy `A`, `B`, `C` oraz `D` były zbugowane.

- Alice jest bardzo dobrą programistką i potrafi naprawić bossa `A` oraz `B`
- Bob jest wciąż początkującym programistą i naprawił jedynie bossa `C`.

### W idealnym świecie

Alice i Bob pracują wspólnie i wymieniają się swoimi poprawkami. W wyniku czego, oba serwery mają w pełni działające bossy `A`, `B` oraz `C`.
W dodatku, Alice i Bob połączą siły aby naprawić również bossa `D`.

Ostatecznie gracze na obu serwerach są zadowoleni, bo grają na w pełni naprawionym contencie.

### W świecie rzeczywistym

Alice i Bob rywalizują ze sobą i ich serwery walczą między sobą. Na serwerze Alice działają jedynie bossy `A` i `B`. Tymczasem na serwerze Boba jedynie boss `C`.
Niektórzy gracze z serwera Boba przenoszą się na serwer Alice. Sewer Boba zamyka się po jakimś czasie. Niektórzy gracze Alice przestali grać, ponieważ mieli dość robienia jedynie bossów `A` oraz `B`, ponieważ bossy `C` oraz `D` nie działają.

W wyniku powyższego, gracze na obu serwerach są mniej szczęśliwi niż w poprzednim scenariuszu. Alice zarabiła więcej pieniędzy poprzez dotacje, niż zarobił Bob.

### Licencja emulatorów WoWa

W zasadzie, kod MaNGOS/TrinityCore (oraz pochodzących od nich rpoejtków) jest wypuszczony pod [licencją GNU GPL](https://pl.wikipedia.org/wiki/GNU_General_Public_License).

W uproszczeniu, treść licencji brzmi: używaj kodu jak ci się podoba, bez płacenia za niego, tak długo jak zmiany do tego kodu są wypuszczane pod tą samą licencją.
Reasumując - licencja tych projektów wymaga od użytkowników by upublicznili i udostępnili swoje zmiany w kodzie.

Oczywiście, większość serwerów używa tej licencji jako **papieru toaletowego**. W przeciwnym wypadku, nie byłoby serwera "lepiej naprawionego" niż inne.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Kłamstwa o prywatnych serwerach

Oto lista kłamstw, które powtarzają administratorzy prywatnych serwerów:


### "Napisaliśmy ten emulator"

Fake news. Nie ma znaczenia ile zmian "ty" zrobiłeś. Wszyscy zaczeliśmy od projektu bazującego na MaNGOS.

Może napisales jakieś poprawki, ale większość kodu to wciąż MaNGOS/TrinityCore.

Może jesteś naprawdę dobry i przepisałeś większość kodu przez ostatnie lata. Wciąż, zacząłeś od MaNGOSa. Bez niego, pierwszego dnia, nie miałbyś nawet działającego mechanizmu logowania.

### "Naprawiliśmy X"

W większości przypadków, nikt z nich niczego nie naprawił.
Po prostu pobrali poprawki pochodzące od społeczności, która rozwija oprogramowanie open-source i zaaplikowali je do "swojego" emulatora.
Niemniej, wciąż przypisują sobie wszystkie zasługi.

### "NAPRAWDĘ naprawiliśmy X"

Niektóre serwery prywatne naprawdę naprawiają rzeczy samodzielnie. Mają często zespół deweloperski, który jest opłacany z dotacji pochodzących od graczy.

Większość z nich nie dzieli się poprawkami z społecznością programistyczną.

Cóż, społeczność która dała (za darmo) oprogramowanie, z którego korzystasz by prowadzić swój serwer, prosi cię byś się podzielił z nim, ale wciąż tego nie robisz. I tak cię nienawidzę.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## "Usprawiedliwiania" serwerów prywatnych


### "Nie dzielę się nimi, bo chcę by mój serwer był wyjątkowy, lepszy niż inne"

Fantastycznie Mistrzu. To teraz pomyśl o tym: jeśli WSZYSCY programiści zrobili tak jakty, to ani ty, ani twój praywatny serwer by nie istniały.

Dlaczego? A dlatego, że ani MaNGOS (ani TrinityCore, AzerothCore, etc ...) by nie istniały.
Te projekty istnieją dzięki programistom którzy, w przeciwieństwie do Ciebie, dzielą się swoim kodem.

Jeśli wszyscy programiści by nie upubliczniali swojego kodu, to nie mielibyśmy żadnego sensownego emulatora WoWa, a ty byś nie mógł otworzyć swojego prywatnego serwera bo nie miałbyś na czym bazować.


### "Jeślu udostępnię swoje poprawki, to konkurencja je ukradnie"

Tu nie ma co "kraść". Nie mogą "ukraść" tego kodu, bo on nie "należy" do Ciebie. Nie, nawet jeśli go to ty go napisałeś.

Idea otwartego oprogramowania jest jasna: możesz korzystać z kodu za darmo, przy czym każda modyfikacja MUSI być publiczna.

Oh, nie zgadzasz się? W porządku. To nie używaj żadnego otwartoźródłowego oprogramowania i napisz swój emulator WoW od podstaw. 

## W jaki sposób to wpływa na graczy

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
