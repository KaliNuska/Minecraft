## Mapas:
**En este directorio se encuentran las copias de seguridad de los mapas en los cuales trabajo.**  
Son los siguientes:  
### 1.8:
  * [*Redstone Tests*](BAK%20-%20Redstone%20Tests%20-%201.8%20%5B11-04-16%5D.zip?raw=true)  

### 1.9:
  * *Survival 1.9*:  
   * [1](BAK%20-%20Survival%20-%201.9%20%5B11-04-16%5D%20(1).rar?raw=true)  
   * [2](BAK%20-%20Survival%20-%201.9%20%5B11-04-16%5D%20(2).rar?raw=true)  
   * [3](BAK%20-%20Survival%20-%201.9%20%5B11-04-16%5D%20(3).rar?raw=true)  
  * [*ExpBottle*](ExpBottle.zip?raw=true)  
    ![](http://i.imgur.com/kxb4Jplt.png)  
  * [*Gamemode Detector 1.9*](Gamemode%20Detector%20%5B1.9%5D.schematic?raw=true)  
  * [*Right Click Detection 1.9*](Right%20Click%20Detection%20%5B1.9%5D.schematic?raw=true)  
    ![](http://i.imgur.com/A4Yofr9t.png)  
  * [*Timer de 6 minutos*](Timer%20de%206%20min.schematic?raw=true)  
  * [*Stats AffectedBlocks*](%5BComandos%5D%20Stats%20AffectedBlocks%20%5B+1.9%5D.schematic?raw=true)  

### 1.10:
 * [*Mecánica de escalera horizontal*](%5BComandos%5D%20Mec%C3%A1nica%20de%20escalera%20horizontal.schematic?raw=true)  
 Comandos:  

 > `/scoreboard players set @a item 0`  
 > `/scoreboard players set @a item 1 {SelectedItem:{id:"minecraft:shears",Count:1b}}`  
 > `/execute @a ~ ~ ~ detect ~ ~1.9 ~ minecraft:iron_bars -1 /scoreboard players add @a[score_colgar_min=0,score_colgar=1] colgar 1`  
 > `/execute @a[score_colgar_min=1] ~ ~ ~ /playsound minecraft:entity.bat.takeoff ambient @a[score_colgar_min=1,score_colgar=1] ~ ~ ~ 1 2 1`  
 > `/scoreboard players remove @a[score_colgar_min=2] colgar 1`  
 > `/execute @a ~ ~ ~ detect ~ ~1.9 ~ minecraft:iron_bars -1 /scoreboard players add @a[score_colgar_min=1,score_colgar=1] colgar 1`  
 > `/execute @a ~ ~ ~ detect ~ ~2.799 ~ air -1 /scoreboard players set @a colgar 0`  
 > `/effect @a[score_colgar=1,score_colgar_min=0] minecraft:levitation 0`  
 > `/effect @a[score_colgar_min=2] minecraft:levitation 1 0 true`  
 > `/effect @a[score_item=0] minecraft:levitation 0`  
 > `/effect @a[score_shift_min=1] minecraft:levitation 0`  
 > `/execute @a[score_shift_min=1] ~ ~ ~ /tp @a[score_colgar_min=2,score_colgar=2,c=1,r=0] ~ ~-.5 ~`  
 > `/execute @a[score_shift_min=1] ~ ~ ~ /playsound minecraft:entity.bat.takeoff ambient @a[score_colgar_min=2,score_colgar=2,c=1,r=1] ~ ~ ~ 1 2 1`  
 > `/scoreboard players set @a[score_shift_min=1] colgar 0`  
 > `/scoreboard players set @a shift 0`  

 * [*Ban gamemode 1.10*](%5BCMD%5D%20Ban%20gamemode%20%5B1.10%5D.schematic?raw=true)  
  [![](http://i.imgur.com/tYIXUwst.png)](http://i.imgur.com/tYIXUws.png)
 Comandos:  
 
 > `/scoreboard objectives add c dummy Jugadores en c`  
 > `/scoreboard players set @a[name=##] c 100`  
 > `/scoreboard players add @a c 0`  
 > `/scoreboard players set @a[m=1,score_c=0,score_c_min=0] c 1`  
 > `/tellraw @a[score_c_min=1,score_c=1] {"text":"X","bold":true,"color":"red"}`  
 > `/gamemode survival @a[score_c_min=1,score_c=1]`  
 > `/scoreboard players set @a[score_c_min=1,score_c=1] c 0`  

### 1.11:
 * [*Ban gamemode*](%5BCMD%5D%20Ban%20gamemode%20%5B1.11%5D.schematic?raw=true)  
  [![](http://i.imgur.com/tYIXUwst.png)](http://i.imgur.com/tYIXUws.png)
 Comandos:  
 
 > `/scoreboard objectives add c dummy Jugadores en c`  
 > `/scoreboard players set @a[name=##] c 100`  
 > `/scoreboard players add @a c 0`  
 > `/scoreboard players set @a[m=1,score_c=0,score_c_min=0] c 1`  
 > `/tellraw @a[score_c_min=1,score_c=1] {"text":"X","bold":true,"color":"red"}`  
 > `/gamemode survival @a[score_c_min=1,score_c=1]`  
 > `/scoreboard players set @a[score_c_min=1,score_c=1] c 0`  
