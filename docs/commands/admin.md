# Admin Commands

Server administration commands for spawning mobs and configuring weapons.

---

## `/narutosummon`

Summon **Naruto mod mobs**, including passively standing Tailed Beasts and traders.

```
/narutosummon <group> <mob> [amount] [player]
```

| Parameter | Description |
|-----------|-------------|
| `group` | The mob group/category |
| `mob` | The specific mob to summon |
| `amount` | Number of mobs to spawn (optional, default 1) |
| `player` | Spawn near this player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandNarutoSummon` |

!!! tip
    This command can summon a variety of special entities beyond regular mobs, including stationary Tailed Beasts for events or decorative purposes, and NPC traders.

!!! example
    ```
    /narutosummon beast Kurama 1 Steve
    ```

---

## `/addsword`

Add the **item you are currently holding** to the `OtherSwords.cfg` configuration. This makes the weapon **scale with the player's Naruto stats**.

```
/addsword
```

| | |
|---|---|
| **Permission** | OP |
| **Requires** | Must be holding an item |
| **Source** | `CommandAddSword` |

!!! info
    After running this command, the held item will be registered as a scaling weapon. Its damage will dynamically adjust based on the player's Naruto stats, just like built-in mod weapons.
