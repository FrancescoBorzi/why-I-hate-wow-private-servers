# Dlaczego nienawidzę większości prywatnych serwerów WoW

*Napisane przez Francesco Borzi' aka Shin*

Dlaczego jest wciąż tak wiele błędów w prywatnych serwerach WoW-a, mimo że istnieją od tak wielu lat?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Nie martw się, nie jest kolejna typowa pogadanka o prawach autorskich Blizzarda.
Chcę po prostu wyjaśnić, dlaczego nienawidzę większości prywatnych serwerów [World of Warcraft](https://pl.wikipedia.org/wiki/World_of_Warcraft).

## Wprowadzenie

Byłem zafascynowany emulacją WoW-a, odkąd skończyłem 14 lat. Pamiętam, gdy dołączyłem po raz pierwszy do jednego z tych "specjalnych realmów" - było mnóstwo bugów, ale przynajmniej mogłem grać za darmo. Wiesz, nie miałem wtedy złamanego grosza, więc nie miałem żadnej alternatywy. 

Mając 15 lat, zacząłem się zastanawiać, w jaki sposób prywatne serwery działają i mogą istnieć, szczególnie z technicznego punktu widzenia. Czy ktoś może ukradł kod od [Blizzarda](https://pl.wikipedia.org/wiki/Blizzard_Entertainment)? Nie miałem pojęcia - byłem młody i niedoświadczony! Mimo to zacząłem próbować i z pomocą mojego starego przyjaciela (Fabio) udało mi się zainstalować serwer WoW-a na moim własnym komputerze.

W tamtym czasie nie byłem w stanie sobie wyobrazić, ile satysfakcji będę miał i ilu rzeczy będę mógł nauczyć się dzięki temu magicznemu światu.

Może to zabrzmieć dziwnie, ale ten świat fascynuje mnie również teraz, gdy jestem dorosły. Do tego stopnia, że poświęciłem mu [pracę magisterską z informatyki](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![praca-magisterska-z-emulacji-wow](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Niemniej, wciąż: **Nienawidzę większości prywatnych serwerów i bardzo chcę wytłumaczyć, dlaczego.**

## Kilka pojęć technicznych

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Aby wytłumaczyć mój punkt widzenia, będę musiał wtrącić swoje trzy grosze o tym, jak działa WoW. Postaram się to wytłumaczyć w kilku prostych słowach.

### Jak działa oryginalny World of Warcraft

Na poziomie oprogramowania - są dwa programy, które pełnią kluczowe funkcje:

- **APLIKACJA KLIENCKA** - czyli program "World of Warcraft", który jest zainstalowany przez każdego gracza na jego komputerze, aby umożliwić dostęp do gry;

- **APLIKACJA SERWEROWA** - czyli program który jest uruchamiany na serwerach.

Cały proces jest bardzo prosty - wszyscy Klienci (gracze) podłączają się do serwera, by wchodzić w interakcje między sobą. Klient gry wie, jaki jest adres serwera, bo jest on przechowywany w sławnym już pliku "**realmlist.wtf**"  (dlatego właśnie musisz edytować ten plik, aby podłączyć się do innego serwera).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Jak działają serwery prywatne WoW-a?

Gdy grasz na serwerach prywatnych, zasada jest dokładnie taka sama. Różnica jest w oprogramowaniu, z którego korzystasz

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**KLIENT**. Każdy ma dostęp do oryginalnego klienta World of Warcraft. Możesz go łatwo zdobyć, kupując go lub pobierając z internetu. Jest to ten sam program, z którego byś korzysta(ł/ła), chcąc grać na oficjalnym serwerze. Rzecz jasna, różne serwery prywatne mają różne wersje klienta, ale zawsze odnoszą się do oryginalnego klienta gry. Musisz jedynie dokonać małej zmiany w pliku "realmlist.wtf" przez zmianę adresu oryginalnego serwera na adres serwera prywatnego. Tyle.

**SERWER**. Tutaj sprawa ma się całkowicie inaczej. Nikt spoza Blizzarda nie ma dostępu do oryginalnego oprogramowania, na którym działają oficjalne serwery World of Warcraft. Więc te aplikacje są całkowicie inne niż oryginalna.

### Inżynieria wsteczna

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Każde oprogramowanie uruchamiające prywatny serwer powstało poprzez "inżynierię wsteczną" czyli technikę, która w prostych słowach oznacza - "Próbuję napisać program, który imituje zachowanie innego programu, ale bez patrzenia na oryginalny kod."

Pytanie jest następujące: kto zaimplementował to oprogramowanie i kiedy to się stało?


#### Dygresja odnośnie praw autorskich

*Cały materiał chroniony prawem autorskim (obrazy, dźwięki, modele 3D, loga itd.) znajduje się wewnątrz aplikacji klienckiej. Aplikacja serwerowa zawiera tylko liczby i tekst. Wobec tego jest w pełni legalnym użycie go w celach edukacyjnych.*

## Aplikacje serwerowe nieoficjalnych serwerów WoW

Kto tworzy oprogramowanie serwerowe (potocznie nazywane emulatorem), dzięki któremu można uruchomić prywatny serwer WoW? I jak on to zrobił?



### Złożoność

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Nie musisz być ekspertem, aby zrozumieć, że napisanie aplikacji serwerowej dla MMORPG o tak dużym zasięgu, jak World of Warcraft, nie jest dziecięcą igraszką.

Blizzard jest dużą firmą z tysiącami pracowników. Napisanie programu, który imituje działanie ich aplikacji serwerowej, zdecydowanie nie jest trywialne i wykonalne dla pojedynczej osoby (lub małej grupy programistów).

Nie jest to tylko kwestia złożoności. Pomyślmy o każdej bardzo trywialnej, ale powtarzalnej czynnności jak dodanie każdego NPC do świata, uwzględniając każdy jeden przedmiot, który może z nich paść z procentowym prawdopodobieństwem jego uzyskania itd. Straszna praca. Nie wspominając w ogóle o wszystkich złożonych zadaniach, które wymagają godzin studiowania i testowania - takich jak mechanika czarów, mechanika przeciwników itd.

Po krótce - nawet najlepszy programista na świecie nie byłby w stanie zrobić całej tej pracy samodzielnie.

Jednak serwery prywatne istnieją i oprogramowanie do ich uruchomienia również. Niektóre serwery prywatne są teraz w stanie zaoferować jakość rozgrywki nieodbiegającą wiele od oryginału (tutaj odwołuję się głównie do starych dodatków).

Jak jest to możliwe?

### MaNGOS i otwartoźródłowy model rozwoju oprogramowania

> Jeśli ty masz jabłko i ja mam jabłko, i wymienimy się tymi jabłkami, to wtedy ty i ja wciąż będziemy mieli po jednym jabłku. Ale jeśli ty masz pomysł i ja mam pomysł, i wymienimy się tymi pomysłami, to wtedy obaj będziemy mieli dwa pomysły. (George Bernard Shaw)

Upraszczając: program otwartoźródłowy to taki, którego kod jest publiczny.

W kontekście serwerów prywatnych, otwarte źródła pełnią kluczową rolę.

Niektórzy gracze-weterani mogą pamiętać, że niegdyś jakość gry na prywatnych serwerach pozostawiała wiele do życzenia. Prawie nic nie działało. Na przykład jeśli grałeś rogue'em w stealth mogłeś zostać stargetowany przez każdą osobę, która wpisała `/target TwojeImie`. Zgadnij, którą klasę wybrałem dla mojej pierwszej postaci...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Prawdziwą rewolucją okazał się [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), czyli open-source'owy projekt powstały w 2005, którego celem było stworzenie serwera (aplikacji) World of Warcraft.
Wspaniałą wiadomością o MaNGOS, poza jego siłą, był fakt, że był on aplikacją otwartoźródłową. Jego kod był całkowicie publiczny i każdy użytkownik na świecie mógł przestudiować go i zaoferować swój wkład (zarówno w kontekście dodawania lub naprawy mechanik, ale także przy raportowaniu bugów).


Jedynie w ten sposób, dzięki udziałowi wielu wolontariuszy z różnych krajów, było możliwe stworzenie aplikacji serwerowej, która będzie w stanie emulować World of Warcraft, zapewniając wyższą jakość rozgrywki.

W 2009 roku powstał inny, bazujący na MaNGOS, emulator - [TrinityCore](https://www.trinitycore.org/).

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Do dziś znaczna większość prywatnych serwerów korzysta z oprogramowania bazującego na MaNGOS/TrinityCore.

Przez lata powstawały [różne projekty](http://mangosrumors.org/best-wow-emulator-2020/) i bazowały one na kodzie MaNGOS/TrinityCore, różniąc się głównie wspieraną wersją WoW. 
Na przkład [AzerothCore](https://www.azerothcore.org/) dla 3.3.5, [OregonCore](https://github.com/OregonCore) dla 2.4.3, [SkyFire](https://www.projectskyfire.org/) dla 5.4.8, [CMaNGOS](https://cmangos.net/) dla Classic/TBC/WOTLK, oraz wiele innych... Bazujących na MaNGOS i/lub TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Podsumowanie

Prywatne serwery osiągnęły obecną jakość jedynie dzięki udziałowi wielu współautorów (contributors), którzy na przestrzeni lat (od 2005 do dzisiaj) zaimplementowali coraz więcej funkcjonalności.

Dzisiaj każdy doświadczony użytkownik komputera, niebędący programistą, może z łatwością zainstalować serwer WoW.

## Open source vs serwery prywatne

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hipotetyczny scenariusz

Załóżmy, że zarówno Alice i Bob mają swój prywatny serwer WoW. Załóżmy również, że korzystają z tej samej wersji gry.
Zarówno Alice, jak i Bob chcą wypuścić nową zawartość (content) dla swoich graczy, która dotychczas była niedostępna, bo bossy `A`, `B`, `C` oraz `D` były zbugowane.

- Alice jest bardzo dobrą programistką i potrafi naprawić bossa `A` oraz `B`
- Bob jest wciąż początkującym programistą i naprawił jedynie bossa `C`.

### W idealnym świecie

Alice i Bob pracują wspólnie i wymieniają się swoimi poprawkami. W wyniku czego, oba serwery mają w pełni działające bossy `A`, `B` oraz `C`.
W dodatku, Alice i Bob połączą siły aby naprawić również bossa `D`.

Ostatecznie gracze na obu serwerach są zadowoleni, bo grają na w pełni naprawionym contencie.

### W świecie rzeczywistym

Alice i Bob rywalizują ze sobą i ich serwery walczą między sobą. Na serwerze Alice działają jedynie bossy `A` i `B`. Tymczasem na serwerze Boba jedynie boss `C`.
Niektórzy gracze z serwera Boba przenoszą się na serwer Alice. Sewer Boba zamyka się po jakimś czasie. Niektórzy gracze Alice przestali grać, ponieważ mieli dość robienia jedynie bossów `A` oraz `B`, ponieważ bossy `C` oraz `D` nie działają.

W wyniku powyższego, gracze na obu serwerach są mniej szczęśliwi niż w poprzednim scenariuszu. Alice zarobiła więcej pieniędzy poprzez dotacje, niż zarobił Bob.

### Licencja emulatorów WoWa

W zasadzie, kod MaNGOS/TrinityCore (oraz pochodzących od nich rpoejtków) jest wypuszczony pod [licencją GNU GPL](https://pl.wikipedia.org/wiki/GNU_General_Public_License).

W uproszczeniu treść licencji brzmi: używaj kodu jak ci się podoba, bez płacenia za niego, tak długo jak zmiany do tego kodu są wypuszczane pod tą samą licencją.
Reasumując - licencja tych projektów wymaga od użytkowników, by upublicznili i udostępnili swoje zmiany w kodzie.

Oczywiście, większość serwerów używa tej licencji jako **papieru toaletowego**. W przeciwnym wypadku, nie byłoby serwera "lepiej naprawionego" niż inne.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Kłamstwa o prywatnych serwerach

Oto lista kłamstw, które powtarzają administratorzy prywatnych serwerów:


### "Napisaliśmy ten emulator"

Fake news. Nie ma znaczenia ile zmian "ty" zrobiłeś. Wszyscy zaczeliśmy od projektu bazującego na MaNGOS.

Może napisałeś jakieś poprawki, ale większość kodu to wciąż MaNGOS/TrinityCore.

Może jesteś naprawdę dobry i przepisałeś większość kodu przez ostatnie lata. Wciąż zacząłeś od MaNGOSa. Bez niego, pierwszego dnia, nie miałbyś nawet działającego mechanizmu logowania.

### "Naprawiliśmy X"

W większości przypadków nikt z nich niczego nie naprawił.
Po prostu pobrali poprawki pochodzące od społeczności, która rozwija oprogramowanie open-source i zaaplikowali je do "swojego" emulatora.
Niemniej, wciąż przypisują sobie wszystkie zasługi.

### "NAPRAWDĘ naprawiliśmy X"

Niektóre serwery prywatne naprawdę naprawiają pewne rzeczy samodzielnie. Mają często zespół deweloperski, który jest opłacany z dotacji pochodzących od graczy.

Większość z nich nie dzieli się poprawkami ze społecznością programistyczną.

Cóż, społeczność, która dała (za darmo) oprogramowanie, z którego korzystasz, by prowadzić swój serwer, prosi cię byś się podzielił z nią, ale wciąż tego nie robisz. Więc i tak cię nienawidzę.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## "Usprawiedliwianie się" serwerów prywatnych


### "Nie dzielę się nimi, bo chcę by mój serwer był wyjątkowy, lepszy niż inne."

Fantastycznie mistrzu. To teraz pomyśl o tym: jeśli WSZYSCY programiści zrobiliby tak jak ty, to ani ty, ani twój prywatny serwer by nie istniały.

Dlaczego? A dlatego, że ani MaNGOS (ani TrinityCore, AzerothCore, etc ...) by nie istniały.
Te projekty istnieją dzięki programistom którzy, w przeciwieństwie do ciebie, dzielą się swoim kodem.

Jeśli wszyscy programiści nie upublicznialiby swojego kodu, nie mielibyśmy żadnego sensownego emulatora WoWa, a ty nie mógłbyś otworzyć swojego prywatnego serwera, bo nie miałbyś na czym bazować.


### "Jeśli udostępnię swoje poprawki, to konkurencja je ukradnie"

Tu nie ma co "kraść". Nie mogą "ukraść" tego kodu, bo on nie "należy" do Ciebie. Nie, nawet jeśli to ty go napisałeś.

Idea otwartego oprogramowania jest jasna: możesz korzystać z kodu za darmo, przy czym każda modyfikacja MUSI być publiczna.

Oh, nie zgadzasz się? W porządku. To nie używaj żadnego otwartoźródłowego oprogramowania i napisz swój emulator WoW od podstaw. 

## W jaki sposób to wpływa na graczy

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Zdaję sobie sprawę, że ta cała historia o etyce i licencjach znaczy bardzo niewiele dla przeciętnego gracza World of Warcraft.
Gracze po prostu chcą grać na stabilnym i dobrze załatanym serwerze. Nie obchodzi ich za bardzo, czy serwer współpracuje z społecznością open-source, czy nie.

Ale... spróbuj spojrzeć na to z innej perspektywy.

Developerów projektów open-source (MaNGOS, TrinityCore, AzerothCore, etc ...) nie obchodzi, co robią serwery prywatne.
Oczywiście, jako developera wkurza Cię, gdy jakiś przypadkowy admin serwera przypisuje sobie Twoją pracę, ale ostatecznie nie zmienia to Twojego życia.
Wielu programistów robi to dla zabawy i chęci rozwoju.

Jeśli WSZYSTKIE serwery prywatne współpracowałyby w duchu open-source, to życia graczy by się zmieniły całkowicie.
Wiecie, w tym przypadku każdy serwer mógłby dostarczyć dużo lepsze doświadczenie z grania na jakimkolwiek dodatku. Przytaczany wcześniej przykład Alice i Boba również można do tego zaliczyć.

Rzeczywitość jest taka: jest mnóstwo serwerów prywatnych dookoła świata, każdy z nich pracuje nad tymi samymi problemami, ścigając się w tym, kto napisze poprawkę szybciej i lepiej.
Jeśli współpracowaliby ze sobą zamiast rywalizować, uniknęliby niepotrzebnej pracy i mieliby więcej czasu oraz mocy przerobowych. Zdecydowanie mogliby osiągnąć dużo więcej.

*Notka: jakość (i rywalizacja) prywatnych serwerów nie powinny polegać (tylko) na naprawianiu, ale również innych czynnikach - takich jak umięjętności zarządzających nimi administratorów. Jakość społeczności pełni fundamentalną rolę, dokładnie tak jak na serwerach Blizzarda (które są równe z technicznego punktu widzenia).*

Jeśli prywatny serwer się zamyka, a jego developerzy nie podzielą się swoją pracą, to ich praca przepada na zawsze.

## Demaskowanie kłamstw

### Oficjalna lista twórców

Najbardziej interesującą rzeczą jest to, że wszystkie projekty bazujące na MaNGOS są w pełni publiczne, zatem możliwe jest bardzo dokładne sprawdzenie, kto kontrybuował do nich.

W związku z powyższym - listy wszystkich kontrybutorów tych projektów są całkowicie publiczne i KAŻDY jest w stanie sprawdzić, kto i co naprawił.

Dla przykładu:

- Oficjalna lista współtwórców MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Oficjalna lista współtwórców TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Oficjalna lista współtwórców AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: Możesz znaleźć autora tego artykułu na każdej z tych list.

### Lista oficjalnych commitów

Każdy projekt otwartoźródłowy (generalnie - hostowany na GitHubie) posiada listę commitów zrealizowanych przez różnych programistów. Każdy commit posiada informację o autorze i dacie, kiedy został wykonany. 

Jest bardzo łatwo zweryfikować takie informacje - otwórz oficjalne repozytorium danego emulatora. Na przykład wyszukaj w Google "TrinityCore github" albo "AzerothCore github" i spójrz.

Zobaczysz, kto się czym zajmuje. Zobaczysz wszystkie linie kodu, ich autorów, komentarze innych deweloperów itd. Zobaczysz wszystko. Koniec z kłamstwami!


## Co mogę zrobić jako gracz?

Moja rada to: graj i wspieraj serwery prywatne, które współpracują z środowiskami open-source, niezależnie od dodatku czy emulatora, z którego korzystają. 

Albo przynajmniej unikaj serwerów które rozpuszczają plotki, przypisując sobie cudzą pracę i usuwając informacje o oryginalnych autorach.


### Naucz się więcej o darmowym oprogramowaniu

- https://www.gnu.org/software/software.pl.html
- https://www.fsf.org/about/what-is-free-software


## Podziękowania

Specjalne podziękowania dla *Laury Bartiromo*
