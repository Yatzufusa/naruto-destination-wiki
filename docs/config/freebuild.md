# Freebuild & Spawns Configuration

## FreebuildConfig.cfg

Controls NPC spawning (traders and senseis), randomizer pricing, and mob drop rates.

---

### Trader Spawns

Toggle which types of traders spawn in the world.

| Setting | Description |
|---------|-------------|
| `DoTradersSpawn` | Master toggle for all traders |
| `DoMedicalTradersSpawn` | Medical supply traders |
| `DoFoodTradersSpawn` | Food traders |
| `DoNinjaToolTradersSpawn` | Ninja tool traders |
| `DoArmorTradersSpawn` | Armor traders |
| `DoRandomizerTradersSpawn` | Randomizer traders (sell natures, KKG, etc.) |
| `DoJutsuTradersSpawn` | Jutsu scroll traders |

### Sensei Spawns

Toggle which senseis spawn in the world.

| Setting | Description |
|---------|-------------|
| `DoSenseiSpawn` | Master toggle for all senseis |
| `DoTaijutsuSenseiSpawn` | Taijutsu sensei |
| `DoMedicalSenseiSpawn` | Medical sensei |
| `DoKenjutsuSenseiSpawn` | Kenjutsu sensei |

---

### Randomizer Pricing

Configure the price and drop chance for each type of randomizer sold by traders.

| Randomizer Type | Configurable Settings |
|-----------------|----------------------|
| Nature | Price, drop chance |
| Mangekyou | Price, drop chance |
| Land | Price, drop chance |
| Clan | Price, drop chance |
| Kekkei Genkai | Price, drop chance |
| Curse Mark | Price, drop chance |
| Sage | Price, drop chance |
| Dojutsu | Price, drop chance |
| Tailed Beast | Price, drop chance |

!!! tip
    Make rare randomizers (Tailed Beast, Dojutsu) expensive and uncommon to maintain server economy balance.

---

### Mob Drops

| Setting | Default | Description |
|---------|---------|-------------|
| `RyoDropChanceMultiplier` | *varies* | Multiplier for Ryo currency drops |
| `TokenDropChanceMultiplier` | *varies* | Multiplier for token drops |
| `RequirePlayerKillForDrops` | *varies* | If `true`, only player kills trigger drops (not mob farms with automated killing) |
| `HostileKillChakraXPRange` | *e.g.* `"10-20"` | Range of chakra XP from killing hostile mobs |
| `PassiveKillChakraXPRange` | *e.g.* `"1-5"` | Range of chakra XP from killing passive mobs |

!!! warning
    `RequirePlayerKillForDrops` is important for economy balance. If disabled, fully automated mob farms can generate unlimited tokens.
