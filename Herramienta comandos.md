## Herramientas para crear comandos:  
### Coloración de la sintaxis:  
Cosiste en colorear el texto según los parámetros que pongo a continuación:  
#### Argumentos:  
En los argumentos, cada palabra delante y detrás de un signo `=` será coloreada, preferentemente de azul.  
#### NBT Tags:  
Aplicar un color a cada NBT Tag en el comando. Para esto hará falta una lista completa de todas las que haya disponibles y se colorearán todas las que coincidan con alguna. *Habrá que tener en cuenta las mayúsculas y que coincida la palabra entera, no trozos de ella*.  
#### Niveles de paréntesis:  
Tanto las llaves como los corchetes serán coloreados con el fin de indicar la profundidad que tienen.  
Los **corchetes** que coincidan en un nivel se colorearán de azul y se oscurecerá conforme aumente su nivel. Si se alcanza el color más oscuro, se emipeza desde el claro de nuevo.  
Las **laves**, de apertura y cierre, se colorearán con distintas tonalidades de rojo. Partiendo del rojo, se irá cambiando y oscureciendo, con el fin de que no puedan ser confundidas con los corchetes. Al igual que con estos otros, se comenzará de nuevo a aplicar el color cuando haya alcanzado el último.  
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
**Si, en vez de llaves o corchetes no cerramos unas comillas:**  
/give @p minecraft:diamond_sword 1 0 {display:{Name:**"**Daga},Unbreakable:1b,ench:[{id:19s,lvl:1s},{id:16s,lvl:3s}]}  

### Autoindicar los tipos de tag:  
### Formatear y condensar el comando:  
