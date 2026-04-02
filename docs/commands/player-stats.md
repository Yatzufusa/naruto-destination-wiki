# Player Stats

Commands for managing player experience, levels, points, and jutsu mastery.

---

## `/levelup`

Directly level up a player's **Naruto Level**.

```
/levelup <amount> [player]
```

| Parameter | Description |
|-----------|-------------|
| `amount` | Number of levels to add |
| `player` | Target player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandLevelup` |

!!! example
    ```
    /levelup 5 Steve
    /levelup 10
    ```

---

## `/narutoexp`

Grant or set a player's **Naruto XP**.

```
/narutoexp <give|set> <amount> <player>
```

| Parameter | Description |
|-----------|-------------|
| `give` | Add XP on top of current amount |
| `set` | Set XP to an exact value |
| `amount` | The XP amount |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandEXP` |

!!! example
    ```
    /narutoexp give 5000 Steve
    /narutoexp set 0 Notch
    ```

---

## `/mastery`

Handle **jutsu mastery** stats for a player.

```
/mastery <addxp|setxp|setlevel|levelup> <amount|level> [player] [slot|jutsu_name]
```

| Parameter | Description |
|-----------|-------------|
| `addxp` | Add mastery XP to a jutsu |
| `setxp` | Set mastery XP to an exact value |
| `setlevel` | Set mastery level directly |
| `levelup` | Level up mastery by amount |
| `amount\|level` | The XP amount or level number |
| `player` | Target player (optional) |
| `slot\|jutsu_name` | Target jutsu by slot number or name (optional) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandMastery` |

!!! example
    ```
    /mastery addxp 1000 Steve Rasengan
    /mastery setlevel 5 Steve 1
    ```

---

## `/points`

Unified command for managing **Skill Points**, **Jutsu Points**, and **Reset Points**.

```
/points <skill|jutsu|reset> <give|set|take> <amount> [player]
```

| Parameter | Description |
|-----------|-------------|
| `skill` | Target Skill Points |
| `jutsu` | Target Jutsu Points |
| `reset` | Target Reset Points |
| `give\|set\|take` | The operation to perform |
| `amount` | Point amount |
| `player` | Target player (optional) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandPoints` |

!!! tip
    This command is a unified wrapper. You can also use the shorthand commands below.

---

## `/skp`

Shorthand for managing **Skill Points**.

```
/skp <give|set|take> <amount> <player>
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSkillPoints` |

---

## `/jp`

Shorthand for managing **Jutsu Points**.

```
/jp <give|set|take> <amount> <player>
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandJutsuPoints` |

---

## `/rp`

Shorthand for managing **Reset Points**.

```
/rp <give|set|take> <amount> <player>
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandResetPoints` |

!!! example "Points Examples"
    ```
    /points skill give 10 Steve
    /skp give 10 Steve
    /jp set 50 Notch
    /rp take 5 Steve
    ```
