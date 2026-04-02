# Player Unlocks

These commands manage what abilities, dojutsus, sage modes, and other special powers a player has unlocked.

---

## `/release`

Manage a player's **nature releases** and **kekkei genkai (KKG)**.

```
/release <give|take> <nature|kkg> <input> [player]
```

| Parameter | Description |
|-----------|-------------|
| `give\|take` | Whether to grant or remove the release |
| `nature\|kkg` | Whether this is a nature release or kekkei genkai |
| `input` | The name of the nature or KKG |
| `player` | Target player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandRelease` |

!!! example
    ```
    /release give nature Fire Steve
    /release take kkg WoodRelease Notch
    ```

---

## `/dojutsu`

Manage a player's **dojutsus** (eye techniques).

```
/dojutsu <give|take> <dojutsu> [player]
```

| Parameter | Description |
|-----------|-------------|
| `give\|take` | Whether to grant or remove the dojutsu |
| `dojutsu` | One of the available dojutsus (see below) |
| `player` | Target player (optional, defaults to self) |

**Available Dojutsus:**

| Dojutsu | Description |
|---------|-------------|
| `sharingan` | Base Sharingan |
| `mangekyousharingan` | Mangekyo Sharingan |
| `eternalmangekyousharingan` | Eternal Mangekyo Sharingan |
| `rinnegan` | Rinnegan |
| `byakugan` | Byakugan |
| `tenseigan` | Tenseigan |
| `ketsuryugan` | Ketsuryugan |
| `jouganblue` | Jougan (Blue) |
| `jouganred` | Jougan (Red) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandDojutsu` |

!!! example
    ```
    /dojutsu give sharingan Steve
    /dojutsu take rinnegan Notch
    ```

---

## `/setbyakugou`

Set a player's **Byakugou** (Strength of a Hundred Seal) stage.

```
/setbyakugou <player> <stage>
```

| Parameter | Description |
|-----------|-------------|
| `player` | Target player name |
| `stage` | The Byakugou stage number |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandByakugou` |

---

## `/setcm`

Configure a player's **Curse Mark**.

```
/setcm <stage|type|random> <value> <player>
```

| Parameter | Description |
|-----------|-------------|
| `stage` | Set the curse mark stage |
| `type` | Set the curse mark type |
| `random` | Assign a random curse mark |
| `value` | The stage number, type name, or random seed |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandCurseMark` |

!!! example
    ```
    /setcm stage 2 Steve
    /setcm type Heaven Steve
    /setcm random true Notch
    ```

---

## `/eightgates`

Set how many of the **Eight Gates** a player has unlocked.

```
/eightgates unlocked [0-8] [player]
```

| Parameter | Description |
|-----------|-------------|
| `0-8` | Number of gates unlocked (0 = none, 8 = all) |
| `player` | Target player (optional) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandEightGates` |

!!! example
    ```
    /eightgates unlocked 5 Steve
    ```

---

## `/karmaseal`

Manage a player's **Karma Seal**.

```
/karmaseal <type|size> <value> <player>
```

| Parameter | Description |
|-----------|-------------|
| `type` | Set the Karma seal type |
| `size` | Set the Karma seal size/stage |
| `value` | The type name or size value |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandKarmaSeal` |

!!! example
    ```
    /karmaseal type Isshiki Steve
    /karmaseal size 2 Notch
    ```

---

## `/otsutsuki`

Manage a player's **Otsutsuki DNA**.

```
/otsutsuki <give|take|healthboost> [player] [amount]
```

| Parameter | Description |
|-----------|-------------|
| `give` | Grant Otsutsuki DNA |
| `take` | Remove Otsutsuki DNA |
| `healthboost` | Set health boost amount |
| `player` | Target player (optional) |
| `amount` | Health boost amount (for `healthboost`) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandOtsutsuki` |

!!! example
    ```
    /otsutsuki give Steve
    /otsutsuki healthboost Steve 20
    ```

---

## `/setsage`

Set a player's **Sage Mode** type.

```
/setsage <type> <player>
```

| Parameter | Description |
|-----------|-------------|
| `type` | The sage mode type (e.g. Toad, Snake, Slug) |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSageMode` |

!!! example
    ```
    /setsage Toad Steve
    ```

---

## `/sharingansize`

Set the player's unlocked **Sharingan progression level** (1-Tomoe through Rinnegan).

```
/sharingansize <size> <player>
```

| Parameter | Description |
|-----------|-------------|
| `size` | The progression level |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSharinganSize` |

!!! info
    This controls how far along the Sharingan evolution tree the player has progressed (1-Tomoe, 2-Tomoe, 3-Tomoe, Mangekyo, Eternal Mangekyo, Rinnegan).

---

## `/sixpathssagemode`

Toggle **Six Paths Sage Mode** for a player.

```
/sixpathssagemode <player>
```

| Parameter | Description |
|-----------|-------------|
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSixPathsSageMode` |

!!! warning "Currently Disabled"
    Six Paths Sage Mode is currently disabled while it is being reworked. This command may not function as expected.

---

## `/sstage`

Set a player's **Susano'o stage** (size/form).

```
/sstage <stage> <player>
```

| Parameter | Description |
|-----------|-------------|
| `stage` | The Susano'o stage/form number |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSusanoo` |

---

## `/tailedbeast`

Manage a player's **Tailed Beast** (Bijuu).

```
/tailedbeast <tailed_beast|+N|-N|remove> <player>
```

| Parameter | Description |
|-----------|-------------|
| `tailed_beast` | Name or number of the tailed beast to assign |
| `+N` / `-N` | Increment or decrement the tailed beast number |
| `remove` | Remove the player's tailed beast |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandTailedBeast` |

!!! example
    ```
    /tailedbeast Kurama Steve
    /tailedbeast +1 Steve
    /tailedbeast remove Notch
    ```

---

## `/truthseekingorbs`

Activate **Truth-Seeking Orbs** for a player.

```
/truthseekingorbs <player>
```

| Parameter | Description |
|-----------|-------------|
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandTruthseekingOrbs` |

---

## `/mangekyoupattern`

Set the **Mangekyo Sharingan pattern** for a player.

```
/mangekyoupattern <pattern> <player>
```

| Parameter | Description |
|-----------|-------------|
| `pattern` | The MS pattern name (e.g. Itachi, Obito, Sasuke) |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandMangekyouPattern` |

!!! tip
    Available patterns include character names like Itachi, Obito, Sasuke, and custom patterns like Dragozai and NoHxpee. Check your mod configuration for the full list.

!!! example
    ```
    /mangekyoupattern Itachi Steve
    /mangekyoupattern Obito Notch
    ```
