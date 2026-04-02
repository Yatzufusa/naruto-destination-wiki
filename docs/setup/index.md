# Server Setup Guide

This guide walks you through setting up a **Naruto Destination** server from scratch, including the recommended server jar, plugins, and client modpack.

---

## Prerequisites

- **Minecraft 1.7.10**
- **Java 8** (required for Forge 1.7.10)
- A server machine or hosting service

---

## Step 1: Server Jar

We strongly recommend using **Crucible** as your server jar. Crucible is a maintained fork for Forge 1.7.10 that provides Bukkit/Spigot plugin support alongside Forge mods.

[:octicons-download-16: Download Crucible v5.4](https://github.com/CrucibleMC/Crucible/releases/tag/v5.4){ .md-button .md-button--primary }

!!! warning "Libraries Folder"
    If you use Crucible, you **must** also replace your `libraries/` folder with the one provided in our server starter package. Without this, the server may fail to start or have compatibility issues.

### Setting Up Crucible

1. Download `Crucible.jar` from the link above (or use the one in our starter package)
2. Place it in your server root directory
3. Replace the `libraries/` folder with the one from the starter package
4. Create a start script:

    ```bash
    java -Xmx4G -Xms2G -jar Crucible.jar nogui
    ```

5. Run the server once to generate config files, then stop it
6. Accept the EULA in `eula.txt`

---

## Step 2: Install Naruto Destination

1. Download the latest version of the mod from the official Discord channel
2. Place the `.jar` file into your server's `mods/` folder
3. Start the server — the mod **automatically installs all dependencies** on first startup
4. Place the same `.jar` into your client modpack's `mods/` folder

!!! important "Version Matching"
    Only the **two major version numbers** need to match between server and client.

    For example, with version `1.16.2`:

    - Server: `1.16.2` and Client: `1.16.5` — **Compatible** (both `1.16`)
    - Server: `1.16.2` and Client: `1.17.0` — **Not compatible** (different minor version)

---

## Step 3: Plugins

Since Crucible supports Bukkit/Spigot plugins, here are the recommended plugins for your server:

[:octicons-arrow-right-24: Full plugin list with download links](plugins.md)

| Plugin | Purpose |
|--------|---------|
| **Essentials** | Core server management (spawn, homes, kits, economy) |
| **WorldGuard** | Region protection |
| **WorldEdit** | Map building tools |
| **PermissionsEx** | Permission management for commands and features |
| **GriefPrevention** | Player land claiming |
| **GreatKits** | Daily kit system |
| **MagicSpells** | Apply commands to items |

---

## Step 4: Client Modpack

Set up a modpack for your players with the Naruto Destination mod and recommended companion mods.

[:octicons-arrow-right-24: Full mod list with download links](mods.md)

---

## Step 5: Configuration

After first startup, the mod generates config files in `config/NarutoDestination/`. These control everything from XP rates to jutsu damage.

[:octicons-arrow-right-24: Configuration Reference](../config/index.md)

---

## Starter Package

We provide a ready-made starter package in the official Discord that includes:

- `Crucible.jar` server jar
- Pre-configured `libraries/` folder
- Example server and plugin configs
- CustomNPC+ animations, NPC examples, and textures

Check the announcements channel in our Discord for the download link.
