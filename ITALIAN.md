# Perché odio la maggior parte dei server privati di WoW

Perché i server privati continuano ad essere pieni di **bug**, nonostante esistono da tantissimi anni?

![wow-facepalm](http://pureawesome.net/wow/110404_facepalm.jpg)

No, non si tratta della solita ramanzina sul copyright, la Blizzard, etc...
Voglio solo spiegarvi perché odio la maggior parte de server privati di [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft).

## Introduzione

Il mondo dei server privati di WoW mi ha affascinato sin dal primo momento, quando avevo 14 anni ed entravo per la prima volta in questi reami speciali dove, a quei tempi, tutto era buggatissimo, ma potevi giocare senza pagare niente. Essendo totalmente al verde, non avevo altre alternative.

A 15 anni iniziai a chiedermi come funzionassero davvero i server privati e come fosse possibile la loro esistenza, tecnicamente parlando. Qualcuno aveva rubato il codice alla [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment)? Non ne avevo idea, ero giovane e totalmente ignorante in materia. Ma iniziai a smanettare e, con l'aiuto di un amico più grande di me (Fabio), riuscii finalmente ad installare un server di WoW nel mio PC.

A quei tempi non avevo ancora idea di quante soddisfazioni avrei avuto e quante cose avrei imparato grazie a questo mondo magico.

Sembrerà strano, ma questo mondo mi affascina tantissimo anche adesso, da adulto. Mi ha affascinato così tanto da dedicarci pure la mia tesi di laurea di Informatica.

Rimane però questo fatto: **odio la maggior parte dei server privati e ho tanta voglia di spiegarvi il perché.**


## Tecnicismi

![wow-sleeping](https://vignette.wikia.nocookie.net/wowwiki/images/2/22/Sleeping_undead.jpg/revision/latest/scale-to-width-down/180?cb=20050308164208)

Per spiegarvi il mio punto di vista è necessaria una piccola parentesi tecnica riguardante il funzionamento di WoW, che proverò a spiegare con parole semplici.

### Come funziona World of Warcraft (originale)

A livello di software, ci sono due programmi che sono gli attori principali di questo gioco:

- l'**APPLICAZIONE CLIENT**: sarebbe il programma "World of Warcraft" che ogni giocatore installa nel proprio computer per poter accedere al gioco.

- l'**APPLICAZIONE SERVER**: è il programma che gira nelle macchine server

Il funzionamento è molto semplice: tutti i Client (i giocatori) si collegano ad un Server per poter interagire tra loro. Il client conosce l'indirizzo del server perché lo ha memorizzato dentro il famoso file "**realmlist.wtf**" (ecco perché per cambiare server bisogna modificare questo file).

![client-server](https://static.wixstatic.com/media/132132_a149ee7a94d04ea1b5ea8295b73bb939.jpg/v1/fill/w_421,h_310,al_c,lg_1,q_80/132132_a149ee7a94d04ea1b5ea8295b73bb939.webp)

### Come funzionano i server privati

Quando si gioca nei server privati, il principio è esattamente lo stesso. La differenza sta nei programmi utilizzati.

![wow-defias](http://pureawesome.net/wow/2016/160419_defias02a.jpg)

**CLIENT**. Tutti hanno accesso al client originale di World of Warcraft. è possibile ottenerlo banalmente acquistandolo o scaricandolo da internet. Questo programma è esattamente lo stesso che si userebbe per giocare nel server ufficiale. Ovviamente server privati diversi hanno versioni del client diverse, ma sono sempre versioni del client originale. Per questo basta fare una piccola modifica al file "realmlist.wtf", sostituire l'indirizzo del server offy con quello di un server privato, ed il gioco è fatto.

**SERVER**. Qua il discorso cambia radicalmente. Nessuno, al di fuori della Blizzard, ha accesso ai software originali che fanno girare i server ufficiali di World of Warcraft. Quindi i programmi in questione sono totalmente diversi rispetto a quello originale.

### Reverse engineering

![reverse-engineering](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSq8szLp9BwRzL_q5cjSaWAkvTmM0AvbjqC0A&usqp=CAU)

Tutti i software che fanno girare i server privati sono state realizzati con la tecnica del "reverse engineering". Che in parole povere equivale a dire "provo a scrivere un programma che imita il funzionamento di un altro programma, senza però poter avere accesso al codice originale".

La domanda da porsi adesso è chi e quando ha implementato questi software.


#### Parentesi sul copyright

*Tutto il materiale coperto da copyright (immagini, suoni, modelli 3D, loghi, etc...) risiede nell'applicazione client.
L'applicazione server contiene esclusivamente valori numerici e testuali. Pertanto, se utilizzata a scopi didattici, è perfettamente legale.*


## Applicazioni server non ufficiali di WoW

Chi crea le applicazioni software che fanno girare i server privati di WoW (comunemente detti "emulatori") ? E come ci sono riusciti ?



### Complessità

![complex](https://static1.smartbear.co/smartbear/media/blog/wp/code-complexity-600x348.jpg)

Non c'è bisogno di essere esperti per comprendere che scrivere un applicazione server per un MMORPG della portata di World of Warcraft non è certamente un gioco da ragazzi.

La Blizzard è una grande azienda con migliaia di impiegati. Scrivere un programma che "imita" il funzionamento della loro applicazione server, non è certamente un qualcosa banale né fattibile da un singolo individuo (o da un piccolo gruppo di programmatori).

E non è solo questione di complessità. Si pensi anche a task molto banali ma ripetitivi, come aggiungere ogni singolo NPC nel mondo, incluso ogni singolo item del suo loot con la propria percentuale di chance, etc.. Un lavoro enorme insomma. Per non parlare di task molto complessi che richiedono ore e ore di studi e di test, come le meccaniche delle spell, dei boss, etc.

Insomma.... nemmeno il programmatore più bravo del mondo riuscirebbe a fare tutto questo lavoro da solo.

Eppure esistono i server privati, ed i software che li fanno girare. Ed alcuni server privati riescono ormai ad offrire una qualità di gioco non molto distante da quella originale (qui mi riferisco principalmente alle vecchie espansioni).

Com'è stato possibile tutto ciò ?


### MaNGOS ed il modello di sviluppo open source

> Se tu hai una mela, e io ho una mela, e ce le scambiamo, allora tu ed io abbiamo sempre una mela ciascuno. Ma se tu hai un’idea, ed io ho un’idea, e ce le scambiamo, allora abbiamo entrambi due idee. (George Bernard Shaw)

Giusto per dirla semplice: un programma open source è un programma il cui codice è pubblico.

Nell'ambito dei server privati, l'open source gioca un ruolo fondamentale.

I giocatori più veterani si ricorderanno che un tempo nei server privati la qualità di gioco era davvero pessima. Non funzionava quasi niente.
Ad esempio, se eri un rogue in stealth potevi essere targettato da chiunque avesse scritto `/target Tuonome`. Indovinate che classe era il mio primo personaggio...

![mangos-logo](https://azerothshard.org/wp-content/uploads/2015/10/MaNGOS_Logo.gif)

La vera rivoluzione fu [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), un progetto open source creato nel 2005, il cui scopo era fornire un'applicazione server per World of Warcraft.
La grande novità di MaNGOS, che fu anche il suo punto di forza, fu proprio il fatto che essendo un’applicazione open source, il suo codice veniva reso completamente pubblico, e qualunque utente da qualunque parte del mondo poteva studiarlo e proporre il proprio contributo (sia in termini di aggiunta o fix di meccaniche del gioco, ma anche in termini di segnalazione dei bug presenti).

Solo in questo modo, grazie ai contributi di tantissimi volontari di diverse nazionalità, si riuscì a sviluppare un’applicazione server in grado di emulare World of Warcraft garantendo una qualità di un certo livello.

Nel 2009 nasceva [TrinityCore](https://www.trinitycore.org/), basato su MaNGOS, altro progetto storicamente molto importante.

![trinitycore-logo](https://azerothshard.org/wp-content/uploads/2015/10/trinitycore.png)

Ad oggi, la stragrande maggioranza dei server privati girano su applicazioni basate su MaNGOS/TrinityCore.

Negli anni sono nati [diversi progetti](http://mangosrumors.org/best-wow-emulator-2020/) open source basati sul codice di MaNGOS/TrinityCore, che variano principalmente in base alla versione di WoW supportata.
Ad esempio [AzerothCore](https://www.azerothcore.org/) per la 3.3.5, [OregonCore](https://github.com/OregonCore) per la 2.4.3, [SkyFire](https://www.projectskyfire.org/) per la 5.4.3, [CMaNGOS](https://cmangos.net/) per Classic (e non solo), e molti altri... tutti basati su MaNGOS e/o TrinityCore.

![azerothcore-authserver](https://user-images.githubusercontent.com/18329778/41039336-5710165c-69c3-11e8-8631-0b6348a032c7.png)

### Riepilogando

Dunque nei server privati si è arrivati alla qualità di cui godiamo oggi solo grazie ai tantissimi contributori che nell'arco di tutti questi anni (dal 2005 ad oggi) hanno implementato sempre più funzionalità del gioco.

Banalmente, oggi chiunque abbia un minimo di dimestichezza col PC può riuscire ad installare facilmente un server di WoW, senza nemmeno dover necessariamente essere un programmatore.



## Open source vs server privati

![alice-and-bob](https://blogs.airdropalert.com/wp-content/uploads/2018/11/alice_bob-300x169.jpg)

### Scenario ipotetico

Supponiamo che Alice e Bob hanno un server privato ciascuno, e supponiamo che siano alla stessa versione del gioco.
Sia Alice che Bob vogliono rilasciare un nuovo content ai loro giocatori, che finora era chiuso in quanto i boss `A`, `B`, `C` e `D` sono parecchio buggati.

- Alice è una sviluppatrice molto in gamba e riesce a fixare sia i boss `A` che `B`
- Bob è ancora alle prime armi e riesce a fixare solamente il boss `C`

### In un mondo ideale

Alice e Bob collaborano tra loro e si scambiano i propri fix. Come risultato, entrambi i loro server avranno i boss `A`, `B` e `C` perfettamente fixati.
Inoltre Alice e Bob uniranno le loro forze per lavorare anche a `D`.

Come risultato, i players di entrambi i server sono molto contenti perché giocano con un content completamente fixato.

### Nel mondo reale

Alice e Bob sono rivali e quindi si fanno la guerra tra loro. Nel server di Alice, solo i boss `A` e `B` funzionano. Mentre in quello di Bob funziona solo `C`.
Alcuni giocatori si spostano dal server di Bob a quello di Alice. Il server di Bob dopo un po' chiude. Alcuni dei giocatori del server di Alice smettono di giocare perché stufi di fare sempre `A` e `B` in quanto `C` e `D` non funzionano.

Come risultato, i players di entrambi i server sono meno contenti rispetto allo scenario precedente. Pero' Alice ha guadagnato più soldi tramite le donazioni dei giocatori rispetto a Bob.

### La licenza degli emulatori di WoW

In realta' il codice di MaNGOS/TrinityCore (e progetti derivati) viene rilasciato sotto licenza [GNU GPL](https://en.wikipedia.org/wiki/GNU_General_Public_License).

Tale licenza, detto in parole semplici, dice la seguente: usa pure il codice per fare quello che ti pare, senza pagare nulla, a patto che qualsiasi modifica al codice originale, venga anch'essa rilasciata sotto la stessa licenza.
Praticamente la licenza di questi progetti imporrebbe a chi li utilizza di pubblicare qualsiasi modifica al core.

Ovviamente la maggior parte dei server privati usa questa licenza come **carta igienica**. Altrimenti non dovrebbero esistere server privati "più fixati" rispetto ad altri.

![toilet-paper](https://image.freepik.com/free-photo/pyramid-made-out-toilet-paper-rolls_23-2148524935.jpg)


## Le bugie dei server privati

Ecco una classifica delle bugie più comuni con cui gli amministratori dei server privati prendono in giro i propri giocatori:


### "Questo core l'abbiamo scritto noi"

Fake news. Non importa di quante modifiche "voi" abbiate fatto. Siete comunque partiti da un progetto MaNGOS-based.

Magari avete fatto qualche miglioria, ma la maggior parte del codice resta comunque quello di MaNGOS/TrinityCore.

Magari siete davvero bravi e nel tempo avete riscritto la maggior parte del codice.
Ma siete comunque partiti da MaNGOS. Senza di esso al day 1 non vi funzionerebbe nemmeno il login.



### "Abbiamo fixato X"

Nella stragrande maggioranza dei casi, nessuno di loro ha veramente fixato niente.
Semplicemente aggiornando il loro core, scaricando i fix che provengono dalla comunita' open source.
Quindi state spacciando per vostri fix fatti da altri.


### "Abbiamo (veramente) fixato X"

Alcuni server privati fixano davvero roba per conto loro. Spesso hanno team di sviluppo dedicati e pagati con i soldi provenienti dalle donazioni degli utenti.

La maggior parte di loro non condivide questi fix con la comunità' di sviluppo.

Beh, la licenza GPL del software che state usando per far girare il vostro server vi impone di condividerli, ma voi non lo fate. Quindi vi odio lo stesso.

![pinocchio](https://www.21secolo.news/wp-content/uploads/2020/02/pinocchio4-kTJG-U3010254149790Ae-1224x916@Corriere-Web-Sezioni-593x443-1.jpg)

## Le "giustificazioni" dei server privati


### "Li mantengo privati per rendere il mio server un posto speciale, migliore rispetto agli altri"

Ok campione. Prova a riflettere su questo: se TUTTI i dev avessero fatto come te, non esisteresti nemmeno tu ed il tuo server privato.

perché? Semplicemente perché non esisterebbe nè MaNGOS (ne TrinityCore, AzerothCore, etc...). 
Questi progetti esistono proprio grazie a dev che, a differenza tua, hanno condiviso il proprio codice.

A quel punto stavamo ancora senza emulatori di WoW decenti ed il tuo server privato non potevi proprio aprirtelo.


### "Se condividessi i miei fix, i server competitor se li ruberebbero"

Non c'è niente da "rubare". Quel codice non possono "rubartelo" perché non "appartiene" a te. No, nemmeno se lo hai scritto tu veramente.

La licenza GPL di MaNGOS parla chiaro: puoi usare gratuitamente quel codice, a patto che ogni sua modifica DEVE essere resa pubblica.

Non sei d'accordo? Benissimo. Allora non usare codice rilasciato sotto licenza GPL e scriviti davvero il tuo emulatore partendo da 0.



## Impatto sui giocatori

![wow-dranei-crying](https://thedaytonight.com/wp-content/uploads/2013/01/a-sad-wow-player-289x300.jpg)

Mi rendo conto perfettamente che tutta questa storia che parla di eticita' e licenze varie interessa davvero poco al giocatore medio di World of Warcraft.
I giocatori vogliono tendenzialmente giocare in un server stabile e ben fixato, gliene frega davvero poco se questo server collabora con l'open source o meno.

Pero' provate un attimo a vederla da un'altra prospettiva.

A dev dei vari progetti open source (MaNGOS, TrinityCore, AzerothCore, etc...) in fondo frega davvero poco quello che fanno i server privati.
Certo, fa incazzare vedere Tizio e Caio che spacciano il tuo fix per proprio, ma alla fine non cambia la vita.

Quelli a cui cambierebbe la vita davvero, se TUTTI i server privati collaborassero con l'open source, sarebbero proprio i giocatori.

Eh gia', perché se fosse cosi', TUTTI i server privati avrebbero una qualita' di gioco di gran lunga superiore a quella di cui godiamo oggi. In tutte le espansioni.

Vedi per esempio il caso di Alice e Bob di prima. Quello è un esempio molto semplificato, giusto per far capire il concetto.

Ma la realtà' è proprio questa: ci sono tanti server privati attorno al mondo, ognuno di loro lavora sempre alle stesse cose, facendo a gara a chi le fa prima/meglio.
Se invece collaborassero tra loro, eviterebbero di fare lavoro inutile e avrebbero più tempo e forza lavoro. Quindi riuscirebbero senza ogni dubbio a fare molto di più.

Parentesi: la qualità di un server privato non si dovrebbe misurare (solo) in termini di fix, ma in base a fattori come la bravura della sua amministrazione nel mantenerlo. Anche la qualità della community gioca un ruolo fondamentale, proprio come avviene nei server blizzard (che come fix sono tutti messi allo stesso modo).

Se un server privato chiude, ed i suoi sviluppatori non hanno condiviso il proprio lavoro, esso viene perduto per sempre.

## Smentire le bugie

### Elenco autori ufficiale

La cosa più interessante è che essendo tutti i vari progetti MaNGOS-based completamente pubblici, è possibile verificare accuratamente chi ne siano stati i contributori.

Come risultato, tutte le liste dei contributori di questi progetti sono assolutamente pubbliche e CHIUNQUE puo' verificare chi ha effettivamente fixato cosa.

Per esempio:

- Elenco ufficiale dei contributori di MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Elenco ufficiale dei contributori di TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Elenco ufficiale dei contributori di AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: l'autore di questo articolo è presente in tutti e 3 questi elenchi

### Elenco commits ufficiale

Qualsiasi progetto open source (generalmente hostato su GitHub) ha l'elenco dei commits effettuati dai vari dev. Per ogni commit, è presente sia l'autore che la data.

è molto facile verificare queste informazioni, basta aprire il repository ufficiale dell'emulatore in questione. Cercate su google per esempio "TrinityCore github" oppure "AzerothCore github" e date un'occhiata.

La’ vedrete chi-fa-davvero-cosa. Vedrete tutte le linee di codice, i loro autori, i commenti degli altri dev, etc...etc... Vedrete tutto. Niente più bugie.


## Cosa posso fare come giocatore?

Il mio consiglio è quello di giocare/supportare quei server privati che collaborano con l'open source. A prescindere da quale espansione ed emulatore utilizzino.

O quantomeno, evitare quei server che spacciano il lavoro altrui per proprio, rimuovendo i crediti agli autori originali.


### Approfondimenti sul software libero

- https://www.gnu.org/philosophy/free-sw.it.html
- https://www.linux.it/softwarelibero
- https://www.fsf.org/it/cosa-e-il-software-libero

