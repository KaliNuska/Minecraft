# Taller de Comandos:  
## Índice:  
  * [**Arreglo de Comandos**](#arreglo-de-comandos):  
    * [Comandos Spawners](#comandos-spawners):  
      * [Comando 1](#comando-1-thrownpotion)  
        [*Condensado*](#condensado)  
      * [Comando 2](#comando-2-golden-apple)  
        [*Condensado*](#condensado-1)  

### Arreglo de Comandos:  
#### Comandos Spawners:  
Adaptados para la versión 1.7.10 de Minecraft.  
Para aumentar la compatibilidad en todos los mundos y versiones de la 1.7, modifique las coordenadas y los nombres de las IDs si ve que le dan problemas.
Estos comandos han sido arreglados por KaliNuska, si tiene alguna duda acerca de ellos, por favor, contácteme: [www.twitter.com/Kali_Nuska](www.twitter.com/Kali_Nuska "Kali_Nuska")

##### COMANDO 1, ThrownPotion:  
```
/setblock -868 39 -733 minecraft:mob_spawner 0 keep 
	{
	MaxNearbyEntities:6s,
	RequiredPlayerRange:5s,
	SpawnCount:2s,
	SpawnData:{
		Motion:[
			0:0.0d,
			1:-0.7873698926771374d,
			2:0.0d
		],
		shake:0b,
		xTile:-1s,
		UUIDLeast:-5806148016565785011L,
		Potion:{
			id:373,
			Count:1b,
			Damage:16453s
		},
		inGround:0b,
		Invulnerable:0b,
		Air:300s,
		OnGround:0b,
		Dimension:0,
		PortalCooldown:0,
		Rotation:[
			0:-180.0d,
			1:-90.0d
		],
		EntityId:"ThrownPotion",
		FallDistance:0.0d,
		inTile:"",
		UUIDMost:-1179108807001161319L,
		ownerName:"killercreeper_55",
		zTile:-1s,
		Fire:0s,
		yTile:-1s
	},
	MaxSpawnDelay:60s,
	Delay:1s,
	EntityId:"ThrownPotion",
	id:"MobSpawner",
	SpawnRange:4s,
	MinSpawnDelay:60s,
	SpawnPotentials:[
		0:{
			Type:"ThrownPotion",
			Properties:{
				Motion:[
					0:0.0d,
					1:-0.7873698926771374d,
					2:0.0d
				],
				shake:0b,
				xTile:-1s,
				UUIDLeast:-5806148016565785011L,
				Potion:{
					id:373,
					Count:1b,
					Damage:16453s
				},
				inGround:0b,
				Invulnerable:0b,
				Air:300s,
				OnGround:0b,
				Dimension:0,
				PortalCooldown:0,
				Rotation:[
					0:-180.0d,
					1:-90.0d
				],
				EntityId:"ThrownPotion",
				FallDistance:0.0d,
				inTile:"",
				UUIDMost:-1179108807001161319L,
				ownerName:"killercreeper_55",
				zTile:-1s,
				Fire:0s,
				yTile:-1s
			},
			Weight:1
		}
	]
}
```

###### CONDENSADO:  
    /setblock -868 39 -733 minecraft:mob_spawner 0 keep {MaxNearbyEntities:6s,RequiredPlayerRange:5s,SpawnCount:2s,SpawnData:{Motion:[0:0.0d,1:-0.7873698926771374d,2:0.0d],shake:0b,xTile:-1s,UUIDLeast:-5806148016565785011L,Potion:{id:373,Count:1b,Damage:16453s},inGround:0b,Invulnerable:0b,Air:300s,OnGround:0b,Dimension:0,PortalCooldown:0,Rotation:[0:-180.0d,1:-90.0d],EntityId:"ThrownPotion",FallDistance:0.0d,inTile:"",UUIDMost:-1179108807001161319L,ownerName:"killercreeper_55",zTile:-1s,Fire:0s,yTile:-1s},MaxSpawnDelay:60s,Delay:1s,EntityId:"ThrownPotion",id:"MobSpawner",SpawnRange:4s,MinSpawnDelay:60s,SpawnPotentials:[0:{Type:"ThrownPotion",Properties:{Motion:[0:0.0d,1:-0.7873698926771374d,2:0.0d],shake:0b,xTile:-1s,UUIDLeast:-5806148016565785011L,Potion:{id:373,Count:1b,Damage:16453s},inGround:0b,Invulnerable:0b,Air:300s,OnGround:0b,Dimension:0,PortalCooldown:0,Rotation:[0:-180.0d,1:-90.0d],EntityId:"ThrownPotion",FallDistance:0.0d,inTile:"",UUIDMost:-1179108807001161319L,ownerName:"killercreeper_55",zTile:-1s,Fire:0s,yTile:-1s},Weight:1}]}
***
##### COMANDO 2, Golden Apple:  
```
/setblock ~ ~2 ~ minecraft:mob_spawner 0 keep 
	{
	MaxNearbyEntities:6s,
	RequiredPlayerRange:4s,
	SpawnCount:2s,
	SpawnData:{
		FallDistance:0.0d,
		Item:{
			Count:1b,
			id:322,
			Damage:0s
			},
		Health:5s,
		Fire:1000s,
		Invulnerable:0b,
		Air:300s,
		Dimension:0,
		id:"Item",
		Age:16s
	},
	MaxSpawnDelay:120s,
	Delay:66s,
	EntityId:"Item",
	id:"MobSpawner",
	SpawnRange:4s,
	MinSpawnDelay:100s,
	SpawnPotentials:[
		0:{
			Type:"Item",
			Properties:{
				FallDistance:0.0d,
				Item:{
					Count:1b,
					id:322,
					Damage:0s
				},
				Health:5s,
				Fire:1000s,
				Invulnerable:0b,
				Air:300s,
				Dimension:0,
				id:"Item",
				Age:16s
			},
			Weight:1
		}
	]
}
```

###### CONDENSADO:  
    /setblock ~ ~2 ~ minecraft:mob_spawner 0 keep {MaxNearbyEntities:6s,RequiredPlayerRange:4s,SpawnCount:2s,SpawnData:{FallDistance:0.0d,Item:{Count:1b,id:322,Damage:0s},Health:5s,Fire:1000s,Invulnerable:0b,Air:300s,Dimension:0,id:"Item",Age:16s},MaxSpawnDelay:120s,Delay:66s,EntityId:"Item",id:"MobSpawner",SpawnRange:4s,MinSpawnDelay:100s,SpawnPotentials:[0:{Type:"Item",Properties:{FallDistance:0.0d,Item:{Count:1b,id:322,Damage:0s},Health:5s,Fire:1000s,Invulnerable:0b,Air:300s,Dimension:0,id:"Item",Age:16s},Weight:1}]}
