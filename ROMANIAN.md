# De ce urăsc majoritatea serverelor WoW private

*Scris de Francesco Borzi' aka Shin*

De ce sunt înca asa multe buguri în serverele WoW private, deși ele există de atâția ani?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Nu vă faceți griji, aceasta nu este o lecție obișnuită privind drepturile de autor ale Blizzard.
Doar vreau să explic de ce urăsc majoritatea serverelor [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft) private.

## Introducere

Am fost fascinat de emulația WoW de când aveam 14 ani. Îmi amintesc prima dată când m-am alăturat unuia dintre aceste “realmuri speciale”, pline de buguri, dar cel puțin te puteai juca gratis. Ştii tu, nu aveam un leu în buzunar pe vremea aia, deci nu aveam altă variantă.

La vârsta de 15 ani am început să mă întreb cum de există și funcționează serverele private, în special din punct de vedere tehnic. A furat cineva codul de la [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment) poate? N-aveam idee  – Am fost așa tânăr și nepriceput pe vremea aia! În ciuda acestui fapt, Am început să mă prostesc și, cu ajutorul unui vechi prieten (Fabio) am reușit în cele din urmă să instalez un server WoW pe propriul meu computer.

În acel moment nici nu mi-am putut imagina cât de satisfacut am fost și câte lucruri am învățat multumită acestei lumi magice.

