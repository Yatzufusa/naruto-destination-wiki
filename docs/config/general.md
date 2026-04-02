# General & Starter Configuration

---

## GeneralConfig.cfg

Controls miscellaneous settings including new player setup, seasonal events, and skill learner access.

### General

| Setting | Default | Description |
|---------|---------|-------------|
| `OtsutsukiSpawnChance` | `5.0` | Chance (%) for new players to randomly spawn as Otsutsuki |

### Events

Seasonal events that trigger automatically during their respective months.

| Setting | Default | Description |
|---------|---------|-------------|
| `HoldChristmasEvent` | `true` | Enable Christmas gift drops in December |
| `HoldEasterEvent` | `true` | Enable Easter egg drops in April |

### Starter Items

Control what randomizers new players receive when they first join.

| Setting | Default | Description |
|---------|---------|-------------|
| `StarterClanRandomizer` | `true` | Give new players a random clan |
| `StarterNatureRandomizer` | `true` | Give new players a random nature release |
| `StarterKekkeiGenkaiRandomizer` | `false` | Give new players a random kekkei genkai |
| `StarterLandRandomizer` | `true` | Give new players a random land |
| `StartWithRandomAffiliation` | `true` | Assign new players a random village |

!!! tip
    On most servers, you'll want `StarterKekkeiGenkaiRandomizer` set to `false` so KKG remains a rare unlock. Natures and clans are usually fine to randomize for new players.

### Skill Learners

Control the stat thresholds needed to unlock skill learner NPCs. Set to `-1` to disable the threshold requirement.

| Setting | Default | Description |
|---------|---------|-------------|
| `KenjutsuSkillLearnerThreshold` | `200` | Kenjutsu stat needed to unlock the Kenjutsu learner |
| `MedicalSkillLearnerThreshold` | `200` | Medical stat needed to unlock the Medical learner |
| `TaijutsuSkillLearnerThreshold` | `200` | Taijutsu stat needed to unlock the Taijutsu learner |
| `AllowSkillLearnerPurchase` | `true` | Allow purchasing learner access from traders |

---

## ClientConfig.cfg

Client-side settings. This config is only relevant for the player's game client, not the server.

### Accessibility

| Setting | Default | Description |
|---------|---------|-------------|
| `ColourBlindMode` | `false` | Enable alternative HUD colors for colorblind users |
