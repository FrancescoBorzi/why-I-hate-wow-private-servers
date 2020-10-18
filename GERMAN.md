# Warum ich die meisten WoW P-Server hasse

*Geschrieben von Francesco Borzi' aka Shin*

Warum gibt es noch immer so viele Bugs auf Privat Servern, obwohl sie schon seit so vielen Jahren existieren?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Keine Sorge, das hier wird keine übliche Copyright-Belehrung über Blizzard.
Ich möchte nur erklären, warum ich die meisten [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft) Privat Server hasse.

## Einführung

Ich bin von der WoW-Emulation fasziniert, seit ich 14 Jahre alt bin. Ich erinnere mich, dass, als ich das erste Mal einem dieser "sonderbaren Servern" beitrat, eine Menge Bugs gesehen habe, aber man konnte zumindest umsonst spielen. Wisst ihr, damals hatte ich keinen einzigen Cent, also hatte ich keine Alternative. 

Mit 15 begann ich mich zu fragen, wie private Server tatsächlich funktionieren und existieren könnten, insbesondere aus technischer Sicht. Hat jemand den Code von [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment) gestohlen? Ich hatte keine Ahnung - ich war so jung und unerfahren zu dieser Zeit! Trotzdem fing ich an, herumzualbern, und mit der Hilfe eines alten Freundes (Fabio) gelang es mir schließlich, einen WoW-Server auf meinem eigenen PC zu installieren.

Damals konnte ich mir nicht einmal vorstellen, wie zufrieden ich gewesen wäre und wie viele Dinge ich dank dieser magischen Welt gelernt hätte.

Es mag für euch komisch klingen, aber ich war so davon fasziniert, das ich eine ganze [Masterarbeit in Informatik](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation) zu dem Thema geschrieben habe.

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Trotzdem: **Ich hasse die meisten privaten Server und ich möchte erklären, warum.**

## Einige Fachbegriffe

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Um euch meinen Standpunkt verständlich zu machen, muss ich auf eine kleine technische Klammer über WoW-Arbeitsprozesse eingehen, die ich versuchen werde, in einfache Worte zu fassen.

### Wie das "ursprüngliche" World of Warcraft funktioniert

Auf der Software-Ebene gibt es zwei Programme, die als die Hauptakteure dieses Spiels betrachtet werden könnten:

- die **CLIENT ANWENDUNG** - das ist das eigentliche "World of Warcraft"-Programm, das von jedem Spieler auf seinem Computer installiert wird, um Zugang zum Spiel zu erhalten;

- die **SERVER ANWENDUNG**: das ist das Programm, das auf den Server-Rechnern läuft.

Das Verfahren ist sehr einfach: alle Clients (Spieler) verbinden sich mit einem Server, um miteinander zu interagieren. Der Client kennt die Adresse des Servers, da sie in der berühmten Datei "**realmlist.wtf**" gespeichert ist (deshalb müsst Ihr diese Datei ändern, um zu einem WoW P-Server zu wechseln).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Wie WoW Privat Server funktionieren

Wenn Ihr auf einem WoW P-Server spielt, ist das Prinzip genau dasselbe. Der Unterschied liegt in der Software, die Ihr verwendet.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**. Jeder hat Zugriff auf den ursprünglichen World of Warcraft-Client. Ihr könnt ihn leicht erhalten, indem Ihr ihn kauft oder online herunterladet. Dieses Programm ist genau das Programm, mit dem Ihr auf den offiziellen Servern spielen würdet. Selbstverständlich haben verschiedene private Server verschiedene Client-Versionen, aber sie beziehen sich immer auf den Original-Client. Ihr müsst nur eine kleine Änderung an der Datei "realmlist.wtf" vornehmen umd die Adresse des Original Servers durch die Adresse eines privaten Servers ersetzen. Das ist alles.

**SERVER**. Das ist etwas völlig anderes. Niemand außerhalb von Blizzard hat Zugriff auf die Originalsoftware, die auf den offiziellen World of Warcraft-Servern läuft. Diese Anwendungen unterscheiden sich also völlig von der Originalsoftware.

