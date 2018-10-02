---- Minecraft Crash Report ----

WARNING: coremods are present:
  Wizardry Plugin (wizardry-0.9.7.jar)
  LibLoader (# LibLoader.jar)
  EnderCorePlugin (EnderCore-1.12.2-0.5.37.jar)
  ForgelinPlugin (Forgelin-1.7.4.jar)
  BedPatch (bedpatch-2.2-1.12.2.jar)
  AstralCore (astralsorcery-1.12.2-1.9.4.jar)
  LibrarianLib Plugin (librarianlib-1.12.2-4.15.jar)
  OpenModsCorePlugin (OpenModsLib-1.12.2-0.11.5.jar)
  CoreMod (TickProfiler-1.12-0.0.6.jar)
  Plugin (NotEnoughIDs-1.5.4.2.jar)
  LoadingPlugin (sampler-1.73.jar)
  LoadingPlugin (Quark-r1.5-129.jar)
  MalisisCorePlugin (malisiscore-1.12.2-6.4.0.jar)
  ShetiPhian-ASM (ShetiPhian-ASM-1.12.0.jar)
  FMLPlugin (elulib-0.1.12.jar)
  Inventory Tweaks Coremod (InventoryTweaks-1.64-dev.jar)
  IELoadingPlugin (ImmersiveEngineering-core-0.12-85.jar)
  AppleCore (AppleCore-mc1.12.2-3.1.4.jar)
  TransformerLoader (OpenComputers-MC1.12.2-1.7.2.67.jar)
  CoreMod (Aroma1997Core-1.12.2-2.0.0.0.b156.jar)
  Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. (foamfix-0.10.1-1.12.2.jar)
  RandomPatches (randompatches-1.12.2-1.5.0.4.jar)
  TheBetweenlandsLoadingPlugin (TheBetweenlands-3.3.12-core.jar)
Contact their authors BEFORE contacting forge

// Ouch. That hurt :(

Time: 10/2/18 8:12 PM
Description: Exception generating new chunk

java.lang.VerifyError: Operand stack overflow
Exception Details:
  Location:
    net/minecraft/world/chunk/ChunkPrimer.func_177855_a(IIILnet/minecraft/block/state/IBlockState;)V @4: aload
  Reason:
    Exceeded max stack size.
  Current Frame:
    bci: @4
    flags: { }
    locals: { 'net/minecraft/world/chunk/ChunkPrimer', integer, integer, integer, 'net/minecraft/block/state/IBlockState' }
    stack: { 'net/minecraft/world/chunk/ChunkPrimer', integer, integer, integer }
  Bytecode:
    0x0000000: 2a1b 1c1d 1904 b800 26b1               

	at net.minecraft.world.gen.ChunkGeneratorOverworld.func_185932_a(ChunkGeneratorOverworld.java:204)
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:143)
	at net.minecraft.world.World.func_72964_e(World.java:310)
	at net.minecraft.world.World.func_175726_f(World.java:305)
	at net.minecraft.world.World.func_180495_p(World.java:911)
	at net.minecraft.world.World.func_190529_b(World.java:581)
	at net.minecraft.world.World.func_190522_c(World.java:484)
	at net.minecraft.world.World.markAndNotifyBlock(World.java:390)
	at net.minecraft.world.World.func_180501_a(World.java:361)
	at net.minecraft.world.gen.feature.WorldGenMinable.func_180709_b(WorldGenMinable.java:79)
	at com.brandon3055.draconicevolution.world.DEWorldGenHandler.addOreSpawn(DEWorldGenHandler.java:114)
	at com.brandon3055.draconicevolution.world.DEWorldGenHandler.addOreGen(DEWorldGenHandler.java:60)
	at com.brandon3055.draconicevolution.world.WorldTickHandler.tickEnd(WorldTickHandler.java:48)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler_1892_WorldTickHandler_tickEnd_WorldTickEvent.invoke(.dynamic)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:90)
	at net.minecraftforge.fml.common.eventhandler.EventBus.post(EventBus.java:182)
	at net.minecraftforge.fml.common.FMLCommonHandler.onPostWorldTick(FMLCommonHandler.java:274)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:776)
	at net.minecraft.server.dedicated.DedicatedServer.func_71190_q(DedicatedServer.java:397)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:668)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:526)
	at java.lang.Thread.run(Thread.java:748)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Server thread
Stacktrace:
	at net.minecraft.world.gen.ChunkGeneratorOverworld.func_185932_a(ChunkGeneratorOverworld.java:204)

-- Chunk to be generated --
Details:
	Location: 6,28
	Position hash: 120259084294
	Generator: net.minecraft.world.gen.ChunkGeneratorOverworld@494d603c
Stacktrace:
	at net.minecraft.world.gen.ChunkProviderServer.func_186025_d(ChunkProviderServer.java:143)
	at net.minecraft.world.World.func_72964_e(World.java:310)
	at net.minecraft.world.World.func_175726_f(World.java:305)
	at net.minecraft.world.World.func_180495_p(World.java:911)
	at net.minecraft.world.World.func_190529_b(World.java:581)
	at net.minecraft.world.World.func_190522_c(World.java:484)
	at net.minecraft.world.World.markAndNotifyBlock(World.java:390)
	at net.minecraft.world.World.func_180501_a(World.java:361)
	at net.minecraft.world.gen.feature.WorldGenMinable.func_180709_b(WorldGenMinable.java:79)
	at com.brandon3055.draconicevolution.world.DEWorldGenHandler.addOreSpawn(DEWorldGenHandler.java:114)
	at com.brandon3055.draconicevolution.world.DEWorldGenHandler.addOreGen(DEWorldGenHandler.java:60)
	at com.brandon3055.draconicevolution.world.WorldTickHandler.tickEnd(WorldTickHandler.java:48)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler_1892_WorldTickHandler_tickEnd_WorldTickEvent.invoke(.dynamic)
	at net.minecraftforge.fml.common.eventhandler.ASMEventHandler.invoke(ASMEventHandler.java:90)
	at net.minecraftforge.fml.common.eventhandler.EventBus.post(EventBus.java:182)
	at net.minecraftforge.fml.common.FMLCommonHandler.onPostWorldTick(FMLCommonHandler.java:274)
	at net.minecraft.server.MinecraftServer.func_71190_q(MinecraftServer.java:776)
	at net.minecraft.server.dedicated.DedicatedServer.func_71190_q(DedicatedServer.java:397)
	at net.minecraft.server.MinecraftServer.func_71217_p(MinecraftServer.java:668)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:526)
	at java.lang.Thread.run(Thread.java:748)

