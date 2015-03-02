## Formato NBT en Minecraft:
El formato **NBT** es utilizado en Minecraft para almacenar datos en forma de árbol compuesto por tags. Todas las tags tienen una ID y un nombre propios. La versión original que podemos encontrar en [*Minecraft Beta 1.3*](http://minecraft.gamepedia.com/Version_history/Beta#Beta_1.3) hace uso de la versión `19132` y se actualizó a la `19133` cuando se cambió a [*Anvil*](http://minecraft.gamepedia.com/Anvil_file_format), con la adición de la *TAG_****Int_Array***.  
### Definición de tag:  
Una tag es una parte individual del árbol de datos. El primer byte en una tag determina su ID, le siguen dos bytes para la longitud del nombre de la tag y, por último, el nombre como cadena de caracteres en formato UTF-8.  
*(Nota: TAG_End no está nombrada y no contiene los 2 bytes correspondientes)*  
Los nombres de las tags pueden contener espacios, aunque en Minecraft nunca los almacena con espacios dentro del nombre. Finalmente, dependiendo del tipo de tag, los bytes que siguen son los datos almacenables.  
La siguiente tabla describe cad una de las 12 tags conocidas en la versión `19133` del formato NBT:  

ID | Icono | Tipo de tag | Payload | Descripción | Capacidad de almacenamiento
--- | --- | --- | --- | --- | ---
0 | ![TAG_End](http://i.imgur.com/GbbSJOl.png "TAG_End") | TAG_**End** | Nada. | Used to mark the end of compound tags. This tag does not have a name, so it is only ever a single byte 0. It may also be the type of empty List tags. | Sin capacidad para almacenar datos.
1 | ![TAG_Byte](http://i.imgur.com/DLpKqKK.png "TAG_Byte") | TAG_**Byte** | 1 byte / 8 bits, signed | A signed integral type. Sometimes used for booleans. | Rango comprendido entre `-(2^7)` y `2^7 - 1`: Desde `-128` hasta `127`.
2 | ![TAG_Short](http://i.imgur.com/mOTYBeM.png "TAG_Short") | TAG_**Short** |  2 bytes / 16 bits, signed, big endian | A signed integral type. | Rango comprendido entre `-(2^15)` y `2^15 - 1`: Desde `-32.768` hasta `32.767`
3 | ![TAG_Int](http://i.imgur.com/S24DzxI.png "TAG_Int") | TAG_**Int** |  4 bytes / 32 bits, signed, big endian | A signed integral type. | Rango comprendido entre `-(2^31)` y `2^31 - 1`: Desde `-2.147.483.648` hasta `2.147.483.647`
4 | ![TAG_Long](http://i.imgur.com/DUiiE1O.png "TAG_Long") | TAG_**Long** |  8 bytes / 64 bits, signed, big endian | A signed integral type. | Rango comprendido entre `-(2^63)` y `2^63 - 1`: Desde `-9.223.372.036.854.775.808` hasta `9.223.372.036.854.775.807`.
5 | ![TAG_Float](http://i.imgur.com/SzJFi47.png "TAG_Float") | TAG_**Float** | 4 bytes / 32 bits, signed, big endian, IEEE 754-2008, binary32 | A signed floating point type. | Precision varies throughout number line; See Single-precision floating-point format.
6 | ![TAG_Double](http://i.imgur.com/RHW9hx9.png "TAG_Double") | TAG_**Double** | 8 bytes / 64 bits, signed, big endian, IEEE 754-2008, binary64 | A signed floating point type. | Precision varies throughout number line; See Single-precision floating-point format.
7 | ![TAG_Byte_Array](http://i.imgur.com/tOTGqjP.png "TAG_Byte_Array") | TAG_**Byte_Array** | TAG_Int's payload size, then size TAG_Byte's payloads. | An array of bytes. | Maximum number of elements ranges between `2^31 - 9` y `2^31 - 1`: `2.147.483.639` y `2.147.483.647`, depending on the specific JVM.
8 | ![TAG_String](http://i.imgur.com/c2NRyWV.png "TAG_String") | TAG_**String** | TAG_Short's payload length, then a UTF-8 string with size length. | A UTF-8 string. It has a size, rather than being null terminated. | `32.767` UTF-8 Code Points (see UTF-8 format; most commonly-used characters are a single code point).
9 | ![TAG_List](http://i.imgur.com/S7q49GR.png "TAG_List") | TAG_**List** | TAG_Byte's payload tagId, then TAG_Int's payload size, then size tags' payloads, all of type tagId. | A list of tag payloads, without repeated tag IDs or any tag names. | Due to JVM limitations and the implementation of ArrayList, the maximum number of list elements is `2^31 - 9` o `2.147.483.639`. Also note that List and Compound tags may not be nested beyond a depth of `512`.
10 | ![TAG_Compound](http://i.imgur.com/bRuYarV.png "TAG_Compound") | TAG_**Compound** | Fully formed tags, followed by a TAG_End. | A list of fully formed tags, including their IDs, names, and payloads. No two tags may have the same name. | Unlike lists, there is no hard limit to the amount of tags within a Compound (of course, there is always the implicit limit of virtual memory). Note, however, that Compound and List tags may not be nested beyond a depth of `512`.
11 | ![TAG_Int_Array](http://i.imgur.com/9K6IiQm.png "TAG_Int_Array") | TAG_**Int_Array** | TAG_Int's payload size, then size TAG_Int's payloads | An array of TAG_Int's payloads. | Maximum number of elements ranges between `2^31 - 9` and `2^31 - 1`: `2.147.483.639` and `2.147.483.647`, depending on the specific JVM.