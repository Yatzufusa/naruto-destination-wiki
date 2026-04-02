# Experience & Leveling Configuration

---

## NarutoEXPConfig.cfg

Controls XP rates, rank multipliers, and level-up rewards. This is one of the most important configs for server balance.

### Global XP Multiplier

| Setting | Default | Description |
|---------|---------|-------------|
| `General EXP Multiplier` | `1.0` | Global multiplier applied to all XP gain |

!!! tip
    Set this higher for faster progression (e.g., `2.0` for double XP) or lower for a grindier experience.

### Rank XP Multipliers

Each Ninja Info Card rank has its own XP multiplier. Higher-ranked players earn XP faster.

#### Standard Ranks

| Rank | Default Multiplier |
|------|--------------------|
| Academy Student | 1.0x |
| Villager | 1.0x |
| Genin | 1.1x |
| Chunin | 1.2x |
| Tokubetsu Jonin | 1.3x |
| Jonin | 1.4x |
| Samurai | 1.2x |

#### Special Ranks

| Rank | Default Multiplier |
|------|--------------------|
| Missing-Nin | 1.5x |
| Rogue | 1.5x |
| Anbu | 1.5x |
| Medical Team | 1.5x |
| Intel Team | 1.5x |
| Anbu Captain | 1.6x |
| Medical Captain | 1.6x |
| Intel Captain | 1.6x |
| of the Bloody Mist | 1.6x |

#### Elite Ranks

| Rank | Default Multiplier |
|------|--------------------|
| Explosion Corps | 1.7x |
| Taka | 1.7x |
| Hebi | 1.7x |
| Puppet Brigade | 1.7x |
| 7 Ninja Swordsmen | 1.8x |
| Sannin | 1.9x |
| Kinkaku Force | 1.9x |
| 12 Guardian Ninja | 1.9x |
| Advisor | 1.9x |
| Shadow Kage | 1.95x |

#### Kage-Level Ranks

| Rank | Default Multiplier |
|------|--------------------|
| Kage | 2.0x |
| Hokage | 2.0x |
| Kazekage | 2.0x |
| Mizukage | 2.0x |
| Tsuchikage | 2.0x |
| Raikage | 2.0x |
| Akatsuki | 2.0x |
| Senior Akatsuki | 2.0x |
| Akatsuki Leader | 2.0x |
| White Fang | 2.0x |
| of the Sharingan | 2.0x |
| Yellow Flash | 2.0x |
| Green Beast | 2.0x |

#### Power Tiers (Additional Multipliers)

| Tier | Default Multiplier |
|------|--------------------|
| D-Rank | 1.1x |
| C-Rank | 1.2x |
| B-Rank | 1.3x |
| A-Rank | 1.5x |
| S-Rank | 1.7x |
| Tailed Beast | 2.0x |

### Level-Up Rewards

| Setting | Default | Description |
|---------|---------|-------------|
| `XP For First Level` | `1` | XP required for level 1 |
| `XP Increase` | `0.25` | How much the XP requirement increases per level |
| `SP per Level Up` | `3` | Skill Points awarded per level |
| `JP per Level Up` | `4` | Jutsu Points awarded per level |
| `Reset Point Interval` | `500` | Levels between Reset Point grants |
| `Reset Point Amount` | `1` | Reset Points given per interval |

!!! info "XP Scaling Formula"
    XP required for level N = `XP For First Level` + (`XP Increase` x N)

    With defaults: Level 100 requires `1 + (0.25 × 100) = 26` XP.

---

## LearnerConfig.cfg

Configures the **Skill Learner** progression trees. Each skill learner (Kenjutsu, Medical, Taijutsu) has multiple progression steps.

For each step you can configure:

| Setting Pattern | Description |
|-----------------|-------------|
| `{Step}_Enabled` | Whether this step is available |
| `{Step}_Cost` | JP cost to unlock this step |

!!! tip
    The learner config is dynamically generated based on discovered learners. Start the server once to generate the default values, then customize the costs and toggle steps on/off.
