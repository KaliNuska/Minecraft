## Herramientas para crear comandos:  
### Coloración de la sintaxis:  
Cosiste en colorear el texto según los parámetros que pongo a continuación:  
#### Argumentos:  
En los argumentos, cada palabra delante y detrás de un signo `=` será coloreada, preferentemente de azul.  
![](http://i.imgur.com/PaQ3aWy.png "Ejemplo")  
#### NBT Tags:  
Aplicar un color a cada NBT Tag en el comando. Para esto hará falta una lista completa de todas las que haya disponibles y se colorearán todas las que coincidan con alguna. *Habrá que tener en cuenta las mayúsculas y que coincida la palabra entera, no trozos de ella*. Si la NBT Tag escrita fuese incorrecta o no se detectara, no se aplicaría color alguno.  
![](http://i.imgur.com/UFV7324.png "Ejemplo")  
#### Niveles de paréntesis:  
Tanto las llaves como los corchetes serán coloreados con el fin de indicar la profundidad que tienen.  
Los **corchetes** que coincidan en un nivel se colorearán de azul y se oscurecerá conforme aumente su nivel. Si se alcanza el color más oscuro, se emipeza desde el claro de nuevo.  
Las **laves**, de apertura y cierre, se colorearán con distintas tonalidades de rojo. Partiendo del rojo, se irá cambiando y oscureciendo, con el fin de que no puedan ser confundidas con los corchetes. Al igual que con estos otros, se comenzará de nuevo a aplicar el color cuando haya alcanzado el último.  
![](http://i.imgur.com/WkfMZ9o.png "Ejemplo")  
#### Entrecomillado y demás tipos de tag:  
Todos los caracteres que se encuentren entre comillas tendrán un fondo de color amarillo y sus tonalidades. Si hubiese varias comillas dentro de otras, se cambiará el color, por ejemplo: `Command:"/give @p minecraft:stone 1 0 {display:{Name:"Pedrusco"}}`. Lo mismo debe suceder con el resto de tags; cuando se especifica correctamente si es *short*, se colorea en verde. Si es incorrecto, algo que trataré más adelante, se colorea en rojo.  
### Autosugerir campos:  
Partiendo de una lista de posibilidades, cuando se introduzca, por ejemplo, la NBT Tag `CustomName`, te sugerirá la otra que suale acompañarla: `CustomNameVisible`. Algo similar pasaría con las IDs, que después de poner `id:`, te sugerirá `minecraft:`.  
### Resaltar paréntesis y comillas sin abrir o cerrar:  
Cuando haya más llaves o corchetes abiertos que cerrados, los primeros se resaltarán en rojo, al igual que con las tags incorrectamante introducidas. Si ocurre que hay más cerrados que los que abren, serán los últimos los que se resaltarán. Lo ideal sería, también, que se analizaran distintamente unos de otros, es decir, que las llaves se resalten dependiendo de si están dentro de un corchete. Pondré un ejemplo:  
> **Este comando está correctamente escrito:**  
/give @p minecraft:diamond_sword 1 0 {display:{Name:"Daga"},Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]}  
**Ahora, a este le falta una de la llaves. Concretamente la final:**  
/give @p minecraft:diamond_sword 1 0 **{**display:{Name:"Daga"},Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]  
**A este le falta una por cerrar después de `Name`:**  
/give @p minecraft:diamond_sword 1 0 **{**display:{Name:"Daga",Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]}  
**A este, le falta `display` y una llave:**  
/give @p minecraft:diamond_sword 1 0 {Name:"Daga"},Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]**}**  
**Las llaves de este están bien, pero le falta cerrar un corchete:**  
/give @p minecraft:diamond_sword 1 0 {display:{Name:"Daga"},Unbreakable:1b,ench:**[**{id:19s,lvl:1s},{id:16s,lvl:3s}}  
**Si, en vez de llaves o corchetes no cerramos unas comillas tendrá que resaltarse o avisar al menos:**  
/give @p minecraft:diamond_sword 1 0 {display:{Name:**"**Daga},Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]}  

### Autoindicar los tipos de tag:  
Partiendo nuevamente de una pequeña base de datos con todas las tags, cuando una de ellas se escriba, tendrá que subrayarse con el color que le corresponde al tipo de tag que tiene. En las página habrá una leyenda desplegable que comprenda los rangos de valores para cada una.  
Por ejemplo, al escribir una TAG_Byte, la NBT Tag quedaría subrayada en rojo; una Tag_Double en violeta, y así con el resto. Para las tags Compound, List y Array, no será necesario, ya que se determinan de otra forma.  
### Formatear y condensar el comando:  
Para finalizar, una herramienta que te permita importar comandos y visualizarlos de forma ordenada para luego exportarlos condensados sería lo ideal.  
> Partiendo de esto:  
![Condensado](http://i.imgur.com/vRJ1Fqk.png "Comando condensado")  
Te mostraría esto para editar:  
![Ampliado](http://i.imgur.com/6WYTh49.png "Comando Ampliado")  
En otro cuadro de texto sacaría el comando nuevamente condensado:  
![Condensado](http://i.imgur.com/vRJ1Fqk.png "Comando condensado")  

### Resultados:  
Con todo esto completo, o con lo que sea posible, los comandos deberían quedar similares a esto:  
#### Comando 1:  
![Comando1](http://i.imgur.com/XHYkZCo.png "Comando 1, sin errores")  
##### Comando 2:  
![Comando2](http://i.imgur.com/jm9ENAp.png "Comando 2, falta llave final")  
#### Comando 3:
![Comando3](http://i.imgur.com/X7nwX1P.png "Comando 3, falta llave después de Name")  
#### Comando 4:  
![Comando4](http://i.imgur.com/pcSvQ3A.png "Comando 4, falta llave antes del nombre y un nivel")  
#### Comando 5:  
![Comando5](http://i.imgur.com/mAXgBXK.png "Comando 5, falta cerrar comillas")  
