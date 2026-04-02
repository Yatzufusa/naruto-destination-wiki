# Villages - Admin Commands

Server administration commands for the Villages addon.

---

## `/villagebank`

Open and manage **village banks**.

```
/villagebank [player|affiliation] [affiliation]
/villagebank info [affiliation]
```

**Aliases:** `/vbank`, `/vb`

| Usage | Description |
|-------|-------------|
| `/villagebank` | Open your own village bank |
| `/villagebank info [affiliation]` | View bank information |
| `/villagebank <player>` | Open a specific player's village bank |
| `/villagebank <affiliation>` | Open a specific village's bank |
| `/villagebank <player> <affiliation>` | Open a player's bank in a specific village |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandVillageBank` |

!!! example
    ```
    /vbank
    /vbank info Konoha
    /vbank Steve
    /vbank Konoha
    ```

---

## `/villagebankpages`

Set or add **pages** to a village bank's inventory.

```
/villagebankpages <number|+N> [affiliation]
```

**Aliases:** `/vbankpages`, `/vbp`

| Parameter | Description |
|-----------|-------------|
| `number` | Set the exact number of pages |
| `+N` | Add N pages to the current count |
| `affiliation` | Target village (optional) |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandVillageBankPages` |

!!! example
    ```
    /vbp 5 Konoha
    /vbp +2 Akatsuki
    ```

---

## `/villageranks`

Manage and inspect **village rank holders**.

```
/villageranks <list|info|reload|rebuild> [affiliation] [rank]
```

| Subcommand | Description |
|------------|-------------|
| `list [affiliation] [rank]` | List all rank holders, optionally filtered |
| `info <affiliation> <rank>` | Show detailed info about a specific rank's holders |
| `reload` | Reload rank configuration from disk |
| `rebuild` | Rebuild rank tracking data from the database |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandVillageRanks` |

!!! example
    ```
    /villageranks list
    /villageranks list Konoha
    /villageranks info Konoha Kage
    /villageranks reload
    ```

---

## `/villagesreload`

Reload **Villages addon configurations**. Can reload specific modules or everything.

```
/villagesreload [module|all]
```

| Module | Description |
|--------|-------------|
| `ranks` | Reload rank configuration |
| `relations` | Reload diplomatic relations |
| `transport` | Reload transport locations |
| `bank` | Reload bank configuration |
| `pvp` | Reload PvP rules |
| `permissions` | Reload permission settings |
| `territory` | Reload territory data |
| `all` | Reload all modules |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandVillagesReload` |

!!! tip
    Use specific module reloads when possible to minimize server impact, rather than reloading everything.

!!! example
    ```
    /villagesreload pvp
    /villagesreload ranks
    /villagesreload all
    ```
