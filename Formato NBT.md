The Named Binary Tag format is used by Minecraft for the various files in which it saves data. The format is described by Notch in a very brief specification. The format is designed to store data in a tree structure made up of various tags. All tags have an ID and a name. The original known version was 19132 as introduced in Minecraft Beta 1.3, and since then has been updated to 19133 with Anvil, with the addition of the Int Array tag. The NBT format dates all the way back to Minecraft Indev with tags 0 to 10 in use.

ID | Icono | Tipo de tag | Payload | Descripción | Capacidad de almacenamiento |
-- | ----- | ----------- | ------- | ----------- | --------------------------- |
Content from cell 1 | Content from cell 2 | A | A | A | A |
Content in the first column | Content in the second column | A | A | A | A |


ID | Icono | Tipo de tag | Payload | Descripción | Capacidad de almacenamiento
--- | --- | --- | --- | --- | ---
0 | ![](http://i.imgur.com/GbbSJOl.png) | TAG_**End** | Nada. | Used to mark the end of compound tags. This tag does not have a name, so it is only ever a single byte 0. It may also be the type of empty List tags. | N/A
1 | ![](http://i.imgur.com/DLpKqKK.png) | TAG_**Byte** | 1 byte / 8 bits, signed | A signed integral type. Sometimes used for booleans. | Full range of -(27) to (27 - 1) (-128 to 127)