Poate suna ciudat, dar această lume înca mă fascinează și acum, ca adult, încât am scris o întreagă [teză de master în informatică pe această temă](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Dar totuși: **Urăsc majoritatea serverelor private și vreau să explic de ce.**

## Câțiva termeni tehnici

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Pentru a vă face punctul meu de vedere mai ușor de înțeles, trebuie să intru într-o mică paranteză tehnică despre procesele de lucru WoW, pe care voi încerca să le exprim în cuvinte simple.

### Cum funcționează „originalul” World of Warcraft

La nivel de software, există două programe care ar putea fi considerate principalii actori ai acestui joc:

- **APLICAȚIA CLIENT** - este programul real „World of Warcraft” care este instalat de fiecare jucător pe computerul său pentru a avea acces la joc;

- **APLICAȚIA SERVER**: acesta este programul care rulează pe computerele server.

Procesul este foarte simplu: toți clienții (jucătorii) se conectează la un server pentru a interacționa între ei. Clientul cunoaște adresa serverului, deoarece este stocată în celebrul fișier „realmlist.wtf” (de aceea trebuie să modificați acest fișier pentru a trece la alt server).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Cum funcționează serverele private WoW

Când jucați pe servere private, principiul este exact același. Diferența constă în software-ul pe care îl utilizați.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**. Toată lumea are acces la clientul original World of Warcraft. Îl puteți obține cu ușurință cumpărându-l sau descărcându-l online. Acest program este exact cel pe care l-ați folosi pentru a juca pe serverul oficial. Evident, diferite servere private au versiuni de client diferite, dar se referă întotdeauna la clientul original. Trebuie doar să faceți o mică modificare a fișierului „realmlist.wtf”, înlocuind adresa serverului cu amănuntul cu cea a unui server privat. Asta e tot.

**SERVER**. Acesta este complet diferit. Nimeni din afara Blizzard nu are acces la software-ul original care rulează serverele oficiale World of Warcraft. Deci, aceste aplicații sunt complet diferite de cea originală.

### Inginerie inversă

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Fiecare software care rulează servere private a fost creat prin tehnica de „inginerie inversă”, care, în cuvinte simple, înseamnă "încerc să scriu un program care imită comportamentul unui alt program, fără a privi codul original".

Acum întrebarea este: cine a implementat acest software și când s-a întâmplat?


#### Remarcă privind drepturile de autor

*Întregul material protejat prin drepturi de autor (imagini, sunete, modele 3D, sigle etc ...) se află în interiorul aplicației client.
Aplicația server conține numai numere și texte. Prin urmare, este absolut legal dacă îl utilizați în scopuri educaționale.*

## Aplicatiile server WoW neoficiale

Cine creează aplicațiile software care rulează serverele private WoW (denumite în mod obișnuit „emulatoare”)? Și cum au făcut-o?



### Complexitate

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Nu trebuie să fiți un expert pentru a înțelege că scrierea unei aplicații server pentru un MMORPG cu o țintă atât de mare precum World of Warcraft nu este cu siguranță o joacă de copii.

Blizzard este o companie mare cu mii de angajați. Scrierea unui program care „imită” funcționarea aplicației lor de server nu este cu siguranță banală sau fezabilă pentru o singură persoană (sau un grup mic de programatori).

Și nu este doar o chestiune de complexitate. Să ne gândim la sarcini foarte banale, dar repetitive, cum ar fi adăugarea fiecărui NPC în lume, inclusiv fiecare obiect cu propria șansă procentuală de loot etc. O treabă îngrozitoare, practic. Ca să nu mai vorbim de toate sarcinile foarte complexe care necesită ore de studiu și testare, cum ar fi mecanica spelurilor, mecanica boșilor etc.

Pe scurt ... nici măcar cel mai bun programator din lume nu ar putea să facă toată această muncă pe cont propriu.

Cu toate acestea, există servere private și software-ul care le face să ruleze. Și unele servere private pot acum să ofere o calitate a jocului care nu este departe de cea originală (aici mă refer în principal la vechile expansiuni).

Cum este posibil?

### MaNGOS și modelul de dezvoltare open source

> Dacă tu ai un măr și eu am un măr și vom face schimb între aceste două mere, tu și cu mine vom avea în continuare câte un măr fiecare. Dar, dacă tu ai o idee și eu am o idee și vom face schimb între aceste idei, atunci fiecare dintre noi va avea două idei. (George Bernard Shaw)

Doar pentru a simplifica: un program open source este un program al cărui cod este public.

În contextul serverelor private, open source joacă un rol fundamental.

Unii jucători veterani își pot aminti că odată calitatea jocului pe serverele private era foarte proastă. Aproape nimic nu a funcționat.
De exemplu, dacă ai fi un rogue invizibil, ai putea fi vizat de oricine a scris „/ target Numele tau”. Ghiciți ce clasă am ales pentru primul meu caracter ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Adevărata revoluție a fost [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), un proiect open source creat în 2005, al cărui scop era să ofere o aplicație server pentru World of Warcraft.
Vestea extraordinară despre MaNGOS, precum și tăria sa a constat în faptul că, codul era pe deplin public sub forma open source și orice utilizator din întreaga lume putea să-l studieze și să-și ofere propria contribuție (atât în ceea ce privește adăugarea sau remedierea mecanicii jocului, dar și în ceea ce privește raportarea erorilor).

Numai în acest fel, datorită contribuției multor voluntari de diferite naționalități, a fost posibilă dezvoltarea unei aplicații server capabile să emuleze World of Warcraft cu o calitate a jocului mai înaltă.

În 2009 alt proiect important a luat naștere [TrinityCore](https://www.trinitycore.org/), bazat pe MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Până în prezent, majoritatea covârșitoare a serverelor private rulează pe aplicații bazate pe MaNGOS / TrinityCore.

De-a lungul anilor, [diferite proiecte](http://mangosrumors.org/best-wow-emulator-2020/) au luat naștere, și au fost bazate pe codul MaNGOS / TrinityCore, care variază în principal în funcție de versiunea WoW acceptată.
De exemplu [AzerothCore](https://www.azerothcore.org/) pentru 3.3.5, [OregonCore](https://github.com/OregonCore) pentru 2.4.3, [SkyFire](https://www.projectskyfire.org/) pentru 5.4.8, [CMaNGOS](https://cmangos.net/) pentru Classic/TBC/WOTLK, și multe altele ... Toate bazate pe MaNGOS și / sau TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Recapitulare

Așadar, serverele private au atins o astfel de calitate numai datorită multor colaboratori care au implementat din ce în ce mai multe funcții în joc de-a lungul anilor (din 2005 până astăzi).

Astăzi, orice utilizator experimentat pe computer poate instala cu ușurință un server WoW, fără a fi chiar programator.

## Open source vs servere private

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Scenariu ipotetic

Să presupunem că Alice și Bob au fiecare un server privat și să presupunem că se află pe aceeași versiune a jocului.
Atât Alice, cât și Bob vor să lanseze un nou conținut pentru jucătorii lor, care a fost închis până acum, deoarece boșii „A”, „B”, „C” și „D” sunt destul de eronați.

- Alice este un dezvoltator foarte bun și poate remedia ambii boși `A` și` B`
- Bob este încă un începător și remediază doar bosul `C`

### Într-o lume ideală

Alice și Bob lucrează împreună și își schimbă soluțiile. Ca urmare, ambele servere vor avea boși perfect fixați „A”, „B” și „C”.
În plus, Alice și Bob își vor uni forțele pentru a-l lucra și pe „D”.

Drept urmare, jucătorii de pe ambele servere sunt foarte fericiți, deoarece joacă un conținut complet fixat.

### În lumea reală

Alice și Bob sunt rivali și, prin urmare, își duc războiul unul împotriva celuilalt. În serverul lui Alice, funcționează doar boșii `A` și` B`. În timp ce în serverul lui Bob funcționează doar `C`.
Unii jucători trec de la serverul lui Bob la cel al lui Alice. Serverul lui Bob se închide după un timp. Unii dintre jucătorii serverului Alice se opresc din joc deoarece se satură să facă întotdeauna doar „A” și „B” pentru că „C” și „D” nu funcționează.

Drept urmare, jucătorii ambelor servere sunt mai puțin fericiți decât în scenariul anterior. Alice a câștigat mai mulți bani prin donațiile jucătorilor decât Bob.

### Licența emulatoarelor WoW

În realitate, codul MaNGOS / TrinityCore (și proiectele lor derivate) este eliberat în cadrul [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

În simple cuvinte, această licență spune următoarele: folosiți codul pentru a face orice doriți, fără a plăti nimic, atâta timp cât orice modificare a codului original este eliberată sub aceeași licență.
Practic, licența acestor proiecte impune celor care le folosesc să publice orice modificare facută.

Desigur, majoritatea serverelor private folosesc această licență ca ** hârtie igienică **. Altminteri, nu ar trebui să existe niciun server privat care să fie „mai bine reparat” decât altul.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Minciunile despre serverele private

Aici este o listă de minciuni pe care administratorii multor servere private WoW le spun jucătorilor lor:


### „Noi am scris acest nucleu”

Știri false. Nu contează câte modificări ați făcut „voi”. Cu toate acestea, ați început cu un proiect bazat pe MaNGOS.

Poate că ați făcut unele îmbunătățiri, dar majoritatea codului este încă MaNGOS / TrinityCore.

Poate că ești foarte bun și ai rescris majoritatea codului de-a lungul anilor. Totuși, ați început de la MaNGOS. Fără aceasta, în ziua 1 nici măcar nu ați avea funcția de conectare funcțională.

### "Am reparat X"

În marea majoritate a cazurilor, niciunul dintre ei nu au remediat cu adevărat nimic.
Tocmai au descărcat remedierile provenite de la comunitatea open source și le-au aplicat în nucleul lor.
Cu toate acestea, iau toate creditele.

### "Chiar am reparat X"

Unele servere private chiar repară lucrurile pe cont propriu. De multe ori au echipe de dezvoltare dedicate care sunt plătite cu banii proveniți din donațiile jucătorilor.

Majoritatea nu împărtășesc aceste remedieri comunității open source.

Ei bine, comunitatea care a oferit (gratuit) software-ul pe care îl utilizați pentru a vă rula serverul vă cere să le partajați, dar îl păstrați totuși privat. Așa că vă urăsc oricum.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## "Justificarea" serverelor private


### "Le păstrez private pentru ca serverul meu să devină un loc special, mai bun decât celelalte"

Bine campionule. Încercați să vă gândiți la acest lucru: dacă TOȚI dezvoltatorii v-ar copia, nici dvs., nici serverul dvs. privat nu ar exista.

De ce? Pur și simplu pentru că nici MaNGOS (și nici TrinityCore, AzerothCore etc.) nu ar exista.
Aceste proiecte există datorită dezvoltatorilor care, spre deosebire de dvs., și-au împărtășit codul.

Dacă toți dezvoltatorii își păstrau codul privat, nu am avea un emulator WoW decent și pur și simplu nu v-ați putea deschide serverul privat, deoarece nu ar exista niciun software disponibil.


### "Dacă mi-aș împărtăși remedierile, concurența le-ar fura"

Nu este nimic de „furat”. Nu pot „fura” codul respectiv, deoarece nu vă „aparține”. Nu, nici dacă chiar l-ai scris.

Filozofia open source este clară: puteți utiliza codul gratuit, cu condiția ca orice modificare a acestuia TREBUIE să fie făcută publică.

Nu ești de acord? Bine. Atunci, nu utilizați niciun cod open source și scrieți propriul tau emulator WoW de la zero.

## Cum afectează acest lucru jucătorii

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Înțeleg total că întreaga poveste despre etică și licențe contează foarte puțin pentru jucătorul mediu World of Warcraft.
Jucătorii doresc doar să joace pe un server stabil și bine fixat, nu le pasă prea mult dacă acest server colaborează cu open source sau nu.

Dar ... încearcă o clipă să o vezi dintr-o altă perspectivă.

Dezvoltatorilor de proiecte open source (MaNGOS, TrinityCore, AzerothCore, etc ...) practic nu le pasă prea mult de ceea ce fac serverele private.
Desigur, ca dezvoltator te enervează să vezi un administrator de server aleatoriu care își ia credite pentru munca ta, dar până la urmă nu îți schimbă viața.
Mulți dezvoltatori open source o fac doar în scopuri distractive și educative.

De fapt, dacă TOATE serverele private ar colabora cu open source, viața jucătorilor s-ar schimba complet!
Știți, în acest caz, fiecare server ar oferi o experiență de joc mult mai bună pentru orice expansiune. Exemplul lui Alice și Bob menționat anterior poate fi aplicat și în acest caz.

Cu toate acestea, realitatea este doar asta: există multe servere private în întreaga lume, fiecare dintre ele lucrează întotdeauna la aceleași lucruri, alergând pentru a le face mai repede și mai bine.
Dacă ar colabora între ei, ar evita să facă o muncă inutilă și ar avea mai mult timp și forță de muncă. Deci, cu siguranță ar fi în măsură să realizeze mult mai mult.

* Notă: calitatea (și concurența dintre) serverele private nu ar trebui să fie (numai) de remediere, ci și de alți factori, cum ar fi abilitățile administratorilor săi în gestionarea acestuia. Calitatea comunității joacă, de asemenea, un rol fundamental, la fel cum se întâmplă pe serverele Blizzard (care sunt toate egale din punct de vedere tehnic). *

Dacă un server privat se închide și dezvoltatorii săi nu și-au împărtășit munca, munca respectivă se va pierde pentru totdeauna.

## Expunerea minciunilor

### Lista oficială a autorilor

Cel mai interesant lucru este că toate proiectele bazate pe MaNGOS sunt pe deplin publice, astfel încât se poate verifica exact cine a contribuit la acestea.

Ca rezultat, lista tuturor contribuitorilor la aceste proiecte este complet publică și ORICINE poate verifica cine si ce a remediat.

De exemplu:

- Lista oficială a colaboratorilor MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Lista oficială a colaboratorilor TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Lista oficială a colaboratorilor AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: îl puteți găsi pe autorul acestui articol în toate aceste liste

### Lista oficială de remedii

Orice proiect open source (găzduit în general pe GitHub) are lista remedierilor realizate de diferiții dezvoltatori. Fiecare remediere include atât autorul, cât și data.

Este foarte ușor să verificați aceste informații, trebuie doar să deschideți depozitul oficial al oricărui emulator. Google, de exemplu, „TrinityCore github” sau „AzerothCore github” și doar aruncă o privire.

Veți vedea cine face cu adevărat ce. Veți vedea toate liniile de cod, autorii acestora, comentariile altor dezvoltatori etc. Veți vedea totul. Gata cu minciunile!


## Ce pot face ca jucător?

Sfatul meu este să jucați / să susțineți servere private care colaborează cu open source, în ciuda tipului de expansiune și emulator pe care îl folosesc.

Sau, cel puțin, evitați acele servere care-și atribuie munca altor persoane, eliminând creditele de la autorii originali.

**NEW:** în 2021 noul proiect [ChromieCraft](https://www.chromiecraft.com/about) a fost lansat, un server open-source complet cu un stil twink-progresiv.

![ChromieCraft logo](https://avatars1.githubusercontent.com/u/68329413?s=400&u=084b35243e0aed1becd6a67fa88717eb8c1674d8&v=4)

### Aflați mai multe despre software-ul gratuit

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Mulțumiri

Mulțumiri speciale *Laura Bartiromo*
