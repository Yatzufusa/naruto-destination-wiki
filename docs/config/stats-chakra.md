# Stats & Chakra Configuration

---

## StatsConfig.cfg

Controls maximum stat values, health caps, and intelligence settings.

### Combat Stat Caps

Set the maximum value each combat stat can reach. Use `-1` for unlimited.

| Setting | Default | Description |
|---------|---------|-------------|
| `MaxNinjutsu` | `-1` | Max Ninjutsu stat |
| `MaxTaijutsu` | `-1` | Max Taijutsu stat |
| `MaxGenjutsu` | `-1` | Max Genjutsu stat |
| `MaxKenjutsu` | `-1` | Max Kenjutsu stat |
| `MaxShurikenjutsu` | `-1` | Max Shurikenjutsu stat |
| `MaxSummoning` | `-1` | Max Summoning stat |
| `MaxKinjutsu` | `-1` | Max Kinjutsu stat |
| `MaxSenjutsu` | `-1` | Max Senjutsu stat |
| `MaxMedical` | `-1` | Max Medical stat |
| `MaxSpeed` | `500` | Max Speed stat |
| `MaxSageSoupCounter` | `-1` | Max sage soup uses |
| `SenjutsuPerSoup` | `5` | Senjutsu gained per sage soup |

!!! tip
    Setting stat caps is a great way to create a balanced server meta. For example, capping stats at `1000` prevents extreme power creep.

### Health

| Setting | Default | Description |
|---------|---------|-------------|
| `BaseHealthCap` | `1000` | Maximum base health for all players |
| `MaxTailedBeastHealthBonus` | `500` | Maximum additional health from Tailed Beasts |

### Otsutsuki

| Setting | Default | Description |
|---------|---------|-------------|
| `MaxOtsutsukiHealthBonus` | `500` | Maximum additional health from Otsutsuki DNA |
| `OtsutsukiSelfImplant` | `10` | HP cap increase per self-implant (0 to disable) |
| `OtsutsukiImplantHP` | `50` | HP gained per implant |

### Intelligence

| Setting | Default | Description |
|---------|---------|-------------|
| `IntelligencePerWM` | `"1"` | Intelligence gained per World Mystery (supports ranges like `"1-3"`) |
| `MaxIntelligence` | `100` | Maximum intelligence stat |

---

## ChakraConfig.cfg

Controls how much chakra each stat provides, charging speed, and charging behavior.

### Chakra Per Stat

How much maximum chakra each point in a stat grants.

| Setting | Default | Description |
|---------|---------|-------------|
| `NinjutsuChakra` | `5` | Max chakra per Ninjutsu point |
| `GenjutsuChakra` | `3` | Max chakra per Genjutsu point |
| `TaijutsuChakra` | `0` | Max chakra per Taijutsu point |
| `KenjutsuChakra` | `1` | Max chakra per Kenjutsu point |
| `KinjutsuChakra` | `3` | Max chakra per Kinjutsu point |
| `SenjutsuChakra` | `3` | Max chakra per Senjutsu point |
| `ShurikenjutsuChakra` | `3` | Max chakra per Shurikenjutsu point |
| `SummoningChakra` | `3` | Max chakra per Summoning point |
| `MedicalChakra` | `3` | Max chakra per Medical point |

!!! info "Example Calculation"
    A player with 100 Ninjutsu and 50 Genjutsu would have a max chakra of:
    `(100 × 5) + (50 × 3) = 650` chakra (from those two stats alone).

### Sen Chakra

| Setting | Default | Description |
|---------|---------|-------------|
| `SenjutsuSenChakra` | `5` | Max sen (senjutsu) chakra per Senjutsu point |

### Chakra Charging

| Setting | Default | Description |
|---------|---------|-------------|
| `ChakraChargeSpeedMultiplier` | `1.0` | Multiplier for chakra charge speed |
| `SenChakraChargeSpeedMultiplier` | `1.0` | Multiplier for sen chakra charge speed |
| `AllowJutsusDuringChakraCharge` | `true` | Allow casting jutsus while charging chakra |
| `DebuffDuringChakraCharge` | `true` | Apply slowness while charging chakra |
