# Pourquoi je déteste la plupart des serveurs privés WoW

*Écrit par Francesco Borzi' alias Shin*

Pourquoi y a-t-il encore tant de bugs sur les serveurs privés WoW, alors qu'ils existent depuis tant d'années ?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Ne vous inquiétez pas, ce n'est pas une lecture des droits d'auteur concernant Blizzard.
Je veux juste vous expliquer pourquoi je déteste la plupart des serveurs privés [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft).


## Introduction

Je suis fasciné par l'émulation WoW depuis que j'ai 14 ans. 
Je me souviens que la première fois que j'ai rejoint un de ces "royaumes spéciaux", il y avait beaucoup de bugs, mais on pouvait au moins jouer gratuitement. 
Vous savez, je n'avais pas un sou à l'époque, donc je n'avais pas d'alternative. 

À 15 ans, j'ai commencé à me demander comment les serveurs privés fonctionnaient et pouvaient exister, surtout d'un point de vue technique. 
Quelqu'un a-t-il volé le code de [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment) peut-être ? Je n'en avais aucune idée - j'étais si jeune et inexpérimenté à cette époque ! 
Malgré cela, j'ai commencé à faire des bêtises et, avec l'aide d'un vieil ami (Fabio), j'ai finalement réussi à installer un serveur WoW sur mon propre PC.

À l'époque, je ne pouvais même pas imaginer le degré de satisfaction que j'aurais eu et le nombre de choses que j'aurais apprises grâce à ce monde magique.

Cela peut sembler bizarre, mais ce monde me fascine encore aujourd'hui, à l'âge adulte, au point que j'y ai consacré toute une [thèse de maîtrise en informatique] (https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Mais quand même : **Je déteste la plupart des serveurs privés et je veux vraiment expliquer pourquoi.**


## Quelques termes techniques

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Afin de comprendre mon point de vue, je dois m'attarder sur une petite parenthèse technique "Comment fonction Wow", que je vais essayer de formuler en termes simples.


### Comment fonctionne le World of Warcraft original

Au niveau des logiciels, deux programmes pourraient être considérés comme les principaux acteurs de ce jeu :

- l'**APPLICATION CLIENT** - qui est le véritable programme "World of Warcraft" installé par chaque joueur sur son ordinateur afin d'accéder au jeu ;

- l'**APPLICATION SERVEUR** : c'est le programme qui s'exécute sur les machines serveurs.

Le processus est très simple : tous les clients (joueurs) se connectent à un serveur afin d'interagir entre eux. 
Le client connaît l'adresse du serveur, car elle est stockée dans le fameux fichier "**realmlist.wtf**" (c'est pourquoi vous devez modifier ce fichier pour passer à un autre serveur).

![Client-serveur](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)


### Comment fonctionnent les serveurs privés WoW

Lorsque l'on joue sur des serveurs privés, le principe est exactement le même. 
La différence réside dans le logiciel que vous utilisez.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENT**. Tout le monde a accès au client original de World of Warcraft. Vous pouvez facilement l'obtenir en l'achetant ou en le téléchargeant en ligne. Ce programme est exactement celui que vous utiliseriez pour jouer sur le serveur officiel. Il est évident que les différents serveurs privés ont des versions différentes du client, mais ils se réfèrent toujours au client original. Il vous suffit d'apporter une petite modification au fichier "realmlist.wtf", en remplaçant l'adresse du serveur officiel par celle d'un serveur privé. C'est tout.

**SERVER**. C'est complètement différent. Personne en dehors de Blizzard n'a accès au logiciel original qui fait tourner les serveurs officiels de World of Warcraft. Donc ces applications sont complètement différentes de l'original.


### Rétro-ingénierie

