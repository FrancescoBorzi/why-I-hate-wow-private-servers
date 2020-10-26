# Por qué odio la mayoría de los servidores privados de WoW

**Escrito por Francesco Borzi | alias Shin**
**Editado y traducido por Pagani Walter | Stevej**

¿Por qué hay todavía tantos errores en los servidores privados del WoW, a pesar de que han existido durante tantos años?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

No te preocupes, esta no es la típica conferencia de los derechos de autor sobre Blizzard.
Sólo quiero explicar por qué odio la mayoría de los servidores privados de [World of Warcraft](https://en.wikipedia.org/wiki/World_of_Warcraft).

## Introducción

He estado fascinado por la emulación del WoW desde que tenía 14 años. Recuerdo que la primera vez que me uní a uno de estos "reinos especiales", había un montón de errores, pero al menos se podía jugar gratis. Sabes, no tenía un centavo en ese momento, así que no tenía alternativa.

A los 15 años empecé a preguntarme cómo funcionaban realmente los servidores privados y cómo podían existir, especialmente desde una perspectiva técnica. ¿Alguien robó el código de [Blizzard](https://en.wikipedia.org/wiki/Blizzard_Entertainment) quizás? No tenía ni idea... ¡Era tan joven e inexperto en ese momento! A pesar de eso, y, con la ayuda de un viejo amigo mío (Fabio), finalmente conseguí instalar un servidor de WoW en mi propia PC.

**En aquel entonces no podía imaginar la satisfacción que había obtenido y cuántas cosas habría aprendido gracias a este mundo mágico.**

Puede sonar raro, pero este mundo todavía me fascina ahora, como adulto, en el punto en que dediqué todo un [Tesis de maestría en Ciencias de la Computación sobre este tema](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Pero aún así: **Odio la mayoría de los servidores privados y quiero explicar por qué.**

## Términos técnicos

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Para hacerles entender mi punto de vista, necesito detenerme en un pequeño paréntesis técnico sobre los procesos de trabajo del WoW, que intentaré poner en palabras simples.

### Cómo funciona el World of Warcraft original

A nivel de software, hay dos programas que podrían ser considerados como los principales actores de este juego:

- **APLICACIÓN CLIENTE** - que es el verdadero programa **World of Warcraft** instalado por cada jugador en su ordenador para acceder al juego.

- **APLICACIÓN DE SERVIDOR**: que es el programa que se ejecuta en los servidores.

El proceso es muy simple: todos los clientes (jugadores) se conectan a un servidor para interactuar entre ellos. El cliente conoce la dirección del servidor, ya que está almacenada en el famoso archivo **realmlist.wtf** (por eso hay que modificar este archivo para cambiar a otro servidor).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Cómo funcionan los servidores privados de WoW

Cuando se juega en servidores privados, el principio es exactamente el mismo. La diferencia radica en el software que se utiliza.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENTE**. Todo el mundo tiene acceso al cliente original de World of Warcraft. Puedes conseguirlo fácilmente comprándolo o descargándolo en línea. Este programa es exactamente el que usarías para jugar en el servidor oficial. Obviamente los diferentes servidores privados tienen diferentes versiones de cliente, pero siempre se refieren al cliente original. Sólo tienes que hacer un pequeño cambio en el archivo **realmlist.wtf**, reemplazando la dirección del servidor oficial, por la de un servidor privado. Eso es todo.

**SERVIDOR**. Esto es completamente diferente. Nadie fuera de Blizzard tiene acceso al software original que ejecuta los servidores oficiales de World of Warcraft. Así que estas aplicaciones son completamente diferentes de la original.

### Ingeniería inversa

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Todos los programas que ejecutan servidores privados han sido creados mediante la técnica de "ingeniería inversa", que, en palabras sencillas, significa: **intento escribir un programa que imita el comportamiento de otro programa, sin mirar / tener acceso al código original**.

La pregunta ahora es: ¿quién implementó este software y cuándo ocurrió?

#### Resumen de los derechos de autor

**Todo el material con derechos de autor (imágenes, sonidos, modelos 3D, logotipos, etc...) se encuentra dentro de la aplicación cliente.
La aplicación del servidor sólo contiene números y textos. Por lo tanto, es absolutamente legal si se utiliza con fines educativos.**

## Aplicaciones no oficiales del servidor WoW

¿Quién crea las aplicaciones de software que ejecutan los servidores privados de WoW (comúnmente llamados **emuladores**)? ¿Y cómo lo hacen?

### Complejidad

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

No hace falta ser un experto para entender que escribir una aplicación de servidor para un **MMORPG** con un alcance tan grande como World of Warcraft no es ciertamente un juego de niños.

Blizzard es una gran empresa con miles de empleados. Escribir un programa que "imita" el funcionamiento de su aplicación de servidor no es ciertamente trivial o factible para un solo individuo (o un pequeño grupo de programadores).

Y no es sólo una cuestión de complejidad. Pensemos en tareas muy triviales pero repetitivas, como añadir cada NPC (Non Playable Character) al mundo, incluyendo cada elemento de su botín con su propio porcentaje de probabilidad, etc... Básicamente, un trabajo estupendo. Sin mencionar todas las tareas muy complejas que requieren horas de estudio y pruebas, como la mecánica de los hechizos, la mecánica de los jefes, etc.

En resumen... ni siquiera el mejor programador del mundo podría hacer todo este trabajo por su cuenta.

Sin embargo, existen servidores privados, y el software que los hace funcionar. Y algunos servidores privados son ahora capaces de ofrecer una calidad de juego que no está lejos de la original (aquí me refiero principalmente a las antiguas expansiones).

¿Cómo es posible?

### MaNGOS y el modelo de desarrollo de código abierto

> Si tú tienes una manzana y yo tengo una manzana y nos intercambiamos estas manzanas, entonces tú y yo seguiremos teniendo una manzana cada uno. Pero si tú tienes una idea y yo tengo una idea e intercambiamos estas ideas, entonces cada uno de nosotros tendrá dos ideas. (George Bernard Shaw)

Sólo para hacerlo simple: un programa de código abierto es un programa cuyo código es público.

En el contexto de los servidores privados, el código abierto desempeña un papel fundamental.

Algunos jugadores veteranos pueden recordar que una vez la calidad del juego en los servidores privados era realmente mala. Casi nada funcionaba.
Por ejemplo, si eras un pícaro en sigilo, podrías ser el objetivo de cualquiera que escribiera `/target nickname`. Adivina qué clase elegí para mi primer personaje...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

La verdadera revolución fue [MaNGOS](https://it.wikipedia.org/wiki/MaNGOS), un proyecto de código abierto creado en 2005, cuyo propósito era proporcionar una aplicación de servidor para World of Warcraft.
La gran noticia de MaNGOS, además de su fuerza, fue el hecho de que como aplicación de código abierto, su código era completamente público, y cualquier usuario de todo el mundo podía estudiarlo y ofrecer su propia contribución (tanto en términos de añadir o arreglar mecánicas de juego, como en términos de reportar errores).

Sólo así, gracias a la contribución de muchos voluntarios de diferentes nacionalidades, fue posible desarrollar una aplicación de servidor capaz de emular World of Warcraft con una mayor calidad de juego.

En 2009 nació otro proyecto importante [TrinityCore](https://www.trinitycore.org/), basado en MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Hasta la fecha, la abrumadora mayoría de los servidores privados funcionan con aplicaciones basadas en MaNGOS/TrinityCore.

A lo largo de los años, [diferentes proyectos](http://mangosrumors.org/best-wow-emulator-2020/) se basaron en el código MaNGOS/TrinityCore, y solo varían, en la versión de wow soportada.

Por ejemplo [AzerothCore](https://www.azerothcore.org/) para 3.3.5, [OregonCore](https://github.com/OregonCore) para 2.4.3, [SkyFire](https://www.projectskyfire.org/) para 5.4.8, [CMaNGOS](https://cmangos.net/) para Classic/TBC/WOTLK, y muchos otros... Todos ellos basados en MaNGOS y/o TrinityCore.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Resumen

Por lo tanto, los servidores privados han alcanzado tal calidad, sólo gracias a los numerosos colaboradores que han implementado más y más características del juego a lo largo de los años (desde 2005 hasta hoy).

Hoy en día cualquier usuario de PC sin experiencia en programación, puede instalar y compilar un servidor de Wow.

## Código abierto vs. servidores privados

![Alice-and-bob](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/alice-and-bob.jpg)

### Escenario hipotético

Supongamos que Alice y Bob tienen un servidor privado cada uno, y supongamos que están en la misma versión del juego.
Tanto Alice como Bob quieren lanzar un nuevo contenido a sus jugadores, que ha sido cerrado hasta ahora porque los jefes `A`,` B`, `C` y ` D` tiene varios errores / bugs.

- Alice es muy buena desarrolladora y puede arreglar a los dos jefes: `A` y `B`.
- Bob sigue siendo un principiante y sólo arregla al jefe `C`.

### En un mundo ideal

Alice y Bob trabajan juntos e intercambian sus arreglos. Como resultado, ambos servidores tendrán jefes perfectamente arreglados `A`,` B` y `C`.
Además, Alice y Bob unirán sus fuerzas para trabajar en `D` también.

Como resultado, los jugadores de ambos servidores están muy contentos porque juegan un contenido completamente funcional.

### En el mundo real

Alice y Bob son rivales y por eso se hacen la guerra entre ellos. En el servidor de Alice, sólo los jefes `A` y `B` funcionan. Mientras que en el servidor de Bob sólo funciona `C`.
Algunos jugadores se mueven del servidor de Bob al de Alice constantemente. El servidor de Bob se cierra después de un tiempo. Algunos de los jugadores del servidor de Alice dejan de jugar porque se cansan de hacer siempre sólo `A` y `B` porque `C` y `D` no funcionan.

Como resultado, los jugadores de ambos servidores están menos contentos que en el escenario anterior. Alice ganó más dinero a través de las donaciones.

### La licencia de los emuladores de WoW

En realidad, el código MaNGOS/TrinityCore (y sus proyectos derivados) es liberado bajo el [GNU GPL license](https://en.wikipedia.org/wiki/GNU_General_Public_License).

En palabras sencillas, esta licencia dice lo siguiente: 
**Usa el código para hacer lo que quieras, sin pagar nada, siempre y cuando cualquier modificación del código original sea también liberada bajo la misma licencia.
Básicamente, la licencia de estos proyectos requiere que aquellos que los usan publiquen cualquier cambio al público y lo compartan con el resto de la comunidad..**

Por supuesto, la mayoría de los servidores privados usan esta licencia como **papel higiénico**. De lo contrario, no debería haber ningún servidor privado que funcione mejor que otro.

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Las mentiras sobre los servidores privados

Aquí hay una lista de mentiras que los administradores de muchos servidores privados de WoW siguen diciendo a sus jugadores:

### Escribimos este núcleo / core

Falsas noticias. No importa cuántos cambios hayas hecho "tú", empezaste con un proyecto basado en MaNGOS.

Tal vez hayas hecho algunas mejoras, pero la mayor parte del código sigue siendo de MaNGOS/TrinityCore.

Tal vez eres muy bueno y has reescrito la mayor parte del código a lo largo de los años. Aun así, empezaste desde MaNGOS. Sin él, ni siquiera habrías conseguido que funcionara el inicio de sesión.

### Hemos arreglado "x" bug.

En la gran mayoría de los casos, ninguno de ellos ha arreglado realmente nada. Acaban de descargar las correcciones provenientes de la comunidad de código abierto y las han aplicado a su núcleo. Aún así se llevan todos los créditos. Esto es muy fácil de comprobar realmente. Si sos jugador de wow, podrás observar que prácticamente ningún servidor, tiene los créditos de la comunidad que lo ayuda a llevar adelante el proyecto. Incluso, muchos de ellos, se desesperan por eliminar dichos créditos mediante diferentes pretextos.

### "Nosotros (realmente) arreglamos X"

Algunos servidores privados realmente arreglan las cosas por su cuenta. A menudo tienen equipos de desarrollo dedicados que son pagados con el dinero de las donaciones de los jugadores.

La mayoría de ellos no comparten estos arreglos con la comunidad de desarrollo.

Bueno, la licencia GPL del software que estás usando para ejecutar tu servidor te pide que lo compartas, pero aún así lo mantienes privado. Así que te odio de todas formas.

### Eliminamos los créditos por un tema de seguridad. **(Stevej)**

Con la excusa de ocultar los créditos, muchas personas argumentan, que si los jugadores conocieran de antemano el emulador que se usa en su comunidad, podrían hacer uno de los diferentes errores que han sido reportados pero no arreglados por la misma. Entonces, justifican no exponer dichos créditos por ese motivo. Luego cuando tienen un ataque de DDoS corren desesperados a los brazos de las comunidades para pedir ayuda / soporte.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## Las "justificaciones" de los servidores privados


### "Los mantengo en privado para hacer de mi servidor un lugar especial, mejor que los otros"

Muy bien, campeón. Intenta pensar en esto: si TODOS los desarrolladores hicieran lo mismo, ni tú ni tu servidor privado podrían funcionar.

¿Por qué? Simplemente porque ni MaNGOS (ni TrinityCore, AzerothCore, etc...) existirían.
**Estos proyectos existen gracias a los desarrolladores que, a diferencia de ti, compartieron su código.**

Si todos los desarrolladores mantuvieran su código privado, no tendríamos un emulador de WoW decente y no podrías abrir tu servidor privado, porque no habría ningún software disponible.

### "Si compartiera mis arreglos, la competencia las robaría"

**No hay nada que robar. No pueden robar ese código porque no te pertenece**. Ni siquiera sé si realmente lo escribiste.

La filosofía del código abierto es clara: puedes usar ese código de forma gratuita, siempre que cualquier modificación de él, DEBE hacerse pública.

¿No estás de acuerdo? Está bien. Entonces no uses ningún código abierto y escribe tu propio emulador de WoW desde cero.

## Cómo afecta esto a los jugadores

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Entiendo totalmente que toda esta historia sobre la ética y las licencias importa muy poco al jugador medio de World of Warcraft.
Los jugadores sólo quieren jugar en un servidor estable y bien arreglado, no les importa mucho si este servidor colabora con el código abierto o no.

Pero... intenta por un momento verlo desde otra perspectiva.

A los desarrolladores de los proyectos de código abierto (MaNGOS, TrinityCore, AzerothCore, etc...) básicamente no les importa mucho lo que hacen los servidores privados.
Por supuesto, como desarrollador te molesta ver a algún administrador de servidores al azar tomando créditos por tu trabajo, pero al final no cambia tu vida.
Muchos desarrolladores de código abierto sólo lo hacen por diversión y con fines educativos.

En realidad, si TODOS los servidores privados colaboraran con el código abierto, ¡las vidas de los jugadores cambiarían por completo!
En ese caso, cada servidor proporcionaría una experiencia de juego mucho mejor para cualquier expansión. El ejemplo de Alice y Bob mencionado anteriormente puede aplicarse a este caso también.

Sin embargo, la realidad es justamente esa: hay muchos servidores privados en todo el mundo, cada uno de ellos siempre trabaja en las mismas cosas.
Si en cambio colaboraran entre ellos, evitarían hacer trabajos innecesarios y tendrían más tiempo y mano de obra. Así que seguramente serían capaces de lograr mucho más.

**Nota: la calidad (y la competencia entre) los servidores privados no debe ser (sólo) de arreglos / fixs, sino también de otros factores como la habilidad de sus administradores para manejarlo. La calidad de la comunidad también juega un papel fundamental, al igual que ocurre con los servidores de Blizzard (que son todos iguales desde el punto de vista técnico).**

Si un servidor privado se cierra, y sus desarrolladores no han compartido su trabajo, ese trabajo se perderá para siempre.

## Exponer las mentiras

### Lista oficial de autores

Lo más interesante es que todos los proyectos basados en MaNGOS son completamente públicos, por lo que es posible verificar con precisión quiénes contribuyeron a ellos.

Como resultado, todas las listas de contribuyentes de estos proyectos son absolutamente públicas y CUALQUIER persona puede verificar quién arregló qué.

Por ejemplo:

- Lista oficial de colaboradores de MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Lista oficial de colaboradores de TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Lista oficial de colaboradores de AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PD: puedes encontrar al autor de este artículo en todas estas listas

### Lista oficial de compromisos

Cualquier proyecto de código abierto (generalmente alojado en GitHub) tiene la lista de commits realizados por los diferentes desarrolladores. Para cada commit, tanto el autor como la fecha están ahí.

Es muy fácil verificar esta información, basta con abrir el repositorio oficial de cualquier emulador. Busca en Google por ejemplo "TrinityCore github" o "AzerothCore github" y echa un vistazo.

Verás quién hace realmente qué. Verás todas las líneas de código, sus autores, los comentarios de otros desarrolladores, etc. Verás todo. No más mentiras!

## ¿Qué puedo hacer como jugador?

Mi consejo es que jueguen/soporten los servidores privados que colaboran con el código abierto, a pesar del tipo de expansión y emulador que utilizan.

O, por lo menos, evitar los servidores que venden el trabajo de otras personas por su cuenta, eliminando los créditos de los autores originales.

### Más información sobre el software libre

- https://www.gnu.org/software/software.en.html
- https://www.fsf.org/about/what-is-free-software

## Gracias

Agradecimientos especiales a **Laura Bartiromo**
