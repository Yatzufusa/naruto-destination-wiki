# Villages - Territory

Commands for creating and managing territorial zones.

---

## `/territory`

Full territory management &mdash; create, delete, configure, claim, and teleport to territories.

```
/territory <subcommand> [args...]
```

**Aliases:** `/terr`

### Subcommands

#### `create` &mdash; Create a Territory

```
/territory create <radius> <name>
```

Creates a new territory centered on your current position.

| Parameter | Description |
|-----------|-------------|
| `radius` | The radius (in blocks) of the territory |
| `name` | Display name for the territory |

---

#### `delete` &mdash; Delete a Territory

```
/territory delete <id>
```

| Parameter | Description |
|-----------|-------------|
| `id` | The territory ID |

---

#### `list` &mdash; List Territories

```
/territory list [page]
```

Lists all territories with pagination.

---

#### `info` &mdash; Territory Details

```
/territory info <id>
```

Shows detailed information about a specific territory (owner, radius, settings, etc.).

---

#### `set` &mdash; Change Settings

```
/territory set <id> <setting> <value>
```

Modify a territory's configuration.

| Parameter | Description |
|-----------|-------------|
| `id` | The territory ID |
| `setting` | The setting name to change |
| `value` | The new value |

---

#### `claim` &mdash; Assign Owner

```
/territory claim <id> <affiliation>
```

Set which village/affiliation owns the territory.

---

#### `unclaim` &mdash; Remove Owner

```
/territory unclaim <id>
```

Remove the owner from a territory, making it neutral.

---

#### `tp` &mdash; Teleport

```
/territory tp <id>
```

Teleport to the center of a territory.

---

#### `here` &mdash; Current Location

```
/territory here
```

Show which territory (if any) you are currently standing in.

---

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandTerritory` |

!!! example
    ```
    /territory create 100 "Konoha Village"
    /territory list
    /territory claim 1 Konoha
    /territory set 1 pvp true
    /territory here
    /terr tp 1
    ```
