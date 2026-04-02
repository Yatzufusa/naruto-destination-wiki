# Combat & Enemies Configuration

---

## TaijutsuConfig.cfg

Controls fist-fighting damage and Eight Gates requirements.

### Fist Damage

| Setting | Default | Description |
|---------|---------|-------------|
| `TaijutsuBaseDamage` | `1` | Base damage from fist attacks (no Taijutsu stat) |
| `TaijutsuScaling` | `0.04` | Additional damage per point of Taijutsu |

!!! info "Damage Formula"
    Fist damage = `TaijutsuBaseDamage` + (`TaijutsuScaling` x Taijutsu stat)

    Example: A player with 500 Taijutsu deals `1 + (0.04 × 500) = 21` fist damage.

### Eight Gates Requirements

Each gate has two requirement types — a **static** Taijutsu threshold and a **percentage** of max Taijutsu.

| Gate | Static Default | Percentage Default |
|------|----------------|--------------------|
| First Gate | 100 | 0.05 (5%) |
| Second Gate | 250 | 0.10 (10%) |
| Third Gate | 500 | 0.15 (15%) |
| Fourth Gate | 750 | 0.25 (25%) |
| Fifth Gate | 1500 | 0.40 (40%) |
| Sixth Gate | 2500 | 0.55 (55%) |
| Seventh Gate | 4000 | 0.75 (75%) |
| Eighth Gate | 5000 | 0.95 (95%) |

Each gate also has a `MinCharge` value for the minimum charge required to activate it.

---

## KenjutsuConfig.cfg

Controls sword technique damage scaling, static damage, and cooldowns.

### Techniques

| Technique | Scaling | Static Damage | Cooldown (ticks) |
|-----------|---------|---------------|------------------|
| HeavenCutter | 0.08 | 5 | 100 |
| CrescentMoon | 0.09 | 5 | 100 |
| ShockwaveSlash | 0.06 | 5 | 100 |
| Moonlight | 0.07 | 5 | 100 |
| Flash | 0.10 | 5 | 100 |

!!! info "Damage Formula"
    Technique damage = `Static Damage` + (`Scaling` x Kenjutsu stat)

    Example: Flash with 500 Kenjutsu = `5 + (0.10 × 500) = 55` damage.

---

## MedicalConfig.cfg

Controls Byakugou (Strength of a Hundred Seal) stage requirements.

### Byakugou Stages

| Stage | Name | Static Req. | % Req. | Min Charge |
|-------|------|-------------|--------|------------|
| 2 | Creation Rebirth | 500 | 0.05 (5%) | 10 |
| 3 | Strength of a Hundred | 1000 | 0.12 (12%) | 25 |

!!! note
    `BaseHealthRegeneration` and `PercentageHealthRegeneration` exist in this config but are currently unused.

---

## EnemyConfig.cfg

Controls enemy spawning, health, damage, speed, and aggro range. Each enemy type has its own configuration section.

### Master Toggle

| Setting | Default | Description |
|---------|---------|-------------|
| `MasterSpawnToggle` | `true` | Global on/off for all enemy spawning |

### Enemy Types

Each enemy has the following configurable values:

| Setting | Description |
|---------|-------------|
| `Spawn` | Enable/disable this enemy's spawning |
| `Health` | Enemy max health |
| `MeleeDamage` | Base melee damage |
| `MovementSpeed` | Movement speed |
| `AggroRange` | Distance (blocks) at which the enemy detects players |

### Default Values

| Enemy | Health | Damage | Speed | Aggro |
|-------|--------|--------|-------|-------|
| Genin | 30 | 2.0 | 0.4 | 20 |
| Chunin | *varies* | *varies* | *varies* | *varies* |
| Jonin | *varies* | *varies* | *varies* | *varies* |
| Rock Lee | *varies* | *varies* | *varies* | *varies* |
| Sakura Haruno | *varies* | *varies* | *varies* | *varies* |
| Hidan | *varies* | *varies* | *varies* | *varies* |
| Orochimaru | *varies* | *varies* | *varies* | *varies* |
| Seven Swordsmen | *varies* | *varies* | *varies* | *varies* |

!!! info "Seven Swordsmen"
    The Seven Swordsmen have an additional setting: `MinKenjutsuToSpawn` (default: `500`). They only spawn near players who meet this Kenjutsu threshold.

!!! tip "Balancing Enemies"
    Start by adjusting Genin and Chunin stats for early-game balance, then scale Jonin and above for endgame. Use `MasterSpawnToggle: false` during initial server setup.
