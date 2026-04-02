# Commands Overview

Complete reference for all Naruto Destination base mod commands, organized by category.

| Category | Description | Commands |
|----------|-------------|----------|
| [Info Card](info-card.md) | Set player affiliation, clan, land, and rank | 4 |
| [Player Unlocks](player-unlocks.md) | Manage natures, dojutsus, sage modes, tailed beasts, and more | 13 |
| [Player Stats](player-stats.md) | Handle XP, levels, points, and jutsu mastery | 7 |
| [Quality of Life](quality-of-life.md) | Chakra, tokens, conversion, stat inspection, and rankings | 7 |
| [Debugging Tools](debugging.md) | Config reloads, NBT inspection, entity debugging | 5 |
| [Admin Commands](admin.md) | Mob summoning and sword configuration | 2 |

---

## Master Command

### `/destination`

```
/destination <command>
```

The master command hub that auto-fills all other commands you have permission to use. Use this as your starting point when you're unsure of exact command names.

| | |
|---|---|
| **Permission** | Level 0 (all players) |
| **Source** | `CommandDestination` |

---

## Reading Command Syntax

```
/command <required_arg> [optional_arg]
```

| Notation | Meaning |
|----------|---------|
| `<arg>` | You **must** provide this argument |
| `[arg]` | This argument is **optional** |
| `a\|b\|c` | Pick **one** of the listed options |