### Reverse Engineering (Nachkonstruktion)

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Jede Software, die auf privaten Servern läuft, wurde durch die "Reverse Engineering"-Technik erstellt, was in einfachen Worten bedeutet: "Ich versuche, ein Programm zu schreiben, das das Verhalten eines anderen Programms imitiert, ohne den Originalcode zu betrachten".

Die Frage ist nun: Wer hat diese Software implementiert und wann ist das geschehen?


#### Exkurs über das Urheberrecht

*Das gesamte urheberrechtlich geschützte Material (Bilder, Töne, 3D-Modelle, Logos usw. ...) befindet sich innerhalb der Client-Anwendung.
Die Server-Anwendung enthält nur Zahlen und Texte. Daher ist es absolut legal, wenn Sie sie für Bildungszwecke verwenden.*

## Inoffizielle WoW-Server-Anwendungen

Wer erstellt die Software-Anwendungen, die die privaten Server von WoW (allgemein "Emulatoren" genannt) betreiben? Und wie haben sie das gemacht?



### Komplexität

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Man muss kein Experte sein, um zu verstehen, dass das schreiben einer Serveranwendung für ein MMORPG mit einem so großen Umfang wie World of Warcraft sicherlich kein Kinderspiel ist.

Blizzard ist ein großes Unternehmen mit Tausenden von Mitarbeitern. Ein Programm zu schreiben, das den Betrieb ihrer Serveranwendung "imitiert", ist sicherlich nicht trivial oder für eine einzelne Person (oder eine kleine Gruppe von Programmierern) machbar.

Und es ist nicht nur eine Frage der Komplexität. Denken wir an sehr triviale, aber sich wiederholende Aufgaben, wie das Hinzufügen jedes einzelnen NPCs in die Welt, einschließlich jedes einzelnen Gegenstandes ihrer Beute mit seinem eigenen Prozentsatz der Chance, usw. . Im Grunde eine großartige Arbeit. Ganz zu schweigen von all den sehr komplexen Aufgaben, die stundenlanges Studieren und Testen erfordern, wie z.B. Zaubermechaniken, Bossmechaniken, usw.

Kurz gesagt: ..... Nicht einmal der beste Programmierer der Welt könnte all diese Arbeit allein bewältigen.

Dennoch gibt es Privat Server und die Software, die sie zum Laufen bringt. Und einige Privat Server sind jetzt in der Lage, eine Spielqualität anzubieten, die nicht weit von der ursprünglichen Qualität entfernt ist (hier beziehe ich mich hauptsächlich auf die alten Erweiterungen).

Wie ist das möglich?

### MaNGOS und das Open-Source-Entwicklungsmodell

> Wenn du einen Apfel hast und ich habe einen Apfel, und wir tauschen diese Äpfel aus, dann hast du und ich immer noch je einen Apfel. Aber wenn du eine Idee hast und ich eine Idee habe und wir diese Ideen austauschen, dann wird jeder von uns zwei Ideen haben. (George Bernard Shaw)

Nur um es einfach zu machen: Ein Open-Source-Programm ist ein Programm, dessen Code öffentlich ist.

Im Zusammenhang mit Privat Servern spielt die "Open Source" eine fundamentale Rolle.

Einige erfahrene Spieler erinnern sich vielleicht daran, dass die Spielqualität auf privaten Servern einmal wirklich schlecht war. Fast nichts funktionierte.
Wenn du zum Beispiel ein unsichtbarer Schurke warst, konntest du von jedem ins Visier genommen werden, der `/target <Dein Name>` schrieb. Rate mal, welche Klasse ich für meinen ersten Charakter gewählt habe ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

Die wahre Revolution war [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), ein 2005 gegründetes Open-Source-Projekt, dessen Zweck es war, eine Serveranwendung für World of Warcraft bereitzustellen.
Die große Neuigkeit von MaNGOS, aber auch seine Stärke, war die Tatsache, dass sein Code als Open-Source-Anwendung vollständig öffentlich war und jeder Benutzer aus der ganzen Welt ihn studieren und seinen eigenen Beitrag leisten konnte (sowohl in Bezug auf das Hinzufügen oder Beheben von Spielmechaniken, aber auch in Bezug auf das Melden von Fehlern).

