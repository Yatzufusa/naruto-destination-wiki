# Quality of Life

Utility commands for everyday player and admin convenience.

---

## `/chakra`

Manage a player's **chakra**.

```
/chakra <give|take|set> <amount> [player]
```

Running `/chakra` with no arguments shows your current chakra.

| Parameter | Description |
|-----------|-------------|
| `give\|take\|set` | The operation to perform |
| `amount` | Chakra amount |
| `player` | Target player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP (with args) / Player (no args, self only) |
| **Source** | `CommandChakra` |

!!! example
    ```
    /chakra
    /chakra give 500 Steve
    /chakra set 1000 Notch
    ```

---

## `/senchakra`

Manage a player's **Sen chakra** (Senjutsu chakra).

```
/senchakra <give|take|set> <amount> [player]
```

Running `/senchakra` with no arguments shows your current sen chakra.

| Parameter | Description |
|-----------|-------------|
| `give\|take\|set` | The operation to perform |
| `amount` | Sen chakra amount |
| `player` | Target player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP (with args) / Player (no args, self only) |
| **Source** | `CommandSenChakra` |

---

## `/consumetoken`

Consume all **stat tokens** of a specific type in your inventory at once.

```
/consumetoken <sp|jp|xp|rp|all>
```

| Parameter | Description |
|-----------|-------------|
| `sp` | Consume Skill Point tokens |
| `jp` | Consume Jutsu Point tokens |
| `xp` | Consume XP tokens |
| `rp` | Consume Reset Point tokens |
| `all` | Consume all token types |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandConsumeToken` |

!!! tip
    Use `/consumetoken all` to quickly redeem all tokens in your inventory at once instead of right-clicking each one.

---

## `/convert`

Convert **money (Ryo)** or **stat tokens** into the highest craftable denomination in your inventory.

```
/convert <ryo|tokens> [sp|xp|jp]
```

| Parameter | Description |
|-----------|-------------|
| `ryo` | Convert Ryo currency |
| `tokens` | Convert stat tokens |
| `sp\|xp\|jp` | Filter to a specific token type (optional) |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandConvert` |

---

## `/investsp`

Invest free **Skill Points** into specific stats in bulk.

```
/investsp <stat> <amount|all>
/investsp <percentages> <amount|all>
```

| Parameter | Description |
|-----------|-------------|
| `stat` | The stat to invest in |
| `amount` | Number of SP to invest, or `all` for everything |
| `percentages` | Distribute SP across stats by percentage |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandInvestSP` |

!!! example
    ```
    /investsp Ninjutsu all
    /investsp Taijutsu 50
    ```

---

## `/narutoinspect`

Inspect another player's **Naruto stats**.

```
/narutoinspect <player|uuid>
```

| Parameter | Description |
|-----------|-------------|
| `player\|uuid` | Target player name or UUID |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandNarutoInspect` |

---

## `/rank`

Display **stat rankings** for players.

```
/rank [online|alltime] [stat] [player]
```

| Parameter | Description |
|-----------|-------------|
| `online` | Only show currently online players |
| `alltime` | Show all-time rankings |
| `stat` | Filter by a specific stat |
| `player` | Look up a specific player's position |

| | |
|---|---|
| **Permission** | Player |
| **Source** | `CommandRank` |

!!! example
    ```
    /rank online
    /rank alltime Ninjutsu
    /rank alltime level Steve
    ```
