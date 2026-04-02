# Kage Vote - Admin Commands

Administrative commands for managing Kage elections. All require **OP (level 2)**.

---

## `/kagevote start`

Start a new **Kage election** for a village.

```
/kagevote start <affiliation> <duration>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The village holding the election |
| `duration` | How long the election lasts |

**Duration Formats:**

| Format | Example | Meaning |
|--------|---------|---------|
| `Nm` | `30m` | 30 minutes |
| `Nh` | `2h` | 2 hours |
| `Nd` | `1d` | 1 day |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteStart` |

!!! example
    ```
    /kagevote start Konoha 2h
    /kagevote start Sunagakure 1d
    ```

---

## `/kagevote end`

**Conclude** an active election and declare the winner as the new Kage.

```
/kagevote end <affiliation>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The village whose election to conclude |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteEnd` |

!!! info
    The candidate with the most votes wins. If there's a tie, refer to your server's configured tiebreaker rules.

---

## `/kagevote cancel`

**Cancel** an active election without declaring a winner.

```
/kagevote cancel <affiliation>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The village whose election to cancel |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteCancel` |

!!! warning
    Cancelling discards all votes and candidate registrations for that election.

---

## `/kagevote add`

Manually **add a player** as a candidate to an election.

```
/kagevote add <affiliation> <player>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The village election to add them to |
| `player` | The player to register as a candidate |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteAdd` |

---

## `/kagevote remove`

**Remove a candidate** from an active election.

```
/kagevote remove <affiliation> <player>
```

| Parameter | Description |
|-----------|-------------|
| `affiliation` | The village election |
| `player` | The candidate to remove |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteRemove` |

---

## `/kagevote ban`

**Ban a player** from running as a candidate in any future election.

```
/kagevote ban <player>
```

| Parameter | Description |
|-----------|-------------|
| `player` | The player to ban |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteBan` |

---

## `/kagevote unban`

**Remove a ban**, allowing the player to run as a candidate again.

```
/kagevote unban <player>
```

| Parameter | Description |
|-----------|-------------|
| `player` | The player to unban |

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteUnban` |

---

## `/kagevote reload`

**Reload** the Kage Vote configuration from disk.

```
/kagevote reload
```

| | |
|---|---|
| **Permission** | OP (level 2) |
| **Source** | `CommandKageVoteReload` |