![Rétro-ingénierie](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Tous les logiciels qui font tourner des serveurs privés ont été créés par la technique de la "rétro-ingénierie", qui signifie en termes simples "j'essaie d'écrire un programme qui imite le comportement d'un autre programme, sans regarder le code original".

La question qui se pose maintenant est la suivante : qui a mis en œuvre ce logiciel et quand cela s'est-il produit ?

#### Parenthèse sur le droit d'auteur

*Toutes les ressources protégé par des droits d'auteur (images, sons, modèles 3D, logos, etc...) se trouve dans l'application du client.
L'application serveur ne contient que des chiffres et des textes. Par conséquent, si elle est utilisée à des fins éducatives, elle est parfaitement légale.*


## Applications Serveur non officielles

Qui crée les applications logicielles qui font fonctionner les serveurs privés WoW (communément appelés "émulateurs") ? Et comment s'y prennent-ils ?


### Complexité

![Complexe](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Il n'est pas nécessaire d'être un expert pour comprendre qu'écrire une application serveur pour un MMORPG d'une telle envergure comme World of Warcraft n'est certainement pas un jeu d'enfant.

Blizzard est une grande entreprise qui compte des milliers d'employés. Écrire un programme qui "imite" le fonctionnement de leur application serveur n'est certainement pas trivial ou faisable pour un seul individu (ou un petit groupe de programmeurs).

Et ce n'est pas seulement une question de complexité. Pensons à des tâches très triviales mais répétitives, comme l'ajout de chaque NPC dans le monde, y compris chaque élément de leur butin avec son propre pourcentage de chance, etc. Un travail formidable, en gros. Sans parler de toutes les tâches très complexes qui nécessitent des heures d'étude et de tests, comme la mécanique des sorts, la mécanique des boss, etc.

Bref... même le meilleur programmeur du monde ne pourrait pas faire tout ce travail tout seul.

Pourtant, il existe des serveurs privés, et les logiciels qui les font fonctionner. Et certains serveurs privés sont maintenant capables d'offrir une qualité de jeu qui n'est pas loin de l'original (ici je me réfère principalement aux anciennes extensions).

Comment cela est-il possible ?


### MaNGOS et le modèle de développement open source

> Si tu as une pomme et que j'ai une pomme et que nous échangeons ces pommes, alors toi et moi aurons toujours une pomme chacun. Mais si vous avez une idée et que j'ai une idée et que nous échangeons ces idées, alors chacun de nous aura deux idées. (George Bernard Shaw)

Pour faire simple : un programme open source est un programme dont le code est public.

Dans le contexte des serveurs privés, l'open source joue un rôle fondamental.

Certains joueurs chevronnés se souviendront peut-être qu'autrefois la qualité des jeux sur les serveurs privés était vraiment mauvaise. Presque rien ne fonctionnait.
Par exemple, si vous étiez un voleur invisible, vous pouviez être ciblé par n'importe qui qui écrivait "/Cible Yourname". Devinez quelle classe était mon premier personnage ...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

La véritable révolution a été [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), un projet open source créé en 2005, dont le but était de fournir une application serveur pour World of Warcraft.
La grande nouveauté de MaNGOS, qui était aussi son point fort, était le fait qu'étant une application open source, son code était rendu entièrement public, et que tout utilisateur du monde entier pouvait l'étudier et apporter sa propre contribution (tant en termes d'ajout ou de correction des mécanismes du jeu, mais aussi en termes de signalement des bugs).

C'est seulement de cette manière, grâce aux contributions de nombreux volontaires de différentes nationalités, qu'il a été possible de développer une application serveur capable d'émuler World of Warcraft en assurant une qualité d'un certain niveau.

En 2009, un autre projet important est né [TrinityCore](https://www.trinitycore.org/), basé sur MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

À ce jour, l'écrasante majorité des serveurs privés fonctionnent sur des applications basées sur MaNGOS/TrinityCore.

Au fil des ans, [différents projets](http://mangosrumors.org/best-wow-emulator-2020/) ont vu le jour, et ils étaient basés sur le code MaNGOS/TrinityCore, qui varie principalement en fonction de la version WoW supportée.
Par exemple [AzerothCore](https://www.azerothcore.org/) pour la version 3.3.5, [OregonCore](https://github.com/OregonCore) pour la version 2.4.3, [SkyFire](https://www.projectskyfire.org/) pour la version 5.4.3, [CMaNGOS](https://cmangos.net/) pour Classic/TBC/WOTLK, et bien d'autres encore ... Tous sont basés sur MaNGOS et/ou TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)


### Récapitulatif

Les serveurs privés ont donc atteint une telle qualité uniquement grâce aux nombreux contributeurs qui ont mis en œuvre de plus en plus de fonctionnalités de jeu au fil des ans (de 2005 à aujourd'hui).

Aujourd'hui, tout utilisateur de PC expérimenté peut facilement installer un serveur WoW, sans même être un programmeur.


## Serveurs open source vs serveurs privés

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)


### Scénario hypothétique

Supposons qu'Alice et Bob aient chacun un serveur privé, et supposons qu'ils soient sur la même version du jeu.
Alice et Bob veulent tous deux proposer un nouveau contenu à leurs joueurs, qui a été fermé jusqu'à présent parce que les boss "A", "B", "C" et "D" sont assez bugués.

- Alice est une très bonne développeuse et peut corriger les deux boss "A" et "B".
- Bob est encore un débutant et ne répare que le boss "C".


### Dans un monde idéal

Alice et Bob travaillent ensemble et s'échangent leurs fix. En conséquence, leurs deux serveurs auront des boss "A", "B" et "C" parfaitement réparés.
De plus, Alice et Bob uniront leurs forces afin de travailler également sur le "D".

En conséquence, les joueurs des deux serveurs sont très heureux car ils jouent un contenu complètement fixe.


### Dans le monde réel

Alice et Bob sont rivaux et se font donc la guerre. Sur le serveur d'Alice, seuls les boss "A" et "B" travaillent. Dans le serveur de Bob, seul "C" fonctionne.
Certains joueurs passent du serveur de Bob à celui d'Alice. Le serveur de Bob se ferme au bout d'un moment. Certains joueurs du serveur d'Alice arrêtent de jouer parce qu'ils sont fatigués de ne faire que A et B, parce que C et D ne fonctionnent pas.

En conséquence, les joueurs des deux serveurs sont moins heureux que dans le scénario précédent. Alice a gagnée plus d'argent grâce aux dons des joueurs que Bob.


### La licence des émulateurs WoW

En fait, le code MaNGOS/TrinityCore (et leurs projets dérivés) est publié sous la [licence GNU GPL](https://en.wikipedia.org/wiki/GNU_General_Public_License).

En termes simples, cette licence dit ce qui suit : utilisez le code pour faire ce que vous voulez, sans rien payer, à condition que toute modification du code original soit également publiée sous la même licence.
Fondamentalement, la licence de ces projets oblige ceux qui les utilisent à publier toute modification au public.

Bien sûr, la plupart des serveurs privés utilisent cette licence comme **papier toilette**. Sinon, il ne devrait pas y avoir de serveur privé qui soit "mieux réparé" que les autres.

![Papier toilette](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Les mensonges sur les serveurs privés

Voici une liste de mensonges que les administrateurs de nombreux serveurs privés de WoW ne cessent de raconter à leurs joueurs :

### "Nous avons écrit ce noyau/core"

Fausses nouvelles. Peu importe le nombre de changements que "vous" avez faits. Vous avez commencé avec un projet basé sur MaNGOS.

Vous avez peut-être apporté quelques améliorations, mais la plus grande partie du code est toujours celle de MaNGOS/TrinityCore.

Peut-être que vous êtes vraiment bon et que vous avez réécrit la plupart du code au fil des ans. Pourtant, vous êtes parti de MaNGOS. Sans lui, le premier jour, vous n'auriez même pas réussi à faire fonctionner la fonction de connexion.

### "Nous avons corrigé X"

Dans la grande majorité des cas, aucun d'entre eux n'a vraiment réglé quoi que ce soit.
Ils ont juste téléchargé les corrections provenant de la communauté open source et les ont appliquées à leur base.
Pourtant, ils prennent tous les crédits.

### "Nous avons (vraiment) réparé X"

Certains serveurs privés réparent vraiment les choses par eux-mêmes. 
Ils ont souvent des équipes de développement dédiées qui sont payées avec l'argent provenant des dons des joueurs.

La plupart d'entre eux ne partagent pas ces corrections avec la communauté de développement.

En fait, la licence GPL du logiciel que vous utilisez pour faire tourner votre serveur vous demande de les partager, mais vous le gardez privé. Donc je vous déteste de toute façon.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## Les "justifications" des serveurs privés :

### "Je les garde privés pour faire de mon serveur un endroit spécial, meilleur que les autres"

D'accord, champion. Essayez de penser à ceci : si TOUS les développeurs faisaient ce que vous faites, ni vous ni votre serveur privé n'existeraient.

Pourquoi ? Tout simplement parce que ni MaNGOS (ni TrinityCore, AzerothCore, etc ...) n'existerait.
Ces projets existent grâce à des développeurs qui, contrairement à vous, ont partagé leur code.

Si tous les développeurs gardaient leur code privé, nous n'aurions pas d'émulateur WoW décent et vous ne pourriez tout simplement pas ouvrir votre serveur privé, car il n'y aurait aucun logiciel disponible.

### "Si je partageais mes correctifs, la concurrence les volerait"

Il n'y a rien à "voler". Ils ne peuvent pas "voler" ce code parce qu'il ne vous "appartient" pas. Non, pas même si vous l'avez vraiment écrit.

La philosophie de l'open source est claire : vous pouvez utiliser ce code gratuitement, à condition que toute modification de ce code DOIT être rendue publique.

Vous n'êtes pas d'accord ? Très bien. Alors n'utilisez pas de code open source et écrivez votre propre émulateur WoW en partant de zéro.


## Comment cela affecte les joueurs

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Je comprends parfaitement que toute cette histoire d'éthique et de licences importe très peu au joueur moyen de World of Warcraft.
Les joueurs veulent juste jouer sur un serveur stable et bien fixé, ils ne se soucient pas beaucoup que ce serveur collabore avec l'open source ou non.

Mais... essayez un instant de voir les choses sous un autre angle.

Les développeurs des projets open source (MaNGOS, TrinityCore, AzerothCore, etc...) ne se soucient pas beaucoup de ce que font les serveurs privés.
Bien sûr, en tant que développeur, cela vous énerve de voir un administrateur de serveur aléatoire prendre des crédits pour votre travail, mais au final cela ne change rien à votre vie.
De nombreux développeurs de logiciels libres le font simplement pour s'amuser et à des fins éducatives.

En fait, si TOUS les serveurs privés collaboraient avec l'open source, la vie des joueurs changerait complètement !
Vous savez, dans ce cas, chaque serveur offrirait une bien meilleure expérience de jeu pour toute extension. L'exemple d'Alice et Bob mentionné plus haut peut être appliqué à ce cas également.

Cependant, la réalité est toute autre : il existe de nombreux serveurs privés dans le monde entier, chacun d'eux travaillant toujours sur les mêmes choses, s'efforçant de les faire plus tôt et mieux.
S'ils collaboraient plutôt les uns avec les autres, ils éviteraient de faire du travail inutile et disposeraient de plus de temps et de main-d'œuvre. Ils pourraient donc sûrement réaliser beaucoup plus de choses.

*Note : la qualité (et la concurrence entre) les serveurs privés ne devrait pas être (seulement) une question de fix, mais aussi d'autres facteurs tels que les compétences de ses administrateurs en matière de gestion. La qualité de la communauté joue également un rôle fondamental, comme c'est le cas pour les serveurs Blizzard (qui sont tous égaux d'un point de vue technique).*

Si un serveur privé ferme, et que ses développeurs n'ont pas partagé leur travail, ce travail sera perdu à jamais.


## Révéler les mensonges

### Liste officielle des auteurs

Le plus intéressant est que tous les projets basés sur MaNGOS sont entièrement publics, il est donc possible de vérifier avec précision qui y a contribué.

Par conséquent, la liste de tous les contributeurs de ces projets est absolument publique et N'IMPORTE QUI peut vérifier qui a réellement fixé quoi.

Par exemple :

- Liste officielle des contributeurs de MaNGOS : https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Liste officielle des contributeurs de TrinityCore : https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Liste officielle des contributeurs d'AzerothCore : https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS : vous pouvez trouver l'auteur de cet article dans toutes ces listes


### Liste officielle des mises à jour

Tout projet open source (généralement hébergé sur GitHub) dispose de la liste des mises à jour réalisés par les différents développeurs. Pour chaque "commit", l'auteur et la date sont indiqués.

Il est très facile de vérifier ces informations, il suffit d'ouvrir le dépôt officiel de tout émulateur. Cherchez sur Google par exemple "TrinityCore github" ou "AzerothCore github" et jetez un oeil.

Vous verrez qui fait vraiment quoi. Vous verrez toutes les lignes de code, leurs auteurs, les commentaires des autres développeurs, etc. Vous verrez tout. Plus de mensonges !


## Que puis-je faire en tant que joueur ?

Mon conseil est que vous jouez/supportiez des serveurs privés qui collaborent avec l'open source, malgré le type d'extension et d'émulateur qu'ils utilisent.

Ou, du moins, évitez les serveurs qui volent le travail d'autres personnes, en supprimant les crédits des auteurs originaux.


### En savoir plus sur les logiciels libres

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software
