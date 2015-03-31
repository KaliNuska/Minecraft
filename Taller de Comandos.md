# Taller de Comandos:  

## Índice:  
>	* [**Arreglo de comandos**](#arreglo-de-comandos):  
>		* [Comandos Spawners](#comandos-spawners):  
>			* [Comando 1](#comando-1-thrownpotion)  
>				[*Condensado*](#condensado)  
>			*	[Comando 2](#comando-2-golden-apple)  
>				[*Condensado*](#condensado-1)  
>	*	[**Recopilación de mecanismos en un comando**](#recopilación-de-mecanismos-en-un-comando)  
>		*	[Comando Elevador](#comando-elevador)  
>			[*Condensado*](#condensado-2)  

### Arreglo de comandos:  
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

### Recopilación de mecanismos en un comando:  
#### Comando elevador:  
```
/summon FallingSand ~ ~2 ~ 
{
	Block:redstone_block,
	Time:1,
	Riding:
	{
		id:FallingSand,
		Block:command_block,
		TileEntityData:
		{
			Command:/fill ~-1 ~-14 ~ ~-1 ~1 ~ redstone_block
		},
		Time:1,
		Riding:
		{
			id:FallingSand,
			Block:command_block,
			TileEntityData:
			{
				Command:/fill ~-1 ~-13 ~ ~ ~2 ~ air
			},
			Time:1,
			Riding:
			{
				id:FallingSand,
				Block:command_block,
				TileEntityData:
				{
					Command:/summon FallingSand ~-1 ~-4 ~15 
					{
						Block:iron_block,
						Time:1,
						Riding:
						{
							id:FallingSand,
							Block:command_block,
							TileEntityData:
							{
								Command:/summon FallingSand ~2 ~-7 ~-2 
								{
									Block:iron_block,
									Time:1,
									Riding:
									{
										id:FallingSand,
										Block:command_block,
										TileEntityData:
										{
											Command:/summon FallingSand ~ ~ ~-2 
											{
												Block:command_block,
												TileEntityData:
												{
													Command:/replaceitem entity @a
													[
														score_eeeeee=2
													] slot.hotbar.1 emerald_block 1 0 
													{
														display:
														{
															Name:"Driveable_Minecart_Boost"
														},
														HideFlags:127,
														ench:
														[
															{
																id:34,
																lvl:10
															}
														]
													}
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/replaceitem entity @a
														[
															score_eeeeee=2
														] slot.hotbar.3 spawn_egg 1 94 
														{
															display:
															{
																Name:"Moving_Platform"
															},
															HideFlags:127,
															ench:
															[
																{
																	id:34,
																	lvl:10
																}
															]
														}
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/replaceitem entity @a
															[
																score_eeeeee=2
															] slot.hotbar.5 coal_block 1 0 
															{
																display:
																{
																	Name:"Platform_Destroyer"
																},
																HideFlags:127,
																ench:
																[
																	{
																		id:34,
																		lvl:10
																	}
																]
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/replaceitem entity @a
																[
																	score_eeeeee=2
																] slot.hotbar.7 iron_block 1 0 
																{
																	display:
																	{
																		Name:"Elevator_Mover"
																	},
																	HideFlags:127,
																	ench:
																	[
																		{
																			id:34,
																			lvl:10
																		}
																	]
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/execute @a
																	[
																		score_ee_min=1
																	] ~ ~ ~ detect ~ ~2.5 ~ iron_block 0 /tp @p
																	[
																		r=1
																	] ~1 ~ ~
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @e
																		[
																			type=MinecartRideable,
																			name=eeeel,
																			score_ee_min=3,
																			score_ee=3
																		] ~ ~2 ~ /effect @a
																		[
																			r=1
																		] 11 1 150 true
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @e
																			[
																				type=MinecartRideable,
																				name=eeeel,
																				score_ee_min=3,
																				score_ee=3
																			] ~ ~ ~ /particle portal ~ ~ ~ 0.4 0.025 0.4 0.01 40 force
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/entitydata @e
																				[
																					type=MinecartRideable,
																					name=eeeel,
																					score_ee_min=3,
																					score_ee=3
																				] 
																				{
																					Motion:
																					[
																						0.0,
																						0.0,
																						0.0
																					]
																				}
																			},
																			Time:1
																		}
																	}
																}
															}
														}
													}
												}
											}
										},
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:command_block,
											TileEntityData:
											{
												Command:/summon FallingSand ~ ~ ~-3 
												{
													Block:command_block,
													TileEntityData:
													{
														Command:/replaceitem entity @a
														[
															score_eeeeee=2
														] slot.hotbar.0 spawn_egg 1 94 
														{
															display:
															{
																Name:"Driveable_Minecart"
															},
															HideFlags:127,
															ench:
															[
																{
																	id:34,
																	lvl:10
																}
															]
														}
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/replaceitem entity @a
															[
																score_eeeeee=2
															] slot.hotbar.2 redstone_block 1 0 
															{
																display:
																{
																	Name:"Destroys_Minecart_Driving_On_It"
																},
																HideFlags:127,
																ench:
																[
																	{
																		id:34,
																		lvl:10
																	}
																]
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/replaceitem entity @a
																[
																	score_eeeeee=2
																] slot.hotbar.4 stained_hardened_clay 1 14 
																{
																	display:
																	{
																		Name:"Platform_Mover"
																	},
																	HideFlags:127,
																	ench:
																	[
																		{
																			id:34,
																			lvl:10
																		}
																	]
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/replaceitem entity @a
																	[
																		score_eeeeee=2
																	] slot.hotbar.6 spawn_egg 1 94 
																	{
																		display:
																		{
																			Name:"Elevator"
																		},
																		HideFlags:127,
																		ench:
																		[
																			{
																				id:34,
																				lvl:10
																			}
																		]
																	}
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @e
																		[
																			type=MinecartRideable,
																			name=eeeel
																		] ~ ~ ~ detect ~ ~2 ~ iron_block 0 /scoreboard players set @e
																		[
																			type=MinecartRideable,
																			name=eeeel,
																			r=1,
																			c=1
																		] ee 2
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @a
																			[
																				score_ee_min=1
																			] ~ ~ ~ /execute @e
																			[
																				type=MinecartRideable,
																				name=eeeel,
																				r=1,
																				c=1
																			] ~ ~ ~ detect ~ ~-1 ~ iron_block 0 /scoreboard players set @e
																			[
																				type=MinecartRideable,
																				name=eeeel,
																				r=1,
																				c=1
																			] ee 1
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @e
																				[
																					type=MinecartRideable,
																					name=eeeel
																				] ~ ~ ~ detect ~ ~-1 ~ iron_block 0 /scoreboard players set @e
																				[
																					type=MinecartRideable,
																					name=eeeel,
																					r=1,
																					c=1
																				] ee 3
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/scoreboard players remove @a
																					[
																						score_ee_min=1
																					] ee 1
																				},
																				Time:1
																			}
																		}
																	}
																}
															}
														}
													}
												}
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/summon FallingSand ~ ~ ~-4 
													{
														Block:command_block,
														TileEntityData:
														{
															Command:/scoreboard players set @a ee 2 
															{
																Riding:
																{
																	id:MinecartRideable,
																	CustomName:"eeeel"
																}
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/execute @e
																[
																	type=MinecartRideable,
																	name=eeeel,
																	score_ee_min=1,
																	score_ee=1
																] ~ ~ ~ /particle portal ~ ~-0.35 ~ 0 0.15 0 0.1 30 force
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/entitydata @e
																	[
																		type=MinecartRideable,
																		name=eeeel,
																		score_ee_min=2,
																		score_ee=2
																	] 
																	{
																		Motion:
																		[
																			0.0,
																			-0.1,
																			0.0
																		]
																	}
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/entitydata @e
																		[
																			type=MinecartRideable,
																			name=eeeel,
																			score_ee_min=1,
																			score_ee=1
																		] 
																		{
																			Motion:
																			[
																				0.0,
																				0.1,
																				0.0
																			]
																		}
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/kill @e
																			[
																				type=Item,
																				score_e_min=1
																			]
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/scoreboard players set @e
																				[
																					type=Item
																				] e 1 
																				{
																					Item:
																					{
																						id:minecraft:dye,
																						Damage:0s
																					}
																				}
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=Squid,
																						name=Elevator,
																						score_e_min=1,
																						score_e=1
																					] ~ ~ ~ /summon MinecartRideable ~ ~ ~ 
																					{
																						CustomName:"eeeel",
																						Invulnerable:1
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/scoreboard players add @e
																						[
																							type=Squid,
																							name=Elevator
																						] e 1
																					},
																					Time:1
																				}
																			}
																		}
																	}
																}
															}
														}
													}
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/summon FallingSand ~ ~ ~-5 
														{
															Block:command_block,
															TileEntityData:
															{
																Command:/execute @e
																[
																	type=ArmorStand,
																	name=eeemP
																] ~ ~ ~ detect ~ ~-1 ~ coal_block 0 /kill @e
																[
																	type=!Player,
																	r=1
																]
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/scoreboard players add @e
																	[
																		type=ArmorStand,
																		name=eeeblock2
																	] e 1
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @e
																		[
																			type=ArmorStand,
																			name=eeemP
																		] ~ ~0.75 ~ /particle dripLava ~ ~ ~ 0 0 0 0.01 1 force
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @e
																			[
																				type=ArmorStand,
																				name=eeemP
																			] ~ ~-2 ~ /tp @e
																			[
																				r=1
																			] ~-1 ~ ~
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @e
																				[
																					type=ArmorStand,
																					name=eeemP,
																					score_e_min=1,
																					score_e=2
																				] ~ ~ ~ /entitydata @e
																				[
																					type=Boat,
																					name=eeeboat,
																					r=1,
																					c=1
																				] 
																				{
																					Rotation:
																					[
																						90f
																					]
																				}
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=ArmorStand,
																						name=eeemP,
																						score_e_min=3,
																						score_e=4
																					] ~ ~ ~ /entitydata @e
																					[
																						type=Boat,
																						name=eeeboat,
																						r=1,
																						c=1
																					] 
																					{
																						Rotation:
																						[
																							0f
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/entitydata @e
																						[
																							type=ArmorStand,
																							name=eeemP,
																							score_e_min=4,
																							score_e=4
																						] 
																						{
																							Motion:
																							[
																								0.15,
																								0.0,
																								0.0
																							]
																						}
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/entitydata @e
																							[
																								type=ArmorStand,
																								name=eeemP,
																								score_e_min=3,
																								score_e=3
																							] 
																							{
																								Motion:
																								[
																									-0.15,
																									0.0,
																									0.0
																								]
																							}
																						},
																						Time:1
																					}
																				}
																			}
																		}
																	}
																}
															}
														}
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/summon FallingSand ~ ~ ~-6 
															{
																Block:command_block,
																TileEntityData:
																{
																	Command:/execute @e
																	[
																		type=MinecartRideable,
																		name=eeem
																	] ~ ~ ~ detect ~ ~-1 ~ emerald_block 0 /tp @e
																	[
																		c=1,
																		type=MinecartRideable,
																		name=eeem,
																		r=1
																	] ~ ~1 ~
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @a
																		[
																			score_e_min=1
																		] ~ ~ ~ detect ~ ~ ~ redstone_block 0 /tp @p ~ ~1 ~
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @e
																			[
																				type=MinecartRideable,
																				name=eeem
																			] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /kill @e
																			[
																				c=1,
																				type=MinecartRideable,
																				name=eeem,
																				r=1
																			]
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @e
																				[
																					type=MinecartRideable,
																					name=eeem
																				] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /particle lava ~ ~0.3 ~ 0.3 0.5 0.3 0.5 30 force
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=MinecartRideable,
																						name=eeem
																					] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /playsound mob.irongolem.death @a ~ ~ ~ 1 0.6 1
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/entitydata @e
																						[
																							type=ArmorStand,
																							name=eeemP,
																							score_e_min=2,
																							score_e=2
																						] 
																						{
																							Motion:
																							[
																								0.0,
																								0.0,
																								-0.15
																							]
																						}
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @a
																							[
																								score_e_min=1,
																								rym=160,
																								ry=179
																							] ~ ~ ~ /entitydata @e
																							[
																								c=1,
																								name=eeem,
																								r=1
																							] 
																							{
																								Rotation:
																								[
																									170f
																								],
																								Motion:
																								[
																									-0.193375620372,
																									0.0346331929393,
																									-0.721687640174
																								]
																							}
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @a
																								[
																									score_e_min=1,
																									rym=140,
																									ry=159
																								] ~ ~ ~ /entitydata @e
																								[
																									c=1,
																									name=eeem,
																									r=1
																								] 
																								{
																									Rotation:
																									[
																										150f
																									],
																									Motion:
																									[
																										-0.428545353632,
																										0.0346331929393,
																										-0.612026192589
																									]
																								}
																							},
																							Time:1
																						}
																					}
																				}
																			}
																		}
																	}
																}
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/summon FallingSand ~ ~ ~-7 
																{
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @a
																		[
																			score_e_min=1,
																			rym=120,
																			ry=139
																		] ~ ~ ~ /entitydata @e
																		[
																			c=1,
																			name=eeem,
																			r=1
																		] 
																		{
																			Rotation:
																			[
																				130f
																			],
																			Motion:
																			[
																				-0.612026192589,
																				0.0346331929393,
																				-0.428545353632
																			]
																		}
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @a
																			[
																				score_e_min=1,
																				rym=100,
																				ry=119
																			] ~ ~ ~ /entitydata @e
																			[
																				c=1,
																				name=eeem,
																				r=1
																			] 
																			{
																				Rotation:
																				[
																					110f
																				],
																				Motion:
																				[
																					-0.721687640174,
																					0.0346331929393,
																					-0.193375620372
																				]
																			}
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @a
																				[
																					score_e_min=1,
																					rym=80,
																					ry=99
																				] ~ ~ ~ /entitydata @e
																				[
																					c=1,
																					name=eeem,
																					r=1
																				] 
																				{
																					Rotation:
																					[
																						90f
																					],
																					Motion:
																					[
																						-0.74430290738,
																						0.0346331929393,
																						0.0651180666251
																					]
																				}
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @a
																					[
																						score_e_min=1,
																						rym=60,
																						ry=79
																					] ~ ~ ~ /entitydata @e
																					[
																						c=1,
																						name=eeem,
																						r=1
																					] 
																					{
																						Rotation:
																						[
																							70f
																						],
																						Motion:
																						[
																							-0.677144259214,
																							0.0346331929393,
																							0.315757553747
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @a
																						[
																							score_e_min=1,
																							rym=40,
																							ry=59
																						] ~ ~ ~ /entitydata @e
																						[
																							c=1,
																							name=eeem,
																							r=1
																						] 
																						{
																							Rotation:
																							[
																								50f
																							],
																							Motion:
																							[
																								-0.528312019802,
																								0.0346331929393,
																								0.528312019802
																							]
																						}
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @a
																							[
																								score_e_min=1,
																								rym=20,
																								ry=39
																							] ~ ~ ~ /entitydata @e
																							[
																								c=1,
																								name=eeem,
																								r=1
																							] 
																							{
																								Rotation:
																								[
																									30f
																								],
																								Motion:
																								[
																									-0.315757553747,
																									0.0346331929393,
																									0.677144259214
																								]
																							}
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @a
																								[
																									score_e_min=1,
																									rym=0,
																									ry=19
																								] ~ ~ ~ /entitydata @e
																								[
																									c=1,
																									name=eeem,
																									r=1
																								] 
																								{
																									Rotation:
																									[
																										10f
																									],
																									Motion:
																									[
																										-0.0651180666251,
																										0.0346331929393,
																										0.74430290738
																									]
																								}
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @a
																									[
																										score_e_min=1,
																										rym=-20,
																										ry=-1
																									] ~ ~ ~ /entitydata @e
																									[
																										c=1,
																										name=eeem,
																										r=1
																									] 
																									{
																										Rotation:
																										[
																											-10f
																										],
																										Motion:
																										[
																											0.193375620372,
																											0.0346331929393,
																											0.721687640174
																										]
																									}
																								},
																								Time:1
																							}
																						}
																					}
																				}
																			}
																		}
																	}
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/summon FallingSand ~ ~ ~-8 
																	{
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @a
																			[
																				score_e_min=1,
																				rym=-40,
																				ry=-21
																			] ~ ~ ~ /entitydata @e
																			[
																				c=1,
																				name=eeem,
																				r=1
																			] 
																			{
																				Rotation:
																				[
																					-30f
																				],
																				Motion:
																				[
																					0.428545353632,
																					0.0346331929393,
																					0.612026192589
																				]
																			}
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @a
																				[
																					score_e_min=1,
																					rym=-60,
																					ry=-41
																				] ~ ~ ~ /entitydata @e
																				[
																					c=1,
																					name=eeem,
																					r=1
																				] 
																				{
																					Rotation:
																					[
																						-50f
																					],
																					Motion:
																					[
																						0.612026192589,
																						0.0346331929393,
																						0.428545353632
																					]
																				}
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @a
																					[
																						score_e_min=1,
																						rym=-80,
																						ry=-61
																					] ~ ~ ~ /entitydata @e
																					[
																						c=1,
																						name=eeem,
																						r=1
																					] 
																					{
																						Rotation:
																						[
																							-70f
																						],
																						Motion:
																						[
																							0.721687640174,
																							0.0346331929393,
																							0.193375620372
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @a
																						[
																							score_e_min=1,
																							rym=-100,
																							ry=-81
																						] ~ ~ ~ /entitydata @e
																						[
																							c=1,
																							name=eeem,
																							r=1
																						] 
																						{
																							Rotation:
																							[
																								-90f
																							],
																							Motion:
																							[
																								0.74430290738,
																								0.0346331929393,
																								-0.0651180666251
																							]
																						}
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @a
																							[
																								score_e_min=1,
																								rym=-120,
																								ry=-101
																							] ~ ~ ~ /entitydata @e
																							[
																								c=1,
																								name=eeem,
																								r=1
																							] 
																							{
																								Rotation:
																								[
																									-110f
																								],
																								Motion:
																								[
																									0.677144259214,
																									0.0346331929393,
																									-0.315757553747
																								]
																							}
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @a
																								[
																									score_e_min=1,
																									rym=-140,
																									ry=-121
																								] ~ ~ ~ /entitydata @e
																								[
																									c=1,
																									name=eeem,
																									r=1
																								] 
																								{
																									Rotation:
																									[
																										-130f
																									],
																									Motion:
																									[
																										0.528312019802,
																										0.0346331929393,
																										-0.528312019802
																									]
																								}
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @a
																									[
																										score_e_min=1,
																										rym=-160,
																										ry=-141
																									] ~ ~ ~ /entitydata @e
																									[
																										c=1,
																										name=eeem,
																										r=1
																									] 
																									{
																										Rotation:
																										[
																											-150f
																										],
																										Motion:
																										[
																											0.315757553747,
																											0.0346331929393,
																											-0.677144259214
																										]
																									}
																								},
																								Time:1,
																								Riding:
																								{
																									id:FallingSand,
																									Block:command_block,
																									TileEntityData:
																									{
																										Command:/execute @a
																										[
																											score_e_min=1,
																											rym=-180,
																											ry=-161
																										] ~ ~ ~ /entitydata @e
																										[
																											c=1,
																											name=eeem,
																											r=1
																										] 
																										{
																											Rotation:
																											[
																												-170f
																											],
																											Motion:
																											[
																												0.0651180666251,
																												0.0346331929393,
																												-0.74430290738
																											]
																										}
																									},
																									Time:1
																								}
																							}
																						}
																					}
																				}
																			}
																		}
																	}
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/summon FallingSand ~ ~ ~-9 
																		{
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/entitydata @e
																				[
																					type=ArmorStand,
																					name=eeemP,
																					score_e_min=1,
																					score_e=1
																				] 
																				{
																					Motion:
																					[
																						0.0,
																						0.0,
																						0.15
																					]
																				}
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=ArmorStand,
																						name=eeemP
																					] ~ ~ ~ detect ~-1 ~1 ~ stained_hardened_clay 14 /scoreboard players set @e
																					[
																						type=ArmorStand,
																						name=eeemP,
																						r=1,
																						c=1
																					] e 4
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @e
																						[
																							type=ArmorStand,
																							name=eeemP
																						] ~ ~ ~ detect ~1 ~1 ~ stained_hardened_clay 14 /scoreboard players set @e
																						[
																							type=ArmorStand,
																							name=eeemP,
																							r=1,
																							c=1
																						] e 3
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @e
																							[
																								type=ArmorStand,
																								name=eeemP
																							] ~ ~ ~ detect ~ ~1 ~1 stained_hardened_clay 14 /scoreboard players set @e
																							[
																								type=ArmorStand,
																								name=eeemP,
																								r=1,
																								c=1
																							] e 2
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @e
																								[
																									type=ArmorStand,
																									name=eeemP
																								] ~ ~ ~ detect ~ ~1 ~-1 stained_hardened_clay 14 /scoreboard players set @e
																								[
																									type=ArmorStand,
																									name=eeemP,
																									r=1,
																									c=1
																								] e 1
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @e
																									[
																										type=Squid,
																										name=Moving_Platform,
																										score_e_min=1,
																										score_e=1
																									] ~ ~ ~ /summon Boat ~ ~-1 ~ 
																									{
																										CustomName:"eeeboat",
																										Invulnerable:1,
																										Riding:
																										{
																											id:ArmorStand,
																											CustomName:"eeemP",
																											Equipment:
																											[
																												{
																												},
																												{
																												},
																												{
																												},
																												{
																												},
																												{
																													Damage:1,
																													id:planks
																												}
																											],
																											Invulnerable:1,
																											NoBasePlate:1,
																											ShowArms:0,
																											Small:1,
																											Invisible:1,
																											DisabledSlots:2039552
																										}
																									}
																								},
																								Time:1,
																								Riding:
																								{
																									id:FallingSand,
																									Block:command_block,
																									TileEntityData:
																									{
																										Command:/kill @e
																										[
																											type=Squid,
																											score_e_min=3
																										]
																									},
																									Time:1,
																									Riding:
																									{
																										id:FallingSand,
																										Block:command_block,
																										TileEntityData:
																										{
																											Command:/tp @e
																											[
																												type=Squid,
																												score_e_min=2
																											] ~ ~-5 ~
																										},
																										Time:1
																									}
																								}
																							}
																						}
																					}
																				}
																			}
																		}
																	},
																	Time:1
																}
															}
														}
													}
												}
											}
										}
									}
								}
							},
							Time:1,
							Riding:
							{
								id:FallingSand,
								Block:command_block,
								TileEntityData:
								{
									Command:/summon FallingSand ~ ~-6 ~-2 
									{
										Block:iron_block,
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:command_block,
											TileEntityData:
											{
												Command:/summon FallingSand ~1 ~-3 ~ 
												{
													Block:emerald_block,
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/fill ~2 ~2 ~3 ~-2 ~2 ~-11 bedrock
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/tellraw @a
																[
																	r=200
																] 
																{
																	"text":"  This machine is fully assembled.",
																	"color":"green",
																	"bold":"true"
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/fill ~-1 ~ ~ ~-1 ~-5 ~ quartz_block
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/setblock ~-1 ~-1 ~-3 command_block 0 replace 
																		{
																			Command:/testfor @a
																			[
																				score_eeeeee_min=11
																			]
																		}
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/setblock ~-1 ~-3 ~-3 command_block 0 replace 
																			{
																				Command:/testfor @a
																				[
																					score_eeeeee=3
																				]
																			}
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/setblock ~-1 ~1 ~-2 unpowered_comparator 2
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/setblock ~-1 ~-1 ~-2 unpowered_comparator 2
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/fill ~-1 ~ ~-2 ~-1 ~4 ~-3 quartz_block
																					},
																					Time:1
																				}
																			}
																		}
																	}
																}
															}
														}
													}
												}
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/fill ~1 ~-7 ~-11 ~1 ~3 ~3 stained_glass 15 replace stained_glass
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/summon FallingSand ~1 ~ ~-10 
														{
															Block:redstone_block,
															Time:1
														}
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/summon FallingSand ~ ~ ~-5 
															{
																Block:iron_block,
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @a
																		[
																			score_eeeeee_min=10,
																			score_eeeeee=10
																		] ~ ~ ~ /execute @e
																		[
																			type=ArmorStand,
																			name=eeemP
																		] ~ ~ ~ /kill @e
																		[
																			type=!Player,
																			r=1
																		]
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @a
																			[
																				score_eeeeee_min=10
																			] ~ ~ ~ /kill @e
																			[
																				type=ArmorStand,
																				name=eeeMove
																			]
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @a
																				[
																					score_eeeeee_min=10
																				] ~ ~ ~ /scoreboard objectives remove eeeee
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @a
																					[
																						score_eeeeee_min=10
																					] ~ ~ ~ /scoreboard objectives remove eeee
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @a
																						[
																							score_eeeeee_min=10
																						] ~ ~ ~ /scoreboard objectives remove eee
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @a
																							[
																								score_eeeeee_min=10
																							] ~ ~ ~ /scoreboard objectives remove ee
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/clear @a
																								[
																									score_eeeeee_min=10,
																									score_eeeeee=10
																								]
																							},
																							Time:1
																						}
																					}
																				}
																			}
																		}
																	}
																}
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/summon FallingSand ~ ~ ~-6 
																{
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @a
																		[
																			score_eeeeee_min=10
																		] ~ ~ ~ /scoreboard objectives remove e
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/scoreboard players add @a
																			[
																				score_eeeeee_min=4
																			] eeeeee 1
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/scoreboard players add @a
																				[
																					score_eeeeee=2
																				] eeeeee 1
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/replaceitem entity @a
																					[
																						score_eeeeee=2
																					] slot.hotbar.8 spawn_egg 1 94 
																					{
																						display:
																						{
																							Name:"Movable_Block"
																						},
																						HideFlags:127,
																						ench:
																						[
																							{
																								id:34,
																								lvl:10
																							}
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/scoreboard players set @a
																						[
																							score_eeee_min=10
																						] eeee 0
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/tp @p
																							[
																								score_eeee_min=10
																							] ~ ~1.5 ~
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @p
																								[
																									rym=45,
																									ry=135,
																									score_eeee_min=10
																								] ~-1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e
																								[
																									type=ArmorStand,
																									name=eeeMove,
																									r=1,
																									c=1
																								] ~1 ~ ~ /execute @p
																								[
																									r=1,
																									score_eee_min=1
																								] ~-1 ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e
																								[
																									type=ArmorStand,
																									name=eeeMove,
																									r=1,
																									c=1
																								] eeee 3
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @p
																									[
																										rym=45,
																										ry=135,
																										score_eee_min=1
																									] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /execute @p ~-1 ~ ~ detect ~-1 ~ ~ air 0 /scoreboard players set @e
																									[
																										type=ArmorStand,
																										name=eeeMove,
																										r=1,
																										c=1
																									] eeee 4
																								},
																								Time:1
																							}
																						}
																					}
																				}
																			}
																		}
																	}
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/summon FallingSand ~ ~ ~-7 
																	{
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/execute @p
																			[
																				rym=-135,
																				ry=-45,
																				score_eeee_min=10
																			] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e
																			[
																				type=ArmorStand,
																				name=eeeMove,
																				r=1,
																				c=1
																			] ~-1 ~ ~ /execute @p
																			[
																				r=1,
																				score_eee_min=1
																			] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e
																			[
																				type=ArmorStand,
																				name=eeeMove,
																				r=1,
																				c=1
																			] eeee 4
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/execute @p
																				[
																					rym=-135,
																					ry=-45,
																					score_eee_min=1
																				] ~ ~ ~ detect ~1 ~ ~ bedrock 0 /execute @p ~1 ~ ~ detect ~1 ~ ~ air 0 /scoreboard players set @e
																				[
																					type=ArmorStand,
																					name=eeeMove,
																					r=1,
																					c=1
																				] eeee 3
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @p
																					[
																						rym=136,
																						ry=-136,
																						score_eeee_min=10
																					] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /execute @e
																					[
																						type=ArmorStand,
																						name=eeeMove,
																						r=1,
																						c=1
																					] ~ ~ ~1 /execute @p
																					[
																						r=1,
																						score_eee_min=1
																					] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /scoreboard players set @e
																					[
																						type=ArmorStand,
																						name=eeeMove,
																						r=1,
																						c=1
																					] eeee 1
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @p
																						[
																							rym=136,
																							ry=-136,
																							score_eee_min=1
																						] ~ ~ ~ detect ~ ~ ~-1 bedrock 0 /execute @p ~ ~ ~-1 detect ~ ~ ~-1 air 0 /scoreboard players set @e
																						[
																							type=ArmorStand,
																							name=eeeMove,
																							r=1,
																							c=1
																						] eeee 2
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @p
																							[
																								rym=-44,
																								ry=44,
																								score_eeee_min=10
																							] ~ ~ ~1 detect ~ ~ ~ bedrock 0 /execute @e
																							[
																								type=ArmorStand,
																								name=eeeMove,
																								r=1,
																								c=1
																							] ~ ~ ~-1 /execute @p
																							[
																								r=1,
																								score_eee_min=1
																							] ~ ~ ~1 detect ~ ~ ~ bedrock 0 /scoreboard players set @e
																							[
																								type=ArmorStand,
																								name=eeeMove,
																								r=1,
																								c=1
																							] eeee 2
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @e
																								[
																									type=ArmorStand,
																									name=eeeMove
																								] ~ ~ ~ detect ~ ~-1 ~ air 0 /summon FallingSand ~ ~ ~ 
																								{
																									Block:bedrock,
																									Time:1,
																									DropItem:0,
																									Motion:
																									[
																										0.0,
																										0.05,
																										0.0
																									]
																								}
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @p
																									[
																										rym=-44,
																										ry=44,
																										score_eee_min=1
																									] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /execute @p ~ ~ ~1 detect ~ ~ ~1 air 0 /scoreboard players set @e
																									[
																										type=ArmorStand,
																										name=eeeMove,
																										r=1,
																										c=1
																									] eeee 1
																								},
																								Time:1,
																								Riding:
																								{
																									id:FallingSand,
																									Block:command_block,
																									TileEntityData:
																									{
																										Command:/scoreboard players set @e
																										[
																											type=ArmorStand
																										] eeee 0
																									},
																									Time:1
																								}
																							}
																						}
																					}
																				}
																			}
																		}
																	}
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/summon FallingSand ~ ~ ~-8 
																		{
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/kill @e
																				[
																					type=ArmorStand,
																					name=eeeMove,
																					score_eeeee_min=20
																				]
																			},
																			Time:1,
																			Riding:
																			{
																				id:FallingSand,
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=ArmorStand,
																						name=eeeMove,
																						score_eeee_min=4,
																						score_eeee=4
																					] ~ ~ ~ /summon FallingSand ~1 ~ ~ 
																					{
																						Block:bedrock,
																						Time:1,
																						DropItem:0,
																						Motion:
																						[
																							-0.3,
																							0.05,
																							0.0
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/scoreboard players remove @a
																						[
																							score_eee_min=1
																						] eee 1
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @e
																							[
																								type=ArmorStand,
																								name=eeeMove
																							] ~ ~ ~ detect ~ ~ ~ air 0 /scoreboard players add @e
																							[
																								type=ArmorStand,
																								name=eeeMove
																							] eeeee 2
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @e
																								[
																									type=ArmorStand,
																									name=eeeMove,
																									score_eeee_min=3,
																									score_eeee=3
																								] ~ ~ ~ /summon FallingSand ~-1 ~ ~ 
																								{
																									Block:bedrock,
																									Time:1,
																									DropItem:0,
																									Motion:
																									[
																										0.3,
																										0.05,
																										0.0
																									]
																								}
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/scoreboard players set @a
																									[
																										score_eee_min=10
																									] eee 2
																								},
																								Time:1,
																								Riding:
																								{
																									id:FallingSand,
																									Block:command_block,
																									TileEntityData:
																									{
																										Command:/execute @e
																										[
																											type=ArmorStand,
																											name=eeeMove
																										] ~ ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e
																										[
																											type=ArmorStand,
																											name=eeeMove
																										] eeeee 0
																									},
																									Time:1,
																									Riding:
																									{
																										id:FallingSand,
																										Block:command_block,
																										TileEntityData:
																										{
																											Command:/execute @e
																											[
																												type=ArmorStand,
																												name=eeeMove,
																												score_eeee_min=2,
																												score_eeee=2
																											] ~ ~ ~ /summon FallingSand ~ ~ ~1 
																											{
																												Block:bedrock,
																												Time:1,
																												DropItem:0,
																												Motion:
																												[
																													0.0,
																													0.05,
																													-0.3
																												]
																											}
																										},
																										Time:1
																									}
																								}
																							}
																						}
																					}
																				}
																			}
																		}
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/summon FallingSand ~ ~ ~-9 
																			{
																				Block:command_block,
																				TileEntityData:
																				{
																					Command:/execute @e
																					[
																						type=ArmorStand,
																						name=eeeMove,
																						score_eeee_min=1,
																						score_eeee=1
																					] ~ ~ ~ /summon FallingSand ~ ~ ~-1 
																					{
																						Block:bedrock,
																						Time:1,
																						DropItem:0,
																						Motion:
																						[
																							0.0,
																							0.05,
																							0.3
																						]
																					}
																				},
																				Time:1,
																				Riding:
																				{
																					id:FallingSand,
																					Block:command_block,
																					TileEntityData:
																					{
																						Command:/execute @a
																						[
																							rym=136,
																							ry=-136,
																							score_eee_min=1
																						] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /execute @e
																						[
																							type=ArmorStand,
																							name=eeeMove,
																							r=1,
																							c=1
																						] ~ ~ ~ /execute @p
																						[
																							r=2
																						] ~ ~ ~ detect ~ ~ ~-1 bedrock 0 /scoreboard players add @p eeee 2
																					},
																					Time:1,
																					Riding:
																					{
																						id:FallingSand,
																						Block:command_block,
																						TileEntityData:
																						{
																							Command:/execute @e
																							[
																								type=ArmorStand,
																								name=eeeMove,
																								score_eeee_min=4,
																								score_eeee=4
																							] ~ ~ ~ /tp @e
																							[
																								type=ArmorStand,
																								name=eeeMove,
																								c=1
																							] ~-1 ~ ~
																						},
																						Time:1,
																						Riding:
																						{
																							id:FallingSand,
																							Block:command_block,
																							TileEntityData:
																							{
																								Command:/execute @a
																								[
																									rym=-44,
																									ry=44,
																									score_eee_min=1
																								] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /execute @e
																								[
																									type=ArmorStand,
																									name=eeeMove,
																									r=1,
																									c=1
																								] ~ ~ ~ /execute @p
																								[
																									r=2
																								] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /scoreboard players add @p eeee 2
																							},
																							Time:1,
																							Riding:
																							{
																								id:FallingSand,
																								Block:command_block,
																								TileEntityData:
																								{
																									Command:/execute @e
																									[
																										type=ArmorStand,
																										name=eeeMove,
																										score_eeee_min=3,
																										score_eeee=3
																									] ~ ~ ~ /tp @e
																									[
																										type=ArmorStand,
																										name=eeeMove,
																										c=1
																									] ~1 ~ ~
																								},
																								Time:1,
																								Riding:
																								{
																									id:FallingSand,
																									Block:command_block,
																									TileEntityData:
																									{
																										Command:/execute @a
																										[
																											rym=45,
																											ry=135,
																											score_eee_min=1
																										] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /execute @e
																										[
																											type=ArmorStand,
																											name=eeeMove,
																											r=1,
																											c=1
																										] ~ ~ ~ /execute @p
																										[
																											r=2
																										] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /scoreboard players add @p eeee 2
																									},
																									Time:1,
																									Riding:
																									{
																										id:FallingSand,
																										Block:command_block,
																										TileEntityData:
																										{
																											Command:/execute @e
																											[
																												type=ArmorStand,
																												name=eeeMove,
																												score_eeee_min=2,
																												score_eeee=2
																											] ~ ~ ~ /tp @e
																											[
																												type=ArmorStand,
																												name=eeeMove,
																												c=1
																											] ~ ~ ~-1
																										},
																										Time:1,
																										Riding:
																										{
																											id:FallingSand,
																											Block:command_block,
																											TileEntityData:
																											{
																												Command:/execute @e
																												[
																													type=Squid,
																													score_e_min=1,
																													score_e=1,
																													name=Movable_Block
																												] ~ ~ ~ /setblock ~ ~ ~ bedrock
																											},
																											Time:1
																										}
																									}
																								}
																							}
																						}
																					}
																				}
																			}
																		},
																		Time:1
																	}
																}
															}
														}
													}
												}
											}
										}
									}
								},
								Time:1,
								Riding:
								{
									id:FallingSand,
									Block:command_block,
									TileEntityData:
									{
										Command:/summon FallingSand ~ ~-5 ~-12 
										{
											Block:command_block,
											TileEntityData:
											{
												Command:/execute @a
												[
													rym=-135,
													ry=-45,
													score_eee_min=1
												] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e
												[
													type=ArmorStand,
													name=eeeMove,
													r=1,
													c=1
												] ~ ~ ~ /execute @p
												[
													r=2
												] ~ ~ ~ detect ~1 ~ ~ bedrock 0 /scoreboard players add @p eeee 2
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/execute @e
													[
														type=ArmorStand,
														name=eeeMove,
														score_eeee_min=1,
														score_eeee=1
													] ~ ~ ~ /tp @e
													[
														type=ArmorStand,
														name=eeeMove,
														c=1
													] ~ ~ ~1
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/scoreboard players remove @a
														[
															score_eeee_min=1
														] eeee 1
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/execute @e
															[
																type=ArmorStand,
																name=eeeMove,
																score_eeee_min=1
															] ~ ~ ~ /setblock ~ ~ ~ air
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/execute @e
																[
																	type=ArmorStand,
																	name=eeeMove
																] ~ ~ ~ /particle townaura ~ ~0.5 ~ 0.3 0.3 0.3 0.1 1 force
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/execute @e
																	[
																		type=Squid,
																		score_e_min=1,
																		score_e=1,
																		name=Movable_Block
																	] ~ ~ ~ /summon ArmorStand ~ ~ ~ 
																	{
																		CustomName:"eeeMove",
																		Invulnerable:1,
																		NoBasePlate:1,
																		Invisible:1,
																		DisabledSlots:2039552
																	}
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/scoreboard players add @e
																		[
																			type=Squid,
																			name=Movable_Block
																		] e 1
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/fill ~1 ~ ~8 ~1 ~7 ~ air
																		},
																		Time:1
																	}
																}
															}
														}
													}
												}
											}
										}
									},
									Time:1,
									Riding:
									{
										id:FallingSand,
										Block:command_block,
										TileEntityData:
										{
											Command:/summon FallingSand ~2 ~-4 ~-12 
											{
												Block:command_block,
												TileEntityData:
												{
													Command:/scoreboard players add @e
													[
														type=Squid,
														name=Moving_Platform
													] e 1
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/execute @a
														[
															score_e_min=1
														] ~ ~ ~ /particle flame ~ ~0.5 ~ 0.1 0.1 0.1 0.01 1 force
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/scoreboard players remove @a
															[
																score_e_min=1
															] e 1
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/scoreboard players set @a e 2 
																{
																	Riding:
																	{
																		id:MinecartRideable,
																		CustomName:"eeem"
																	}
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/execute @e
																	[
																		type=MinecartRideable,
																		name=eeem
																	] ~ ~ ~ /particle smoke ~ ~-0.35 ~ 0.1 0 0.1 0.01 30 force
																},
																Time:1,
																Riding:
																{
																	id:FallingSand,
																	Block:command_block,
																	TileEntityData:
																	{
																		Command:/execute @e
																		[
																			type=Squid,
																			score_e_min=1,
																			score_e=1,
																			name=Driveable_Minecart
																		] ~ ~ ~ /summon MinecartRideable ~ ~ ~ 
																		{
																			CustomName:"eeem",
																			Invulnerable:1
																		}
																	},
																	Time:1,
																	Riding:
																	{
																		id:FallingSand,
																		Block:command_block,
																		TileEntityData:
																		{
																			Command:/scoreboard players add @e
																			[
																				type=Squid,
																				name=Driveable_Minecart
																			] e 1
																		},
																		Time:1,
																		Riding:
																		{
																			id:FallingSand,
																			Block:command_block,
																			TileEntityData:
																			{
																				Command:/fill ~-1 ~ ~8 ~-1 ~7 ~ redstone_block
																			},
																			Time:1
																		}
																	}
																}
															}
														}
													}
												}
											}
										},
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:iron_block,
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:iron_block,
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:iron_block,
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/scoreboard objectives add eeeeee dummy eeeeee
														},
														Time:1
													}
												}
											}
										}
									}
								}
							}
						}
					} 
				},
				Time:1,
				Riding:
				{
					id:FallingSand,
					Block:command_block,
					TileEntityData:
					{
						Command:/summon FallingSand ~ ~-3 ~15 
						{
							Block:iron_block,
							Time:1,
							Riding:
							{
								id:FallingSand,
								Block:command_block,
								TileEntityData:
								{
									Command:/fill ~2 ~1 ~-13 ~-2 ~1 ~1 stained_hardened_clay 11 replace stained_glass 0
								},
								Time:1,
								Riding:
								{
									id:FallingSand,
									Block:command_block,
									TileEntityData:
									{
										Command:/fill ~2 ~-6 ~-13 ~-2 ~-6 ~1 stained_hardened_clay 11 replace stained_glass 0
									},
									Time:1,
									Riding:
									{
										id:FallingSand,
										Block:command_block,
										TileEntityData:
										{
											Command:/summon FallingSand ~-1 ~-4 ~-3 
											{
												Block:command_block,
												TileEntityData:
												{
													Command:/summon FallingSand ~ ~3 ~-3 
													{
														Block:command_block,
														TileEntityData:
														{
															Command:/fill ~-1 ~-1 ~7 ~3 ~9 ~-8 air
														},
														Time:1
													}
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/scoreboard objectives remove eeeeee
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/fill ~1 ~6 ~-10 ~1 ~-3 ~4 stained_glass 14 replace stained_glass
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:quartz_block,
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/fill ~1 ~8 ~-10 ~1 ~-1 ~4 stained_glass 5 replace stained_glass
																},
																Time:1
															}
														}
													}
												}
											}
										},
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:command_block,
											TileEntityData:
											{
												Command:/scoreboard objectives add eeeee dummy eeeee
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/scoreboard objectives add eeee dummy eeee
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/scoreboard objectives add eee stat.crouchOneCm eee
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/scoreboard objectives add ee dummy ee
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/scoreboard objectives add e dummy e
															},
															Time:1
														}
													}
												}
											}
										}
									}
								}
							}
						} 
					},
					Time:1,
					Riding:
					{
						id:FallingSand,
						Block:command_block,
						TileEntityData:
						{
							Command: /summon FallingSand ~1 ~-2 ~15 
							{
								Block:iron_block,
								Time:1,
								Riding:
								{
									id:FallingSand,
									Block:command_block,
									TileEntityData:
									{
										Command:/setworldspawn ~ ~ ~
									},
									Time:1,
									Riding:
									{
										id:FallingSand,
										Block:command_block,
										TileEntityData:
										{
											Command:/tellraw @a
											[
												r=200
											] 
											{
												"text":" ",
												"color":"red"
											}
										},
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:command_block,
											TileEntityData:
											{
												Command:/tellraw @a
												[
													r=200
												] 
												{
													"text":"  3. Don't act like it's your own work.",
													"color":"red"
												}
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/tellraw @a
													[
														r=200
													] 
													{
														"text":"  2. Don't use this command to participate in a competition.",
														"color":"red"
													}
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/tellraw @a
														[
															r=200
														] 
														{
															"text":"  1. Credit IJAMinecraft if you're using this command.",
															"color":"red"
														}
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/tellraw @a
															[
																r=200
															] 
															{
																"text":"",
																"extra":
																[
																	{
																		"text":"  https://www.youtube.com/user/IJAMinecraft",
																		"color":"gold",
																		"clickEvent":
																		{
																			"action":"open_url",
																			"value":"https://www.youtube.com/user/IJAMinecraft"
																		}
																	}
																]
															}
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:command_block,
															TileEntityData:
															{
																Command:/tellraw @a
																[
																	r=200
																] 
																{
																	"text":" 'Transport Mechanics'",
																	"bold":"true",
																	"color":"gold",
																	"extra":
																	[
																		{
																			"text":" Command by IJAMinecraft",
																			"color":"white",
																			"bold":"false"
																		}
																	]
																}
															},
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/tellraw @a
																	[
																		r=200
																	] 
																	{
																		"text":" ",
																		"color":"red"
																	}
																},
																Time:1
															}
														}
													}
												}
											}
										}
									}
								}
							} 
						},
						Time:1,
						Riding:
						{
							id:FallingSand,
							Block:command_block,
							TileEntityData:
							{
								Command:/fill ~1 ~-8 ~14 ~-1 ~ ~14 redstone_block
							},
							Time:1,
							Riding:
							{
								id:FallingSand,
								Block:command_block,
								TileEntityData:
								{
									Command:/setblock ~ ~-4 ~1 wall_sign 2 destroy 
									{
										Text1:"{text:'[Destroy]',color:red,bold:true}",
										Text2:"{text:'Right-click this',color:black}",
										Text3:"{text:'sign to destroy',color:black}",
										Text4:"{text:'the machine!',color:black,clickEvent:{action:run_command,value:'/scoreboard players set @p eeeeee 4'}}"
									}
								},
								Time:1,
								Riding:
								{
									id:FallingSand,
									Block:command_block,
									TileEntityData:
									{
										Command:/setblock ~ ~-2 ~1 wall_sign 2 destroy 
										{
											Text1:"{text:'[Get Items]',color:dark_green,bold:true}",
											Text2:"{text:'Right-click this',color:black}",
											Text3:"{text:'sign to get',color:black}",
											Text4:"{text:'your items!',color:black,clickEvent:{action:run_command,value:'/scoreboard players set @p eeeeee 0'}}"
										}
									},
									Time:1,
									Riding:
									{
										id:FallingSand,
										Block:command_block,
										TileEntityData:
										{
											Command:/setblock ~ ~ ~1 wall_sign 2 destroy 
											{
												Text1:"{text:'Transport',color:dark_red,bold:true}",
												Text2:"{text:'Mechanics',color:dark_red}",
												Text3:"{text:'Command by',color:black}",
												Text4:"{text:'IJAMinecraft',color:black,clickEvent:{action:run_command,value:'/tell @p Hi.'}}"
											}
										},
										Time:1,
										Riding:
										{
											id:FallingSand,
											Block:command_block,
											TileEntityData:
											{
												Command:/fill ~1 ~-4 ~3 ~-1 ~4 ~15 air
											},
											Time:1,
											Riding:
											{
												id:FallingSand,
												Block:command_block,
												TileEntityData:
												{
													Command:/fill ~2 ~-3 ~2 ~-2 ~5 ~16 stained_glass 0 hollow
												},
												Time:1,
												Riding:
												{
													id:FallingSand,
													Block:command_block,
													TileEntityData:
													{
														Command:/fill ~2 ~-3 ~2 ~-2 ~-3 ~16 bedrock
													},
													Time:1,
													Riding:
													{
														id:FallingSand,
														Block:command_block,
														TileEntityData:
														{
															Command:/fill ~2 ~-2 ~2 ~-2 ~40 ~16 air
														},
														Time:1,
														Riding:
														{
															id:FallingSand,
															Block:redstone_block,
															Time:1,
															Riding:
															{
																id:FallingSand,
																Block:command_block,
																TileEntityData:
																{
																	Command:/gamerule commandBlockOutput false
																},
																Time:1
															}
														}
													}
												}
											}
										}
									}
								}
							}
						}
					}
				}
			}
		}
	}
}
```
##### CONDENSADO:  
	/summon FallingSand ~ ~2 ~ {Block:redstone_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~-1 ~-14 ~ ~-1 ~1 ~ redstone_block},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~-1 ~-13 ~ ~ ~2 ~ air},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~-1 ~-4 ~15 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~2 ~-7 ~-2 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-2 {Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.1 emerald_block 1 0 {display:{Name:"Driveable_Minecart_Boost"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.3 spawn_egg 1 94 {display:{Name:"Moving_Platform"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.5 coal_block 1 0 {display:{Name:"Platform_Destroyer"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.7 iron_block 1 0 {display:{Name:"Elevator_Mover"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_ee_min=1] ~ ~ ~ detect ~ ~2.5 ~ iron_block 0 /tp @p[r=1] ~1 ~ ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeeel,score_ee_min=3,score_ee=3] ~ ~2 ~ /effect @a[r=1] 11 1 150 true},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeeel,score_ee_min=3,score_ee=3] ~ ~ ~ /particle portal ~ ~ ~ 0.4 0.025 0.4 0.01 40 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=MinecartRideable,name=eeeel,score_ee_min=3,score_ee=3] {Motion:[0.0,0.0,0.0]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-3 {Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.0 spawn_egg 1 94 {display:{Name:"Driveable_Minecart"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.2 redstone_block 1 0 {display:{Name:"Destroys_Minecart_Driving_On_It"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.4 stained_hardened_clay 1 14 {display:{Name:"Platform_Mover"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.6 spawn_egg 1 94 {display:{Name:"Elevator"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeeel] ~ ~ ~ detect ~ ~2 ~ iron_block 0 /scoreboard players set @e[type=MinecartRideable,name=eeeel,r=1,c=1] ee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_ee_min=1] ~ ~ ~ /execute @e[type=MinecartRideable,name=eeeel,r=1,c=1] ~ ~ ~ detect ~ ~-1 ~ iron_block 0 /scoreboard players set @e[type=MinecartRideable,name=eeeel,r=1,c=1] ee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeeel] ~ ~ ~ detect ~ ~-1 ~ iron_block 0 /scoreboard players set @e[type=MinecartRideable,name=eeeel,r=1,c=1] ee 3},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players remove @a[score_ee_min=1] ee 1},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-4 {Block:command_block,TileEntityData:{Command:/scoreboard players set @a ee 2 {Riding:{id:MinecartRideable,CustomName:"eeeel"}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeeel,score_ee_min=1,score_ee=1] ~ ~ ~ /particle portal ~ ~-0.35 ~ 0 0.15 0 0.1 30 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=MinecartRideable,name=eeeel,score_ee_min=2,score_ee=2] {Motion:[0.0,-0.1,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=MinecartRideable,name=eeeel,score_ee_min=1,score_ee=1] {Motion:[0.0,0.1,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/kill @e[type=Item,score_e_min=1]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players set @e[type=Item] e 1 {Item:{id:minecraft:dye,Damage:0s}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=Squid,name=Elevator,score_e_min=1,score_e=1] ~ ~ ~ /summon MinecartRideable ~ ~ ~ {CustomName:"eeeel",Invulnerable:1}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @e[type=Squid,name=Elevator] e 1},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-5 {Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ detect ~ ~-1 ~ coal_block 0 /kill @e[type=!Player,r=1]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @e[type=ArmorStand,name=eeeblock2] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~0.75 ~ /particle dripLava ~ ~ ~ 0 0 0 0.01 1 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~-2 ~ /tp @e[r=1] ~-1 ~ ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP,score_e_min=1,score_e=2] ~ ~ ~ /entitydata @e[type=Boat,name=eeeboat,r=1,c=1] {Rotation:[90f]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP,score_e_min=3,score_e=4] ~ ~ ~ /entitydata @e[type=Boat,name=eeeboat,r=1,c=1] {Rotation:[0f]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=ArmorStand,name=eeemP,score_e_min=4,score_e=4] {Motion:[0.15,0.0,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=ArmorStand,name=eeemP,score_e_min=3,score_e=3] {Motion:[-0.15,0.0,0.0]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-6 {Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeem] ~ ~ ~ detect ~ ~-1 ~ emerald_block 0 /tp @e[c=1,type=MinecartRideable,name=eeem,r=1] ~ ~1 ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1] ~ ~ ~ detect ~ ~ ~ redstone_block 0 /tp @p ~ ~1 ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeem] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /kill @e[c=1,type=MinecartRideable,name=eeem,r=1]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeem] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /particle lava ~ ~0.3 ~ 0.3 0.5 0.3 0.5 30 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeem] ~ ~ ~ detect ~ ~-1 ~ redstone_block 0 /playsound mob.irongolem.death @a ~ ~ ~ 1 0.6 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/entitydata @e[type=ArmorStand,name=eeemP,score_e_min=2,score_e=2] {Motion:[0.0,0.0,-0.15]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=160,ry=179] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[170f],Motion:[-0.193375620372,0.0346331929393,-0.721687640174]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=140,ry=159] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[150f],Motion:[-0.428545353632,0.0346331929393,-0.612026192589]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-7 {Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=120,ry=139] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[130f],Motion:[-0.612026192589,0.0346331929393,-0.428545353632]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=100,ry=119] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[110f],Motion:[-0.721687640174,0.0346331929393,-0.193375620372]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=80,ry=99] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[90f],Motion:[-0.74430290738,0.0346331929393,0.0651180666251]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=60,ry=79] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[70f],Motion:[-0.677144259214,0.0346331929393,0.315757553747]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=40,ry=59] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[50f],Motion:[-0.528312019802,0.0346331929393,0.528312019802]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=20,ry=39] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[30f],Motion:[-0.315757553747,0.0346331929393,0.677144259214]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=0,ry=19] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[10f],Motion:[-0.0651180666251,0.0346331929393,0.74430290738]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-20,ry=-1] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-10f],Motion:[0.193375620372,0.0346331929393,0.721687640174]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-8 {Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-40,ry=-21] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-30f],Motion:[0.428545353632,0.0346331929393,0.612026192589]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-60,ry=-41] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-50f],Motion:[0.612026192589,0.0346331929393,0.428545353632]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-80,ry=-61] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-70f],Motion:[0.721687640174,0.0346331929393,0.193375620372]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-100,ry=-81] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-90f],Motion:[0.74430290738,0.0346331929393,-0.0651180666251]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-120,ry=-101] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-110f],Motion:[0.677144259214,0.0346331929393,-0.315757553747]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-140,ry=-121] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-130f],Motion:[0.528312019802,0.0346331929393,-0.528312019802]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-160,ry=-141] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-150f],Motion:[0.315757553747,0.0346331929393,-0.677144259214]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1,rym=-180,ry=-161] ~ ~ ~ /entitydata @e[c=1,name=eeem,r=1] {Rotation:[-170f],Motion:[0.0651180666251,0.0346331929393,-0.74430290738]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-9 {Block:command_block,TileEntityData:{Command:/entitydata @e[type=ArmorStand,name=eeemP,score_e_min=1,score_e=1] {Motion:[0.0,0.0,0.15]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ detect ~-1 ~1 ~ stained_hardened_clay 14 /scoreboard players set @e[type=ArmorStand,name=eeemP,r=1,c=1] e 4},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ detect ~1 ~1 ~ stained_hardened_clay 14 /scoreboard players set @e[type=ArmorStand,name=eeemP,r=1,c=1] e 3},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ detect ~ ~1 ~1 stained_hardened_clay 14 /scoreboard players set @e[type=ArmorStand,name=eeemP,r=1,c=1] e 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ detect ~ ~1 ~-1 stained_hardened_clay 14 /scoreboard players set @e[type=ArmorStand,name=eeemP,r=1,c=1] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=Squid,name=Moving_Platform,score_e_min=1,score_e=1] ~ ~ ~ /summon Boat ~ ~-1 ~ {CustomName:"eeeboat",Invulnerable:1,Riding:{id:ArmorStand,CustomName:"eeemP",Equipment:[{},{},{},{},{Damage:1,id:planks}],Invulnerable:1,NoBasePlate:1,ShowArms:0,Small:1,Invisible:1,DisabledSlots:2039552}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/kill @e[type=Squid,score_e_min=3]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tp @e[type=Squid,score_e_min=2] ~ ~-5 ~},Time:1}}}}}}}}},Time:1}}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~-6 ~-2 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~1 ~-3 ~ {Block:emerald_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~2 ~3 ~-2 ~2 ~-11 bedrock},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":"  This machine is fully assembled.","color":"green","bold":"true"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~-1 ~ ~ ~-1 ~-5 ~ quartz_block},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~-1 ~-1 ~-3 command_block 0 replace {Command:/testfor @a[score_eeeeee_min=11]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~-1 ~-3 ~-3 command_block 0 replace {Command:/testfor @a[score_eeeeee=3]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~-1 ~1 ~-2 unpowered_comparator 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~-1 ~-1 ~-2 unpowered_comparator 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~-1 ~ ~-2 ~-1 ~4 ~-3 quartz_block},Time:1}}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~-7 ~-11 ~1 ~3 ~3 stained_glass 15 replace stained_glass},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~1 ~ ~-10 {Block:redstone_block,Time:1}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-5 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10,score_eeeeee=10] ~ ~ ~ /execute @e[type=ArmorStand,name=eeemP] ~ ~ ~ /kill @e[type=!Player,r=1]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /kill @e[type=ArmorStand,name=eeeMove]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /scoreboard objectives remove eeeee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /scoreboard objectives remove eeee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /scoreboard objectives remove eee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /scoreboard objectives remove ee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/clear @a[score_eeeeee_min=10,score_eeeeee=10]},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-6 {Block:command_block,TileEntityData:{Command:/execute @a[score_eeeeee_min=10] ~ ~ ~ /scoreboard objectives remove e},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @a[score_eeeeee_min=4] eeeeee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @a[score_eeeeee=2] eeeeee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/replaceitem entity @a[score_eeeeee=2] slot.hotbar.8 spawn_egg 1 94 {display:{Name:"Movable_Block"},HideFlags:127,ench:[{id:34,lvl:10}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players set @a[score_eeee_min=10] eeee 0},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tp @p[score_eeee_min=10] ~ ~1.5 ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=45,ry=135,score_eeee_min=10] ~-1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~1 ~ ~ /execute @p[r=1,score_eee_min=1] ~-1 ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 3},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=45,ry=135,score_eee_min=1] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /execute @p ~-1 ~ ~ detect ~-1 ~ ~ air 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 4},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-7 {Block:command_block,TileEntityData:{Command:/execute @p[rym=-135,ry=-45,score_eeee_min=10] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~-1 ~ ~ /execute @p[r=1,score_eee_min=1] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 4},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=-135,ry=-45,score_eee_min=1] ~ ~ ~ detect ~1 ~ ~ bedrock 0 /execute @p ~1 ~ ~ detect ~1 ~ ~ air 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 3},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=136,ry=-136,score_eeee_min=10] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~1 /execute @p[r=1,score_eee_min=1] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=136,ry=-136,score_eee_min=1] ~ ~ ~ detect ~ ~ ~-1 bedrock 0 /execute @p ~ ~ ~-1 detect ~ ~ ~-1 air 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=-44,ry=44,score_eeee_min=10] ~ ~ ~1 detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~-1 /execute @p[r=1,score_eee_min=1] ~ ~ ~1 detect ~ ~ ~ bedrock 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove] ~ ~ ~ detect ~ ~-1 ~ air 0 /summon FallingSand ~ ~ ~ {Block:bedrock,Time:1,DropItem:0,Motion:[0.0,0.05,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @p[rym=-44,ry=44,score_eee_min=1] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /execute @p ~ ~ ~1 detect ~ ~ ~1 air 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove,r=1,c=1] eeee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players set @e[type=ArmorStand] eeee 0},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-8 {Block:command_block,TileEntityData:{Command:/kill @e[type=ArmorStand,name=eeeMove,score_eeeee_min=20]},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=4,score_eeee=4] ~ ~ ~ /summon FallingSand ~1 ~ ~ {Block:bedrock,Time:1,DropItem:0,Motion:[-0.3,0.05,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players remove @a[score_eee_min=1] eee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove] ~ ~ ~ detect ~ ~ ~ air 0 /scoreboard players add @e[type=ArmorStand,name=eeeMove] eeeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=3,score_eeee=3] ~ ~ ~ /summon FallingSand ~-1 ~ ~ {Block:bedrock,Time:1,DropItem:0,Motion:[0.3,0.05,0.0]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players set @a[score_eee_min=10] eee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove] ~ ~ ~ detect ~ ~ ~ bedrock 0 /scoreboard players set @e[type=ArmorStand,name=eeeMove] eeeee 0},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=2,score_eeee=2] ~ ~ ~ /summon FallingSand ~ ~ ~1 {Block:bedrock,Time:1,DropItem:0,Motion:[0.0,0.05,-0.3]}},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~ ~-9 {Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=1,score_eeee=1] ~ ~ ~ /summon FallingSand ~ ~ ~-1 {Block:bedrock,Time:1,DropItem:0,Motion:[0.0,0.05,0.3]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[rym=136,ry=-136,score_eee_min=1] ~ ~ ~-1 detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~ /execute @p[r=2] ~ ~ ~ detect ~ ~ ~-1 bedrock 0 /scoreboard players add @p eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=4,score_eeee=4] ~ ~ ~ /tp @e[type=ArmorStand,name=eeeMove,c=1] ~-1 ~ ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[rym=-44,ry=44,score_eee_min=1] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~ /execute @p[r=2] ~ ~ ~ detect ~ ~ ~1 bedrock 0 /scoreboard players add @p eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=3,score_eeee=3] ~ ~ ~ /tp @e[type=ArmorStand,name=eeeMove,c=1] ~1 ~ ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[rym=45,ry=135,score_eee_min=1] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~ /execute @p[r=2] ~ ~ ~ detect ~-1 ~ ~ bedrock 0 /scoreboard players add @p eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=2,score_eeee=2] ~ ~ ~ /tp @e[type=ArmorStand,name=eeeMove,c=1] ~ ~ ~-1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=Squid,score_e_min=1,score_e=1,name=Movable_Block] ~ ~ ~ /setblock ~ ~ ~ bedrock},Time:1}}}}}}}}},Time:1}}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~-5 ~-12 {Block:command_block,TileEntityData:{Command:/execute @a[rym=-135,ry=-45,score_eee_min=1] ~1 ~ ~ detect ~ ~ ~ bedrock 0 /execute @e[type=ArmorStand,name=eeeMove,r=1,c=1] ~ ~ ~ /execute @p[r=2] ~ ~ ~ detect ~1 ~ ~ bedrock 0 /scoreboard players add @p eeee 2},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=1,score_eeee=1] ~ ~ ~ /tp @e[type=ArmorStand,name=eeeMove,c=1] ~ ~ ~1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players remove @a[score_eeee_min=1] eeee 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove,score_eeee_min=1] ~ ~ ~ /setblock ~ ~ ~ air},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=ArmorStand,name=eeeMove] ~ ~ ~ /particle townaura ~ ~0.5 ~ 0.3 0.3 0.3 0.1 1 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=Squid,score_e_min=1,score_e=1,name=Movable_Block] ~ ~ ~ /summon ArmorStand ~ ~ ~ {CustomName:"eeeMove",Invulnerable:1,NoBasePlate:1,Invisible:1,DisabledSlots:2039552}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @e[type=Squid,name=Movable_Block] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~ ~8 ~1 ~7 ~ air},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~2 ~-4 ~-12 {Block:command_block,TileEntityData:{Command:/scoreboard players add @e[type=Squid,name=Moving_Platform] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @a[score_e_min=1] ~ ~ ~ /particle flame ~ ~0.5 ~ 0.1 0.1 0.1 0.01 1 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players remove @a[score_e_min=1] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players set @a e 2 {Riding:{id:MinecartRideable,CustomName:"eeem"}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=MinecartRideable,name=eeem] ~ ~ ~ /particle smoke ~ ~-0.35 ~ 0.1 0 0.1 0.01 30 force},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/execute @e[type=Squid,score_e_min=1,score_e=1,name=Driveable_Minecart] ~ ~ ~ /summon MinecartRideable ~ ~ ~ {CustomName:"eeem",Invulnerable:1}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard players add @e[type=Squid,name=Driveable_Minecart] e 1},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~-1 ~ ~8 ~-1 ~7 ~ redstone_block},Time:1}}}}}}}}},Time:1,Riding:{id:FallingSand,Block:iron_block,Time:1,Riding:{id:FallingSand,Block:iron_block,Time:1,Riding:{id:FallingSand,Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add eeeeee dummy eeeeee},Time:1}}}}}}}}} },Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~-3 ~15 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~1 ~-13 ~-2 ~1 ~1 stained_hardened_clay 11 replace stained_glass 0},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~-6 ~-13 ~-2 ~-6 ~1 stained_hardened_clay 11 replace stained_glass 0},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/summon FallingSand ~-1 ~-4 ~-3 {Block:command_block,TileEntityData:{Command:/summon FallingSand ~ ~3 ~-3 {Block:command_block,TileEntityData:{Command:/fill ~-1 ~-1 ~7 ~3 ~9 ~-8 air},Time:1}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives remove eeeeee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~6 ~-10 ~1 ~-3 ~4 stained_glass 14 replace stained_glass},Time:1,Riding:{id:FallingSand,Block:quartz_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~8 ~-10 ~1 ~-1 ~4 stained_glass 5 replace stained_glass},Time:1}}}}}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add eeeee dummy eeeee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add eeee dummy eeee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add eee stat.crouchOneCm eee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add ee dummy ee},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/scoreboard objectives add e dummy e},Time:1}}}}}}}}} },Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command: /summon FallingSand ~1 ~-2 ~15 {Block:iron_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setworldspawn ~ ~ ~},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":" ","color":"red"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":"  3. Don't act like it's your own work.","color":"red"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":"  2. Don't use this command to participate in a competition.","color":"red"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":"  1. Credit IJAMinecraft if you're using this command.","color":"red"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":"","extra":[{"text":"  https://www.youtube.com/user/IJAMinecraft","color":"gold","clickEvent":{"action":"open_url","value":"https://www.youtube.com/user/IJAMinecraft"}}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":" 'Transport Mechanics'","bold":"true","color":"gold","extra":[{"text":" Command by IJAMinecraft","color":"white","bold":"false"}]}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/tellraw @a[r=200] {"text":" ","color":"red"}},Time:1}}}}}}}}} },Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~-8 ~14 ~-1 ~ ~14 redstone_block},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~ ~-4 ~1 wall_sign 2 destroy {Text1:"{text:'[Destroy]',color:red,bold:true}",Text2:"{text:'Right-click this',color:black}",Text3:"{text:'sign to destroy',color:black}",Text4:"{text:'the machine!',color:black,clickEvent:{action:run_command,value:'/scoreboard players set @p eeeeee 4'}}"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~ ~-2 ~1 wall_sign 2 destroy {Text1:"{text:'[Get Items]',color:dark_green,bold:true}",Text2:"{text:'Right-click this',color:black}",Text3:"{text:'sign to get',color:black}",Text4:"{text:'your items!',color:black,clickEvent:{action:run_command,value:'/scoreboard players set @p eeeeee 0'}}"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/setblock ~ ~ ~1 wall_sign 2 destroy {Text1:"{text:'Transport',color:dark_red,bold:true}",Text2:"{text:'Mechanics',color:dark_red}",Text3:"{text:'Command by',color:black}",Text4:"{text:'IJAMinecraft',color:black,clickEvent:{action:run_command,value:'/tell @p Hi.'}}"}},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~1 ~-4 ~3 ~-1 ~4 ~15 air},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~-3 ~2 ~-2 ~5 ~16 stained_glass 0 hollow},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~-3 ~2 ~-2 ~-3 ~16 bedrock},Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/fill ~2 ~-2 ~2 ~-2 ~40 ~16 air},Time:1,Riding:{id:FallingSand,Block:redstone_block,Time:1,Riding:{id:FallingSand,Block:command_block,TileEntityData:{Command:/gamerule commandBlockOutput false},Time:1}}}}}}}}}}}}}}}}