-- System Details --
Details:
	Minecraft Version: 1.12.2
	Operating System: Linux (amd64) version 3.16.0-6-amd64
	Java Version: 1.8.0_131, Oracle Corporation
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 19205771024 bytes (18316 MB) / 22441623552 bytes (21402 MB) up to 22441623552 bytes (21402 MB)
	JVM Flags: 2 total; -Xmx22000M -Xms22000M
	IntCache: cache: 0, tcache: 0, allocated: 13, tallocated: 95
	FML: MCP 9.42 Powered by Forge 14.23.4.2765 279 mods loaded, 279 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored

	| State     | ID                                   | Version                         | Source                                                    | Signature                                |
	|:--------- |:------------------------------------ |:------------------------------- |:--------------------------------------------------------- |:---------------------------------------- |
	| UCHIJAAAA | minecraft                            | 1.12.2                          | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | mcp                                  | 9.42                            | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | FML                                  | 8.0.99.99                       | forge-1.12.2-14.23.4.2765-universal.jar                   | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | forge                                | 14.23.4.2765                    | forge-1.12.2-14.23.4.2765-universal.jar                   | e3c3d50c7c986df74c645c0ac54639741c90a557 |
	| UCHIJAAAA | openmodscore                         | 0.11.5                          | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | foamfixcore                          | 7.7.4                           | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | opencomputers|core                   | 1.7.2.67                        | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | randompatches                        | 1.12.2-1.5.0.4                  | randompatches-1.12.2-1.5.0.4.jar                          | None                                     |
	| UCHIJAAAA | elucore                              | 1.0                             | minecraft.jar                                             | None                                     |
	| UCHIJAAAA | crafttweaker                         | 4.1.9                           | CraftTweaker2-1.12-4.1.9.jar                              | None                                     |
	| UCHIJAAAA | mtlib                                | 3.0.5                           | MTLib-3.0.5.jar                                           | None                                     |
	| UCHIJAAAA | modtweaker                           | 4.0.13                          | modtweaker-4.0.14.jar                                     | None                                     |
	| UCHIJAAAA | jei                                  | 4.12.0.216                      | jei_1.12.2-4.12.0.216.jar                                 | None                                     |
	| UCHIJAAAA | abyssalcraft                         | 1.9.4.12                        | AbyssalCraft-1.12.2-1.9.4.12.jar                          | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
	| UCHIJAAAA | chisel                               | MC1.12.2-0.2.1.34               | Chisel-MC1.12.2-0.2.1.34.jar                              | None                                     |
	| UCHIJAAAA | baubles                              | 1.5.2                           | Baubles-1.12-1.5.2.jar                                    | None                                     |
	| UCHIJAAAA | endercore                            | 1.12.2-0.5.37                   | EnderCore-1.12.2-0.5.37.jar                               | None                                     |
	| UCHIJAAAA | thaumcraft                           | 6.1.BETA24                      | Thaumcraft-1.12.2-6.1.BETA24.jar                          | None                                     |
	| UCHIJAAAA | codechickenlib                       | 3.2.1.351                       | CodeChickenLib-1.12.2-3.2.1.351-universal.jar             | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | redstoneflux                         | 2.0.2                           | RedstoneFlux-1.12-2.0.2.3-universal.jar                   | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | cofhcore                             | 4.5.3                           | CoFHCore-1.12.2-4.5.3.20-universal.jar                    | None                                     |
	| UCHIJAAAA | brandonscore                         | 2.4.4                           | BrandonsCore-1.12.2-2.4.4.173-universal.jar               | None                                     |
	| UCHIJAAAA | cofhworld                            | 1.2.0                           | CoFHWorld-1.12.2-1.2.0.5-universal.jar                    | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | thermalfoundation                    | 2.5.0                           | ThermalFoundation-1.12.2-2.5.0.19-universal.jar           | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | draconicevolution                    | 2.3.13                          | Draconic-Evolution-1.12.2-2.3.13.306-universal.jar        | None                                     |
	| UCHIJAAAA | thermalexpansion                     | 5.5.0                           | ThermalExpansion-1.12.2-5.5.0.29-universal.jar            | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | enderio                              | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderiointegrationtic                | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | mantle                               | 1.12-1.3.2.24                   | Mantle-1.12-1.3.2.24.jar                                  | None                                     |
	| UCHIJAAAA | twilightforest                       | 3.8.654                         | twilightforest-1.12.2-3.8.654-universal.jar               | None                                     |
	| UCHIJAAAA | tconstruct                           | 1.12.2-2.10.1.87                | TConstruct-1.12.2-2.10.1.87.jar                           | None                                     |
	| UCHIJAAAA | acintegration                        | 1.6.6                           | AbyssalCraft Integration-1.12.2-1.6.6.jar                 | 220f10d3a93b3ff5fbaa7434cc629d863d6751b9 |
	| UCHIJAAAA | fastbench                            | 1.5.3                           | FastWorkbench-1.12.2-1.5.3.jar                            | None                                     |
	| UCHIJAAAA | actuallyadditions                    | 1.12.2-r140                     | ActuallyAdditions-1.12.2-r140.jar                         | None                                     |
	| UCHIJAAAA | actuallybaubles                      | 1.1                             | ActuallyBaubles-1.12-1.1.jar                              | None                                     |
	| UCHIJAAAA | additionalbanners                    | 1.1.42                          | AdditionalBanners-1.12.2-1.1.42.jar                       | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | ic2                                  | 2.8.99-ex112                    | industrialcraft-2-2.8.99-ex112.jar                        | de041f9f6187debbc77034a344134053277aa3b0 |
	| UCHIJAAAA | libvulpes                            | 0.2.8.-37                       | LibVulpes-1.12.2-0.2.8-37-universal.jar                   | None                                     |
	| UCHIJAAAA | advancedrocketry                     | 1.4.0.-101                      | AdvancedRocketry-1.12.2-1.4.0-101-universal.jar           | None                                     |
	| UCHIJAAAA | appliedenergistics2                  | rv5-stable-11                   | appliedenergistics2-rv5-stable-11.jar                     | None                                     |
	| UCHIJAAAA | bdlib                                | 1.14.3.12                       | bdlib-1.14.3.12-mc1.12.2.jar                              | None                                     |
	| UCHIJAAAA | ae2stuff                             | 0.7.0.4                         | ae2stuff-0.7.0.4-mc1.12.2.jar                             | None                                     |
	| UCHIJAAAA | aiimprovements                       | 0.0.1.1                         | AIImprovements-1.12.1-0.0.1b1.jar                         | None                                     |
	| UCHIJAAAA | akashictome                          | 1.2-10                          | AkashicTome-1.2-10.jar                                    | None                                     |
	| UCHIJAAAA | extrautils2                          | 1.0                             | extrautils2-1.12-1.9.2.jar                                | None                                     |
	| UCHIJAAAA | flyringbaublemod                     | 0.3.1_1.12-d4e654e              | angelRingToBauble-1.12-0.3.1.50+d4e654e.jar               | None                                     |
	| UCHIJAAAA | applecore                            | 3.1.4                           | AppleCore-mc1.12.2-3.1.4.jar                              | None                                     |
	| UCHIJAAAA | appleskin                            | 1.0.9                           | AppleSkin-mc1.12-1.0.9.jar                                | None                                     |
	| UCHIJAAAA | botania                              | r1.10-356                       | Botania r1.10-356.jar                                     | None                                     |
	| UCHIJAAAA | conarm                               | 1.1.1                           | conarm-1.12.2-1.1.1.jar                                   | 5d5b8aee896a4f5ea3f3114784742662a67ad32f |
	| UCHIJAAAA | biomesoplenty                        | 7.0.1.2399                      | BiomesOPlenty-1.12.2-7.0.1.2399-universal.jar             | None                                     |
	| UCHIJAAAA | natura                               | 1.12.2-4.3.2.62                 | natura-1.12.2-4.3.2.62.jar                                | None                                     |
	| UCHIJAAAA | reborncore                           | 3.10.0.332                      | RebornCore-1.12.2-3.10.0.332-universal.jar                | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| UCHIJAAAA | techreborn                           | 2.17.3.815                      | TechReborn-1.12.2-2.17.3.815-universal.jar                | 8727a3141c8ec7f173b87aa78b9b9807867c4e6b |
	| UCHIJAAAA | forestry                             | 5.8.1.341                       | forestry_1.12.2-5.8.1.341.jar                             | None                                     |
	| UCHIJAAAA | theoneprobe                          | 1.4.24                          | theoneprobe-1.12-1.4.24.jar                               | None                                     |
	| UCHIJAAAA | immersiveengineering                 | 0.12-85                         | ImmersiveEngineering-0.12-85.jar                          | 4cb49fcde3b43048c9889e0a3d083225da926334 |
	| UCHIJAAAA | immersivepetroleum                   | 1.1.9                           | immersivepetroleum-1.12.2-1.1.9.jar                       | None                                     |
	| UCHIJAAAA | forgelin                             | 1.7.4                           | Forgelin-1.7.4.jar                                        | None                                     |
	| UCHIJAAAA | computercraft                        | 1.80pr1                         | ComputerCraft1.80pr1.jar                                  | None                                     |
	| UCHIJAAAA | mcmultipart                          | 2.5.3                           | MCMultiPart-2.5.3.jar                                     | None                                     |
	| UCHIJAAAA | mekanism                             | 1.12.2-9.4.13.349               | Mekanism-1.12.2-9.4.13.349.jar                            | None                                     |
	| UCHIJAAAA | teslacorelib                         | 1.0.15                          | tesla-core-lib-1.12.2-1.0.15.jar                          | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | industrialforegoing                  | 1.12.2-1.12.2                   | industrialforegoing-1.12.2-1.11.2-212.jar                 | None                                     |
	| UCHIJAAAA | cucumber                             | 1.1.1                           | Cucumber-1.12.2-1.1.1.jar                                 | None                                     |
	| UCHIJAAAA | mysticalagriculture                  | 1.6.13                          | MysticalAgriculture-1.12-1.6.13.jar                       | None                                     |
	| UCHIJAAAA | mysticalagradditions                 | 1.2.8                           | mysticalagradditions-1.12-1.2.8.jar                       | None                                     |
	| UCHIJAAAA | harvestcraft                         | 1.12.2z                         | Pam's HarvestCraft 1.12.2z.jar                            | None                                     |
	| UCHIJAAAA | mcjtylib_ng                          | 3.0.5                           | mcjtylib-1.12-3.0.5.jar                                   | None                                     |
	| UCHIJAAAA | rftools                              | 7.56                            | rftools-1.12-7.56.jar                                     | None                                     |
	| UCHIJAAAA | rustic                               | 1.0.9                           | rustic-1.0.9.jar                                          | None                                     |
	| UCHIJAAAA | integrationforegoing                 | 1.12.2-1.7.4                    | IntegrationForegoing-1.12.2-1.7.4.jar                     | 4ffa87db52cf086d00ecc4853a929367b1c39b5c |
	| UCHIJAAAA | valkyrielib                          | 1.12.2-2.0.15.1                 | valkyrielib-1.12.2-2.0.15.1.jar                           | None                                     |
	| UCHIJAAAA | environmentaltech                    | 1.12.2-2.0.15.1                 | environmentaltech-1.12.2-2.0.15.1.jar                     | None                                     |
	| UCHIJAAAA | forgemultipartcbe                    | 2.5.0.71                        | ForgeMultipart-1.12.2-2.5.0.71-universal.jar              | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | mrtjpcore                            | 2.1.3.35                        | MrTJPCore-1.12.2-2.1.3.35-universal.jar                   | None                                     |
	| UCHIJAAAA | projectred-core                      | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-Base.jar                       | None                                     |
	| UCHIJAAAA | projectred-exploration               | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-world.jar                      | None                                     |
	| UCHIJAAAA | psi                                  | r1.1-59                         | Psi-r1.1-59.jar                                           | None                                     |
	| UCHIJAAAA | plustic                              | 6.5.2.0                         | plustic-6.5.2.0.jar                                       | None                                     |
	| UCHIJAAAA | armoryexpansion                      | 0.1.4                           | armoryexpansion-0.1.4.jar                                 | None                                     |
	| UCHIJAAAA | aroma1997core                        | 2.0.0.0.b156                    | Aroma1997Core-1.12.2-2.0.0.0.b156.jar                     | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | aroma1997sdimension                  | 2.0.0.2.b81                     | Aroma1997s-Dimensional-World-1.12.2-2.0.0.2.b81.jar       | dfbfe4c473253d8c5652417689848f650b2cbe32 |
	| UCHIJAAAA | astralsorcery                        | 1.9.4                           | astralsorcery-1.12.2-1.9.4.jar                            | a0f0b759d895c15ceb3e3bcb5f3c2db7c582edf0 |
	| UCHIJAAAA | atmtweaks                            | 1.2                             | atmtweaks-1.2.jar                                         | None                                     |
	| UCHIJAAAA | morphtool                            | 1.2-16                          | Morph-o-Tool-1.2-16.jar                                   | None                                     |
	| UCHIJAAAA | quark                                | r1.5-129                        | Quark-r1.5-129.jar                                        | None                                     |
	| UCHIJAAAA | autoreglib                           | 1.3-20                          | AutoRegLib-1.3-20.jar                                     | None                                     |
	| UCHIJAAAA | badwithernocookiereloaded            | 1.12.2-3.1.14                   | badwithernocookiereloaded-1.12.2-3.1.14.jar               | None                                     |
	| UCHIJAAAA | bedpatch                             | 2.2                             | bedpatch-2.2-1.12.2.jar                                   | 6bf7527e690fb5e8719b9832bce5000a3e87dfe6 |
	| UCHIJAAAA | betterbuilderswands                  | 0.11.1                          | BetterBuildersWands-1.12-0.11.1.245+69d0d70.jar           | None                                     |
	| UCHIJAAAA | bibliocraft                          | 2.4.5                           | BiblioCraft[v2.4.5][MC1.12.2].jar                         | None                                     |
	| UCHIJAAAA | binniecore                           | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | binniedesign                         | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | genetics                             | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | botany                               | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | extrabees                            | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | extratrees                           | 2.5.0.168                       | binnie-mods-1.12.2-2.5.0.168.jar                          | None                                     |
	| UCHIJAAAA | blockcraftery                        | 0.1.3                           | blockcraftery-0.1.3.jar                                   | None                                     |
	| UCHIJAAAA | blooddebug                           | 0.0.1.-9                        | BloodDebug-1.12.2-0.0.1-9.jar                             | None                                     |
	| UCHIJAAAA | cyclicmagic                          | 1.16.10                         | Cyclic-1.12.2-1.16.10.jar                                 | 1bc8f8dbe770187a854cef35dad0ff40ba441bbe |
	| UCHIJAAAA | kjlib                                | 1.0.4                           | kjlib-1.0.4.jar                                           | None                                     |
	| UCHIJAAAA | inventorygenerators                  | 1.2.2                           | inventorygenerators-1.2.2.jar                             | None                                     |
	| UCHIJAAAA | mobtotems                            | 1.12.1-0.3.0                    | mobtotems-1.12.1-0.3.0.jar                                | None                                     |
	| UCHIJAAAA | guideapi                             | 1.12-2.1.6-61                   | Guide-API-1.12-2.1.6-61.jar                               | None                                     |
	| UCHIJAAAA | bloodmagic                           | 1.12.2-2.3.3-101                | BloodMagic-1.12.2-2.3.3-101.jar                           | None                                     |
	| UCHIJAAAA | bookshelf                            | 2.3.553                         | Bookshelf-1.12.2-2.3.553.jar                              | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | careerbees                           | 1.0                             | careerbees-0.4.0.jar                                      | None                                     |
	| UCHIJAAAA | ceramics                             | 1.12-1.3.4                      | Ceramics-1.12-1.3.4.jar                                   | None                                     |
	| UCHIJAAAA | chameleon                            | 1.12-4.1.3                      | Chameleon-1.12-4.1.3.jar                                  | None                                     |
	| UCHIJAAAA | chiselsandbits                       | 14.23                           | chiselsandbits-14.23.jar                                  | None                                     |
	| UCHIJAAAA | cyclopscore                          | 0.11.10                         | CyclopsCore-1.12.2-0.11.10.jar                            | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | colossalchests                       | 1.6.11                          | ColossalChests-1.12.2-1.6.11.jar                          | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | commoncapabilities                   | 1.4.0                           | CommonCapabilities-1.12-1.4.0.jar                         | None                                     |
	| UCHIJAAAA | refinedstorage                       | 1.6.5                           | refinedstorage-1.6.5.jar                                  | 57893d5b90a7336e8c63fe1c1e1ce472c3d59578 |
	| UCHIJAAAA | compactmachines3                     | 3.0.12                          | compactmachines3-1.12.2-3.0.12-b215.jar                   | None                                     |
	| UCHIJAAAA | compactsolars                        | 1.12.2-5.0.17.340               | CompactSolars-1.12.2-5.0.17.340-universal.jar             | None                                     |
	| UCHIJAAAA | asielib                              | 1.0.0                           | Computronics-1.12.1-1.6.5.jar                             | None                                     |
	| UCHIJAAAA | opencomputers                        | 1.7.2.67                        | OpenComputers-MC1.12.2-1.7.2.67.jar                       | None                                     |
	| UCHIJAAAA | computronics                         | 1.6.5                           | Computronics-1.12.1-1.6.5.jar                             | None                                     |
	| UCHIJAAAA | cookingforblockheads                 | 6.4.44                          | CookingForBlockheads_1.12.2-6.4.44.jar                    | None                                     |
	| UCHIJAAAA | cosmeticarmorreworked                | 1.12.2-v3                       | CosmeticArmorReworked-1.12.2-v3.jar                       | aaaf83332a11df02406e9f266b1b65c1306f0f76 |
	| UCHIJAAAA | tombmanygraves2api                   | 1.12.2-1.0.0                    | tombmanygraves2api-1.12.2-1.0.0.jar                       | None                                     |
	| UCHIJAAAA | tombmanygraves                       | 1.12-4.1.0                      | TombManyGraves-1.12-4.1.0.jar                             | None                                     |
	| UCHIJAAAA | cosmeticarmorreworked|tombmanygraves | 1.12.2-v3                       | CosmeticArmorReworked-1.12.2-v3.jar                       | aaaf83332a11df02406e9f266b1b65c1306f0f76 |
	| UCHIJAAAA | craftingtweaks                       | 8.1.9                           | CraftingTweaks_1.12.2-8.1.9.jar                           | None                                     |
	| UCHIJAAAA | crafttweakerjei                      | 2.0.2                           | CraftTweaker2-1.12-4.1.9.jar                              | None                                     |
	| UCHIJAAAA | darkutils                            | 1.8.211                         | DarkUtils-1.12.2-1.8.211.jar                              | d476d1b22b218a10d845928d1665d45fce301b27 |
	| UCHIJAAAA | defaultworldgenerator-port           | 1.12-2.3                        | DefaultWorldGenerator-port-1.12-2.3.jar                   | None                                     |
	| UCHIJAAAA | diethopper                           | 1.1                             | diethopper-1.1.jar                                        | None                                     |
	| UCHIJAAAA | dismantler                           | 0.1.2                           | dismantler-0.1.2.jar                                      | None                                     |
	| UCHIJAAAA | dldungeonsjdg                        | 1.11.1                          | DoomlikeDungeons-1.11.1-MC1.12.2.jar                      | None                                     |
	| UCHIJAAAA | embers                               | 0.230                           | embers-0.230.jar                                          | None                                     |
	| UCHIJAAAA | enderiobase                          | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderioconduits                      | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderioconduitsappliedenergistics    | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderioconduitsopencomputers         | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderioconduitsrefinedstorage        | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderiointegrationforestry           | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderiointegrationticlate            | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | ftblib                               | 5.3.0.51                        | FTBLib-5.3.0.51.jar                                       | None                                     |
	| UCHIJAAAA | enderiomachines                      | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderiopowertools                    | 5.0.31                          | EnderIO-1.12.2-5.0.31.jar                                 | None                                     |
	| UCHIJAAAA | enderstorage                         | 2.4.5.135                       | EnderStorage-1.12.2-2.4.5.135-universal.jar               | f1850c39b2516232a2108a7bd84d1cb5df93b261 |
	| UCHIJAAAA | exchangers                           | 1.12.2-2.7.3                    | Exchangers-1.12.2-2.7.3.jar                               | 4ffa87db52cf086d00ecc4853a929367b1c39b5c |
	| UCHIJAAAA | excore                               | 2.0.0-beta19-1.12.2             | EXCore-2.0.0-beta19-1.12.2.jar                            | None                                     |
	| UCHIJAAAA | extracells                           | 2.5.13                          | ExtraCells-1.12.2-2.5.13a60.jar                           | None                                     |
	| UCHIJAAAA | shadowmc                             | 3.8.0                           | ShadowMC-1.12-3.8.0.jar                                   | None                                     |
	| UCHIJAAAA | extrarails                           | 1.3.0                           | ExtraRails-1.12-1.3.0.jar                                 | None                                     |
	| UCHIJAAAA | zerocore                             | 1.12-0.1.2.2                    | zerocore-1.12-0.1.2.2.jar                                 | None                                     |
	| UCHIJAAAA | bigreactors                          | 1.12.2-0.4.5.49                 | ExtremeReactors-1.12.2-0.4.5.49.jar                       | None                                     |
	| UCHIJAAAA | fairylights                          | 2.1.3                           | fairylights-2.1.3-1.12.2.jar                              | None                                     |
	| UCHIJAAAA | fencejumper                          | 1.0.5                           | fencejumper-1.12-1.0.5.jar                                | None                                     |
	| UCHIJAAAA | flamingo                             | 1.12-1.11                       | Flamingo-1.12-v1.11.jar                                   | None                                     |
	| UCHIJAAAA | flatcoloredblocks                    | mc1.12-6.6                      | flatcoloredblocks-mc1.12-6.6.jar                          | None                                     |
	| UCHIJAAAA | foamfix                              | 0.10.1-1.12.2                   | foamfix-0.10.1-1.12.2.jar                                 | None                                     |
	| UCHIJAAAA | microblockcbe                        | 2.5.0.71                        | ForgeMultipart-1.12.2-2.5.0.71-universal.jar              | None                                     |
	| UCHIJAAAA | minecraftmultipartcbe                | 2.5.0.71                        | ForgeMultipart-1.12.2-2.5.0.71-universal.jar              | None                                     |
	| UCHIJAAAA | ftbutilities                         | 5.3.0.50                        | FTBUtilities-5.3.0.50.jar                                 | None                                     |
	| UCHIJAAAA | funkylocomotion                      | 1.0                             | funky-locomotion-1.12.2-1.1.2.jar                         | None                                     |
	| UCHIJAAAA | gendustry                            | 1.6.5.8                         | gendustry-1.6.5.8-mc1.12.2.jar                            | None                                     |
	| UCHIJAAAA | pressure                             | 1.3.1.9                         | pressure-1.3.1.9-mc1.12.2.jar                             | None                                     |
	| UCHIJAAAA | advgenerators                        | 0.9.20.12                       | generators-0.9.20.12-mc1.12.2.jar                         | None                                     |
	| UCHIJAAAA | helpfixer                            | 1.12.1-1.5.18                   | HelpFixer-1.12.1-1.5.18.jar                               | None                                     |
	| UCHIJAAAA | ichunutil                            | 7.1.4                           | iChunUtil-1.12.2-7.1.4.jar                                | None                                     |
	| UCHIJAAAA | immersivetech                        | 1.3.10                          | immersivetech-1.12-1.3.10.jar                             | None                                     |
	| UCHIJAAAA | initialinventory                     | 2.0.2                           | InitialInventory-3.0.0.jar                                | None                                     |
	| UCHIJAAAA | integrateddynamics                   | 0.11.17                         | IntegratedDynamics-1.12.2-0.11.17.jar                     | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | integrateddynamicscompat             | 1.0.0                           | IntegratedDynamics-1.12.2-0.11.17.jar                     | None                                     |
	| UCHIJAAAA | integratedtunnels                    | 1.5.6                           | IntegratedTunnels-1.12.2-1.5.6.jar                        | bd0353b3e8a2810d60dd584e256e364bc3bedd44 |
	| UCHIJAAAA | integratedtunnelscompat              | 1.0.0                           | IntegratedTunnels-1.12.2-1.5.6.jar                        | None                                     |
	| UCHIJAAAA | inventorytweaks                      | 1.64-dev+release.110.b4fac73    | InventoryTweaks-1.64-dev.jar                              | 55d2cd4f5f0961410bf7b91ef6c6bf00a766dcbe |
	| UCHIJAAAA | ironbackpacks                        | 1.12.2-3.0.8-12                 | IronBackpacks-1.12.2-3.0.8-12.jar                         | None                                     |
	| UCHIJAAAA | ironchest                            | 1.12.2-7.0.46.831               | ironchest-1.12.2-7.0.46.831.jar                           | None                                     |
	| UCHIJAAAA | jaopca                               | 1.12.2-2.2.8.91                 | JAOPCA-1.12.2-2.2.8.91.jar                                | None                                     |
	| UCHIJAAAA | oredictinit                          | 1.12.2-2.2.1.68                 | JAOPCA-1.12.2-2.2.8.91.jar                                | None                                     |
	| UCHIJAAAA | jaopcaadditions                      | 1.12.2-2.2.1.9                  | JAOPCAAdditions-1.12.2-2.2.1.9.jar                        | None                                     |
	| UCHIJAAAA | jeibees                              | 0.9.0.5                         | jeibees-0.9.0.5-mc1.12.2.jar                              | None                                     |
	| UCHIJAAAA | journeymap                           | 1.12.2-5.5.2                    | journeymap-1.12.2-5.5.2.jar                               | None                                     |
	| UCHIJAAAA | jmfixer                              | 1                               | JourneyMapFixer-1.12.2-1-SERVER.jar                       | None                                     |
	| UCHIJAAAA | justenoughdimensions                 | 1.6.0-dev.20180913.002135       | justenoughdimensions-1.12.2-1.6.0-dev.20180913.002135.jar | 2b03e1423915a189b8094816baa18f239d576dff |
	| UCHIJAAAA | kleeslabs                            | 5.4.11                          | KleeSlabs_1.12.2-5.4.11.jar                               | None                                     |
	| UCHIJAAAA | librarianlib                         | 4.15                            | librarianlib-1.12.2-4.15.jar                              | None                                     |
	| UCHIJAAAA | lostcities                           | 2.0.11                          | lostcities-1.12-2.0.11.jar                                | None                                     |
	| UCHIJAAAA | lostsouls                            | 1.1.4                           | lostsouls-1.12-1.1.4.jar                                  | None                                     |
	| UCHIJAAAA | magipsi                              | 1.3                             | MagicalPsi-1.3.jar                                        | None                                     |
	| UCHIJAAAA | magicbees                            | 1.0                             | MagicBees-1.12.2-3.1.10.jar                               | None                                     |
	| UCHIJAAAA | malisiscore                          | 1.12.2-6.4.0                    | malisiscore-1.12.2-6.4.0.jar                              | None                                     |
	| UCHIJAAAA | malisisdoors                         | 1.12.2-7.3.0                    | malisisdoors-1.12.2-7.3.0.jar                             | None                                     |
	| UCHIJAAAA | mekanismgenerators                   | 9.4.11                          | MekanismGenerators-1.12.2-9.4.13.349.jar                  | None                                     |
	| UCHIJAAAA | mekanismtools                        | 9.4.11                          | MekanismTools-1.12.2-9.4.13.349.jar                       | None                                     |
	| UCHIJAAAA | minecolonies                         | 1.12.2-0.9.127-ALPHA            | minecolonies-1.12.2-0.9.127-ALPHA-universal.jar           | None                                     |
	| UCHIJAAAA | morpheus                             | 1.12-3.3.2                      | Morpheus-1.12-3.3.2.jar                                   | None                                     |
	| UCHIJAAAA | naturescompass                       | 1.5.1                           | NaturesCompass-1.12.2-1.5.1.jar                           | None                                     |
	| UCHIJAAAA | nmsot                                | 1.2.2-mc1.12.2                  | NoMobSpawningOnTrees-1.2.2-mc1.12.2.jar                   | None                                     |
	| UCHIJAAAA | neid                                 | 1.5.4.2                         | NotEnoughIDs-1.5.4.2.jar                                  | None                                     |
	| UCHIJAAAA | notenoughwands                       | 1.7.1                           | notenoughwands-1.12-1.7.1.jar                             | None                                     |
	| UCHIJAAAA | nuclearcraft                         | 2.11g                           | NuclearCraft-2.11g--1.12.2.jar                            | None                                     |
	| UCHIJAAAA | nutrition                            | 3.5.0                           | Nutrition-1.12.2-3.5.0.jar                                | None                                     |
	| UCHIJAAAA | xnet                                 | 1.7.4                           | xnet-1.12-1.7.4.jar                                       | None                                     |
	| UCHIJAAAA | ocxnetdriver                         | 1.0.2                           | ocxnetdriver-1.0.2-b11.jar                                | None                                     |
	| UCHIJAAAA | oreexcavation                        | 1.4.129                         | OreExcavation-1.4.129.jar                                 | None                                     |
	| UCHIJAAAA | oeintegration                        | 2.3.3                           | oeintegration-2.3.3.jar                                   | None                                     |
	| UCHIJAAAA | openmods                             | 0.11.5                          | OpenModsLib-1.12.2-0.11.5.jar                             | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
	| UCHIJAAAA | openblocks                           | 1.7.6                           | OpenBlocks-1.12.2-1.7.6.jar                               | d2a9a8e8440196e26a268d1f3ddc01b2e9c572a5 |
	| UCHIJAAAA | overloaded                           | 0.0.53                          | Overloaded-1.12.2-0.0.53.jar                              | 644f38521a349310a5dae0239577dc7beebefaec |
	| UCHIJAAAA | p455w0rdslib                         | 2.0.35                          | p455w0rdslib-1.12-2.0.35.jar                              | None                                     |
	| UCHIJAAAA | packmode                             | 1.2.0                           | packmode-1.12.2-1.2.0.jar                                 | None                                     |
	| UCHIJAAAA | pamscookables                        | 1.1                             | pamscookables-1.1.jar                                     | None                                     |
	| UCHIJAAAA | parry                                | 1.0                             | parry-1.0-hotfix.jar                                      | None                                     |
	| UCHIJAAAA | placebo                              | 1.4.1                           | Placebo-1.12.2-1.4.1.jar                                  | None                                     |
	| UCHIJAAAA | plants2                              | 2.10.3                          | Plants-1.12.2-2.10.3.jar                                  | None                                     |
	| UCHIJAAAA | shetiphiancore                       | 3.5.8                           | shetiphiancore-1.12.0-3.5.8.jar                           | None                                     |
	| UCHIJAAAA | platforms                            | 1.4.6                           | platforms-1.12.0-1.4.6.jar                                | None                                     |
	| UCHIJAAAA | pneumaticcraft                       | 1.12.2-0.7.8-259                | pneumaticcraft-repressurized-1.12.2-0.7.8-259.jar         | None                                     |
	| UCHIJAAAA | portalgun                            | 7.0.2                           | PortalGun-1.12.2-7.0.2.jar                                | None                                     |
	| UCHIJAAAA | portality                            | 1.0-SNAPSHOT                    | portality-1.12.2-1.0.4-6.jar                              | None                                     |
	| UCHIJAAAA | sonarcore                            | 5.0.15                          | sonarcore-1.12.2-5.0.15-13.jar                            | None                                     |
	| UCHIJAAAA | practicallogistics2                  | 3.0.4                           | practicallogistics2-1.12.2-3.0.4.jar                      | None                                     |
	| UCHIJAAAA | projectred-compat                    | 1.0                             | ProjectRed-1.12.2-4.9.1.92-compat.jar                     | None                                     |
	| UCHIJAAAA | projectred-integration               | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-integration.jar                | None                                     |
	| UCHIJAAAA | projectred-transmission              | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-integration.jar                | None                                     |
	| UCHIJAAAA | projectred-fabrication               | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-fabrication.jar                | None                                     |
	| UCHIJAAAA | projectred-illumination              | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-lighting.jar                   | None                                     |
	| UCHIJAAAA | projectred-expansion                 | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-mechanical.jar                 | None                                     |
	| UCHIJAAAA | projectred-relocation                | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-mechanical.jar                 | None                                     |
	| UCHIJAAAA | projectred-transportation            | 4.9.1.92                        | ProjectRed-1.12.2-4.9.1.92-mechanical.jar                 | None                                     |
	| UCHIJAAAA | quantumstorage                       | 4.6.2                           | QuantumStorage-1.12-4.6.2.jar                             | None                                     |
	| UCHIJAAAA | quickleafdecay                       | 1.2.4                           | QuickLeafDecay-MC1.12.1-1.2.4.jar                         | None                                     |
	| UCHIJAAAA | rangedpumps                          | 0.5                             | rangedpumps-0.5.jar                                       | None                                     |
	| UCHIJAAAA | realfilingcabinet                    | 0.1.65                          | realfilingcabinet-1.12.1-0.1.65.jar                       | None                                     |
	| UCHIJAAAA | rebornstorage                        | 1.0.0                           | RebornStorage-1.12.2-3.2.2.65.jar                         | None                                     |
	| UCHIJAAAA | redstonearsenal                      | 2.5.1                           | RedstoneArsenal-1.12.2-2.5.1.13-universal.jar             | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | refinedstorageaddons                 | 0.4.2                           | refinedstorageaddons-0.4.2.jar                            | None                                     |
	| UCHIJAAAA | xreliquary                           | 1.12.2-1.3.4.767                | Reliquary-1.12.2-1.3.4.767.jar                            | None                                     |
	| UCHIJAAAA | rftoolscontrol                       | 1.9.1                           | rftoolsctrl-1.12-1.9.1.jar                                | None                                     |
	| UCHIJAAAA | rftoolsdim                           | 5.61                            | rftoolsdim-1.12-5.61.jar                                  | None                                     |
	| UCHIJAAAA | rftoolspower                         | 1.1.1                           | rftoolspower-1.12-1.1.1.jar                               | None                                     |
	| UCHIJAAAA | roots                                | 0.104                           | roots-2-0.104.jar                                         | None                                     |
	| UCHIJAAAA | sampler                              | 1.73                            | sampler-1.73.jar                                          | None                                     |
	| UCHIJAAAA | woodenshears                         | @MAJOR@.@MINOR@.@REVIS@.@BUILD@ | SBM-WoodenShears-1.12-0.0.1b8.jar                         | None                                     |
	| UCHIJAAAA | thermaldynamics                      | 2.5.1                           | ThermalDynamics-1.12.2-2.5.1.14-universal.jar             | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | simplyjetpacks                       | 2.2.7.45                        | SimplyJetpacks2-1.12.2-2.2.7.45.jar                       | None                                     |
	| UCHIJAAAA | slimyboyos                           | 1.0.0                           | SlimyBoyos-1.0.0.jar                                      | None                                     |
	| UCHIJAAAA | soulshardstow                        | 1.12-2.7.6-56                   | SoulShards-TOW-1.12-2.7.6-56.jar                          | None                                     |
	| UCHIJAAAA | stevescarts                          | 2.4.23.115                      | StevesCarts-1.12.2-2.4.23.115.jar                         | None                                     |
	| UCHIJAAAA | storagedrawers                       | 1.12-5.3.5                      | StorageDrawers-1.12.2-5.3.7.jar                           | None                                     |
	| UCHIJAAAA | storagedrawersextra                  | @VERSION@                       | StorageDrawersExtras-1.12-3.1.0.jar                       | None                                     |
	| UCHIJAAAA | terraqueous                          | 1.4.13                          | terraqueous-1.12.0-1.4.13.jar                             | None                                     |
	| UCHIJAAAA | tcinventoryscan                      | 2.0.10                          | ThaumicInventoryScanning_1.12.2-2.0.10.jar                | None                                     |
	| UCHIJAAAA | thermalcultivation                   | 0.3.0                           | ThermalCultivation-1.12.2-0.3.0.7-universal.jar           | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | thermalinnovation                    | 0.3.0                           | ThermalInnovation-1.12.2-0.3.0.7-universal.jar            | 8a6abf2cb9e141b866580d369ba6548732eff25f |
	| UCHIJAAAA | tickprofiler                         | 1.12-0.0.6                      | TickProfiler-1.12-0.0.6.jar                               | None                                     |
	| UCHIJAAAA | tinker_io                            | release 2.6.1                   | tinker_io-1.12.2-release 2.6.1.jar                        | None                                     |
	| UCHIJAAAA | tinkertoolleveling                   | 1.12.2-1.0.5.DEV.30c7957        | TinkerToolLeveling-1.12.2-1.0.5.jar                       | None                                     |
	| UCHIJAAAA | topaddons                            | 1.12.2-1.9.0                    | topaddons-1.12.2-1.9.0.jar                                | None                                     |
	| UCHIJAAAA | traverse                             | 1.6.0                           | Traverse-1.12.2-1.6.0-69.jar                              | None                                     |
	| UCHIJAAAA | unloader                             | 1.2.0                           | unloader-1.2.0.jar                                        | None                                     |
	| UCHIJAAAA | usefulnullifiers                     | 1.5.0                           | usefulnullifiers-1.5.0.jar                                | None                                     |
	| UCHIJAAAA | universalmodifiers                   | 1.12.2-1.0.9a                   | valkyrielib-1.12.2-2.0.15.1.jar                           | None                                     |
	| UCHIJAAAA | waim                                 | 1.0.0                           | WAIM-1.0.0.jar                                            | None                                     |
	| UCHIJAAAA | wanionlib                            | 1.12.2-1.5                      | WanionLib-1.12.2-1.5.jar                                  | None                                     |
	| UCHIJAAAA | waterstrainer                        | 3.2.0                           | WaterStrainer-1.12-3.2.0.jar                              | None                                     |
	| UCHIJAAAA | waystones                            | 4.0.63                          | Waystones_1.12.2-4.0.63.jar                               | None                                     |
	| UCHIJAAAA | wirelesscharger                      | 1.12.2-1.0.5                    | WirelessCharger-1.12.2-1.0.5.jar                          | aaaf83332a11df02406e9f266b1b65c1306f0f76 |
	| UCHIJAAAA | wct                                  | 3.9.67                          | WirelessCraftingTerminal-1.12.2-3.9.67.jar                | None                                     |
	| UCHIJAAAA | wizardry                             | 0.9.7                           | wizardry-0.9.7.jar                                        | None                                     |
	| UCHIJAAAA | woot                                 | 1.12.2-1.4.4                    | woot-1.12.2-1.4.4.jar                                     | None                                     |
	| UCHIJAAAA | worldedit                            | 6.1.8                           | worldedit-forge-mc1.12-6.1.8-dist.jar                     | None                                     |
	| UCHIJAAAA | worldutils                           | 0.4.2                           | worldutils-1.12.2-0.4.2.jar                               | 2b03e1423915a189b8094816baa18f239d576dff |
	| UCHIJAAAA | xtones                               | 1.12-1.0.8-11                   | Xtones-1.12-1.0.8-11.jar                                  | None                                     |
	| UCHIJAAAA | ynot                                 | 0.2.3                           | YNot-0.2.3.jar                                            | None                                     |
	| UCHIJAAAA | industrialwires                      | 1.7-31                          | IndustrialWires-1.7-31.jar                                | 7e11c175d1e24007afec7498a1616bef0000027d |
	| UCHIJAAAA | thebetweenlands                      | 3.3.12                          | TheBetweenlands-3.3.12-universal.jar                      | 38067d6878811efb38b6a045521cfd80b9b60b38 |
	| UCHIJAAAA | elulib                               | 0.1.12                          | elulib-0.1.12.jar                                         | None                                     |
	| UCHIJAAAA | librarianliblate                     | 4.15                            | librarianlib-1.12.2-4.15.jar                              | None                                     |
	| UCHIJAAAA | teslacorelib_registries              | 1.0.15                          | tesla-core-lib-1.12.2-1.0.15.jar                          | None                                     |
	| UCHIJAAAA | unidict                              | 1.12.2-2.7b                     | UniDict-1.12.2-2.7b.jar                                   | None                                     |
	| UCHIJAAAA | wrapup                               | 1.12-1.1.3                      | WrapUp-1.12-1.1.3.jar                                     | None                                     |

	Loaded coremods (and transformers): 
