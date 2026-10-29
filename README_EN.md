<p align="center"><img src="src/main/resources/logo.png" alt="Suitcase Glider logo" width="180"></p>

# Suitcase Glider
**A suitcase that unfolds into a glider when the ground gets too close.**

[![Minecraft](https://img.shields.io/badge/Minecraft-1.20.1-62B47A?style=flat-square)](https://www.minecraft.net/)
[![Forge](https://img.shields.io/badge/Forge-47.4.28-e88348?style=flat-square)](https://files.minecraftforge.net/)
![Java 17](https://img.shields.io/badge/Java-17-596C8C?style=flat-square)
![Version 0.1.0](https://img.shields.io/badge/Version-0.1.0-4D7CAB?style=flat-square)

[**Русский**](README.md) · **English** · [Download the mod](https://github.com/Deenfoool/suit-case-glider/raw/refs/heads/main/suitcaseglider-0.1.0.jar) · [Report an issue](https://github.com/Deenfoool/suit-case-glider/issues)

---

## 🎒 About

**Suitcase Glider** is a Minecraft Java Edition mod that turns a handheld suitcase into an automatically deploying glider. Keep it selected in your **main hand**: when a dangerous fall is detected, its wings unfold to slow your descent. Normal short jumps do not trigger it.

Unlike Elytra, the suitcase is designed for **controlled descent**, not climbing or firework-powered flight. Your armor slots stay free.

## ✨ Features

- **Automatic deployment** based on fall distance and clearance to the surface.
- **Controlled descent** guided by your view direction; the glider folds on landing.
- **Custom 3D model and animations** for carrying, opening, gliding, and folding.
- **Dyeable fabric** with a crafting-grid dye recipe; the frame keeps its color.
- **Durability and repair:** 192 durability points, wear during gliding, repair with leather.
- **Enchantments:** Unbreaking and **Soaring I–III**; Soaring reduces descent speed.
- **Multiplayer support:** glider state is synchronized between server and clients.

**Controls:** hold the suitcase in your main hand. No separate deploy key is needed. Switching items ends the glide. Both hands are occupied during flight, and attacks/interactions are blocked.

## 🧵 Crafting recipe

| Leather | Leather | Leather |
|:---:|:---:|:---:|
| Stick | String | Stick |
| Stick | Empty | Stick |

Craft the suitcase at a regular crafting table. Combine it with a dye to recolor its fabric.

## 📥 Installation

| Requirement | Version |
|---|---|
| Minecraft Java Edition | **1.20.1** |
| Minecraft Forge | **47.4.28** (development/build version) |
| Java for building | **JDK 17** |
| Additional mods | **None** |

1. Install Minecraft Forge for **Minecraft 1.20.1**.
2. Download [**Suitcase Glider 0.1.0 (.jar)**](https://github.com/Deenfoool/suit-case-glider/raw/refs/heads/main/suitcaseglider-0.1.0.jar).
3. Place the JAR in the `mods` folder of your Forge profile.
4. Launch Minecraft using that profile.

For multiplayer, **both the server and connecting players** need the mod. The downloadable JAR in this repository is not rebuilt automatically when source files change.

## 🛠 Building from source

You need **JDK 17** and an internet connection to fetch Gradle dependencies.

```powershell
# Windows PowerShell
.\gradlew.bat build
```

```bash
# Linux / macOS
./gradlew build
```

Output: `build/libs/`.

Development checks:

```powershell
.\gradlew.bat test
.\gradlew.bat runServer -Psmoke
```

The `-Pvisual` and `-Prendercheck` modes are intended **only for development**, using a separate test world. Included tests have not been asserted to pass in every environment.

## 🗂 Project layout

```text
src/main/java/dev/salum/suitcaseglider/   Game logic, glider item, networking, client renderer
src/main/resources/                        Models, animations, textures, localization, recipes
src/test/                                  Flight-policy tests
gradle/                                    Gradle Wrapper
build.gradle                               Build configuration
gradle.properties                          Version and mod metadata
README_RU.md                               Detailed notes (Russian)
```

Editable `.bbmodel` files referenced by [the original Russian documentation](README_RU.md) are **not currently included** in this repository; the runtime animation data `glider_scene.json` is included.

## 📄 Licensing & feedback

The [mod metadata](gradle.properties) declares **All Rights Reserved**. The license of Minecraft Forge does **not** automatically apply to this mod's own source code.

Please [open an issue](https://github.com/Deenfoool/suit-case-glider/issues) for bugs or feature requests. Include your Minecraft and Forge versions, reproduction steps, and a log if available.

[Version notes](CHANGELOG.md) · [Русская версия](README.md) · [Detailed technical notes (RU)](README_RU.md)
