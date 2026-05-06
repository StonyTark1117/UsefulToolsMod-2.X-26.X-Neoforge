# Changelog

## 2.2.1-1.21.1-neoforge

Initial NeoForge 1.21.1 release, ported from the Forge 1.21.1 source. Feature parity with the Forge variant.

### Compatibility

- Minecraft 1.21.1
- NeoForge 21.1.219+

### Optional integrations

- JEI 19.27.0.340+ — Spectral Infuser recipe category
- WTHIT (waila) 12.10.1+ — Ghost ectoplasm armor info
- Cloth Config 15.0.140+ — In-game config screen

### Port notes

- Migrated from Forge APIs to NeoForge equivalents (`net.minecraftforge.*` → `net.neoforged.neoforge.*`, `RegistryObject` → `DeferredHolder`, `ForgeTier` → `SimpleTier`, etc.)
- Tick events updated to NeoForge's split `PlayerTickEvent.Post` / `LevelTickEvent.Post`
- `LivingHurtEvent` → `LivingIncomingDamageEvent`, `MobSpawnEvent.FinalizeSpawn` → `FinalizeSpawnEvent`
- Menu screen registration moved to `RegisterMenuScreensEvent`
- Biome modifier JSONs relocated to the `neoforge:` namespace, fixing a silent ore-generation failure in pre-release builds
