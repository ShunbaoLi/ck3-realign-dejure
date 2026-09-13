# CK3 Realign Vassal De Jure (更定封臣法理)

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-ck3--realign--dejure-181717.svg?logo=github)](https://github.com/ShunbaoLi/ck3-realign-dejure)
[![Changelog](https://img.shields.io/badge/Changelog-Keep_a_Changelog-blueviolet.svg)](CHANGELOG.md)
[![CK3 Version](https://img.shields.io/badge/CK3_Version-1.18%20%7C%201.19+-orange.svg)](https://ck3.paradoxwikis.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**[简体中文](README.md) | [English](README.en.md)**

</div>

---

## 📌 About the Project

**CK3 Realign Vassal De Jure** is a quality-of-life utility mod designed for *Crusader Kings III*.

In long campaigns and overhauls (such as East Asia/TGP or Byzantine administrative realms), dynastic marriages, successions, conquests, and internal transfers frequently cause vassal lands to become fragmented, riddled with enclaves, and de jure disconnected.

This mod introduces a sovereign **Imperial Boundary Decree** right-click character interaction. Lieges can easily and permanently realign all territories ruled by their vassals into the de jure realm of the vassal's primary title with a single click. Furthermore, emperors can directly incorporate king vassals' kingdoms into their imperial de jure borders without waiting for centuries of de jure drift.

> 📜 **Complete Version History & Changes**: See [CHANGELOG.md](CHANGELOG.md).

---

## ⚔️ Feature Matrix

| Target Scope | Trigger Condition | Execution Effect | Purpose & Scope |
| :--- | :--- | :--- | :--- |
| **Dukes / Jiedushi** (`tier_duchy`) | Non-de jure counties exist under their direct or vassal domain | Realigns all counties held by the duke or their subordinate vassals **instantly and permanently into the duke's primary title de jure** | Eliminates duchy-level enclaves and border gore |
| **Kings / Protectorates** (`tier_kingdom`) | Non-de jure duchies exist under their direct or vassal domain | Realigns all duchies held by the king or their subordinate vassals **instantly and permanently into the king's primary title de jure** | Reconstructs grand vassal borders and regional administrative zones |
| **Emperors over King Vassals** (`tier_empire`) | King's kingdom is not yet de jure part of the liege's empire | Realigns the kingdom title **instantly and permanently into the emperor's primary imperial de jure** | Unifies the imperial realm without waiting for 100-year drift |

---

## ⚙️ Game Rules Configuration

Freely configure the cost balance in the game rules at the start of a new campaign:

- **Free / Sandbox Mode (Default)**:
  - No prestige or legitimacy cost.
  - No Crown Authority level requirements.
- **Realistic / Balanced Mode**:
  - Each realignment decree costs **150 Prestige** and **50 Legitimacy**.
  - Requires the liege to hold **Medium Crown Authority (Level 2) or higher**.

---

## 🏛️ DLC & Government Compatibility

Built with a **purely additive architecture**, this mod touches no vanilla files and guarantees zero conflicts:

| System / Government | Status | Details |
| :--- | :---: | :--- |
| **All DLCs** | Supported | Native compatibility with *The Golden Peacock* (TGP), *Roads to Power*, *Legends of the Dead*, and future releases |
| **Celestial Empire (TGP)** | Supported | Supports Jiedushi, Duhufu, and Chinese imperial bureaucracy |
| **Byzantine Administrative** | Supported | Supports Strategoi, themes, and imperial administrative laws |
| **Feudal / Clan / Tribal / Nomadic** | Supported | Balanced mode supports all authority law ladders |
| **Save Game Compatibility** | Supported | Safe to enable or disable in ongoing saves at any time |

---

## 📦 Installation Guide

### Option 1: Steam Workshop (Recommended)
Subscribe to the mod on the Steam Workshop, then enable it in your Paradox Launcher playset.

### Option 2: Manual Local Installation
1. Download the latest release from GitHub and extract the archive.
2. Place the folder into your local CK3 mod directory:
   - **Windows**: `Documents\Paradox Interactive\Crusader Kings III\mod\ck3realigndejure`
   - **Linux**: `~/.local/share/Paradox Interactive/Crusader Kings III/mod/ck3realigndejure`
   - **macOS**: `~/Documents/Paradox Interactive/Crusader Kings III/mod/ck3realigndejure`
3. Ensure `ck3realigndejure.mod` is copied to the parent `mod/` directory.
4. Launch Crusader Kings III and activate the mod in the launcher.

---

## 🤝 Community & Contributions Welcome

If you encounter any edge cases or would like to propose new features:

1. **Open an Issue**: Report issues or suggestions on [GitHub Issues](https://github.com/ShunbaoLi/ck3-realign-dejure/issues).
2. **Submit a Pull Request**:
   - Fork the repository and create a feature branch.
   - Ensure all `.txt` and `.yml` files are encoded in **UTF-8 with BOM**.
   - Note changes in [CHANGELOG.md](CHANGELOG.md) under `[Unreleased]`.

---

## 📜 License

Distributed under the [MIT License](LICENSE).  
Copyright (c) 2026 ShunbaoLi.
