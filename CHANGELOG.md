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

## [1.0.5] - 2026-09-15

### Fixed
- **支持帝国级行台/总督封臣与下属王国更定 (Support Empire-tier Vassals & Subordinate Kingdoms)**：
  - [CN] 新增对帝国级封臣（`tier_empire`，如中华天朝行台、都督府等）的主头衔法理更定支持，一键将其名下及所有下属封臣实际统辖的非本法理王国划入其帝国法理（如将流求路更定入荆扬行台）。
  - [EN] Added support for empire-tier vassals (`tier_empire`, such as Hangtai/Grand Viceroys), realigning all subordinate kingdoms held directly or by their vassals into their imperial de jure.
  - [CN] 修复将王国划归皇帝法理时未遍历封臣下属（`any_vassal_or_below`）的缺陷，确保转封给大封臣的王国领地亦能被精准检测与更定。
  - [EN] Fixed missing traversal of subordinate vassals (`any_vassal_or_below`) for kingdom titles, ensuring kingdoms transferred under grand vassals are correctly detected and realigned.
  - [CN] 领主等级判定全面适配霸权/天朝大一统级（`tier_hegemony`，如大唐帝国 `h_china`），解除原版仅限制在 `tier_empire` 的逻辑约束。
  - [EN] Expanded liege tier check to encompass Hegemony-tier rulers (`tier_hegemony`, e.g. `h_china`).

---

### Removed
- 移除"拟真平衡模式"游戏规则选项，Mod 现在仅提供无限制沙盒模式：更定封臣法理无任何威望、正统性或君权消耗。
- 删除 common/game_rules/realign_dejure_game_rules.txt。
- 移除所有与平衡模式相关的本地化键。
## [1.0.3] - 2026-09-14

### Added
- 交互选项在条件不满足时，现在显示 ❗ 条件提示（战争状态、平衡模式君权要求、平衡模式合法性要求、无可更定法理等），与原版交互风格一致。
- 新增本地化键：ealign_dejure_not_at_war、ealign_dejure_requires_legitimacy。
## [1.0.2] - 2026-09-14

### Fixed
- 更定封臣法理交互菜单现在正确显示图标（与"转封封臣"交互一致，使用 icon_vassal）。
## [1.0.1] - 2026-09-13
### Fixed
- **排除世家宅邸与名义头衔 (Exclude Noble Families & Titular Titles)**：
  - [CN] 为所有头衔判定增加 `is_noble_family_title = no`、`is_landless_type_title = no` 与 `is_titular = no` 过滤器。
  - [EN] Added title filtering for `is_noble_family_title = no`, `is_landless_type_title = no`, and `is_titular = no`.
  - [CN] 彻底修复在行政制与天朝官僚制（TGP）下，封臣的世家宅邸头衔（如“东方家族”、“苫家族”等庄园伯爵领）以及无实体版图的名义头衔被错误更定法理领主的 Bug。
  - [EN] Fixed edge case where Administrative and Celestial Empire noble family estate titles (e.g. House Estates) and titular titles were erroneously realigned as de jure vassals.

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
