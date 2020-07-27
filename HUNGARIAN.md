# Miért utálom a legtöbb privát WoW szervert?
* írta: Francesco Borzi aka Shin *

Miért van még mindig ilyen ilyen rengeteg rossz minőségű privát szerver ennyi év után is?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Ne aggódjatok, ez nem az általános szerzői jog lecke a Blizzard-ról. Csak szeretném kifejteni, hogy miért utálom a legtöbb privát WoW szervert.

## Bevezető

14 éves korom óta elbűvölt a WoW emuláció. Emlékszem az első alkalomra amikor csatlakoztam az egyik ilyen "speciális realm-re". Tele volt hibákkal, de legalább ingyen tudtam játszani. Tudjátok abban az időben egy fillérem sem volt, tehát nem volt más lehetőségem.

15 éves koromban elkezdtem tanakodni azon, hogy is működik és létezhet valójában egy ilyen privát szerver technikai szemszögből. Talán ellopta volna valaki a forráskódot a Blizzard-tól? Fogalmam sem volt. Fiatal voltam és tapasztalatban akkoriban. Ennek ellenére elkezdtem bütykölni és egy barátom - Fabio - segítségével végre összeállítottam egy szervert a saját számítógépemen.

Akkoriban el sem tudtam képzelni azt az elégedettséget, örömöt és azt a sok mindent amit ettől a varázslatos világtól tanultam.

Furcsán hangozhat, de ez a világ a mai napig elbűvöl még felnőttként is. Annyira, hogy a [mester diplomám disszertációját](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation) erről írtam.

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Mindezek ellenére még mindig utálom a szerverek többségét.

## Néhány technikai fogalom

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Ahhoz, hogy megértsd a nézőpontomat, el kell magyarázzak pár technikai dolgot a WoW működéséröl. Megpróbálom egyszerűen.

### Ahogy az eredeti World of Warcraft működik

Szoftveres szinten 2 programot tekinthetünk a játék fő komponensének.

- A kliens applikácó : ami valójában az aktuális World of Warcraft telepítés minden játékos számítógépén, hogy elérjék a szervereket.

- A szerver applikáció:  ami a Blizzard szerverein fut.

