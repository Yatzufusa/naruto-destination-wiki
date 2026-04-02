# Info Card Commands

These commands modify a player's **Ninja Info Card** &mdash; the profile that displays their affiliation, clan, land, and rank. Some of these values also affect gameplay mechanics.

---

## `/affiliation`

Set the affiliation (village) of a player on their Ninja Info Card.

```
/affiliation <affiliation> <player>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The affiliation/village name to assign |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandAffiliation` |

!!! example
    ```
    /affiliation Konoha Steve
    /affiliation Akatsuki Notch
    ```

---

## `/setclan`

Set the clan of a player on their Ninja Info Card. The clan also has **gameplay effects** on certain jutsus.

```
/setclan <clan> <player>
```

| Parameter | Description |
|-----------|-------------|
| `clan` | The clan name to assign |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandClan` |

!!! note
    Clan affects some jutsu behavior. Make sure the clan name matches a valid clan in the mod configuration.

!!! example
    ```
    /setclan Uchiha Steve
    /setclan Hyuga Notch
    ```

---

## `/setland`

Set the land of a player on their Ninja Info Card.

```
/setland <land> <player>
```

| Parameter | Description |
|-----------|-------------|
| `land` | The land name to assign |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandLand` |

!!! example
    ```
    /setland "Land of Fire" Steve
    ```

---

## `/setrank`

Set the rank of a player on their Ninja Info Card. Rank also affects **XP gain rates**.

```
/setrank <rank> <player>
```

| Parameter | Description |
|-----------|-------------|
| `rank` | The rank to assign |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandSetRank` |

!!! warning
    Rank directly influences XP gain multipliers. Changing a player's rank will affect how fast they level up.

!!! example
    ```
    /setrank Genin Steve
    /setrank Jonin Notch
    ```
