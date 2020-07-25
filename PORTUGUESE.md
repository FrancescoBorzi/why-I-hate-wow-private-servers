# Por que eu odeio a maioria dos servidores privados WoW

*Escrito por Francesco Borzi' aka Shin*

Por que ainda existem tantos bugs nos servidores privados WoW, apesar de existirem há tantos anos?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

Não se preocupe, esta não é a palestra habitual sobre direitos autorais da Blizzard.
Eu só quero explicar porque odeio a maioria dos servidores privados [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft).

## Introdução

Fico fascinado com a emulação de WoW desde os 14 anos. Lembro-me de que na primeira vez que entrei em um desses "reinos especiais", havia muitos bugs, mas você podia jogar de graça, pelo menos. Sabe, eu não tinha um centavo vermelho na época, então não tinha alternativa.

Aos 15 anos, comecei a me perguntar como os servidores privados realmente funcionavam e poderiam existir, especialmente do ponto de vista técnico. Alguém roubou o código da [Blizzard] (https://en.wikipedia.org/wiki/Blizzard_Entertainment) talvez? Eu não tinha ideia - eu era tão jovem e inexperiente na época! Apesar disso, comecei a brincar e, com a ajuda de um velho amigo meu (Fabio), finalmente consegui instalar um servidor WoW no meu próprio PC.

Naquela época, eu nem conseguia imaginar a quantidade de satisfação que teria e quantas coisas teria aprendido graças a este mundo mágico.

Pode parecer estranho, mas esse mundo ainda me fascina agora, como adulto, no ponto em que dediquei um tempo inteiro. [Tese de Mestrado em Ciência da Computação para este tema](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![Wow-Emulação-Tese](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Mas ainda: **Eu odeio a maioria dos servidores privados e realmente quero explicar por que.**

## Poucos termos técnicos

![Wow-Dormir](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Para fazer você entender meu ponto de vista, preciso me concentrar em um pequeno parêntese técnico sobre os processos de trabalho do WoW, que tentarei colocar em palavras simples.

### Como o World of Warcraft original funciona

No nível do software, existem dois programas que podem ser considerados os principais atores deste jogo:

- O **APLICATIVO DO CLIENTE** - que é o programa "World of Warcraft" real instalado por cada jogador em seu computador para acessar o jogo;

- O **APLICATIVO DO SERVIDOR**: que é o programa que é executado nas máquinas do servidor.

O processo é muito simples: todos os Clientes (jogadores) se conectam a um Servidor para interagir uns com os outros. O cliente conhece o endereço do servidor, pois ele é armazenado no famoso arquivo "**realmlist.wtf**" (é por isso que você tem que modificar este arquivo para mudar para outro servidor).

![Cliente-servidor](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Como funcionam os servidores privados woW

Ao jogar em servidores privados, o princípio é exatamente o mesmo. A diferença está no software que você usa.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENTE**. Todo mundo tem acesso ao cliente original do World of Warcraft. Você pode facilmente obtê-lo comprando-o ou baixando-o on-line. Este programa é exatamente o que você usaria para jogar no servidor oficial. Obviamente, diferentes servidores privados têm versões diferentes de clientes, mas eles sempre se referem ao cliente original. Você só precisa fazer uma pequena alteração no arquivo "realmlist.wtf", substituindo o endereço do endereço do servidor de varejo por o de um servidor privado. É isso, é isso.

**SERVER**. Isto é completamente diferente. Ninguém fora da Blizzard tem acesso ao software original que executa os servidores oficiais do World of Warcraft. Portanto, essas aplicações são completamente diferentes das originais.

### Engenharia reversa

![Engenharia reversa](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Todos os softwares que executam servidores privados foram criados através da técnica de "engenharia reversa", que, em palavras simples, significa "Tento escrever um programa que imita o comportamento de outro programa, sem olhar para o código original".

A questão agora é: quem implementou esse software e quando isso aconteceu?


#### Digressão sobre os direitos autorais

*Todo o material protegido por direitos autorais (imagens, sons, modelos 3D, logotipos, etc...) está localizado dentro do aplicativo do cliente.
O aplicativo do servidor contém apenas números e textos. Portanto, é absolutamente legal se você usá-lo para fins educacionais.*

## Aplicativos não oficiais do servidor WoW

Quem cria os aplicativos de software que executam os servidores privados do WoW (comumente chamados de "emuladores")? E como eles fizeram isso?



### Complexidade

![Complexo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

Você não precisa ser um especialista para entender que escrever um aplicativo de servidor para um MMORPG com um escopo tão grande como World of Warcraft certamente não é brincadeira de criança.

A Blizzard é uma grande empresa com milhares de funcionários. Escrever um programa que "imita" o funcionamento de seu aplicativo de servidor certamente não é trivial ou viável para um único indivíduo (ou um pequeno grupo de programadores).

E não é só uma questão de complexidade. Vamos pensar em tarefas muito triviais, mas repetitivas, como adicionar cada NPC ao mundo, incluindo cada item de seu saque com sua própria porcentagem de chance, etc.. . Um ótimo trabalho, basicamente. Sem mencionar todas as tarefas muito complexas que requerem horas de estudo e testes, como mecânica ortodletal, mecânica de chefe, etc.

Resumindo.... nem mesmo o melhor programador do mundo poderia ser capaz de fazer todo esse trabalho por conta própria.

No entanto, há servidores privados, e o software que os faz executar. E alguns servidores privados agora são capazes de oferecer uma qualidade de jogo que não está longe da original (aqui eu me refiro principalmente às antigas expansões).

Como isso é possível?

### MaNGOS e o modelo de desenvolvimento de código aberto

> Se você tem uma maçã e eu temos uma maçã e nós trocamos essas maçãs então você e eu ainda teremos uma maçã cada. Mas se você tiver uma ideia e eu tiver uma ideia e trocarmos essas ideias, então cada um de nós terá duas ideias. (George Bernard Shaw)

Só para simplificar: um programa de código aberto é um programa cujo código é público.

No contexto dos servidores privados, o código aberto desempenha um papel fundamental.

Alguns jogadores veteranos podem lembrar que uma vez que a qualidade do jogo em servidores privados era muito ruim. Quase nada funcionou.
Por exemplo, se você fosse um Rogue em Modo [stealth] você poderia ser alvo de qualquer um que escreveu '/target Yourname'. Adivinha qual classe escolhi para o meu primeiro personagem...

![Mangos-logotipo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

A verdadeira revolução foi [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), um projeto de código aberto criado em 2005, cujo objetivo era fornecer um aplicativo de servidor para o World of Warcraft.
A grande notícia do MaNGOS, bem como sua força, foi o fato de que, como um aplicativo de código aberto, seu código era completamente público, e qualquer usuário de todo o mundo poderia estudá-lo e oferecer sua própria contribuição (tanto em termos de adicionar ou corrigir mecânica de jogo, mas também em termos de reportar bugs).

Só assim, graças à contribuição de muitos voluntários de diferentes nacionalidades, foi possível desenvolver um aplicativo de servidor capaz de imitar World of Warcraft com maior qualidade de jogo.

Em 2009 nasceu outro projeto importante [TrinityCore](https://www.trinitycore.org/), baseado no MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Até o momento, a esmagadora maioria dos servidores privados são executados em aplicativos baseados em MaNGOS/TrinityCore.

Ao longo dos anos, nasceram [diferentes projetos](http://mangosrumors.org/best-wow-emulador-2020/) e eles foram baseados no código MaNGOS/TrinityCore, que varia principalmente de acordo com a versão wow suportada.
Por exemplo, [AzerothCore](https://www.azerothcore.org/) para 3.3.5, [OregonCore](https://github.com/OregonCore) para 2.4.3, [SkyFire](https://www.projectskyfire.org/) para 5.4.3, [CMaNGOS](https://cmangos.net/) para Classic/TBC/WOTLK, e muitos outros ... Todos eles baseados em MaNGOS e/ou TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Recapitular

Assim, os servidores privados atingiram essa qualidade apenas graças aos muitos colaboradores que implementaram cada vez mais recursos de jogos ao longo dos anos (de 2005 até hoje).

Hoje, qualquer usuário experiente de PC pode facilmente instalar um servidor WoW, sem sequer ser um programador.

## Código aberto vs servidores privados

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Cenário hipotético

Suponha que Alice e Bob tenham um servidor privado cada um, e vamos supor que eles estão na mesma versão do jogo.
Alice e Bob querem lançar um novo conteúdo para seus jogadores, que foi fechado até agora porque os chefes `A`,` B`, `C` E `D` são bastante bugados.

- Alice é uma desenvolvedora muito boa e pode corrigir ambos os chefes `A` E `B`
- Bob ainda é um iniciante e só corrige o chefe `C`

### Em um mundo ideal

Alice e Bob trabalham juntos e trocam suas correções. Como resultado, ambos os seus servidores terão chefes perfeitamente fixos `A`,` B` E `C`.
Além disso, Alice e Bob vão unir forças para trabalhar em `D` também.

Como resultado, os jogadores de ambos os servidores estão muito felizes porque jogam um conteúdo completamente fixo.

### No mundo real

Alice e Bob são rivais e então travam uma guerra um contra o outro. No servidor de Alice, apenas chefes `A` E `B` funciona. Enquanto no servidor do Bob apenas `C` funciona.
Alguns jogadores mudam do servidor do Bob para o da Alice. O servidor do Bob fecha depois de um tempo. Alguns dos jogadores de servidor alice parar de jogar porque eles se cansam de sempre fazer apenas `A` E `B` porque `C` E `D` Não funciona.

Como resultado, os jogadores de ambos os servidores estão menos felizes do que no cenário anterior. Alice ganhou mais dinheiro através de doações de jogadores do que Bob.

### A licença dos emuladores WoW

Na verdade, o código MaNGOS/TrinityCore (e seus projetos derivados) é lançado sob o [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

Em palavras simples, esta licença diz o seguinte: use o código para fazer o que quiser, sem pagar nada, desde que qualquer modificação no código original também seja liberada sob a mesma licença.
Basicamente, a licença desses projetos exige que aqueles que os utilizam publiquem qualquer alteração ao público.

Claro, a maioria dos servidores privados usam esta licença como **papel higiênico**. Caso contrário, não deve haver servidor privado que seja "melhor fixo" do que outros.

![Papel higiênico](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## As mentiras sobre os servidores privados

Aqui está uma lista de mentiras que os administradores de muitos servidores privados wow continuam dizendo aos seus jogadores:


### "Nós escrevemos este núcleo"

Notícias falsas. Não importa quantas mudanças "você" fez. No entanto, você começou com um projeto baseado em MaNGOS.

Talvez você tenha feito algumas melhorias, mas a maior parte do código ainda é mangos/trinitycore.

Talvez você seja muito bom e tenha reescrito a maior parte do código ao longo dos anos. Ainda assim, você começou a partir de MaNGOS. Sem ele, no primeiro dia você nem teria o recurso de login funcionando.

### "Nós consertamos X"

Na grande maioria dos casos, nenhum deles realmente consertou nada.
Eles acabaram de baixar as correções provenientes da comunidade de código aberto e as aplicaram ao seu núcleo.
Ainda assim eles levam todos os créditos.

### "Nós (realmente) consertamos X"

Alguns servidores privados realmente consertam as coisas por conta própria. Eles geralmente têm equipes de desenvolvimento dedicadas que são pagas com o dinheiro proveniente de doações de jogadores.

A maioria deles não compartilha essas correções com a comunidade de desenvolvimento.

Bem, a licença GPL do software que você está usando para executar seu servidor está pedindo para você compartilhá-los, mas você ainda mantê-lo privado. Então eu te odeio de qualquer maneira.

![Pinóquio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## As "justificativas" dos servidores privados


### "Eu os mantenho privados para fazer do meu servidor um lugar especial, melhor do que os outros"

Tudo bem campeão. Tente pensar sobre isso: se todos os desenvolvedores gostassem de você, nem você nem seu servidor privado existiriam.

Porque? Simplesmente porque nem MaNGOS (nem TrinityCore, AzerothCore, etc...) existiriam.
Esses projetos existem graças a desenvolvedores que, ao contrário de você, compartilharam seu código.

Se todos os devs mantivessem seu código privado, não teríamos nenhum emulador WoW decente e você simplesmente não poderia abrir seu servidor privado, porque não haveria nenhum software disponível.


### "Se eu compartilhasse minhas correções, a concorrência as roubaria."

Não há nada para "roubar". Eles não podem "roubar" esse código porque não "pertence" a você. Não, nem mesmo se você realmente escreveu.

A filosofia de código aberto é clara: você pode usar esse código gratuitamente, desde que qualquer modificação dele deve ser tornada pública.

Oh, você não concorda? Bem. Então não use nenhum código-fonte aberto e escreva seu próprio emulador WoW do zero.

## Como isso afeta os jogadores

![Wow-Dranei-chorando](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Eu entendo totalmente que toda essa história sobre ética e licenças importa muito pouco para o jogador médio do World of Warcraft.
Os jogadores só querem jogar em um servidor estável e bem fixo, eles não se importam muito se este servidor colabora com o código aberto ou não.

Mas... tentar por um momento vê-lo de outra perspectiva.

Os desenvolvedores dos projetos de código aberto (MaNGOS, TrinityCore, AzerothCore, etc...) basicamente não se importam muito com o que os servidores privados fazem.
É claro que, como desenvolvedor, ele te irrita para ver algum administrador de servidor aleatório tomando créditos para o seu trabalho, mas no final isso não muda sua vida.
Muitos desenvolvedores de código aberto apenas fazem isso por diversão e fins educacionais.

Na verdade, se todos os servidores privados colaborassem com o código aberto, a vida dos jogadores mudaria completamente!
Você sabe, nesse caso, cada servidor forneceria uma experiência de jogo muito melhor para qualquer expansão. O exemplo de Alice e Bob mencionados antes pode ser aplicado a este caso também.

No entanto, a realidade é exatamente isso: existem muitos servidores privados ao redor do mundo, cada um deles sempre trabalha nas mesmas coisas, correndo para fazê-los cada vez mais cedo e melhor.
Se colaborassem entre si, evitariam fazer um trabalho desnecessário e teriam mais tempo e força de trabalho. Então, eles certamente seriam capazes de alcançar muito mais.

*Nota: a qualidade (e a concorrência entre) servidores privados não devem ser (apenas) sobre a fixação, mas também sobre outros fatores, como as habilidades de seus administradores em gerenciá-lo. A qualidade da comunidade também desempenha um papel fundamental, assim como acontece nos servidores da Blizzard (que são todos iguais do ponto de vista técnico).*

Se um servidor privado fechar, e seus desenvolvedores não compartilharem seu trabalho, esse trabalho será perdido para sempre.

## Expondo mentiras

### Lista oficial de autores

O mais interessante é que todos os projetos baseados em MaNGOS são completamente públicos, por isso é possível verificar com precisão quem contribuiu para eles.

Como resultado, todos os colaboradores listam desses projetos são absolutamente públicos e QUALQUER um pode verificar quem realmente corrigiu o quê.

Por exemplo:

- Lista oficial de colaboradores do MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Lista oficial de colaboradores do TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Lista oficial de colaboradores do AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PS: você pode encontrar o autor deste artigo em todas essas listas

### Lista oficial de compromissos

Qualquer projeto de código aberto (geralmente hospedado no GitHub) tem a lista de compromissos realizados pelos diferentes desenvolvedores. Para cada compromisso, tanto o autor quanto a data estão lá.

É muito fácil verificar essas informações, basta abrir o repositório oficial de qualquer emulador. Google, por exemplo, "TrinityCore github" ou "AzerothCore github" e basta dar uma olhada.

Você vai ver quem-faz-realmente-o quê. Você verá todas as linhas de código, seus autores, outros comentários dev, etc. Você verá tudo. Chega de mentiras!


## O que posso fazer como jogador?

Meu conselho é que você jogue/Apoie servidores privados que colaboram com código aberto, apesar do tipo de expansão e emulador que utilizam.

Ou, pelo menos, evitar aqueles servidores que vendem o trabalho de outras pessoas por conta própria, removendo os créditos dos autores originais.


### Saiba mais sobre software livre

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software


## Obrigado

Agradecimentos especiais a *Laura Bartiromo*
