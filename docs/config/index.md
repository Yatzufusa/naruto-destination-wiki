# Configuration Reference

All Naruto Destination config files are generated in `config/NarutoDestination/` on first server startup. Edit these files while the server is stopped, or use `/narutoconfigreload` to apply changes live.

---

## Config Files Overview

| Config File | What It Controls |
|-------------|------------------|
| [**GeneralConfig.cfg**](general.md#generalconfigcfg) | Otsutsuki spawn chance, seasonal events, starter randomizers, skill learner thresholds |
| [**ClientConfig.cfg**](general.md#clientconfigcfg) | Client-side accessibility options (colorblind mode) |
| [**StatsConfig.cfg**](stats-chakra.md#statsconfigcfg) | Stat caps for all combat skills, health, intelligence, Otsutsuki |
| [**ChakraConfig.cfg**](stats-chakra.md#chakraconfigcfg) | Chakra per stat, sen chakra, charge speed, charge behavior |
| [**NarutoEXPConfig.cfg**](experience.md#narutoexpconfigcfg) | XP multipliers per rank, level-up rewards, XP scaling |
| [**LearnerConfig.cfg**](experience.md#learnerconfigcfg) | Skill learner progression steps and JP costs |
| [**ResetConfig.cfg**](reset.md) | Stat retention on reset, ranking method, what to keep |
| [**TaijutsuConfig.cfg**](combat.md#taijutsuconfigcfg) | Fist damage scaling, Eight Gates requirements |
| [**KenjutsuConfig.cfg**](combat.md#kenjutsuconfigcfg) | Sword technique scaling, static damage, cooldowns |
| [**MedicalConfig.cfg**](combat.md#medicalconfigcfg) | Byakugou stage requirements |
| [**EnemyConfig.cfg**](combat.md#enemyconfigcfg) | Enemy spawn toggles, health, damage, speed, aggro range |
| [**DNAConfig.cfg**](dna-tokens.md#dnaconfigcfg) | DNA identification, implant requirements, drop tables, success chances |
| [**TokenConfig.cfg**](dna-tokens.md#tokenconfigcfg) | SP/JP/XP costs for each token type |
| [**FreebuildConfig.cfg**](freebuild.md) | Trader/sensei spawns, randomizer pricing, drop rates |

---

## Addon Configs

Addons generate their own config files in separate directories:

| Addon | Config File | Location |
|-------|-------------|----------|
| Villages | `BankConfig.cfg` | `config/NarutoDestinationVillages/` |
| Kage Vote | `KageVoteConfig.cfg` | `config/NarutoDestinationKageVote/` |
| XP Events | `XPEventsConfig.cfg` | `config/NarutoDestinationXPEvents/` |

See each addon's wiki page for details on their configurations.

---

## Tips

!!! tip "Live Reloading"
    Use `/narutoconfigreload` to reload configs without restarting the server. For addon configs, each addon has its own reload command (e.g., `/villagesreload`, `/kagevote reload`, `/xpevent reload`).

!!! info "Value of -1"
    In many config files, a value of `-1` means **unlimited** or **disabled**. This is the convention for stat caps and similar settings.

!!! warning "Back Up Your Configs"
    Always back up your config files before making major changes. The mod may overwrite or migrate configs during updates.
