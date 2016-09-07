# Ideas para Posts:  
## Comandos:  

 - [**Formato del texto en el sidebar-display del scoreboard**](#scoreboard-format)
 - [**Loot tables: descripción, tutorial y aplicaciones**](#loot-tables)
 - [**Translate en el texto en JSON**](#translate)
 - [**Cargadores de Chunks**](#chunk-loaders)
 - [**Hojas de cálculo y comandos**](#hojas-de-calculo-y-comandos)
 - [**Guia sobre el Structure Block**](#guia-sobre-el-structure-block)

### Scoreboard Format:
Formato del texto que se muestra en el display lateral (*`sidebar`*) de un scoreboard:  
![](http://i2.wp.com/i.imgur.com/Lf5PQQ7.png)

> [LeMoesh - Tricks to format your scoreboard](http://moesh.ca/tricks-to-format-your-scoreboard/)  

[*Volver arriba*](#ideas-para-posts)


----------
### Loot tables:

> [Skylinerw - Custom Loot Tables](http://www.minecraftforum.net/forums/minecraft-discussion/redstone-discussion-and/command-blocks/2546347-1-9-custom-loot-tables?comment=1)  

[*Volver arriba*](#ideas-para-posts)


----------
### Translate:
> [LeMoesh - With Translate](http://moesh.ca/with-translate/)  
> [LeMoesh - Advanced Translations](http://moesh.ca/advanced-translations/)  
> [Usage of Translate](https://usecanvas.com/minecraft/minecraft-complex-translation/1i9ZLUInU8ul6Xl5CwJMg2)  
> 
> ------
> [LeMoesh - Packaging Resource Packs With Your Map](http://moesh.ca/packaging-resource-packs-with-your-map/)  

[*Volver arriba*](#ideas-para-posts)


----------
### Chunk Loaders:

> [LeMoesh - Spread Loaders (Loading chunks remotely)](http://moesh.ca/spread-loaders/)  
> [SimplySarc - *Remote Chunk Loader*](http://youtu.be/O8dv9P49cKk)  
> [SimplySarc - *The final chunck loader*](https://youtu.be/egqsmXD_oCM)  
> [Skylinerw - Perma-loaded spawn chunks](http://www.minecraftforum.net/forums/mapping-and-modding/maps/1537579-function-1-8-perma-loaded-spawn-chunks-void-world?comment=1)  

[*Volver arriba*](#ideas-para-posts)


----------
### Hojas de calculo y comandos:
Los comandos en Minecraft sirven para infinidad de cosas. Para hacer algunas de ellas, basta con escribir dos o tres comandos y conectarlos a un reloj, pero hay algunas que requieren de gran cantidad de comandos diferentes que, muchas veces, suelen seguir un patrón alfanumérico. El hecho de que todos sean distintos entre sí, por muy pocas diferencias que existan, hace que haya que escribirlos todos individualmente. En estas ocasiones emplear una hoja de cálculo o alguna aplicación similar, servirá para no tener que ir cambiando uno por uno modificando tan solo un par de caracteres, sino para poder crearlos todos de golpe y sin tener que dedicar horas a escribirlos.
Todo programa que realice operaciones matemáticas y permita modificar cadenas de caracteres servirá para automatizar la escritura de muchos comandos que, de no emplear estos programas para hacerlos, se convertirían en una tarea eterna. Los más populares y accesibles son las hojas de cálculo, como las de [*Excel*](https://products.office.com/es-es/excel) o [*Google Spreadsheets*](https://www.google.es/intl/es/sheets/about/), por lo que son las que voy a tratar en el desarrollo de este post.

Por el momento muchos de vosotros no habréis llegado a entender cómo **una hoja de cálculo puede facilitar enormemente la escritura de grupos de muchos comandos**. La respuesta es sencilla: todo se basa en la función de **`concatenar`**. Pondré el ejemplo del comando `clone`, que facilitará la comprensión de lo que pretendo transmitir en este post:
El comando clone sirve para copiar un volumen ortoédrico<sup>[1](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Ortoedro.png/320px-Ortoedro.png)</sup> con un tamaño máximo de **`32768`**<sup>`2^15`</sup> bloques (según está establecido desde la versión [14w26a](http://minecraft.gamepedia.com/14w26a#Changes) hasta la fecha actual [16w35a](http://minecraft.gamepedia.com/16w02a)). Si pretendemos clonar volúmenes superiores al tamaño máximo que permite el comando, necesitaremos emplear varios al mismo tiempo. Imaginemos que queremos clonar un volumen de `16`<sup>`2^4`</sup> chunks para resetear el mapa hardcore que acabamos de crear sin tener que copiarlo nuevamente al directorio de mapas. `16`<sup>`2^4`</sup> chunks son un total de **`1048576`**<sup>`2^20`</sup> bloques, ya que un chunk tiene `65536`<sup>`2^16`</sup> bloques (*`16x256x16`<sup>`2^(4+8+4)`</sup>*). Al ser este número mayor que la cantidad máxima de bloques que permite copiar el comando clone, necesitaremos emplear más comandos. Concretamente **`32`**<sup>`2^5`</sup> comandos, porque es el número que resulta de hallar el cociente de `1048576`<sup>`2^20`</sup> entre `32768`<sup>`2^15`</sup> (*para otros valores que no sean potencias de 2, se redondea a la alza*).
Comenzaremos indicando las coordenadas más pequeñas del volumen que vamos a clonar para así trabajar con números positivos. Suponiendo que el volumen que vamos a clonar se encuentra centrado en `[0,0]`, las coordenadas en las que empezaremos serán `[-32,0,-32]` y como abarcará `16` chunks, las cooredenadas finales serán `[31,256,31]`. Para empezar con la hoja de cálculo habrá que analizar cuántos conjuntos de datos son necesarios para componer el comando completo, en el caso de `/clone` son los siguientes:

    /clone <x1> <y1> <z1> <x2> <y2> <z2> <x> <y> <z>
 
Los tres primeros conjuntos de datos (*`<x1>`, `<y1>` y `<z1>`*) corresponden a la esquina inferior noroeste de nuestro volumen de `16` chunks. Los tres siguientes (*`<x2>`, `<y2>` y `<z2>`*), a la esquina superior sureste.
Los tres últimos (*`<x>`, `<y>` y `<z>`*) ubican la esquina inferior noroeste del lugar donde queramos clonar nuestro volumen.

Iremos ahora a una nueva hoja de cálculo de [*Excel*](https://products.office.com/es-es/excel) o [*Google Spreadsheets*](https://www.google.es/intl/es/sheets/about/) y distribuiremos cada uno de los conjuntos de datos del comando en columnas:
| /clone | x1 | y1 | z1 | x2 | y2 | z2 | x | y | z | OUTPUT |
|:-------|:---|:---|:---|:---|:---|:---|:--|:--|:--|-------:|



> [LeMoesh - Minecraft Command Blocks and Google Spreadsheets](http://moesh.ca/minecraft-command-blocks-and-google-spreadsheets-your-first-steps-to-madness/)  
> [KaliNuska - Hojas de cálculo y comandos](https://github.com/KaliNuska/Minecraft/blob/master/Hojas%20de%20c%C3%A1lculo%20y%20comandos.xlsx?raw=true)


----------

### Guia sobre el Structure Block:

> [Team Woloo](https://youtu.be/543WnTIThGc)  
> [Xisumavoid]()
> [SimplySarc](https://youtu.be/JkQ5TDUnNOg)