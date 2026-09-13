# 更新日志 (Changelog)

All notable changes to this project will be documented in this file.  
本项目的所有重要更新均记录于此文件。

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased] - 待发布
<!-- 社区贡献者请将新功能或修复直接追加到下方对应分类中 / Contributors, please append changes below -->

### Added
### Fixed
### Changed

---

## [1.0.0] - 2026-09-13
### Added
- **更定封臣法理核心机制 (Core De Jure Realignment Mechanism)**：
  - [CN] 引入领主右键封臣交互“更定封臣法理”（`realign_vassal_dejure_interaction`），归类于封臣交互（`interaction_category_vassal`）。
  - [EN] Introduced sovereign vassal right-click character interaction "Realign Vassal De Jure" (`realign_vassal_dejure_interaction`).
  - [CN] 支持公爵/节度使封臣：一键将其直辖或下属非本法理伯爵领全部勘定归属于其主公国法理。
  - [EN] Supported Duchy/Jiedushi tier vassals: Realign all directly held or vassal counties into the de jure realm of their primary duchy.
  - [CN] 支持国王/都护府封臣：一键将其直辖或下属非本法理公国全部勘定归属于其主王国法理。
  - [EN] Supported Kingdom/Protectorate tier vassals: Realign all directly held or vassal duchies into the de jure realm of their primary kingdom.
  - [CN] 支持帝国领主与王国封臣：允许皇帝将王国封臣的王国法理即时划归玩家的帝国主头衔法理。
  - [EN] Supported Emperor liege over King vassals: Seamlessly integrate the king's kingdom title into the emperor's imperial de jure.
- **全 DLC 与全政体深度兼容 (Full DLC & Government Compatibility)**：
  - [CN] 零原版文件覆写（纯追加模式），原生完美兼容原版封建制、部落制、游牧制、拜占庭行政制及《东亚与帝国》（TGP）中华天朝政体、考课官僚制与日本幕府制。
  - [EN] Zero vanilla file overwrites (pure additive architecture). Fully compatible with Feudal, Clan, Tribal, Nomadic, Byzantine Administrative, and TGP Celestial / Meritocratic / Japanese Bureaucracies.
- **游戏规则系统 (Game Rules Configuration)**：
  - [CN] 增加“更定封臣法理规则”（`realign_dejure_cost_rule`）：
    - **免费 / 沙盒模式**（默认）：无需任何威望或正统性消耗，领主随时自由勘定。
    - **拟真平衡模式**：每次更定消耗 150 威望与 50 正统性，且领主必须达到中级（2级）或更高君权。
  - [EN] Added game rule `realign_dejure_cost_rule`:
    - **Free / Sandbox Mode** (Default): No costs or authority requirements.
    - **Realistic / Balanced Mode**: Costs 150 prestige and 50 legitimacy, requiring Medium Crown Authority (Level 2) or higher.
- **完整双语本地化与反馈 (Bilingual Localization & Feedback)**：
  - [CN] 提供符合原版风格的 UTF-8 with BOM 简体中文与英文本地化。
  - [EN] Standard UTF-8 with BOM English and Simplified Chinese localization with instant toast notifications.
