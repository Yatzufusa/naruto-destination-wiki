# Frequently Asked Questions

---

## General

### Can I play this mod in Singleplayer?

Yes! Naruto Destination is fully playable in singleplayer. For the storyline you'll need Mathioks' original mod, but we're adding traders and new enemies so you can get everything in survival.

### Is this an addon or a rework?

Naruto Destination is a **multiplayer-focused rework** of the Mathioks Naruto Anime Mod. It also includes features like tokens and randomizers from well-known addons like Greg's Stardust addon.

### How did Jutsus change?

All jutsus now **scale in damage and cost** with certain stats from the Ninja Info Card. We've also added a **mastery system** so you can train and improve your favourite jutsus. All of this is configurable for server owners and in your personal world.

### What are the benefits for servers?

- Tokens and randomizers for everything
- Greatly improved performance for clients and servers
- Almost everything is configurable, including all jutsus and modes — every server can have its own meta
- A highly configurable in-game wiki you can adjust to your server
- Many multiplayer-related improvements and fixes

### How do I get the mod for my server?

Just download it from the official Discord and drop it into your server's `mods/` folder. The mod **installs all dependencies automatically** on first startup.

See the [Server Setup Guide](setup/index.md) for a complete walkthrough.

---

## Singleplayer Progression

### How do I get modes, releases, and other unlocks in singleplayer?

There's a new type of trader called the **Randomizer Trader**. They sell almost everything available in the game — natures, sage modes, tailed beasts, and more.

### How do I get and use DNA in survival?

There are two ways:

1. **Enemy drops** — Some stronger mod enemies drop DNA
2. **Traders** — Buy DNA from different kinds of traders

To use DNA:

1. **Identify** it first (higher Intelligence gives better results)
2. **Implant** it into yourself with right-click, or into others with sneak + left-click

You can also "re-roll" DNA by crafting 2 identified DNA together to get an unidentified one back (configurable in [DNAConfig](config/dna-tokens.md)).

### How does the XP/leveling system work?

We changed the old system of mobs giving XP directly on kill being the only method of leveling. Now mobs have a **chance to drop different kinds of tokens**, including XP tokens. This also lets you set up proper mob farms for tokens if you want to.

### How do I rank up in singleplayer?

There's a configurable, linear rank-up system ingame. Reach a level threshold and click on the button next to your rank in the Ninja Info Card.

### Does the mission/quest system work in singleplayer?

No. We completely removed the quest system to make the mod more suitable for multiplayer, which was our first priority.

### Can Orochimaru still spawn to get curse marks?

No. We removed all old mobs from spawning in the world and are continuously replacing them with our own which fit our style more. Use Randomizer Traders to obtain curse marks.

### Can I get Truth Seeking Orbs in singleplayer?

Currently there is no way to get the orbs in singleplayer due to our rework of the Tailed Beast Chakra Mode / Six Paths Sage Mode features.

### Why don't weapon recipes show up in JEI/NEI?

There are almost no crafting recipes for weapons in the mod. We're slowly adding enemies that drop them instead.

---

## Game Mechanics

### What do the different modes do?

All modes now give stacking **Damage Multipliers** and **Resistance Multipliers** instead of non-stacking Strength and Resistance potion effects. You can configure the different multipliers for each mode in the `ModeConfig.cfg`.

Modes also have secondary effects:

| Mode | Secondary Effects |
|------|-------------------|
| Byakugan | Entity detection |
| Tenseigan | Night vision |
| Curse Mark | Jump boost |
| *...and more* | |

### Are Tailed Beast Chakra Modes available? What about Sage of Six Paths mode?

Both are currently being worked on. Six Paths Sage Mode is disabled right now for this reason.

### Do the different Karma seals have different strengths?

Yes! Each Karma seal type has **different damage multipliers** configured in `ModeConfig.cfg`. Check the config and adjust to your liking.

---

## Configuration

### Can I configure mob spawn weights/rates?

Not yet, but this is planned for a future update.

### Can I configure how much chakra the chakra scrolls give?

Not yet, but this is planned for the near future.

### Where are all the config files?

All config files are generated in `config/NarutoDestination/` on first startup. See the [Configuration Reference](config/index.md) for a detailed breakdown of every config file.

---

## Integration & Technical

### How do I use CustomNPC scripts with the mod?

Check out the [Naruto Destination Scripting API](https://yatzufusa.github.io/naruto-destination-cnpc-scripting-api/) for all currently available jutsus and methods to integrate them with CustomNPC+.

### I'm experiencing texture bugs with my skin when I unlock Dojutsu

This is caused by the **FoamFix** mod. Remove it from your modpack to fix the issue. See [Mods to Avoid](setup/mods.md#mods-to-avoid) for more details.
