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

Los comandos en Minecraft sirven para infinidad de cosas. Para hacer algunas de ellas, basta con escribir dos o tres comandos y conectarlos a un reloj, pero hay algunas que requieren de gran cantidad de comandos diferentes que, muchas veces, suelen seguir un patrón alfanumérico sencillo que los hace distintos. El hecho de que todos los comandos sean diferentes entre sí, por muy pocas variaciones que existan, hace que haya que escribirlos todos individualmente. En estas ocasiones emplear una hoja de cálculo o alguna aplicación similar, servirá para no tener que ir creando uno por uno modificando tan solo un par de caracteres con respecto al anterior, sino para poder crearlos todos de golpe y sin tener que dedicar horas a escribirlos.

Todo programa que realice operaciones matemáticas y permita modificar cadenas de caracteres servirá para automatizar la escritura de muchos comandos que, de no emplear estos programas para hacerlos, se convertirían en una tarea eterna. Los más populares y accesibles son las hojas de cálculo, como las de [*Excel*](https://products.office.com/es-es/excel) o [*Google Spreadsheets*](https://www.google.es/intl/es/sheets/about/), por lo que son las que voy a tratar en el desarrollo de este post.


Por el momento muchos de vosotros no habréis llegado a entender cómo **una hoja de cálculo puede facilitar enormemente la escritura de grupos de muchos comandos**. La respuesta es sencilla: todo se basa en la función de **`concatenar`**. Pondré un detallado ejemplo con el comando `/clone`, que facilitará la comprensión de lo que pretendo transmitir en este post:

El comando clone sirve para copiar un volumen ortoédrico<sup>[1](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/Ortoedro.png/320px-Ortoedro.png)</sup> con un tamaño máximo de **`32768`**<sup>`2^15`</sup> bloques (según está establecido desde la versión [14w26a](http://minecraft.gamepedia.com/14w26a#Changes) hasta la fecha actual [16w35a](http://minecraft.gamepedia.com/16w02a)). Si pretendemos clonar volúmenes superiores al tamaño máximo que permite el comando, necesitaremos emplear varios al mismo tiempo. Imaginemos que queremos clonar un volumen de `16`<sup>`2^4`</sup> chunks para resetear el mapa hardcore que acabamos de crear sin tener que copiarlo nuevamente al directorio de mapas. `16`<sup>`2^4`</sup> chunks son un total de **`1048576`**<sup>`2^20`</sup> bloques, ya que un chunk tiene `65536`<sup>`2^16`</sup> bloques (*`16x256x16`<sup>`2^(4+8+4)`</sup>*). Al ser este número mayor que la cantidad máxima de bloques que permite copiar el comando clone, necesitaremos emplear más comandos clone. Concretamente **`32`**<sup>`2^5`</sup> comandos, porque es el número que resulta de hallar el cociente de `1048576`<sup>`2^20`</sup> entre `32768`<sup>`2^15`</sup> (*para otros valores que no resulten en números enteros, se redondea a la alza*).

Comenzaremos indicando las coordenadas más pequeñas del volumen que vamos a clonar para así trabajar con números positivos. Suponiendo que el volumen que vamos a clonar se encuentra centrado en `[0,0]`, las coordenadas en las que empezaremos serán `[-32,0,-32]` y como abarcará `16` chunks, las cooredenadas finales serán `[31,255,31]`. Para empezar con la hoja de cálculo habrá que analizar cuántos conjuntos de datos son necesarios para componer el comando completo, en el caso de `/clone` son los siguientes:

    /clone <x1> <y1> <z1> <x2> <y2> <z2> <x> <y> <z>

Los tres primeros conjuntos de datos (*`<x1>`, `<y1>` y `<z1>`*) corresponden a la esquina inferior noroeste de nuestro volumen de `16` chunks. Los tres siguientes (*`<x2>`, `<y2>` y `<z2>`*), a la esquina superior sureste.

Los tres últimos (*`<x>`, `<y>` y `<z>`*) ubican la esquina inferior noroeste del lugar donde queramos clonar nuestro volumen.

Iremos ahora a una nueva hoja de cálculo de [*Excel*](https://products.office.com/es-es/excel) o [*Google Spreadsheets*](https://www.google.es/intl/es/sheets/about/) y distribuiremos cada uno de los conjuntos de datos del comando en columnas añadiendo otras dos para ordenarlos y para los comandos resultantes:

| ÍNDICE | X1 | Y1 | Z1 | X2 | Y2 | Z2 | X | Y | Z | OUTPUT |

|:---|:---|:---|:---|:---|:---|:---|:--|:--|:--|-------:|

Como ya sabemos que el número total de comandos que nos van a hacer falta es de `32`, reservaremos ese número de filas para ir comenzando a calcular los datos.
Para seguir cierto orden, conviene empezar por calcular las componentes de las coordenadas por separado. En nuestro caso, al tratarse de un volumen compuesto por chunks completos, lo más sencillo es comenzar trabajando con las componentes `<y>`. Como un solo comando `/clone` no abarca un chunk entero, sino la mitad, necesitaremos que el volumen clonable por cada comando corresponda a la mitad de un chunk, es decir, de `16x128x16` bloques. Para introducir este valor en nuestra hoja de cálculo y hacer otras operaciones en base a él, emplearemos las funciones `RESTO` o *`MOD`* y `COCIENTE` o *`QUOTIENT`*, que se usan de la siguiente manera:

 - `RESTO` o *`MOD`*, devuelve el resto o residuo de una división, es decir, la cantidad que se le ha de restar al dividendo para que sea un múltiplo del divisor. Cuando dividimos números sucesivos por otro constante, el resto sigue el siguiente patrón:
```
| RESTO(0;8) = 0 | RESTO(8;8) = 0  | RESTO(16;8) = 0 | RESTO(24;8) = 0 |
| RESTO(1;8) = 1 | RESTO(9;8) = 1  | RESTO(17;8) = 1 | RESTO(25;8) = 1 |
| RESTO(2;8) = 2 | RESTO(10;8) = 2 | RESTO(18;8) = 2 | RESTO(26;8) = 2 |
| RESTO(3;8) = 3 | RESTO(11;8) = 3 | RESTO(19;8) = 3 | RESTO(27;8) = 3 |
| RESTO(4;8) = 4 | RESTO(12;8) = 4 | RESTO(20;8) = 4 | RESTO(28;8) = 4 |
| RESTO(5;8) = 5 | RESTO(13;8) = 5 | RESTO(21;8) = 5 | RESTO(29;8) = 5 |
| RESTO(6;8) = 6 | RESTO(14;8) = 6 | RESTO(22;8) = 6 | RESTO(30;8) = 6 |
| RESTO(7;8) = 7 | RESTO(15;8) = 7 | RESTO(23;8) = 7 | RESTO(31;8) = 7 |
```
 - `COCIENTE` o *`QUOTIENT`*, devuelve la parte entera del cociente en una división. Nuevamente, al dividir números sucesivos por otro constante se obtiene un patrón:
```
| COCIENTE(0;8) = 0 | COCIENTE(8;8) = 1  | COCIENTE(16;8) = 2 | COCIENTE(24;8) = 3 |
| COCIENTE(1;8) = 0 | COCIENTE(9;8) = 1  | COCIENTE(17;8) = 2 | COCIENTE(25;8) = 3 |
| COCIENTE(2;8) = 0 | COCIENTE(10;8) = 1 | COCIENTE(18;8) = 2 | COCIENTE(26;8) = 3 |
| COCIENTE(3;8) = 0 | COCIENTE(11;8) = 1 | COCIENTE(19;8) = 2 | COCIENTE(27;8) = 3 |
| COCIENTE(4;8) = 0 | COCIENTE(12;8) = 1 | COCIENTE(20;8) = 2 | COCIENTE(28;8) = 3 |
| COCIENTE(5;8) = 0 | COCIENTE(13;8) = 1 | COCIENTE(21;8) = 2 | COCIENTE(29;8) = 3 |
| COCIENTE(6;8) = 0 | COCIENTE(14;8) = 1 | COCIENTE(22;8) = 2 | COCIENTE(30;8) = 3 |
| COCIENTE(7;8) = 0 | COCIENTE(15;8) = 1 | COCIENTE(23;8) = 2 | COCIENTE(31;8) = 3 |
```


Como queremos dividir un chunk en dos operaciones de clone, nos hará falta que el uso de estas dos funciones resulten en ambas mitades: de `0 a 127` y de `128 a 255`. Igualmente, al tratarse de chunks completos usaremos los mismos datos que para `<y1>` en `<y>`. Resulta ahora evidente que `16` de nuestros 32 comandos se destinarán a clonar la mitad inferior del volumen de 16 chunks y los otros `16` comandos, a la superior. Empleando una de las dos funciones en nuestra hoja de cálculo podemos obtener el resultado esperado de la siguiente forma:
```
| 128*COCIENTE(ÍNDICE0;16)  = 0 | 128*COCIENTE(ÍNDICE16;16) = 128 |
| 128*COCIENTE(ÍNDICE1;16)  = 0 | 128*COCIENTE(ÍNDICE17;16) = 128 |
| 128*COCIENTE(ÍNDICE2;16)  = 0 | 128*COCIENTE(ÍNDICE18;16) = 128 |
| 128*COCIENTE(ÍNDICE3;16)  = 0 | 128*COCIENTE(ÍNDICE19;16) = 128 |
| 128*COCIENTE(ÍNDICE4;16)  = 0 | 128*COCIENTE(ÍNDICE20;16) = 128 |
| 128*COCIENTE(ÍNDICE5;16)  = 0 | 128*COCIENTE(ÍNDICE21;16) = 128 |
| 128*COCIENTE(ÍNDICE6;16)  = 0 | 128*COCIENTE(ÍNDICE22;16) = 128 |
| 128*COCIENTE(ÍNDICE7;16)  = 0 | 128*COCIENTE(ÍNDICE23;16) = 128 |
| 128*COCIENTE(ÍNDICE8;16)  = 0 | 128*COCIENTE(ÍNDICE24;16) = 128 |
| 128*COCIENTE(ÍNDICE9;16)  = 0 | 128*COCIENTE(ÍNDICE25;16) = 128 |
| 128*COCIENTE(ÍNDICE10;16) = 0 | 128*COCIENTE(ÍNDICE26;16) = 128 |
| 128*COCIENTE(ÍNDICE11;16) = 0 | 128*COCIENTE(ÍNDICE27;16) = 128 |
| 128*COCIENTE(ÍNDICE12;16) = 0 | 128*COCIENTE(ÍNDICE28;16) = 128 |
| 128*COCIENTE(ÍNDICE13;16) = 0 | 128*COCIENTE(ÍNDICE29;16) = 128 |
| 128*COCIENTE(ÍNDICE14;16) = 0 | 128*COCIENTE(ÍNDICE30;16) = 128 |
| 128*COCIENTE(ÍNDICE15;16) = 0 | 128*COCIENTE(ÍNDICE31;16) = 128 |
```

A partir de ahora, como las dos mitades de nuestro volumen son idénticas, repetiremos el mismo procedimiento en la de arriba y en la de abajo.
Al tratarse también de un volumen simétrico es indiferente hacer la `<x>` o la `<z>` a continuación, porque cualquiera de las dos se encargará de cambiar entre chunks dentro de una misma orientación, y la restante de cambiar de fila de chunks. *Ver la animación siguiente para comprender mejor esto último*:
![4X->1Z](http://i.giphy.com/l3vRhcbZy7MP6BXnG.gif)

Necesitamos que las coordenadas que estamos calculando desde la hoja de cálculo incluyan a todos los chunks, para lo que haremos que la `<z>` incremente de chunk cada vez que la `<x>` haya pasado por todos los que tiene alineados, es decir, que `<z>` mantendrá un mismo valor hasta que `<x>` haya cambiado 4 veces el suyo (porque son 4 chunks los que se encuentran alineados a un mismo valor de `<z>`). Para reflejar eso en nuestra hoja de cálculo habrá que utilizar lo siguiente:

`16*RESIDUO(ÍNDICE#;4)-32`, para que la `<x>` pase por todos los chunks de una fila y `16*RESIDUO(COCIENTE(ÍNDICE#;4);4)-32`, para que z haga cambiar la fila.
Combinando estas coordenadas con las que obtuvimos anteriormente con la `<y>`, logramos que todos los chunks estén cubiertos mediante clones distintos.
![X1Y1Z1](http://i.imgur.com/mcPdwel.png) ![X1Y1Z1](http://i.imgur.com/ICI2x7u.png)

Rellenar los campos que corresponden a `<x2>`, `<y2>`, y `<z2>`, es realmente sencillo porque es básicamente desplazar las coordenadas de `<X1>`, `<Y1>` y `<Z1>` hasta el otro extremo de cada chunk, lo que se resume en aumentar en `15` el valor de las coordenadas.
![X2Y2Z2](http://i.imgur.com/xCYDQ5o.png)

Lo mismo ocurre con `<X>`, `<Y>` y `<Z>` si nuestra intención es conservar íntegramente el volumen original (puesto que aquí es donde tenemos mayor versatilidad a la hora de clonar por partes si queremos rotar, espejar o modificar la figura completa de otra manera) porque bastará con sumarle a las coordenadas `<X1>`, `<Y1>` y `<Z1>` la distancia que las separa de la ubicación final del volumen completo. Si, por ejemplo, queremos que los 16 chunks queden centrados en `[100,100]` habrá que incrementar en `68` *`(100-32)`* las coordenadas iniciales.
![XYZ](http://i.imgur.com/UfJzLRM.png)

Llegados a este punto hemos hallado los valores de todas las coordenadas que nos hacen falta para clonar por 32 partes nuestro volumen de 16 chunks. Lo que nos falta es componer los comandos sin tener que escribirlos a mano o copiando y pegando las 32 veces. Para ello utilizaremos la función **`CONCATENAR`**:
```
CONCATENAR("/clone ";X1#;" ";Y1#;" ";Z1#;" ";X2#;" ";Y2#;" ";Z2#;" ";X#;" ";Y#;" ";Z#)
```
![OUTPUT](http://i.imgur.com/0P55zY8.png)

Ya hemos creado todos los comandos que nos hacen falta para realizar esta enorme operación de clonado y, por tanto, cumplido el objetivo que buscábamos al comienzo del post. Sin embargo, como añadido imprescindible, tenemos que ser capaces de colocar estos 32 comandos en nuestro mapa de una sola vez. Utilizaremos para este fin la herramienta externa de Minecraft por excelencia llamada *McEdit* con uno de los filtros creado por *texelelf*: *DumpCommandBlocks*. Nos servirá para, teniendo todos los datos necesarios de nuestros comandos en un formato de texto plano, introducirlos en nuestro mapa de Minecraft. Estos datos son, aparte del comando en sí, la ubicación y el modo de funcionamiento de los mismos. Se introducen siguiendo esta sintaxis: 


```
#<x>,<y>,<z>|<ID>|<DataVaule>|<auto 0/1>|0|<ConditionMet 0/1:<CustomName>
</comando>

```

Poniendo el ejemplo de los comandos obtenidos para clonar los 16 chunks:

```
#0,0,0|137|5|1|0|1:@
/clone -32 0 -32 -17 127 -17 68 0 68

#1,0,0|211|5|1|0|1:@
/clone -16 0 -32 -1 127 -17 84 0 68

#2,0,0|211|5|1|0|1:@
/clone 0 0 -32 15 127 -17 100 0 68

#3,0,0|211|5|1|0|1:@
/clone 16 0 -32 31 127 -17 116 0 68

#4,0,0|211|5|1|0|1:@
/clone -32 0 -16 -17 127 -1 68 0 84

#5,0,0|211|5|1|0|1:@
/clone -16 0 -16 -1 127 -1 84 0 84

#6,0,0|211|5|1|0|1:@
/clone 0 0 -16 15 127 -1 100 0 84

#7,0,0|211|5|1|0|1:@
/clone 16 0 -16 31 127 -1 116 0 84

#8,0,0|211|5|1|0|1:@
/clone -32 0 0 -17 127 15 68 0 100

#9,0,0|211|5|1|0|1:@
/clone -16 0 0 -1 127 15 84 0 100

#10,0,0|211|5|1|0|1:@
/clone 0 0 0 15 127 15 100 0 100

#11,0,0|211|5|1|0|1:@
/clone 16 0 0 31 127 15 116 0 100

#12,0,0|211|5|1|0|1:@
/clone -32 0 16 -17 127 31 68 0 116

#13,0,0|211|5|1|0|1:@
/clone -16 0 16 -1 127 31 84 0 116

#14,0,0|211|5|1|0|1:@
/clone 0 0 16 15 127 31 100 0 116

#15,0,0|211|5|1|0|1:@
/clone 16 0 16 31 127 31 116 0 116

#16,0,0|211|5|1|0|1:@
/clone -32 128 -32 -17 255 -17 68 128 68

#17,0,0|211|5|1|0|1:@
/clone -16 128 -32 -1 255 -17 84 128 68

#18,0,0|211|5|1|0|1:@
/clone 0 128 -32 15 255 -17 100 128 68

#19,0,0|211|5|1|0|1:@
/clone 16 128 -32 31 255 -17 116 128 68

#20,0,0|211|5|1|0|1:@
/clone -32 128 -16 -17 255 -1 68 128 84

#21,0,0|211|5|1|0|1:@
/clone -16 128 -16 -1 255 -1 84 128 84

#22,0,0|211|5|1|0|1:@
/clone 0 128 -16 15 255 -1 100 128 84

#23,0,0|211|5|1|0|1:@
/clone 16 128 -16 31 255 -1 116 128 84

#24,0,0|211|5|1|0|1:@
/clone -32 128 0 -17 255 15 68 128 100

#25,0,0|211|5|1|0|1:@
/clone -16 128 0 -1 255 15 84 128 100

#26,0,0|211|5|1|0|1:@
/clone 0 128 0 15 255 15 100 128 100

#27,0,0|211|5|1|0|1:@
/clone 16 128 0 31 255 15 116 128 100

#28,0,0|211|5|1|0|1:@
/clone -32 128 16 -17 255 31 68 128 116

#29,0,0|211|5|1|0|1:@
/clone -16 128 16 -1 255 31 84 128 116

#30,0,0|211|5|1|0|1:@
/clone 0 128 16 15 255 31 100 128 116

#31,0,0|211|5|1|0|1:@
/clone 16 128 16 31 255 31 116 128 116

```

Solo falta abrir *McEdit* y ejecutar el filtro examinando el archivo de texto (creado y guardado) para tener todos los comandos dentro del mapa esperando para ser ejecutados.

Aquí se acerca el final del post, donde te resumo que utilizando el ejemplo del comando clone, muestro la increíble utilidad que ofrecen las hojas de cálculo en el universo de los comandos y donde también te ruego que tengas solidaridad con el post respondiendo con tus dudas o preguntas, si las tienes, y/o con tu opinión. Para concluir pongo a tu disposición la [hoja de cálculo](https://github.com/KaliNuska/Minecraft/blob/master/Hojas%20de%20c%C3%A1lculo%20y%20comandos.xlsx?raw=true) que he creado para el post y el [mapa de los 16 chunks](https://github.com/KaliNuska/Minecraft/blob/master/Mapas/Hojas%20de%20c%C3%A1lculo%20y%20comandos.zip?raw=true) para que observes su funcionamiento, así como enlaces a la herramienta [McEdit](http://www.mcedit-unified.net/) y el filtro [DumpCommandBlocks](http://elemanser.com/DumpCommandBlocks.py).

Muchas gracias por llegar hasta el final del post y espero que pronto lleves a cabo tus proyectos con comandos ayudándote de la información que comparto en él.


> [LeMoesh - Minecraft Command Blocks and Google Spreadsheets](http://moesh.ca/minecraft-command-blocks-and-google-spreadsheets-your-first-steps-to-madness/)  
> [KaliNuska - Hojas de cálculo y comandos](https://github.com/KaliNuska/Minecraft/blob/master/Hojas%20de%20c%C3%A1lculo%20y%20comandos.xlsx?raw=true)


----------

### Guia sobre el Structure Block:

> [Team Woloo](https://youtu.be/543WnTIThGc)  
> [Xisumavoid]()
> [SimplySarc](https://youtu.be/JkQ5TDUnNOg)