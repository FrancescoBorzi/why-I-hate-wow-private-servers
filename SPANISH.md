# Por qué odio la mayoría de servidores privados del WoW

**Escrito originalmente por Francesco Borzi | alias Shin**
**Editado y traducido por Pagani Walter | Stevej y Mathematical**

¿Por qué hay todavía tantos errores en los servidores privados del WoW, a pesar de que han existido durante tantos años?

![Wow-facepalm](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-facepalm.jpeg)

No te preocupes, esta no es una típica conferencia acerca de los Derechos de Autor de Blizzard.
Sólo quiero explicar el motivo de por qué odio la mayoría de los servidores privados de [World of Warcraft](https://es.wikipedia.org/wiki/World_of_Warcraft).

(Y con "odio" no me refiero en un sentido literal, sino meramente metafórico)

## Introducción

He estado fascinado por la emulación del WoW desde que tenía 14 años. Recuerdo que la primera vez que me uní a uno de estos "reinos especiales", había un montón de errores, pero al menos se podía jugar gratis en ellos, que era lo importante en todo caso. Sabes, tampoco tenía un centavo en ese momento de mi vida, así que no tenía otra alternativa.

A los 15 años de edad empecé a preguntarme más seriamente cómo funcionaban realmente los servidores privados y el cómo podían existir, especialmente desde una perspectiva técnica, claro está. ¿Alguien robó el código de [Blizzard](https://es.wikipedia.org/wiki/Blizzard_Entertainment) quizá? Realmente no tenía idea... ¡Era tan joven e inexperto en ese momento! A pesar de ello y con la ayuda de un viejo amigo mío llamado Fabio, finalmente conseguí instalar un servidor del WoW dentro de mi propia PC.

**En aquel entonces no podía llegar a imaginar la satisfacción que había obtenido y cuántas cosas más habría aprendido gracias a este mundo mágico en el que me había sumergido.**

Puede sonar un poco raro, pero todo este mundo me sigue fascinando a día de hoy, ya siendo un adulto claro está, hasta el punto en el que dediqué toda una [Tesis de Maestría en Ciencias de la Computación sobre este mismo tema](https://community.trinitycore.org/topic/13025-just-thank-you-wow-emulation).

![wow-emulation-thesis](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-emulation-thesis.jpeg)

Sin embargo: **Sigo odiando a la mayoría de los Servidores Privados existentes y quiero explicar el por qué.**

## Términos técnicos

![Wow-sleeping](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-sleeping.jpg)

Para hacerles entender mi punto de vista, necesito detenerme en un pequeño paréntesis técnico sobre los procesos de trabajo del WoW, que intentaré poner en palabras simples para todos.

### Cómo funciona el World of Warcraft original

A nivel de software, existen dos programas que podrían ser considerados como los principales actores de este juego:

- **APLICACIÓN CLIENTE** - que es el verdadero programa **World of Warcraft** instalado para cada jugador en su debido ordenador con el objetivo de acceder al juego.

- **APLICACIÓN DE SERVIDOR**: que es el programa ejecutado dentro de los servidores.

El proceso es muy simple: todos los clientes  (o sea, jugadores) se conectan a un servidor común para poder interactuar entre ellos. El cliente de juego conoce la dirección del servidor, ya que está almacenada dentro del famoso archivo **realmlist.wtf** (Por eso siempre debe de modificarse este mismo archivo al momento de querer cambiar de servidor, apuntando hacia una sola dirección en específico).

![Client-server](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/client-server.png)

### Cómo funcionan los servidores privados de WoW

Cuando se juega en servidores privados, el principio es exactamente el mismo. La diferencia radica en el software que se utiliza.

![Wow-Defias](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-defias.jpg)

**CLIENTE**. Todo el mundo tiene acceso al cliente original de World of Warcraft. Puedes obtenerlo fácilmente comprándolo o descargándolo en línea. Este programa es exactamente el que usarías para jugar en el servidor oficial. Obviamente los diferentes servidores privados tienen sus distintas versiones de cliente, pero siempre se refieren al mismo como Cliente Original. Sólo tienes que hacer un pequeño cambio dentro del archivo **realmlist.wtf** ya mencionado anteriormente, reemplazando la dirección del servidor oficial, por la de un servidor privado. Eso es todo, así de simple.

**SERVIDOR**. Esto es completamente diferente. Nadie fuera de Blizzard tiene acceso al software original que ejecuta los servidores oficiales de World of Warcraft. Así que estos programas son completamente diferentes del original.

### Ingeniería inversa

![Reverse engineering](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/reverse-engineering.jpeg)

Todos los programas que ejecutan servidores privados han sido creados mediante la técnica de "ingeniería inversa", que, en palabras sencillas, significa: **intento escribir un programa que imita el comportamiento de otro programa, sin mirar / tener acceso al código original**.

La pregunta ahora es: ¿quién implementó este software y cuándo ocurrió?

#### Resúmen de los Derechos de Autor

**Todo el material con derechos de autor (imágenes, sonidos, modelos 3D, logotipos, etc...) se encuentra dentro de la aplicación cliente.
La aplicación del servidor sólo contiene números y textos. Por lo tanto, es absolutamente legal si se utiliza con fines educativos.**

## Aplicaciones no oficiales del servidor WoW

¿Quién crea las aplicaciones de software que ejecutan los servidores privados de WoW (comúnmente llamados **emuladores**)? ¿Y cómo lo hacen?

### Complejidad

![Complex](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/complex.jpg)

No hace falta ser un experto para entender que escribir un programa de tipo servidor para un **MMORPG** con un alcance tan grande como World of Warcraft no es ciertamente un juego para niños.

Blizzard es una gran empresa con miles de empleados a su disposición. Escribir un programa que "imita" en cierta medida el funcionamiento de su aplicación original de servidor no es ciertamente trivial o factible para un solo individuo (o un pequeño grupo de programadores).

Y no es sólo una cuestión de complejidad. Pensemos en tareas muy triviales pero repetitivas, como añadir cada PNJ (Personaje No Jugable) al mundo, incluyendo cada elemento del botín con su respectivo porcentaje de probabilidad, etc... Básicamente un trabajo estupendo, y difícil. Sin mencionar todas aquellas tareas mucho más complejas que requieren horas de estudio y pruebas sin parar, como la mecánica de los hechizos, la mecánica de los jefes, etc.

En resúmen... ni siquiera el mejor programador del mundo podría hacer todo ese trabajo por su cuenta, necesita de ayuda sí o sí.

Sin embargo, existen multitud de servidores privados, y claro está, el respectivo software que los hace funcionar. Algunos servidores privados son ahora capaces de ofrecer una calidad de juego que no está lejos de la original (aquí me refiero principalmente a las antiguas expansiones).

¿Cómo es posible?

### MaNGOS y su modelo de desarrollo de Código Abierto

> Si tú tienes una manzana y yo tengo una manzana y nos intercambiamos estas manzanas, entonces tú y yo seguiremos teniendo una manzana cada uno. Pero si tú tienes una idea y yo tengo una idea e intercambiamos estas ideas, entonces cada uno de nosotros tendrá dos ideas. (George Bernard Shaw)

Sólo para hacerlo simple: un programa de código abierto es un programa cuyo código es público.

En el contexto de los servidores privados, el código abierto desempeña un papel fundamental.

Algunos jugadores veteranos pueden recordar que una vez la calidad del juego en los servidores privados era realmente mala. Casi nada funcionaba.
Por ejemplo, si eras un pícaro en sigilo, podrías ser el objetivo de cualquiera que escribiera `/target nickname`. Adivina qué clase elegí para mi primer personaje...

![Mangos-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/mangos-logo.gif)

La verdadera revolución fue [MaNGOS](https://www.getmangos.eu/), un proyecto de código abierto creado en 2005, cuyo propósito era proporcionar una aplicación de tipo servidor para World of Warcraft.
La gran noticia de MaNGOS, además de su fuerza, fue el hecho de que como aplicación de código abierto, su código era completamente público y cualquier usuario de todo el mundo podía estudiarlo y ofrecer su propia contribución (tanto en términos de añadir o arreglar mecánicas de juego, como en términos de reportar errores).

Sólo así, gracias a la contribución de muchos voluntarios de diferentes nacionalidades, fue posible desarrollar una aplicación de servidor capaz de emular World of Warcraft con una mayor calidad de juego.

En 2009 nació otro proyecto importante [TrinityCore](https://www.trinitycore.org/), basado en MaNGOS.

![Trinitycore-logo](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/trinitycore-logo.png)

Hasta la fecha, la abrumadora mayoría de los servidores privados funcionan con aplicaciones basadas en MaNGOS/TrinityCore.

A lo largo de los años, [diferentes proyectos](http://mangosrumors.org/best-wow-emulator-2020/) se basaron en el código MaNGOS/TrinityCore, y únicamente varían en la versión del WoW que soportan cada uno de ellos.

Por ejemplo [AzerothCore](https://www.azerothcore.org/) para la 3.3.5, [OregonCore](https://github.com/OregonCore) para la 2.4.3, [SkyFire](https://www.projectskyfire.org/) para la 5.4.8, [CMaNGOS](https://cmangos.net/) para Classic/TBC/WOTLK, y muchos otros más... Todos ellos basados en MaNGOS y/o TrinityCore por supuesto.

![Azerothcore-authserver](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/azerothcore-authserver.png)

### Resúmen

Por tanto, los servidores privados han alcanzado tal calidad, sólo gracias a los numerosos colaboradores que han implementado más y más características del juego a lo largo de los años (desde el año 2005 hasta el día de hoy).

Hoy en día cualquier usuario de PC sin una mínima experiencia en programación puede instalar y compilar un servidor del WoW sin más dilaciones.

## Código Abierto vs Servidores Privados

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

En realidad, el código MaNGOS/TrinityCore (y sus proyectos derivados) es liberado bajo la [GNU GPL license](https://es.wikipedia.org/wiki/GNU_General_Public_License).

En palabras sencillas, esta licencia dice lo siguiente: 
**Usa el código para hacer lo que quieras, sin pagar nada, siempre y cuando cualquier modificación del código original sea también liberada bajo la misma licencia.
Básicamente, la licencia de estos proyectos requiere que aquellos que los usan publiquen cualquier cambio al público y lo compartan con el resto de la comunidad..**

Por supuesto, la mayoría de los servidores privados usan esta licencia como **papel higiénico**. De lo contrario, no debería de haber ningún servidor privado que funcionase mejor que otro por ejemplo.

[Para más información véase mi post al respecto sobre algunas diferencias dentro de estas mismas licencias](https://wowcreador.com/threads/no-todas-las-licencias-gpl-son-iguales.2436/) **(Mathematical)**

![Toilet-paper](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/toilet-paper.jpg)

## Las mentiras y los inventos de los Servidores Privados

Aquí hay una lista de mentiras que los administradores de muchos servidores privados del WoW siguen diciendo a sus jugadores (muchas de ellas bastante ingeniosas he de decir):

### Escribimos este núcleo / core (emulador)

Falacias. No importa cuántos cambios hayas hecho "tú" como individuo independiente, empezaste con todo ello partiendo de un proyecto basado en MaNGOS.

Quizá y hayas hecho algunas mejoras en el mismo, eso es algo que no te rebatiré, pero la mayor parte del código sigue siendo proveniente de MaNGOS/TrinityCore, no tuya como ya podrás apreciar con claridad.

Tal vez eres muy buen programador y quizá hayas reescrito la mayor parte del código a lo largo de los años. Sin embargo, ten muy en cuenta que iniciaste desde MaNGOS. Sin él, ni siquiera tú solito habrías conseguido que funcionara el inicio de sesión de tu juego, por ello te pido un poco más de mente para poder repensar la situación a profundidad y no dejarte llevar por el ego de tus pensamientos.

### Hemos arreglado "x" bug.

En la gran mayoría de los casos, ninguno de ellos ha arreglado realmente nada. Acaban de descargar las correcciones provenientes de la comunidad de código abierto y psoteriormente las han implementado dentro de su emulador. Aún así se llevan todos los créditos. Esto último es muy fácil de desmentir realmente. Si sos jugador de wow, podrás observar que prácticamente ningún servidor, tiene los créditos de la comunidad que lo ayuda a llevar adelante el proyecto. Incluso, muchos de ellos, se desesperan por eliminar dichos créditos mediante diferentes pretextos.

### "Nosotros (realmente) arreglamos X"

Algunos servidores privados realmente arreglan las cosas por su cuenta, lamentablemente. A menudo tienen equipos de desarrollo dedicados que son pagados con el dinero de las donaciones de los jugadores.

La inmensa mayoría de ellos no comparten estos arreglos con la comunidad de desarrollo (Oh sorpresa).

Bueno, la licencia GPL del software que estás usando para ejecutar tu servidor ilegal te pide que lo compartas, pero aún así lo mantienes privado. Así que te odiaré igualmente.

### Eliminamos los créditos por un tema de seguridad. **(Stevej)**

Con la excusa de ocultar los créditos, muchas personas argumentan, que si los jugadores conocieran de antemano el emulador que se usa en su comunidad, podrían hacer uno de los diferentes errores que han sido reportados pero no arreglados por la misma. Entonces, justifican no exponer dichos créditos por ese motivo. Luego cuando tienen un ataque de DDoS corren desesperados a los brazos de las comunidades para pedir ayuda / soporte.

![Pinocchio](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/pinocchio.jpeg)

## Las supuestas 'justificaciones' de los servidores privados


### "Los mantengo en privado para hacer de mi servidor un lugar especial, mejor que los otros"

Muy bien, campeón. Intenta pensar en esto: si TODOS los desarrolladores hicieran lo mismo, ni tú ni tu servidor privado podrían funcionar en primer lugar.

¿Por qué? Simplemente porque ni MaNGOS (ni TrinityCore, AzerothCore, etc...) existirían como tal.
**Estos proyectos existen gracias a los desarrolladores que, a diferencia de ti, sí compartieron su código.**

Si todos los desarrolladores mantuvieran su código en privado, no tendríamos un solo emulador del WoW medianamente decente y tú tampoco podrías abrir tu servidor privado, ya que no habría ningún software disponible.

### "Si compartiera mis arreglos, la 'competencia' las robaría"

**No hay nada que robar. Simplemente no pueden robar un código que no te pertenece en primer lugar**. Ni siquiera existe constancia de que lo hayas escrito tu.

La filosofía del código abierto es clara: puedes usar ese código de forma gratuita, siempre y cuando cualquier modificación hecha en él DEBA de hacerse pública (tu me das, yo te doy, todos ganamos)

¿No estás de acuerdo con este planteamiento? Está bien. Entonces no uses ningún proyecto de código abierto y escribe, por tu propia cuenta un emulador de WoW desde la nada misma.

## Cómo afecta esto a los jugadores

![Wow-Dranei-crying](https://raw.githubusercontent.com/FrancescoBorzi/why-I-hate-wow-private-servers/master/img/wow-dranei-crying.jpg)

Comprendo que toda esta historia sobre la ética y las licencias importa muy poco al jugador promedio de World of Warcraft.
Al final, son los mismos jugadores quienes solamente buscan jugar en el servidor más estable y medianamente funcional que se topen por ahí, no les importa realmente mucho si ese servidor en particular colabora con el código abierto o no.

Sin embargo... intenta, así sea por un momento verlo desde otra perspectiva.

A los desarrolladores de los proyectos de código abierto (MaNGOS, TrinityCore, AzerothCore, etc...) básicamente no les importa mucho lo que hacen los servidores privados.
Por supuesto, como desarrollador te molesta ver a algún administrador de servidores al azar tomando créditos por tu trabajo, pero al final no cambia tu vida.
Muchos desarrolladores de código abierto sólo lo hacen por diversión y con fines educativos, por amor al arte o por amor a la ciencia.

En realidad, si TODOS los servidores privados colaboraran con el código abierto, ¡las vidas de los jugadores cambiarían por completo! (Lamentablemente esto nunca se trató de los jugadores como tal, sino de los beneficios que se obtienen a cambio de ellos mismos, al final sólo son usados como moneda de cambio...)
En ese caso, cada servidor proporcionaría una experiencia de juego mucho mejor para cualquier expansión. El ejemplo de Alice y Bob mencionado anteriormente puede aplicarse a este caso también.

Sin embargo, la realidad es justamente esa: hay muchos servidores privados en todo el mundo, cada uno de ellos siempre trabaja en las mismas cosas.
Si en cambio colaboraran entre ellos, evitarían hacer trabajos innecesarios y tendrían más tiempo y mano de obra. Así que seguramente serían capaces de lograr mucho más.

**Nota: la calidad (y la competencia) entre los servidores privados no debe ser (sólo) de arreglos o modificaciones, sino también de otros factores como por ejemplo la habilidad que tienen sus administradores para saber manejarlo. La calidad de la comunidad también juega un papel fundamental, al igual que ocurre con los servidores de Blizzard (que son todos iguales desde el punto de vista técnico).**

Si un servidor privado es cerrado por motivos varios y sus desarrolladores no han compartido el trabajo hecho allí mismo, me temo que se perderá para siempre y sólo Dios sabrá dónde quedaron esos cambios.

## Exponer las mentiras

### Lista oficial de Autores/Contribuidores

Lo más interesante es que todos aquellos proyectos basados en MaNGOS son enteramente públicos, por lo que es posible verificar con precisión quiénes contribuyeron a ellos independientemente de la época en que lo hicieron.

Como resultado, todas las listas de contribuyentes son completamente públicas y CUALQUIER persona, sea quien sea puede verificar quién fue el que añadió o modificó cada cosa dentro del emulador.

Por decirte algo:

- Lista oficial de colaboradores de MaNGOS: https://github.com/cmangos/mangos-wotlk/blob/master/AUTHORS.md
- Lista oficial de colaboradores de TrinityCore https://github.com/TrinityCore/TrinityCore/blob/3.3.5/AUTHORS
- Lista oficial de colaboradores de AzerothCore https://github.com/AzerothCore/azerothcore-wotlk/graphs/contributors

PD: Tú mismo puedes encontrar al autor de éste mismo artículo (Francesco Borzì aka Shin) en todas las listas ya mencionadas más arriba.

### Lista oficial de Commits

Cualquier proyecto de código abierto (generalmente alojado en GitHub o también en Gitlab) tiene una lista de commits realizados por los diferentes desarrolladores que alguna vez contribuyeron al repositorio. Para cada commit, tanto el autor del mismo como la fecha se encuentran almacenadas allí.

Es realmente fácil verificar esta información, sólo basta con abrir el repositorio oficial de cualquier emulador. Buscar en Google por ejemplo "TrinityCore github" o "AzerothCore github" y verificar aquello que te mencionaba antes.

Con esta información a la mano, tú mismo verás por cuenta propia quién dice hacer realmente qué. Verás todas y cada una de las líneas de código junto con sus respectivos autores y los comentarios de otros desarrolladores, etc. En fin, verás absolutamente todo sin necesidad de explicarlo a detalle. ¡Basta de mentiras!

## ¿Y qué puedo hacer yo como jugador?

Mi consejo es que jueguen y también apoyen a aquellos [Servidores Comunitarios](https://wowcreador.com/threads/servidores-privados-o-servidores-de-la-comunidad-servidores-publicos.2403/) (hacer distinción de los 'servidores privados', que por cierto, de privados no tienen nada) que colaboran directamente con el código abierto, independientemente del tipo de expansión o emulador que utilicen.

Y pues como alternativa a lo primero, por lo menos intenten evitar a toda costa y en la medida de lo posible aquellos servidores que se jactan de vender el trabajo de otras personas haciéndolo pasar como suyo propio, eliminando los créditos de los autores originales en el proceso, burlándose en la cara de la comunidad y haciendo apología de sus actos por "un bien mayor".

**NOVEDAD:** en el año 2021 la comunidad de AzerothCore ha puesto en marcha un nuevo proyecto bajo el nombre de [ChromieCraft](https://www.chromiecraft.com/about), con el principal objetivo de ser un servidor completamente dependiente del [Código Abierto](https://es.wikipedia.org/wiki/C%C3%B3digo_abierto) y con un tinte de progresividad en el mismo.

![ChromieCraft logo](https://avatars1.githubusercontent.com/u/68329413?s=400&u=084b35243e0aed1becd6a67fa88717eb8c1674d8&v=4)

### Más información acerca del software libre

- https://www.gnu.org/philosophy/free-sw.es.html
- https://es.wikipedia.org/wiki/Software_de_c%C3%B3digo_abierto
- https://wowcreador.com/threads/no-todas-las-licencias-gpl-son-iguales.2436/ (Post informativo acerca de las diferencias de las Licencias GPL) **(Mathematical)**


## Agradecimientos

Agradecimientos especiales a **Laura Bartiromo**
