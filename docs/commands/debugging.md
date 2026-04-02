# Debugging Tools

Commands for server administrators to debug and inspect mod state.

---

## `/around`

Show all **entities** around your current position. Useful for debugging mob spawns and entity issues.

```
/around
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandAround` |

---

## `/learner`

Grant a player specific **learner** abilities.

```
/learner <release|all|known> <player>
```

| Parameter | Description |
|-----------|-------------|
| `release` | Give a specific release learner |
| `all` | Give all learners |
| `known` | Give learners for known releases |
| `player` | Target player name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandLearner` |

---

## `/narutoconfigreload`

Reload **all Naruto mod configuration files** without restarting the server.

```
/narutoconfigreload
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandNarutoConfigReload` |

!!! tip
    Use this after editing config files on disk to apply changes live.

---

## `/nbt`

Print a player's **NBT data** directly to the server console for inspection.

```
/nbt [player]
```

| Parameter | Description |
|-----------|-------------|
| `player` | Target player (optional, defaults to self) |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandNbt` |

!!! info
    Output goes to the **server console**, not in-game chat. Server owners use this to verify player stats and debug data issues.

---

## `/reloadwiki`

Reload the **in-game wiki** and resend it to all connected players.

```
/reloadwiki
```

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandReloadWiki` |

---

## `/resetplayer`

**Reset a player's Naruto stats entirely.** This wipes all progress.

```
/resetplayer <uuid|name>
```

| Parameter | Description |
|-----------|-------------|
| `uuid\|name` | Target player UUID or name |

| | |
|---|---|
| **Permission** | OP |
| **Source** | `CommandResetPlayer` |

!!! danger
    This is **irreversible**. The player will lose all Naruto-related progress including levels, jutsu, releases, dojutsus, and points. Use with extreme caution.