Wizardry Plugin (wizardry-0.9.7.jar)
  com.teamwizardry.wizardry.asm.WizardryTransformer
LibLoader (# LibLoader.jar)
  
EnderCorePlugin (EnderCore-1.12.2-0.5.37.jar)
  com.enderio.core.common.transform.EnderCoreTransformer
  com.enderio.core.common.transform.SimpleMixinPatcher
ForgelinPlugin (Forgelin-1.7.4.jar)
  
BedPatch (bedpatch-2.2-1.12.2.jar)
  com.mordenkainen.bedpatch.BedPatchASM
AstralCore (astralsorcery-1.12.2-1.9.4.jar)
  
LibrarianLib Plugin (librarianlib-1.12.2-4.15.jar)
  com.teamwizardry.librarianlib.asm.LibLibTransformer
OpenModsCorePlugin (OpenModsLib-1.12.2-0.11.5.jar)
  openmods.core.OpenModsClassTransformer
CoreMod (TickProfiler-1.12-0.0.6.jar)
  
Plugin (NotEnoughIDs-1.5.4.2.jar)
  ru.fewizz.neid.asm.Transformer
LoadingPlugin (sampler-1.73.jar)
  
LoadingPlugin (Quark-r1.5-129.jar)
  vazkii.quark.base.asm.ClassTransformer
MalisisCorePlugin (malisiscore-1.12.2-6.4.0.jar)
  
ShetiPhian-ASM (ShetiPhian-ASM-1.12.0.jar)
  shetiphian.asm.ClassTransformer
FMLPlugin (elulib-0.1.12.jar)
  elucent.elulib.asm.ASMTransformer
Inventory Tweaks Coremod (InventoryTweaks-1.64-dev.jar)
  invtweaks.forge.asm.ContainerTransformer
IELoadingPlugin (ImmersiveEngineering-core-0.12-85.jar)
  blusunrize.immersiveengineering.common.asm.IEClassTransformer
AppleCore (AppleCore-mc1.12.2-3.1.4.jar)
  squeek.applecore.asm.TransformerModuleHandler
TransformerLoader (OpenComputers-MC1.12.2-1.7.2.67.jar)
  li.cil.oc.common.asm.ClassTransformer
CoreMod (Aroma1997Core-1.12.2-2.0.0.0.b156.jar)
  
Do not report to Forge! Remove FoamFixAPI (or replace with FoamFixAPI-Lawful) and try again. (foamfix-0.10.1-1.12.2.jar)
  pl.asie.foamfix.coremod.FoamFixTransformer
RandomPatches (randompatches-1.12.2-1.5.0.4.jar)
  com.therandomlabs.randompatches.core.RPTransformer
TheBetweenlandsLoadingPlugin (TheBetweenlands-3.3.12-core.jar)
  thebetweenlands.core.TheBetweenlandsClassTransformer
	OpenModsLib class transformers: [llama_null_fix:FINISHED],[horse_base_null_fix:FINISHED],[pre_world_render_hook:ENABLED],[player_render_hook:ENABLED],[horse_null_fix:FINISHED]
	Pulsar/tconstruct loaded Pulses: 
		- TinkerCommons (Enabled/Forced)
		- TinkerWorld (Enabled/Not Forced)
		- TinkerTools (Enabled/Not Forced)
		- TinkerHarvestTools (Enabled/Forced)
		- TinkerMeleeWeapons (Enabled/Forced)
		- TinkerRangedWeapons (Enabled/Forced)
		- TinkerModifiers (Enabled/Forced)
		- TinkerSmeltery (Enabled/Not Forced)
		- TinkerGadgets (Enabled/Not Forced)
		- TinkerOredict (Enabled/Forced)
		- TinkerIntegration (Enabled/Forced)
		- TinkerFluids (Enabled/Forced)
		- TinkerMaterials (Enabled/Forced)
		- TinkerModelRegister (Enabled/Forced)
		- chiselIntegration (Enabled/Not Forced)
		- chiselsandbitsIntegration (Enabled/Not Forced)
		- craftingtweaksIntegration (Enabled/Not Forced)
		- theoneprobeIntegration (Enabled/Not Forced)

	AE2 Version: stable rv5-stable-11 for Forge 14.23.1.2554
	Pulsar/natura loaded Pulses: 
		- NaturaCommons (Enabled/Forced)
		- NaturaOverworld (Enabled/Not Forced)
		- NaturaNether (Enabled/Not Forced)
		- NaturaDecorative (Enabled/Not Forced)
		- NaturaTools (Enabled/Not Forced)
		- NaturaEntities (Enabled/Not Forced)
		- NaturaOredict (Enabled/Forced)
		- NaturaWorld (Enabled/Not Forced)
		- craftingtweaksIntegration (Enabled/Not Forced)

	List of loaded APIs: 
		* AbyssalCraftAPI (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Biome (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Block (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Caps (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Condition (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Disruption (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Energy (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Entity (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Event (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Integration (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Internal (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Item (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Necronomicon (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Recipe (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Ritual (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Spell (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* AbyssalCraftAPI|Structure (1.17.0) from AbyssalCraft-1.12.2-1.9.4.12.jar
		* actuallyadditionsapi (34) from ActuallyAdditions-1.12.2-r140.jar
		* AppleCoreAPI (3.1.0) from AppleCore-mc1.12.2-3.1.4.jar
		* appliedenergistics2|API (rv5) from appliedenergistics2-rv5-stable-11.jar
		* asielibAPI (1.1) from Computronics-1.12.1-1.6.5.jar
		* asielibAPI|tile (1.0) from Computronics-1.12.1-1.6.5.jar
		* asielibAPI|tool (1.1) from Computronics-1.12.1-1.6.5.jar
		* Baubles|API (1.4.0.2) from Baubles-1.12-1.5.2.jar
		* BetterWithModsAPI (Beta 0.6) from Quark-r1.5-129.jar
		* BetweenlandsAPI (1.11.1) from TheBetweenlands-3.3.12-universal.jar
		* bigreactors|API (4.0.1) from ExtremeReactors-1.12.2-0.4.5.49.jar
		* bloodmagic-api (2.0.0) from BloodMagic-1.12.2-2.3.3-101.jar
		* BotaniaAPI (91) from Botania r1.10-356.jar
		* Chisel-API (0.0.1) from Chisel-MC1.12.2-0.2.1.34.jar
		* ChiselAPI|Carving (0.0.1) from Chisel-MC1.12.2-0.2.1.34.jar
		* ChiselsAndBitsAPI (13.8.0) from chiselsandbits-14.23.jar
		* cofhapi (2.5.0) from CoFHCore-1.12.2-4.5.3.20-universal.jar
		* commoncapabilities|api (0.0.1) from CommonCapabilities-1.12-1.4.0.jar
		* ComputerCraft|API (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|FileSystem (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Lua (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Media (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Network (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Peripheral (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Permissions (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Redstone (1.80pr1) from ComputerCraft1.80pr1.jar
		* ComputerCraft|API|Turtle (1.80pr1) from ComputerCraft1.80pr1.jar
		* computronicsAPI (1.3) from Computronics-1.12.1-1.6.5.jar
		* computronicsAPI|audio (1.0) from Computronics-1.12.1-1.6.5.jar
		* computronicsAPI|chat (1.3) from Computronics-1.12.1-1.6.5.jar
		* computronicsAPI|multiperipheral (1.1) from Computronics-1.12.1-1.6.5.jar
		* computronicsAPI|tape (1.0) from Computronics-1.12.1-1.6.5.jar
		* cosmeticarmorreworked|api (1.0.0) from CosmeticArmorReworked-1.12.2-v3.jar
		* CraftingTweaks|API (4.1) from CraftingTweaks_1.12.2-8.1.9.jar
		* DLDungeonsAPI (1.1) from DoomlikeDungeons-1.11.1-MC1.12.2.jar
		* DraconicEvolution|API (1.3) from Draconic-Evolution-1.12.2-2.3.13.306-universal.jar
		* enderioapi (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|addon (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|capacitor (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|conduits (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|farm (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|redstone (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|teleport (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|tools (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* enderioapi|upgrades (4.0.0) from EnderIO-1.12.2-5.0.31.jar
		* ForestryAPI|apiculture (5.0.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|arboriculture (4.3.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|book (5.8.1) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|circuits (3.1.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|climate (5.0.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|core (5.7.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|farming (5.8.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|food (1.1.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|fuels (3.0.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|genetics (5.7.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|greenhouse (5.2.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|gui (5.8.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|hives (4.1.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|lepidopterology (1.4.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|mail (3.1.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|modules (5.7.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|multiblock (3.0.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|recipes (5.4.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|storage (5.0.0) from forestry_1.12.2-5.8.1.341.jar
		* ForestryAPI|world (2.1.0) from forestry_1.12.2-5.8.1.341.jar
		* funkylocomotion_api (2.0) from funky-locomotion-1.12.2-1.1.2.jar
		* gendustryAPI (2.3.0) from gendustry-1.6.5.8-mc1.12.2.jar
		* Guide-API|API (2.0.0) from Guide-API-1.12-2.1.6-61.jar
		* iChunUtil API (1.2.0) from iChunUtil-1.12.2-7.1.4.jar
		* ImmersiveEngineering|API (1.0) from ImmersiveEngineering-0.12-85.jar
		* ImmersiveEngineering|ImmersiveFluxAPI (1.0) from ImmersiveEngineering-0.12-85.jar
		* industrialforegoingapi (5) from industrialforegoing-1.12.2-1.11.2-212.jar
		* integrateddynamics|api (0.2.0) from IntegratedDynamics-1.12.2-0.11.17.jar
		* journeymap|client-api (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-display (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-event (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-model (1.4) from journeymap-1.12.2-5.5.2.jar
		* journeymap|client-api-util (1.4) from journeymap-1.12.2-5.5.2.jar
		* JustEnoughItemsAPI (4.13.0) from jei_1.12.2-4.12.0.216.jar
		* MekanismAPI|core (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|energy (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|gas (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|infuse (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|laser (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|transmitter (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* MekanismAPI|util (9.0.0) from Mekanism-1.12.2-9.4.13.349.jar
		* openblocks|api (1.2) from OpenBlocks-1.12.2-1.7.6.jar
		* opencomputersapi|component (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|core (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|driver (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|driver|item (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|event (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|filesystem (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|internal (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|machine (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|manual (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|network (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* opencomputersapi|prefab (7.0.0-alpha) from OpenComputers-MC1.12.2-1.7.2.67.jar
		* PneumaticCraftApi (1.0) from pneumaticcraft-repressurized-1.12.2-0.7.8-259.jar
		* practicallogistics2-api (3.1) from practicallogistics2-1.12.2-3.0.4.jar
		* pressureAPI (1.3.1.9) from pressure-1.3.1.9-mc1.12.2.jar
		* ProjectEAPI (1.9.4-1.0.0) from p455w0rdslib-1.12-2.0.35.jar
		* projectred|api (2.0) from ProjectRed-1.12.2-4.9.1.92-Base.jar
		* PsiAPI (6) from Psi-r1.1-59.jar
		* QuarkAPI (2) from Quark-r1.5-129.jar
		* reborncoreAPI (3.10.0.332) from RebornCore-1.12.2-3.10.0.332-universal.jar
		* reborncoreAPI|Power (3.10.0.332) from RebornCore-1.12.2-3.10.0.332-universal.jar
		* reborncoreAPI|Recipe (3.10.0.332) from RebornCore-1.12.2-3.10.0.332-universal.jar
		* reborncoreAPI|Tile (3.10.0.332) from RebornCore-1.12.2-3.10.0.332-universal.jar
		* sonarapi (1.0.1) from sonarcore-1.12.2-5.0.15-13.jar
		* stevescartsAPI (${version}) from StevesCarts-1.12.2-2.4.23.115.jar
		* stevescartsAPI|FARMS (${version}) from StevesCarts-1.12.2-2.4.23.115.jar
		* StorageDrawersAPI (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* StorageDrawersAPI|event (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* StorageDrawersAPI|registry (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* StorageDrawersAPI|render (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* StorageDrawersAPI|storage (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* StorageDrawersAPI|storage-attribute (2.1.0) from StorageDrawers-1.12.2-5.3.7.jar
		* techrebornAPI (2.17.3.815) from TechReborn-1.12.2-2.17.3.815-universal.jar
		* TerraqueousAPI (1.0) from terraqueous-1.12.0-1.4.13.jar
		* TerraqueousAPI|Cloud (1.0) from terraqueous-1.12.0-1.4.13.jar
		* TerraqueousAPI|Machines (1.0) from terraqueous-1.12.0-1.4.13.jar
		* TerraqueousAPI|Plant (1.0) from terraqueous-1.12.0-1.4.13.jar
		* Thaumcraft|API (6.0.2) from Thaumcraft-1.12.2-6.1.BETA24.jar
		* theoneprobe_api (1.4.4) from theoneprobe-1.12-1.4.24.jar
		* valkyrielib.api (1.12.2-2.0.10a) from valkyrielib-1.12.2-2.0.15.1.jar
		* wct|api (1.1) from WirelessCraftingTerminal-1.12.2-3.9.67.jar
		* zerocore|API|multiblock (1.10.2-0.0.2) from zerocore-1.12-0.1.2.2.jar
		* zerocore|API|multiblock|rectangular (1.10.2-0.0.2) from zerocore-1.12-0.1.2.2.jar
		* zerocore|API|multiblock|tier (1.10.2-0.0.2) from zerocore-1.12-0.1.2.2.jar
		* zerocore|API|multiblock|validation (1.10.2-0.0.2) from zerocore-1.12-0.1.2.2.jar
	RebornCore: 
		Plugin Engine: 0
		RebornCore Version: 3.10.0.332
		Runtime Debofucsation 1
	Ender IO: No known problems detected.

	!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
	!!!You are looking at the diagnostics information, not at the crash.       !!!
	!!!Scroll up until you see the line with '---- Minecraft Crash Report ----'!!!
	!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

	AE2 Integration: IC2:ON, RC:OFF, MFR:OFF, Waila:OFF, Mekanism:ON, OpenComputers:ON, THE_ONE_PROBE:ON, TESLA:OFF, CRAFTTWEAKER:ON
	Profiler Position: N/A (disabled)
	Player Count: 0 / 20; []
	Is Modded: Definitely; Server brand changed to 'fml,forge'
	Type: Dedicated Server (map_server.txt)
