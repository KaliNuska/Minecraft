The Named Binary Tag format is used by Minecraft for the various files in which it saves data. The format is described by Notch in a very brief specification. The format is designed to store data in a tree structure made up of various tags. All tags have an ID and a name. The original known version was 19132 as introduced in Minecraft Beta 1.3, and since then has been updated to 19133 with Anvil, with the addition of the Int Array tag. The NBT format dates all the way back to Minecraft Indev with tags 0 to 10 in use.

ID | Icono | Tipo de tag | Payload | Descripción | Capacidad de almacenamiento
--- | --- | --- | --- | --- | ---
0 | ![TAG_End](http://i.imgur.com/GbbSJOl.png "TAG_End") | TAG_**End** | Nada. | Used to mark the end of compound tags. This tag does not have a name, so it is only ever a single byte 0. It may also be the type of empty List tags. | N/A
1 | ![TAG_Byte](http://i.imgur.com/GbbSJOl.png "TAG_Byte") | TAG_**Byte** |  |  | 
2 | ![TAG_Short](http://i.imgur.com/GbbSJOl.png "TAG_Short") | TAG_**Short** |  |  | 
3 | ![TAG_Int](http://i.imgur.com/GbbSJOl.png "TAG_Int") | TAG_**Int** |  |  | 
4 | ![TAG_Long](http://i.imgur.com/GbbSJOl.png "TAG_Long") | TAG_**Long** |  |  | 
5 | ![TAG_Float](http://i.imgur.com/GbbSJOl.png "TAG_Float") | TAG_**Float** |  |  | 
6 | ![TAG_Double](http://i.imgur.com/GbbSJOl.png "TAG_Double") | TAG_**Double** |  |  | 
7 | ![TAG_Byte_Array](http://i.imgur.com/GbbSJOl.png "TAG_Byte_Array") | TAG_**Byte_Array** |  |  | 
8 | ![TAG_String](http://i.imgur.com/GbbSJOl.png "TAG_String") | TAG_**String** |  |  | 
9 | ![TAG_List](http://i.imgur.com/GbbSJOl.png "TAG_List") | TAG_**List** |  |  | 
10 | ![TAG_Compound](http://i.imgur.com/GbbSJOl.png "TAG_Compound") | TAG_**Compound** |  |  | 
11 | ![TAG_Int_Array](http://i.imgur.com/GbbSJOl.png "TAG_Int_Array") | TAG_**Int_Array** |  |  | 
