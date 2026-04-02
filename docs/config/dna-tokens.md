# DNA & Tokens Configuration

---

## DNAConfig.cfg

One of the most complex config files. Controls DNA identification, implantation, drop rates, and success chances.

### DNA Combination Recipe

Allows players to combine identified DNA back into unidentified DNA for re-rolling.

| Setting | Default | Description |
|---------|---------|-------------|
| `EnableDNACombinationRecipe` | `true` | Allow crafting DNA together |
| `DNACombinationRequiredAmount` | `2` | Number of DNA needed to combine (1-9) |

### DNA Identification

Controls the Intelligence-based identification system.

| Setting | Default | Description |
|---------|---------|-------------|
| `MinimumIntelligenceToIdentify` | `20` | Minimum Intelligence to identify DNA at all |
| `IntelligenceThresholds` | `[20, 40, 60, 80, 90, 100]` | Intelligence breakpoints for better results |
| `IdentificationSuccessChances` | `[1, 5, 15, 25, 50, 70]` | Success chance (%) at each threshold |

!!! info "How Identification Works"
    At each Intelligence threshold, the player gets the corresponding success chance. A player with 80 Intelligence has a 25% chance of successful identification. Higher Intelligence = better odds.

### DNA Type Probabilities

| Setting | Default | Description |
|---------|---------|-------------|
| `NatureReleaseProbability` | `90` | Chance (%) that random DNA is a Nature Release |
| `OtsutsukiChanceWithinKekkeiGenkai` | `5` | Chance (%) that a KKG result is Otsutsuki instead |

This means there's a `10%` chance of getting a Kekkei Genkai, and within that, a `5%` chance of Otsutsuki — making Otsutsuki DNA extremely rare (`0.5%` overall).

### DNA Type Toggles

Enable or disable specific DNA types from dropping. All default to `true`.

=== "Nature Releases"

    | Toggle | DNA Type |
    |--------|----------|
    | `EnableFireRelease` | Fire Release |
    | `EnableWaterRelease` | Water Release |
    | `EnableWindRelease` | Wind Release |
    | `EnableLightningRelease` | Lightning Release |
    | `EnableEarthRelease` | Earth Release |
    | `EnableYinRelease` | Yin Release |
    | `EnableYangRelease` | Yang Release |

=== "Kekkei Genkai"

    | Toggle | DNA Type |
    |--------|----------|
    | `EnableWoodRelease` | Wood Release |
    | `EnableIceRelease` | Ice Release |
    | `EnableLavaRelease` | Lava Release |
    | `EnableBoilRelease` | Boil Release |
    | `EnableMagnetRelease` | Magnet Release |
    | `EnableStormRelease` | Storm Release |
    | `EnableExplosionRelease` | Explosion Release |
    | `EnableScorchRelease` | Scorch Release |
    | `EnableDustRelease` | Dust Release |
    | `EnableCrystalRelease` | Crystal Release |
    | `EnableSteelRelease` | Steel Release |
    | `EnableKurama` | Kurama Clan |
    | `EnableShikotsumyaku` | Shikotsumyaku |
    | `EnableIburi` | Iburi Clan |

=== "Dojutsu"

    | Toggle | DNA Type |
    |--------|----------|
    | `EnableSharingan` | Sharingan |
    | `EnableByakugan` | Byakugan |
    | `EnableKetsuryugan` | Ketsuryugan |

=== "Otsutsuki"

    | Toggle | DNA Type |
    |--------|----------|
    | `EnableOtsutsukiDNA` | Otsutsuki DNA |

### DNA Implantation Requirements

Minimum Medical stat needed to implant each DNA tier.

| Setting | Default | Description |
|---------|---------|-------------|
| `MinimumMedicalForNatureImplant` | `50` | Medical needed for Nature Release DNA |
| `MinimumMedicalForKekkeiGenkaiImplant` | `300` | Medical needed for KKG DNA |
| `MinimumMedicalForDojutsuImplant` | `500` | Medical needed for Dojutsu DNA |
| `MinimumMedicalForOtsutsuki` | `10000` | Medical needed for Otsutsuki DNA |
| `MinimumMedicalForOtsutsukiAsOtsutsuki` | `0` | Medical needed if already Otsutsuki |

### Implant Success Chances

| Setting | Default | Description |
|---------|---------|-------------|
| `MedicalThresholds` | `[300, 400, 500]` | Medical stat breakpoints |
| `ImplantSuccessChances` | `[20, 40, 70]` | Success chance (%) at each threshold |

### Potion Effects on Implant

Both successful and failed implants apply debuffs. All settings are configurable.

=== "Success Effects"

    | Setting | Default |
    |---------|---------|
    | `SuccessEffectDuration` | `200` ticks (10 seconds) |
    | `SuccessDigSlowLevel` | `5` |
    | `SuccessConfusionLevel` | `50` |
    | `SuccessMoveSlowLevel` | `5` |
    | `SuccessWeaknessLevel` | `50` |

=== "Failure Effects"

    | Setting | Default |
    |---------|---------|
    | `FailureEffectDuration` | `600` ticks (30 seconds) |
    | `FailureDigSlowLevel` | `5` |
    | `FailureConfusionLevel` | `50` |
    | `FailureMoveSlowLevel` | `5` |
    | `FailureWeaknessLevel` | `50` |
    | `FailurePoisonLevel` | `1` |

---

## TokenConfig.cfg

Controls the SP, JP, and XP cost of using each randomizer token type.

### Token Costs by Type

| Token Type | SP Cost | JP Cost | XP Cost |
|------------|---------|---------|---------|
| **Clan** | 10 | 10 | 10 |
| **Nature** | 5 | 5 | 5 |
| **Kekkei Genkai** | 20 | 20 | 20 |
| **Dojutsu** | 30 | 30 | 30 |
| **Tailed Beast** | 100 | 100 | 1000 |

!!! tip
    Tailed Beast tokens are deliberately expensive. Adjust these values to control how easily players can acquire powerful randomizers on your server.
