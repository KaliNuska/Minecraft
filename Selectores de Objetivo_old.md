# ![SELECTORES DE OBJETIVO](http://i.imgur.com/8prOWuF.gif "SELECTORES DE OBJETIVO")

*NOTA. El contenido de este post ha quedado obsoleto tras la actualización de Minecraft 1.13. Si deseas consultar el contenido actualizado lo podrás encontrar aquí: [minecraftmin.net/index.php?topic=7888](http://minecraftmin.net/index.php?topic=7888.msg41434#msg41434).*

## TOC
[Selectores de Objetivo:](#start-of-content)
  * [TOC](#toc)
  * [Introducción](#introducción)
  * [Variables](#variables)
  * [Argumentos](#argumentos)
    * [Seleccionar objetivos mediante coordenadas:](#seleccionar-objetivos-mediante-coordenadas)
    * [Seleccionar objetivos por el radio:](#seleccionar-objetivos-por-el-radio)
    * [Seleccionar objetivos dentro de un volumen:](#seleccionar-objetivos-dentro-de-un-volumen)
    * [Seleccionar objetivos por su modo de juego:](#seleccionar-objetivos-por-su-modo-de-juego)
    * [Seleccionar una cantidad de objetivos:](#seleccionar-una-cantidad-de-objetivos)
    * [Seleccionar objetivos por su experiencia:](#seleccionar-objetivos-por-su-experiencia)
    * [Seleccionar objetivos en base a su puntuación:](#seleccionar-objetivos-en-base-a-su-puntuación)
    * [Seleccionar objetivos por equipo:](#seleccionar-objetivos-por-equipo)
    * [Seleccionar objetivos por su nombre:](#seleccionar-objetivos-por-su-nombre)
    * [Seleccionar objetivos por su ángulo de inclinación de la visión:](#seleccionar-objetivos-por-su-ángulo-de-inclinación-de-la-visión)
    * [Seleccionar objetivos por `tag`:](#seleccionar-objetivos-por-tag)
    * [Seleccionar objetivos por tipo:](#seleccionar-objetivos-por-tipo)
  * [TLDR](#tldr)
  * [Despedida](#despedida)
  * [Historial de cambios](#historial-de-cambios)

## Introducción
**Los selectores de objetivo son utilizados en gran variedad de comandos, formando, en muchos de ellos, una parte esencial en su composición.**

Algunos de los comandos en los que se utilizan serán citados a continuación:
En el comando `clear`, sirven para indicar los jugadores a los que tiene que quitar los items:

    /clear @p[team=Rojo,r=50,m=0] minecraft:stone

En el `effect` sirve para escoger los jugadores a los que aplicar los efectos:

    /effect @a[r=2,m=0] minecraft:blindness 5 3

En el `execute` es una parte fundamental ya que evita que el comando siguiente sea ejecutado en la posición relativa de todas las entidades o jugadores:

    /execute @e[type=Zombie,x=-10,y=60,z=-10,dx=20,dy=5,dz=20] ~ ~ ~ detect ~ ~-1 ~ minecraft:sand -1 /summon LightningBolt

Al igual que es muy necesario en el comando `tp`:

    /tp @e[type=Creeper,r=5] @r[team=Blue]

Sin embargo, hay otros comandos como el `setblock`, `time` o el `clone` en los que no hay necesidad de indicar objetivos y no es preciso emplear selectores.

Además, hay otros comandos que emplean el formato JSON. En éstos, para añadir los selectores habrá que introducirlos de forma distinta: **`selector:"@e"`** o **`selector:\"@p[team=Rojo]\"`**. Éste es el caso del `tellraw` o `title` entre otros:

    /tellraw @a {selector:"@p[r=5]"}
    /title @a title {selector:"@p[r=2]",color:gold}

## Variables
**En los comandos en los que hace falta **especificar** al jugador o entidad al que van dirigidos, ésto se consigue mediante un **argumento** y una serie de **condiciones**.**

Para ello se emplea una variable de selección de objetivo y, opcionalmente, varios argumentos que incrementen las condiciones a satisfacer.

Las variables de selección de objetivo (`@a`, `@p`, `@r`, `@e`) identifican la categoría general de los objetivos que queramos seleccionar. Hay 4 tipos:

| Variable | Descripción |
|:--|:--|
| **`@p`:** | Selecciona al jugador más próximo. *Si dos o más se encontraran a la misma distancia, el que más recientemente se hubiera unido al servidor sería seleccionado.* |
| | Los argumentos servirán para especificar las condiciones que debe tener el jugador más cercano escogido. Por ejemplo, **`@p[m=1]`** seleccionará al jugador más cercano que esté en creativo a pesar de haber otros más cerca que no estén en creativo. |
| | El argumento `c` puede usarse para incrementar el número de jugadores a seleccionar (**`@p[c=5]`** escogerá a los 5 más cercanos). *Si su valor es negativo, pasa a seleccionar a los más lejanos (**`@p[c=-1]`** escogerá al que más lejos se encuentre). |
| **`@r`:** | Esta variable es empleada para seleccionar un jugador aleatorio (o entidad si el argumento `type` está incluido). |
| | Otros argumentos servirán para reducir el rango total de jugadores/entidades del que se escoge uno/a aleatorio/a. Por ejemplo, **`@r[team=Equipo1]`** servirá para seleccionar un jugador del Equipo1 de forma aleatoria. |
| | El argumento `c` puede usarse para incrementar el número de jugadores a seleccionar (**`@r[c=4]`** escogerá a cuatro jugadores aleatoriamente). |
| **`@a`:**  |Selecciona a todos los jugadores, incluyendo a los que han muerto (ninguna de las otras variables los incluye). |
| | En este caso los argumentos servirán para reducir el número de jugadores en la selección. Por ejemplo, **`@a[team=EquipoAzul]`** escogerá a todos los jugadores del EquipoAzul. |
| **`@e`:** | Con esta variable se seleccionan todas las entidades. Incluye a los jugadores. |
| | Los argumentos servirán para diferenciar los tipos de entidad o para reducir el rango de selección. Por ejemplo, **`@e[type=slime]`** sólo escogerá Slimes en la selección y **`@e[name=!Grumm]`** lo hará con todas aquellas entidades que no se llamen Grumm. |

## Argumentos
**Después de introducir la variable de selector de objetivo, puedes elegir emplear argumentos para modificar los objetivos seleccionados.**

Cuando la variable es **`@a`** o **`@e`** los argumentos solamente podrán reducir el rango de selección. Sin embargo, con **`@p`** y **`@r`**, especificarán a partir de qué distancia o característica se empieza a seleccionar el jugador más próximo o aleatorio respectivamente.

Los argumentos se separan entre sí mediante comas y están contenidos dentro de unos corchetes a continuación de la variable:

    @<variable>[<argumento1>=<valor>,<argumento2>=<valor>,<argumento3>=<valor>,...]
***No se permiten espacios ni otros caracteres especiales al definir argumentos. Las comas han de ser empleadas únicamente en separar argumentos, nunca dentro de los mismos.***

Los argumentos son sensibles a las mayúsculas y aquellos que no existan serán ignorados. Por ejemplo: **`@e[type=Zombie]`** detectará a todos los Zombies, pero **`@e[Type=Zombie]`** *(`Type` con mayúscula)* detectará todas las entidades puesto que al no existir `Type`, sino `type`, el argumento se ignora.

En versiones previas a la `1.11`, los cuatro primeros argumentos podían no ser especificados y los valores que hubiera en su lugar corresponderían a los argumentos `x`, `y`, `z` y `r`. Esta funcionalidad fue eliminada del juego y ahora estos argumentos han de ser definidos normalmente.

Anteriormente, los siguientes dos selectores de objetivo funcionaban de forma idéntica: **`@e[x=10,y=64,z=-10,r=20]`** = **`@e[10,64,-10,20]`**. Ahora el primero obtendrá todas las entidades que cumplan esos criterios, mientras que el segundo mostrará un error al intentar ejecutarlo.

A continuación pongo una lista con el uso que se puede hacer de cada argumento:

### Seleccionar objetivos mediante coordenadas:
Los argumentos `x`, `y` y `z` sirven para seleccionar a partir de una posición exacta. Si el radio también se especifica, solamente escogerá a los que se encuentren dentro de la zona indicada por éste.

> ![](http://i.imgur.com/kWE9bYT.png) ![](http://i.imgur.com/jWmCRMe.png)
En el primer caso el comando se ejecutará en los jugadores que ocupen la ubicación del bloque de heno, mientras que en el segundo, en los jugadores que estén dentro de la esfera de radio `r` centrada en las coordenadas `x`, `y` y `z`.

Las coordenadas tienen que ser enteras y no pueden ser relativas (empleando virgulillas (`~~~`)).

### Seleccionar objetivos por el radio:
Existen dos argumentos que permiten seleccionar los objetivos que se encuentren en un radio determinado: `r` y `rm`.

El argumento `r` seleccionará a todos aquellos objetivos que se encuentren dentro del radio indicado. Al contrario, `rm` seleccionará a todos los que estén fuera del radio mínimo.

Al combinar ambos argumentos, sólo serán seleccionados los objetivos que están entre el radio mínimo y el máximo. Ejemplos: **`@e[r=20]`** seleccionará a las entidades que estén en un radio de 20 bloques, **`@e[rm=5]`** sólo lo hará con las que estén a 5 o más bloques de distancia. Sin embargo, **`@e[r=10,rm=5]`** seleccionará todas aquellas entidades que se encuentren en el área de la corona circular de radios 5 y 10.

Cuanto mayor sea el radio, más precisión tendrá el límite de la selección, puesto que el círculo será mayor.

### Seleccionar objetivos dentro de un volumen:
Los argumentos `dx`, `dy` y `dz` son los que nos permiten seleccionar aquellos objetivos que se encuentren dentro del volumen que delimitan. Sus valores han de indicarse siempre como absolutos ya que **no pueden ser negativos**.

Estos argumentos no definen coordenadas, sino que indican la cantidad de bloques que el volumen de selección aumenta en cada eje.

Si los argumentos `x`, `y` y `z` no son determinados, la selección saldrá del lugar de ejecución del comando. Si están determinados, comenzará en las coordenadas que indiquen. Como `dx`, `dy` y `dz` no pueden ser negativos, `x`, `y` y `z` tendrán que referirse al punto inferior al sureste del volumen (puesto que el aumento de esas coordenadas en sus ejes, siempre será positivo).

Al añadir los argumentos `r` o `rm` al selector, los objetivos que se podrán seleccionar tendrán que estar situados dentro del volumen y de los radios indicados.

Por ejemplo, queremos un selector que compruebe si el jugador más cercano se encuentra en una sala cuya esquina inferior sureste se corresponde con las coordenadas `-5`, `55`, `-5`. El tamaño de la sala es un cubo de `10` bloques de arista. El selector que nos hará falta será este: **`@p[x=-5,y=55,z=-5,dx=10,y=10,dz=10]`**.

### Seleccionar objetivos por su modo de juego:
El argumento `m` es el que nos permite detectar el modo de juego de los jugadores.

Los valores admitidos para este argumento son los siguientes:

| **Valor:**| **Modo de juego:** |
|--:|:--|
| `-1`| Todos los modos de juego |
| `0`| Modo survival |
| `1`|  Modo creativo |
| `2`|  Modo aventura |
| `3`|  Modo espectador |

Con el selector **`@p[m=1]`** serán seleccionados todos los jugadores en creativo.

### Seleccionar una cantidad de objetivos:
El argumento `c` nos permite indicar el número de objetivos que queremos que sean seleccionados. Normalmente se añaden los más cercanos al lugar de ejecución del comando.

Cuando se emplea con las variables `@p` o `@r`, si este argumento no está determinado, tiene el valor de 1 por defecto. Por tanto, cualquier número que se le asigne aumentará la cantidad de objetivos. Por el contrario, si se emplea con `@a` o `@e`, seleccionará los que se encuentren más cerca.

Si la distancia de dos o más objetivos al lugar de ejecución del comando es la misma, se escogerá al que más tiempo lleve en el servidor o al primero que se haya creado. Por ejemplo, si dos jugadores están a 3 bloques del bloque de comandos, el único que será seleccionado con **`@p[c=1]`** será el primero que haya entrado al servidor.

Si este argumento tiene un valor negativo, el orden de los objetivos es el contrario. Por ejemplo, **`@p[c=-5]`** seleccionará los 5 jugadores más alejados y, si estuvieran a la misma distancia, a los que más recientemente se hayan unido al servidor.

### Seleccionar objetivos por su experiencia:
Para esta función tenemos dos argumentos: `l` y `lm`.

El argumento `l` sirve para seleccionar a los objetivos con un nivel igual o inferior al del valor asignado. Por el contrario, `lm` seleccionará a los que tengan ese nivel o uno mayor.

Si se determinan los dos argumentos, escogerá los objetivos cuya experiencia esté comprendida en el intervalo de sus valores.

Ejemplos: El selector **`@a[l=5]`** seleccionará a los jugadores que tengan experiencia 5 o menor. Al emplear **`@a[l=10,lm=7]`** se escogerán los jugadores en los que el valor de su experiencia esté comprendida entre 7 y 10, ambos incluidos.

### Seleccionar objetivos en base a su puntuación:
Para esta función tenemos, nuevamente, dos argumentos: `score_<scoreboard>` y `score_<scoreboard>_min`.

Mediante **`@e[score_<scoreboard>=10]`** se seleccionan los objetivos que tengan una puntuación no superior a 10. El caso contrario sucede con **`@e[score_<scoreboard>_min=50]`**.

Cuando ambos argumentos son determinados, se seleccionarán los objetivos que tengan la puntuación comprendida en el intervalo entre los dos. Por ejemplo, **`@a[score_Muertes_min=2]`** escogerá a los jugadores que hayan muerto mínimo de dos veces, pero al añadir el **`score_Muertes=10`** dejará de hacerlo con aquellos que tengan más de 10 muertes.

### Seleccionar objetivos por equipo:
Esta función sólo tiene un argumento disponible: `team`. Este argumento nos permite seleccionar a aquellos objetivos que estén en un team con **`@a[team=Rojo]`**, a los que no estén en ese team con **`@a[team=!Rojo]`** o a los que no estén en ningún equipo: **`@a[team=]`**.

Al añadir los argumentos de `score` permite seleccionar objetivos que, dentro de un team, tengan cierto score.

### Seleccionar objetivos por su nombre:
El argumento que nos permite introducir el nombre que queremos (o no) que tengan los objetivos es: `name`.

Su uso es tan simple como que **`@e[name=jeb_]`** selecionará a todas las entidades nombradas "jeb_". Por el contrario, **`@a[name=!Grumm]`** escogerá a todas las que no se llamen "Grumm".

He de aclarar nuevamente que no se permiten espacios ni otros caracteres especiales al definir argumentos, por lo que esto drberá tenerse en cuenta a la hora de nombrar las entidades.

### Seleccionar objetivos por su ángulo de inclinación de la visión:
Como tenemos dos planos, uno horizontal y otro vertical, nos hará falta un argumento específico para cada uno. Como además tienen máximos y mínimos, tendremos cuatro disponibles:

| **Argumento:**|  **Descripción:**| **Ejemplo:** |
|--:|:--|:--|
| `rx`|  Indica la rotación vertical máxima| **`@a[rx=-45]`** |
| `rxm`| Indica la rotación vertical mínima| **`@a[rxm=-80]`** |
| `ry`| Indica la rotación horizontal máxima| **`@a[ry=45]`** |
| `rym`|  Indica la rotación horizontal mínima| **`@a[rym=80]`** |

Los valores de la rotación vertical están entre -90.0 y 90.0 correspondiendo con arriba y abajo respectivamente.

Los de la horizontal varían desde -180.0 hasta 179.9 correspondiento con las siguientes direcciones:

| **Direción:**| **Valor:**| **Ejemplo:** |
|--:|--:|:--|
| Norte|-180.0| **`@p[ry=-170,rym=170]`** |
| *Nordeste*|-135.0| **`@p[ry=-125,rym=-145]`** |
| Este|-90.0| **`@p[ry=-100,rym=-80]`** |
| *Sudeste*|-45.0| **`@p[ry=-55,rym=-35]`** |
| Sur|-0.0| **`@p[ry=10,rym=-10]`** |
| *Sudoeste*|45.0| **`@p[ry=55,rym=35]`** |
| Oeste|90.0| **`@p[ry=100,rym=80]`** |
| *Noroeste*|135.0| **`@p[ry=145,rym=125]`** |

### Seleccionar objetivos por `tag`:
A la hora de crear una entidad, ésta se puede diferenciar del resto mediante la NBT Tag: `Tags:[]`. La/s tag/s que le haya/n sido introducida/s a la entidad podrá/n ser objeto de selección al emplear la variable `tag` en la detección de objetivos.

Como ejemplo, un `armor_stand` que haya sido creado mediante el comando **`/summon armor_stand ~ ~ ~ {Tags:["TAG1"]}`** podrá ser especificado en la selección de objetivos mediante **`@e[type=armor_stand,tag=TAG1]`**, al igual que todas las entidades que no lo tengan podrán ser seleccionadas mediante **`@e[tag=!TAG1]`**. Además de estas dos funcionalidades más evidentes, la variable `tag` permite seleccionar todas las entidades que tengan y que no tengan tags mediante los selectores **`@e[tag=]`** y **`@e[tag=!]`**, respectivamente.

### Seleccionar objetivos por tipo:
Esta función consiste en poder especificar qué entidades van a ser seleccionadas. Para ello utilizaremos el argumento `type`.

El valor que se le asigne tiene que ser el nombre del tipo de entidad de una entidad existente (debe estar escrita con el formato correspondiente). Si la entidad no es válida, el comando mostrará un error.

Para seleccionar todos los armor_stand del mapa, se utiliza este selector: **`@e[type=minecraft:armor_stand]`**. Por el contrario, para escoger a todas aquellas que no sean slimes, emplea este: **`@e[type=!slime]`**.

Si el argumento `type` se combina con la variable `@r`, cambia su función para seleccionar, de entre todos los ejemplares de la entidad indicada, uno o más de forma aleatoria.

## TLDR
**Para concluir el post, añadiré una relación de las variables y los argumentos con su función:**

| **Variable:**| **Función:** |
|--:|:--|
| @p|  Jugador más cercano |
| @r| Jugador aleatorio |
| @a| Todos los jugadores |
| @e| Todas las entidades |

| **Argumento:**| **Criterio de selección:** |
|--:|:--|
| `x`, `y`, `z`|  Coordenada |
| `r`, `rm`| Radio (máx, mín) |
| `dx`, `dy`, `dz`| Dimensiones del volumen |
| `m`| Modo de juego |
| `c`| Cantidad |
| `l`, `lm`| Nivel de experiencia (máx, mín) |
| `score_[scoreboard]` `score_[scoreboard]_min`|  Puntuación del Scoreboard |
| `team`|  Equipo |
| `name`| Nombre |
| `rx`, `ry`, `rxm`, `rxy`|  Inclinación de la visión (máx, mín) |
| `tag`| Etiqueta |
| `type`| Tipo de entidad |


## Despedida
***Espero que este post sea de utilidad y que sus lectores sepan apreciar el esfuerzo que me ha llevado hacerlo.
Si tienen alguna duda, coméntenla para que se la pueda resolver.***

## Historial de cambios
En Domingo, 20 de Noviembre de 2016 los cambios realizados con respecto a la edición previa del 19 de Enero de 2015 son:

|Cambios|Contenido|
|:--|:--|
| Adaptación del post a los cambios más recientes de la versión oficial 1.11:| |
| |Modificados los nombres de los tipos de mob de acuerdo con los cambios de la versión [16w32a](http://minecraft.gamepedia.com/16w32a). |
| |Las cuatro primeras variables de un selector ya no equivalen a x, y, z y r en caso de no ser indicada su categoría. |
| Corregidos errores de escritura y de formato.| |
| Mejora de la expresión de algunas partes del contenido.| |
| Agregadas dos imágenes.| |

[![Arriba](http://i.imgur.com/lVbypSJ.png "Arriba")](#start-of-content)
