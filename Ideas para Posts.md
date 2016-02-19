# Ideas para Posts:  
## Comandos:  

 - [**Formato del texto en el sidebar-display del scoreboard**](#scoreboard-format)
 - [**Loot tables: descripción, tutorial y aplicaciones**](#loot-tables)
 - [**Translate en el texto en JSON**](#translate)
 - [**Cargadores de Chunks**](#chunk-loaders)
 - [**Hojas de cálculo y comandos**](#hojas-de-calculo-y-comandos)

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
Los comandos en Minecraft sirven para infinidad de cosas. Para hacer algunas de ellas, basta con escribir dos o tres comandos y conectarlos a un reloj, pero hay algunas que requieren de gran cantidad de comandos que, muchas veces, suelen seguir un patrón numérico que haga que se diferencien entre sí. El hecho de que todos sean distintos entre sí, por muy pocas diferencias que existan, hace que haya que escribirlos todos individualmente. En estas ocasiones emplear una hoja de cálculo o alguna aplicación similar, servirá para no tener que ir cambiando uno por uno modificando tan solo un par de caracteres, sino para poder crearlos todos de golpe y sin tener que dedicar horas a escribirlos.
Todo programa que realice operaciones matemáticas y permita modificar cadenas de caracteres servirá para automatizar la escritura de muchos comandos que, de no emplear estos programas para hacerlos, se convertirían en una tarea eterna. Los más popularizados y accesibles son las hojas de cálculo, como las de [*Excel*](https://products.office.com/es-es/excel) o [*Google Spreadsheets*](https://www.google.es/intl/es/sheets/about/), por lo que son las que voy a tratar en el desarrollo de este post.

Por el momento muchos de vosotros no habréis llegado a entender cómo **una hoja de cálculo puede facilitar enormemente la escritura de grupos de muchos comandos**. La respuesta es sencilla: todo se basa en la función de **`concatenar`**. Pondré el ejemplo del comando `clone`, que facilitará la comprensión de lo que pretendo transmitir en este post:
El comando clone sirve para copiar un volumen ortoédrico<sup>[1](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Ortoedro.png/320px-Ortoedro.png)</sup> con un tamaño máximo de **`32768`**<sup>`2^15`</sup> bloques (según está establecido desde la versión [14w26a](http://minecraft.gamepedia.com/14w26a#Changes) hasta la fecha actual [16w02a](http://minecraft.gamepedia.com/16w02a)). Si pretendemos clonar volúmenes superiores al tamaño máximo que permite el comando, necesitaremos emplear varios al mismo tiempo. Imaginemos que queremos clonar un volumen de `8`<sup>`2^3`</sup> chunks para resetear el mapa hardcore que acabamos de crear sin tener que copiarlo nuevamente al directorio de mapas. `8`<sup>`2^3`</sup> chunks son un total de **`524288`**<sup>`2^19`</sup> bloques, ya que un chunk tiene `65536`<sup>`2^16`</sup> bloques (*`16x16x256`*). Al ser este número mayor que la cantidad máxima de bloques que permite copiar el comando clone, necesitaremos emplear más comandos. Concretamente **`16`**, porque es el número que resulta de hallar el cociente de `524288` entre `32768` (*para otros valores inexactos se redondea a la alza*).
Comenzaremos indicando las coordenadas más pequeñas del volumen que vamos a clonar para así trabajar con números positivos. Suponiendo que el volumen que vamos a clonar se encuentra centrado en `[0,128,0]`, las coordenadas en las que empezaremos serán `[-32,0,-32]`.
> [LeMoesh - Minecraft Command Blocks and Google Spreadsheets](http://moesh.ca/minecraft-command-blocks-and-google-spreadsheets-your-first-steps-to-madness/)  