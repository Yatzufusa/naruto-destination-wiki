# XP Events - Commands

All XP Event functionality is accessed through the `/xpevent` command.

```
/xpevent [subcommand] [args...]
```

| | |
|---|---|
| **Base Permission** | Player (level 0) |
| **Admin Subcommands** | Require OP |
| **Source** | `CommandXPEvent` |

---

## `/xpevent status`

View the **current XP event status**, including active multiplier, time remaining, and schedule.

```
/xpevent status
```

| | |
|---|---|
| **Permission** | Player |

---

## `/xpevent gui`

Open the **XP Event management GUI** for visual event control.

```
/xpevent gui
```

| | |
|---|---|
| **Permission** | OP |

---

## `/xpevent now`

**Start an XP event immediately** with a specified multiplier and duration.

```
/xpevent now <multiplier|threshold> <duration>
```

### Multiplier Values

| Value | Multiplier |
|-------|------------|
| `1.15` | 1.15x XP |
| `1.5` | 1.5x XP |
| `1.75` | 1.75x XP |
| `2` | 2x XP |
| `3` | 3x XP |
| Custom | Any value between 1.0 and 10.0 |
| `threshold` | Use the threshold system (incremental steps) |

### Duration Values

| Value | Duration |
|-------|----------|
| `1h` | 1 hour |
| `2h` | 2 hours |
| `6h` | 6 hours |
| `12h` | 12 hours |
| `1d` | 1 day |
| `2d` | 2 days |
| `3d` | 3 days |
| `7d` | 7 days |
| `today` | Until end of today |
| `thisweek` | Until end of this week |
| `thismonth` | Until end of this month |

| | |
|---|---|
| **Permission** | OP |

!!! example
    ```
    /xpevent now 2 6h
    /xpevent now 1.5 today
    /xpevent now threshold 1d
    ```

---

## `/xpevent automatic`

Configure **automatic XP events** that trigger on specific days of the week.

```
/xpevent automatic <multiplier> <days...>
```

| Parameter | Description |
|-----------|-------------|
| `multiplier` | The XP multiplier to apply |
| `days` | One or more days of the week |

**Day Values:** `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday`

| | |
|---|---|
| **Permission** | OP |

!!! example
    ```
    /xpevent automatic 2 saturday sunday
    /xpevent automatic 1.5 friday
    ```

---

## `/xpevent stop`

**Stop** the currently active XP event.

```
/xpevent stop
```

| | |
|---|---|
| **Permission** | OP |

---

## `/xpevent setmultiplier`

**Override** the effective XP multiplier without starting or stopping an event.

```
/xpevent setmultiplier <value>
```

| Parameter | Description |
|-----------|-------------|
| `value` | The new multiplier value |

| | |
|---|---|
| **Permission** | OP |

---

## `/xpevent threshold`

Configure the **threshold system** for incremental multiplier steps.

```
/xpevent threshold <set|increase|decrease|list> [step]
```

| Subcommand | Description |
|------------|-------------|
| `set <step>` | Set the threshold step directly |
| `increase [step]` | Increase the threshold by one step (or specified amount) |
| `decrease [step]` | Decrease the threshold by one step (or specified amount) |
| `list` | List all configured threshold steps |

| | |
|---|---|
| **Permission** | OP |

!!! info "Threshold System"
    Thresholds allow progressive XP events where the multiplier increases in steps. Each step has a configured multiplier value. Use `list` to see the available steps and their values.

---

## `/xpevent reload`

**Reload** the XP Events configuration from disk.

```
/xpevent reload
```

| | |
|---|---|
| **Permission** | OP |

---

## `/xpevent help`

Display the **help message** with available subcommands.

```
/xpevent help
```

| | |
|---|---|
| **Permission** | Player |
