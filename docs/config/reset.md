# Reset System Configuration

## ResetConfig.cfg

Controls what happens when a player is reset (via `/resetplayer` or the reset system). This includes stat retention rates based on ranking and what progression elements are kept.

---

### Stat Retention by Rank

When a player is reset, they retain a **percentage** of their stats based on their server ranking. Top-ranked players keep more of their progress.

These settings apply separately to **Skill Points**, **Jutsu Points**, and **Levels** (each has its own category with the same structure).

| Rank Position | Default Retention |
|---------------|-------------------|
| Rank 1 | 5.0% |
| Rank 2 | 4.5% |
| Rank 3 | 4.0% |
| Rank 4 | 3.5% |
| Rank 5 | 3.0% |
| Rank 6 | 2.5% |
| Rank 7 | 2.0% |
| Rank 8 | 1.8% |
| Rank 9 | 1.6% |
| Rank 10 | 1.4% |
| Rank 11+ | 1.0% |

!!! info
    Retention is a float between `0.0` (keep nothing) and `1.0` (keep everything). The default of `0.05` for Rank 1 means the #1 ranked player keeps 5% of their stats after a reset.

---

### What to Keep on Reset

| Setting | Default | Description |
|---------|---------|-------------|
| `Keep Clan` | `false` | Preserve the player's clan after reset |
| `Keep Affiliation` | `false` | Preserve the player's village after reset |
| `Keep Land` | `false` | Preserve the player's land after reset |
| `Keep Rank` | `false` | Preserve the player's rank after reset |
| `Keep Known Clans` | `false` | Preserve discovered clan knowledge |
| `Keep Known Bijuu` | `false` | Preserve discovered bijuu knowledge |

!!! tip
    Most servers set `Keep Affiliation` and `Keep Clan` to `true` so players don't lose their village identity on reset, while resetting all combat stats.

---

### Ranking Method

Determines which stat is used to calculate a player's rank position for retention purposes.

| Setting | Default | Description |
|---------|---------|-------------|
| `Ranking Method` | `"TOTAL_STATS"` | How to rank players |

**Valid values:**

| Value | Ranks By |
|-------|----------|
| `TOTAL_STATS` | Sum of all combat stats |
| `LEVEL` | Naruto level |
| `NINJUTSU` | Ninjutsu stat |
| `TAIJUTSU` | Taijutsu stat |
| `GENJUTSU` | Genjutsu stat |
| `KENJUTSU` | Kenjutsu stat |
| `SHURIKENJUTSU` | Shurikenjutsu stat |
| `SUMMONING` | Summoning stat |
| `KINJUTSU` | Kinjutsu stat |
| `SENJUTSU` | Senjutsu stat |
| `MEDICAL` | Medical stat |