A folyamat nagyon egyszerű: minden kliens csatlakozik a szerverhez, hogy a játékosok tudjanak egymással kommunikálni. A kliens tárolja a szerver  hozzáférési címét, ami a híres "realmlist.wtf" fájlban van tárolva. (Ezért kell módosítanod a fájlt, ha más szerverre szeretnél csatlakozni.)

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Ahogy a privát WoW szerverek működnek
Alapvetően ugyanaz az elv, csak a használt programokban van különbség.
![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

Kliens applikácó: mindenki számára elérhető az eredeti WoW kliens. Egyszerüen csak megvesszük vagy letöltjük. Ez teljesen ugyanaz a program, amit az eredeti szerveren való játékhoz használnál. Természetesen különböző privát szerverek más és más kliens verziókat használhatnak, de mindenesetben az eredeti kliensre hivatkoznak. Neked csak a "realmlist.wtf" fájlban kell lecserélned a hivatalos szerver címét az általad választott szerver címével.

Szerver applikáció: Ez teljesen eltérő a hivatalos verziótól. Senkinek sincs hozzáférése az eredeti Blizzard által használt szerverszoftver forráskódjához - ezért is emulálunk.
### Reverse engineering - avagy "fordított fejlesztés"
![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Minden emulátor (szerver applikáció) ezzel a technikával készült. Röviden: ez eredeti forráskód ismerete nélkül fejlesztünk olyan programot, ami képes arra, mint az eredeti.
A kérdés: Ki és mikor találta ki mindezt?

#### Kitérő a szerzői jogra

* A teljes szerzői jog védelme alatt álló tartalom (képek, hangok, 3D modellek, logók stb ...) a kliens applikációban található. Az emulátor kizárólag számokat és betűket tartalmaz. Ezért teljesen legális ezeket oktatási célokra használni.*

## Az emulátorok
Ki és hogyan készíti az emulátorokat?


### Összetettség
![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Nem kell hozzáértőnek lenned, hogy megértsd: egy ilyen MMORPG emulátor fejlesztése, mint a WoW, nem gyerekjáték.

A Blizzard egy nagy cég, több ezer alkalmazottal. Egy emulátor fejlesztése nem 1 embernek, mégcsak nem is egy kis csapatni programozónak való feladat.

Mindazonáltal ez nem csak az összetettségről szól. Csak gondoljunk a legegyszerű ismétlődő feladatokra: az NPC-k elhelyezése, annak loot táblájának beállítása minden tárggyal. Alapvetően egy borzalmas feladat. A többi, összetettebb feladatot ami órákat vesz igény nem is említve. Például: Boss mechanizmusok, spell mechanizmusok tesztelése.

Röviden: a világ legjobb programozója sem lenne erre képes egyedül.
Nekünk mégis itt vannak a privát szerverek és az emulátorok. Néhány szerver az eredetihez nagyon hasonló játékélményt tud nyújtani.
Hogyan lehetséges ez?

### MaNGOS és a nyílt forráskódú (open source) fejlesztés
> Ha mindkettőnknek van egy almája és cserélünk, mindkettőnknek ugyanúgy lesz egy almája. Viszont ha mindkettőnknek van egy ötlete és cserélünk, akkor mindkettőnknek 2 ötlete lesz. (George Barnard Shaw)

Egyszerűség kedvéért: a nyílt forráskódú programok forráskódjai mindenki számára elérhetőek.

Az emulátorok fejlesztésében az open-source alapvető és meghatározó szerepet játszik.

Néhány veterán játékos még emlékszik talán, hogy mennyire rossza volt a privát szerverek minősége. Szinte semmi sem működött. Például ha rogue-ként stealth-ben voltál, a /target teneved segitségével még mindig ki tudtak jelölni. Vajon mit választottam első karakteremként?...
![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

A valódi áttörést a MaNGOS nyílt forráskódú project megalapítása jelentette 2005-ben. A célja egy emulátor létrehozása volt. A MaNGOS legnagyob erőssége az, hogy nyílt forráskódú. Ezáltal bárki szabadon tanulmányozhatta és hozzájárulhatot a fejlődéséhez - ahogy csak tudott. Legyen az tényleges programkód vagy csak hibák jelentése.

Csak ezúton lehetett elérni - rengeteg különböző nemzetiségű önkéntés segítségével - azt, hogy egy olyan emulátor jöjjön létre, ami sokkal jobb játékélményt tud nyújtani.

2009-ben született egy másik fontos project ami a MaNGOS alapjain nyugszik: TrinityCore.
![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Mind a mai napig a legtöbb privát szerver MaNGOS/TrinityCore alapú emulátort használ.

Az évek alatt több különböző project is születtett a különböző WoW kiegészítők megjelenésével, amik szintén MaNGOS/TrinityCore alapokon nyugszanak. Például: AzerothCore for 3.3.5, OregonCore for 2.4.3, SkyFire for 5.4.3, CMaNGOS for Classic/TBC/WotLK. És még sok másik. Mindegyik közös alapokon:  MaNGOS/TrinityCore.
![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Visszatekintés

Csak az önkéntes hozzájárulóknak köszönhető, akik egyre több és több funkciót tettek elérhetővé a játékban, hogy ilyen jó minőségű emulátorok léteznek napjainkban. 
Olyanok, amiket bárki, akár programozói tapasztalat nélkül is képes üzembe helyezni a saját számítógépén.
## Nyílt forráskód vs privát szerverek
![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Az elméleti eset

Tegyük fel, hogy Alice és Bob mindketten privát szerver tulajdonosok. Valamint feltételezzük, hogy mindketten a játék ugyanazon verziójával foglalkoznak.
Mindketten új kontentet akarnak elérhetővé tenni a szerverükön, ami eddig nem volt elérhető mert A B C D bossok hibásak voltak.

Alice egy nagyon jó fejlesztő, kijavította A és B bossokat.
Bob még csak egy kezdő, csak a C bosst tudta kijavítani.
### Az ideális világban

Alice és Bob együtt dolgoznak és megosztják egymással a fixeiket. Ennek eredményeként A B C bossok mindkettjük szerverén működni fognak. Valamint ennek eredményeként egyesítik erőforrásaikat és együtt dolgoznak D bosson.

Ennek ereményeként mindkét szerver játékosai boldogok, mert minden boss működik és szinte hibátlan a kínált kontent.
### A való világban

Alice és bob riválisok, szinte háborúban állnak egymással. Alice szerverén csak A és B bossok funkcionálnak, míg BoB szerverén csak a C. Néhány játékosok BoB szerveréről Alice-hez vándorol. BoB szervere bezár. Ezekután Alice szerverén a játékosok abbahagyják a játékot, mivel unalmas mindig csak A és B bossokat gyilkolni mert C és D nem működik.

Ennek eredménye, hogy a játékosok sokkal rosszabbul járnak, mitn az ideális esetben. Valamint Alice több támogatást zsebelt be, mint Bob.
### A WoW emulátorok licensze
MaNGOS / TrinityCore és az összes ezeken alapuló project a GNU GPL licensz alatt áll.
A licensz tartalma egyszerűsítve: bármire használhatod a forráskódot díjmentesen, mindaddig míg az általad végzett módosítások szintén a [GNU GPL licensz](https://en.wikipedia.org/wiki/GNU_General_Public_License) alatt állnak .

Alapvetően a licensz megköveteli, hogy a módisításaidat  tedd publikussá.
Természetesn a legtöbb privátszerver ezt a licenszt WC papírként használja. Máskülönben nem lenne egyik szerver jobb a másiknál.
![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Privát szerverek és a hazugságok
Egy kis lista, amit a privát szerver tulajdonosok ismételgetnek a játékosaiknak:

### " Mi fejlesztettük ezt az emulátort"

Kamu. Abszolút nem számít ti mennyi módosítást végeztetek, mindent egy MaNGOS alapú emulátorral kezdtétek. Valamint valószínű, hogy a forráskód legjava még mindig MaNGOS/TrinityCore.
Talán tényleg nagyon jók vagytok és még a forráskód legjavát is átdolgoztátok. Mégis: MaNGOS az alap, nélküle mégcsak be sem tudtatok volna logolni a játékba az első napon.
### " Mi kijavítottuk ezt és ezt"

A legtöbb esetben ti nem tesztek semmit, csak a letöltitek a a nyílt forráskódot használó közösség javításait és hozzáadjátok a forráskódhoz.
### " Mi (tényleg) kijavítottuk ezt és ezt"

Néhány szerveren tényleg van ilyen. Ahol a szerveren befojt támogatás egy részét fizetett fejlesztőkre fordítják. Ezeket a fixet természetesen nem teszik közzé a szervertulajdonosok.

Nos, a MaNGOS/TrinityCore alapú emulátor licensze megköveteli, hogy megoszzák ezeket. - Tehát igen, utálom a privát szervereket.
![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## ítélkezés a privát szerverek felett


### " Megtartom a fixeim, hogy jobb legyek a többieknél."
Rendben, akkor gondolj csak erre: ha MINDEN fejlesztő úgy tett volna, mint te, akkor te szervered sem létezne.

Miért? Mert se a MaNGOS sem a TrinityCore nem létezne. Ezek azért léteznek, mert ellenben veled, ezek a fejlesztők megosztották a forráskódjaikat.

Ha minden fejlesztő zárt forráskóddal dolgozna, nem lenne jó minőségű emulátor. Tehát te sem nyithattad volna meg a szerveredet, mert nem lenne emulátorod.

### " Ha megosztanám a fixeim, a konkurencia lenyúlná."

Nincs mit lenyúlni, mert ez nem a TE forráskódod. Még akkor sem, ha saját magad írtad.

A nyílt forráskód filozófiája egyszerű és tiszta: díjmentesen használhatod a forráskódot, de minden modosítást nyílttá KELL tenned.

Nem értesz egyet? Rendben. Akkor ne használj nyílt forráskódú szoftvereket. Fogd magad és fejlessz sajátot a nulláról.

## Hogyan hat mindez a játékosokra?
![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Én teljesen megértem, hogy ez a teljes történet abszolút nem érdekli, szinte semmit sem jelent az átlag WoW játékosnak. Ők csak egy stabil és jól működő szerveren szeretnének játszani attól függetlenül, hogy nyílt forráskódú az emulátor vagy sem.

De egy pillanatra próbáljátok más szemszögből nézni ezt az egészet.

Alapvetóen a nyilt forráskódú projectek (MaNGOS, TrinityCore, AzerothCore) fejlesztőit nem érdekli, hogy mit csinál egy privát szerver tulajdonosa. Természetesen, mint fejlesztő, bosszantja őket, ha magadénak hirdeted az ő munkájukat. Végeredményben nem változtat az életükön. Valamennyien csak a móka vagy tanulás kedvéért csinálják. De képzeld magadat a helyükbe.


Mindazonáltal gondolj bele Alice és Bob példáján keresztül: ha minden szerver megosztaná amilye van, nem kellene rengeteg időt ugyanarra a dologra fordítani, versenyezni a másikkal ki fixeli ezt vagy azt hamarabb. Sokkal több erőforrás lenne szabad arra, amit még senki sem fixelt.

Megjegyzés: a privát szerverek közti versengés nem csak arról kellene szóljon, hogy mi mennyire működik. Az adminisztrátorok hozzáértése, a közösség menedzselése mind fontos. Egy jó közösség alapvető szerepet játszik csakúgy, mint az eredeti Blizzard szervereken.

Ha egy privátszerver bezárja kaput, a munka mind a semmibe vész amennyiben a forráskód nem nyílt.
## A hazugságok leleplezése

### Hivatalos szerzők listája
A legérdekesebb dolog, hogy minden MaNGOS alapú project teljesen publikjus. Tehát lehetséges, hogy leellenőrizzük pontosan kik is járultak hozzá.

Ennek eredménye, hogy a hozzájárulók listája teljesen nyilvános és bárki megtekintheti.

Például:
- MaNGOS https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

Megjegyzés: e cikk írója mindhárom listán megtalálható.
### Eredeti fixek listája

Minden - általában GitHub-on hosztolt - nyílt forráskódú projectnek van egy listája a különböző fejlesztők fixeiről (commit-ek). Minden fixhez tartozik egy szerzó (author) és dátum.

Nagyon egyszerű ellenőrizni ki és mit csinál. Csak keress rá a project github oldalára, például: "TrinityCore github" vagy "AzerothCore github" és vess rá egy pillantást.

Minden ott lesz előtted. Ki, mit, mikor. A teljes forráskód, más fejlesztők megjgyzései stb ... Nincs több hazugság!

## Mit tehetek én, a játékos?
Azt tanácsolom, hogy olyan privát szerveren játssz, ami elfogadja az open-source filozófiát. De legalábbis kérlek, hogy kerüld az olyan szervereket, ahol mások más tollával ékeskednek.


### Tudj meg többet az ingyen szoftverekről


- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Köszönet

Külön köszönet Laura Bartimoro-nak!*