Nur auf diese Weise, dank des Beitrags vieler Freiwilliger verschiedener Nationalitäten, war es möglich, eine Serveranwendung zu entwickeln, die World of Warcraft mit einer höheren Spielqualität emulieren kann.

Im Jahr 2009 wurde ein weiteres wichtiges Projekt geboren: [TrinityCore](https://www.trinitycore.org/), basierend auf MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Bis heute läuft die große Mehrheit der Privat Servern auf MaNGOS/TrinityCore-basierten Anwendungen.

Über die Jahre wurden, [verschiedene Projekte](http://mangosrumors.org/best-wow-emulator-2020/) geboren, und sie basierten auf dem MaNGOS/TrinityCore-Code, die hauptsächlich je nach der unterstützten WoW-Version variieren.
Als Beispiel hierfür [AzerothCore](https://www.azerothcore.org/) für 3.3.5, [OregonCore](https://github.com/OregonCore) für 2.4.3, [SkyFire](https://www.projectskyfire.org/) für 5.4.3, [CMaNGOS](https://cmangos.net/) für Classic/TBC/WOTLK, und viele weitere ... Sie alle basieren auf MaNGOS und/oder TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Zusammenfassung

Die Privat Server haben eine solche Qualität also nur dank der vielen Mitwirkenden erreicht, die im Laufe der Jahre (von 2005 bis heute) immer mehr Spielfunktionen implementiert haben.

Heute kann jeder erfahrene PC-Benutzer problemlos einen WoW-Server installieren, ohne selbst Programmierer zu sein.

## Open Source vs. P-Server

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Hypothetisches Szenario

Nehmen wir an, dass Alice und Bob jeweils einen Privat Server haben, und nehmen wir an, sie befinden sich auf derselben Version des Spiels.
Sowohl Alice als auch Bob wollen ihren Spielern einen neuen Inhalt zur Verfügung stellen, der bisher geschlossen wurde, weil die Bosse `A`, `B`, `C` und `D` ziemlich fehlerhaft sind.

- Alice ist eine sehr gute Entwicklerin und kann beide Bosse `A` und `B` reparieren
- Bob ist noch ein Anfänger und repariert nur den Boss `C`

### In einer idealen Welt

Alice und Bob arbeiten zusammen und tauschen ihre Lösungen aus. Das Ergebnis ist, dass ihre beiden Server die Bosse `A`, `B` und `C` perfekt korrigiert haben.
Darüber hinaus werden Alice und Bob ihre Kräfte vereinen, um auch an `D` zu arbeiten.

Das Ergebnis ist, dass die Spieler auf beiden Servern sehr zufrieden sind, weil sie einen komplett funktionierenden Inhalt spielen.

### In der realen Welt

Alice und Bob sind Rivalen, und so führen sie Krieg gegeneinander. In Alices Server funktionieren nur die Bosse `A` und `B`. Während in Bobs Server nur `C` funktioniert.
Einige Spieler wechseln von Bobs Server zu Alices Server. Bobs Server schließt nach einer Weile. Einige Spieler von Alices Server hören auf zu spielen, weil sie es leid sind, immer nur `A` und `B` zu spielen, weil `C` und `D` nicht funktionieren.

Infolgedessen sind die Spieler auf beiden Servern weniger glücklich als im vorherigen Szenario. Alice hat durch Spenden mehr Geld verdient als Bob.

### Die Lizenz der WoW-Emulatoren

Tatsächlich wird der MaNGOS/TrinityCore-Code (und die davon abgeleiteten Projekte) unter der [GNU GPL Lizenz](https://en.wikipedia.org/wiki/GNU_General_Public_License) veröffentlicht.

In einfachen Worten sagt diese Lizenz folgendes: Verwenden Sie den Code, um zu tun, was immer Sie wollen, ohne etwas zu bezahlen, solange jede Änderung am Originalcode ebenfalls unter derselben Lizenz veröffentlicht wird.
Grundsätzlich verlangt die Lizenz dieser Projekte, dass diejenigen, die sie benutzen, alle Änderungen der Öffentlichkeit zugänglich machen.

Natürlich verwenden die meisten Privat Server diese Lizenz als **Toilettenpapier**. Ansonsten sollte es keinen Privat Server geben, der "besser gefixt" ist als andere.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Die Lügen über die privaten Server

Hier ist es eine Liste von Lügen, die die Administratoren vieler privater WoW-Server ihren Spielern immer wieder erzählen:


### "Wir haben diesen Core erstellt"

Fake News. Es spielt keine Rolle, wie viele Änderungen "Du" vorgenommen hast. Du hast jedoch mit einem MaNGOS-basierten Projekt begonnen.

Vielleicht hast Du einige Verbesserungen vorgenommen, aber der größte Teil des Codes gehört immer noch zu MaNGOS/TrinityCore.

Vielleicht bist Du wirklich gut und hast den größten Teil des Codes über die Jahre neu geschrieben. Trotzdem hast Du mit MaNGOS begonnen. Ohne MaNGOS hättest Du am 1. Tag nicht einmal die Anmeldefunktion zum Funktionieren gebracht.

### "Wir haben X repariert"

In den allermeisten Fällen hat keiner von euch wirklich etwas repariert.
Du hast einfach nur die Korrekturen aus der Open-Source-Gemeinschaft heruntergeladen und sie in deinem Core angewendet.
Dennoch nimmst Du alle Lorbeeren ein.

### "Wir haben X (wirklich) repariert"

Einige private Server reparieren Dinge wirklich von sich aus. Sie haben oft dedizierte Entwicklungsteams, die mit dem Geld aus Spenden bezahlt werden.

Die meisten von ihnen teilen diese Fehlerbehebungen nicht mit der Entwicklergemeinde.

Nun, die Gemeinschaft, die Ihnen die Software, die Sie zum Betrieb Ihres Servers verwenden, (kostenlos) zur Verfügung gestellt hat, bittet Dich darum, diese weiterzugeben, aber Ihr behaltet sie trotzdem privat. Ich hasse euch also trotzdem.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## Die "Rechtfertigungen" der Privat Server


### "Ich behalte sie privat, um meinen Server zu einem besonderen Ort zu machen, besser als die anderen"

Alles klar, du Held. Versuch, darüber nachzudenken: Wenn ALLE Entwickler es so machen würden wie du, würde es weder dich noch deinen Privat Server geben.

Und warum? Ganz einfach, weil weder MaNGOS (noch TrinityCore, AzerothCore, usw. ...) existieren würde.
Diese Projekte existieren dank der Entwickler, die, im Gegensatz zu Dir, ihren Code mit anderen geteilt haben.

Wenn alle Entwickler ihren Code privat hielten, hätten wir keinen anständigen WoW-Emulator und Ihr könntet euren Privat Server einfach nicht öffnen, weil es keine Software gäbe.


### "Wenn ich meine Korrekturen teilen würde, würde die Konkurrenz sie stehlen"

Es gibt nichts zu "stehlen". Sie können diesen Code nicht "stehlen", weil er Dir nicht "gehört". Nein, nicht einmal, wenn Du ihn wirklich geschrieben hast.

Die Open-Source-Philosophie ist klar: Du kannst diesen Code kostenlos verwenden, vorausgesetzt, dass jede Änderung daran öffentlich gemacht werden MUSS.

Meinst D nicht auch? In Ordnung. Dann verwende keinen Open-Source-Code und schreib Deinen eigenen WoW-Emulator von Grund auf neu.

## Wie sich dies auf die Spieler auswirkt

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Ich verstehe vollkommen, dass diese ganze Geschichte über Ethik und Lizenzen für den durchschnittlichen Spieler von World of Warcraft sehr wenig Bedeutung hat.
Spieler wollen einfach nur auf einem stabilen und gut gescripteten Server spielen, ihnen ist es egal, ob dieser Server mit Open Source zusammenarbeitet oder nicht.

Aber... versucht einen Moment lang, es aus einer anderen Perspektive zu sehen.

Die Entwickler der Open-Source-Projekte (MaNGOS, TrinityCore, AzerothCore, etc ...) kümmern sich im Grunde genommen nicht viel darum, was Privat Server tun.
Natürlich ärgert es Sie als Entwickler, wenn Sie sehen, wie irgendein zufälliger Server-Administrator Credits für Ihre Arbeit bekommt, aber am Ende ändert das nichts an Ihrem Leben.
Viele Open-Source-Entwickler tun es nur aus Spaß und zu Bildungszwecken.

Eigentlich, wenn ALLE Privat Server mit Open Source zusammenarbeiten würden, würde sich das Leben der Spieler komplett ändern!
Weisst du, in diesem Fall würde jeder Server ein viel besseres Spielerlebnis für jede Erweiterung bieten. Das bereits erwähnte Beispiel von Alice und Bob lässt sich auch auf diesen Fall anwenden.

Die Realität ist jedoch genau das: Es gibt viele Privat Server auf der ganzen Welt, jeder von ihnen arbeitet immer an den gleichen Dingen und rast darum, sie früher und besser zu erledigen.
Wenn Ihr stattdessen miteinander zusammenarbeiten würdet, würdet Ihr unnötige Arbeit vermeiden und hättet mehr Zeit und Arbeitskräfte. So könntet Ihr sicherlich viel mehr erreichen.

*Bemerkung: Die Qualität (und der Wettbewerb zwischen) Privat Servern sollte sich nicht (nur) auf die Fehlerbehebung beziehen, sondern auch auf andere Faktoren wie die Fähigkeiten der Administratoren, diese zu verwalten. Die Qualität der Community spielt ebenfalls eine fundamentale Rolle, genau wie bei den Blizzard-Servern (die aus technischer Sicht alle gleich sind).*

Wenn ein Privat Server geschlossen wird und seine Entwickler ihre Arbeit nicht freigegeben haben, ist diese Arbeit für immer verloren.

## Lügen aufdecken

### Offizielle Autorenliste

Das Interessanteste daran ist, dass alle MaNGOS-basierten Projekte vollständig öffentlich sind, so dass genau überprüft werden kann, wer zu ihnen beigetragen hat.

Infolgedessen ist die Liste aller Mitwirkenden dieser Projekte absolut öffentlich, und JEDER kann überprüfen, wer was tatsächlich festgelegt hat.

For example:

- Offizielle Liste der MaNGOS-Beitragsleistenden: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Offizielle Liste der TrinityCore-Mitwirkenden: https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Offizielle Liste der AzerothCore-Mitwirkenden: https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: Ihr könnt den Autor dieses Artikels in all diesen Listen finden

### Liste der offiziellen Commits (Beiträgen zur Entwicklung)

Jedes Open-Source-Projekt (in der Regel auf GitHub gehostet) hat die Liste der Commits, die von den verschiedenen Entwicklern realisiert wurden. Für jeden Commit sind sowohl der Autor als auch das Datum angegeben.

Es ist sehr einfach, diese Informationen zu überprüfen, öffnet einfach das offizielle Repository eines beliebigen Emulators. Google zum Beispiel "TrinityCore github" oder "AzerothCore github" und schau einfach nach.

Ihr werdet sehen, wer wirklich was macht. Ihr seht alle Codezeilen, ihre Autoren, die Kommentare anderer Entwickler usw. Ihr werdet alles sehen. Es gibt keine Lügen mehr!


## Was kann ich als Spieler tun?

Mein Rat ist, dass Du Privat Server spielen/unterstützen solltest, die mit Open Source zusammenarbeiten, trotz der Art der Erweiterung und des Emulators, die sie verwenden.

Oder vermeide zumindest solche Server, die die Arbeit anderer Leute auf eigene Faust verhökern, indem sie die Credits der Originalautoren entfernen.


### Erfahren Sie mehr über Open Source Software

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Danke

Besonderer Dank gilt *Laura Bartiromo*
