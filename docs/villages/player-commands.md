# Villages - Player Commands

Commands available to all players for interacting with the village system.

---

## `/villages`

The main **village hub** command. Opens the village GUI or navigates directly to a specific section.

```
/villages [gui|stats|bank|transport|ranks|relations|help]
```

**Aliases:** `/v`, `/villageshub`

| Subcommand | Description |
|------------|-------------|
| *(none)* | Open the main village GUI |
| `gui` | Open the main village GUI |
| `stats` / `statistics` | View your village's statistics |
| `bank` | Open your village's bank |
| `transport` / `tp` | Open the fast travel system |
| `ranks` / `leadership` | View your village's rank holders |
| `relations` / `relationships` | View alliances, wars, and neutral standings |
| `help` | Show available subcommands |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Requires** | Must be a player (not console) |
| **Source** | `CommandVillages` |

!!! example
    ```
    /villages
    /v stats
    /v bank
    /v transport
    ```

---

## `/villagepvp`

Check **PvP rules**, your status, and loot information.

```
/villagepvp <status|check|rules|loot|reload>
```

**Aliases:** `/vpvp`

| Subcommand | Description |
|------------|-------------|
| `status` | Show your current PvP status and protection info |
| `check <player>` | Check your PvP status against another specific player |
| `rules` | Display the current PvP ruleset |
| `loot` | Show the loot pool and drop rules |
| `reload` | Reload PvP configuration (OP only) |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Requires** | Must be a player (not console) |
| **Source** | `CommandVillagePvP` |

!!! note
    The `reload` subcommand requires OP, even though the base command is player-accessible.

!!! example
    ```
    /vpvp status
    /vpvp check Steve
    /vpvp rules
    ```

---

## `/villagerelation`

View and manage **diplomatic relations** between villages &mdash; wars, alliances, and neutral standings.

```
/villagerelation <war|ally|neutral|view|list|gui> [affiliation]
```

**Aliases:** `/vr`, `/relation`

| Subcommand | Description |
|------------|-------------|
| `war <affiliation>` | Declare war on another village |
| `ally <affiliation>` | Propose or accept an alliance |
| `neutral <affiliation>` | Set a neutral/peace relation |
| `view [affiliation]` | View relationships for a specific village |
| `list` | List all current relationships across all villages |
| `gui <affiliation>` | Open the relation management GUI |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Requires** | Must be a player; war/ally/neutral require Kage or leader rank |
| **Source** | `CommandVillageRelation` |

!!! warning
    Declaring war, proposing alliances, and setting neutral standings require **Kage-level authority** within your village. Regular players can only view and list relations.

!!! example
    ```
    /vr list
    /vr view Konoha
    /vr war Akatsuki
    /vr ally Sunagakure
    ```
