# Villages - Leadership Commands

Commands for village leaders to manage ranks, promotions, and transport networks.

---

## `/narutopromote`

**Promote** a player to a special village rank, or remove their rank.

```
/narutopromote <player> <rank>
/narutopromote <player> remove
```

| Parameter | Description |
|-----------|-------------|
| `player` | Target player name |
| `rank` | The rank to promote to (see below) |
| `remove` | Remove the player's special rank |

**Promotable Ranks:**

| Rank | Description |
|------|-------------|
| `Advisor` | Village advisor |
| `AnbuCaptain` | ANBU captain |
| `ShadowKage` | Shadow Kage (second-in-command) |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Requires** | Must hold a leader rank: Kage, ShadowKage, or Akatsuki Leader |
| **Source** | `CommandNarutoPromote` |

!!! warning
    Only village leaders (Kage, ShadowKage, Akatsuki Leader) can promote players. Regular players cannot use this command.

!!! example
    ```
    /narutopromote Steve Advisor
    /narutopromote Notch AnbuCaptain
    /narutopromote Steve remove
    ```

---

## `/narutotransport`

Manage the **fast travel / transport** network. Set locations, unlock destinations for players, and teleport.

```
/narutotransport <tp|set|unlock|gui> <affiliation|custom> [name] [player]
```

**Aliases:** `/ntp`

| Subcommand | Description |
|------------|-------------|
| `tp <location> [player]` | Teleport to a transport location |
| `set <affiliation\|custom> [name]` | Set a transport destination at your current position |
| `unlock <affiliation\|custom> [name] [player]` | Unlock a destination for a player |
| `gui [player]` | Open the transport GUI |

| | |
|---|---|
| **Permission** | Player (level 0) |
| **Requires** | `set` and teleporting others require OP |
| **Source** | `CommandNarutoTransport` |

!!! info "Location Types"
    - **Affiliation locations** are tied to a specific village (e.g. Konoha's main gate)
    - **Custom locations** are freeform named destinations

!!! example
    ```
    /ntp gui
    /ntp tp Konoha
    /ntp set Konoha
    /ntp unlock Konoha Steve
    /ntp set custom TrainingGrounds
    ```
