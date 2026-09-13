# 更定封臣法理 (CK3 Realign Vassal De Jure)

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-ck3--realign--dejure-181717.svg?logo=github)](https://github.com/ShunbaoLi/ck3-realign-dejure)
[![Changelog](https://img.shields.io/badge/Changelog-Keep_a_Changelog-blueviolet.svg)](CHANGELOG.md)
[![CK3 Version](https://img.shields.io/badge/CK3_Version-1.18%20%7C%201.19+-orange.svg)](https://ck3.paradoxwikis.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

**[简体中文](README.md) | [English](README.en.md)**

</div>

---

## 📌 项目简介

**更定封臣法理 (CK3 Realign Vassal De Jure)** 是一款专为《十字军之王3》（Crusader Kings III）打造的高质量功能性 Mod。

在原版游玩与各大 Mod（如天朝东亚、拜占庭等）中，封臣由于联姻、继承、征服或内部调动，常年出现**辖地法理犬牙交错、飞地横生、法理不一**的混乱局面，严重破坏强迫症领主的版图审美与行政法理秩序。

本 Mod 为玩家领主赋予至高无上的**“疆理勘定”**皇权敕令：只需在封臣角色上**右键交互**，即可一键将该封臣实际统辖的所有非本法理土地正式更定为其主头衔之法定法理；若封臣为国王且玩家为皇帝，更可将该王国法理直接整合入玩家帝国。

> 📜 **版本更新日志与演进历史**：请参阅 [CHANGELOG.md](CHANGELOG.md)。

---

## ⚔️ 核心功能矩阵 (Feature Matrix)

| 适用对象 | 触发条件 | 勘定效果 (Execution Effect) | 机制深度 |
| :--- | :--- | :--- | :--- |
| **公爵 / 节度使** (`tier_duchy`) | 其直辖或下属伯爵领中存在非本公国法理土地 | 将其名下及所有下属封臣管辖的全部伯爵领，**即时且永久更定为该公爵主头衔的法理** | 根治节度使/公国法理飞地与破碎领地 |
| **国王 / 都护府** (`tier_kingdom`) | 其直辖或下属公国中存在非本王国法理土地 | 将其名下及所有下属封臣管辖的全部公国，**即时且永久更定为该王国主头衔的法理** | 规范大封臣疆域，重塑都护府与封王法理 |
| **皇帝对王国封臣** (`tier_empire`) | 王国封臣的王国法理尚未归属于玩家帝国 | 将该封臣名下的王国法理，**即时且永久划归为玩家帝国主头衔的法理** | 规避百年法理漂移，实现真正的大一统敕定 |

---

## ⚙️ 游戏规则配置 (Game Rules)

开局可在游戏规则中自由选择适合您的游戏风格：

- **免费 / 沙盒模式（默认）**：
  - 无需消耗任何威望与正统性。
  - 无君权等级限制，开局即可随意勘定。
- **拟真平衡模式**：
  - 每次更定封臣法理需消耗 **150 威望** 与 **50 正统性（Legitimacy）**。
  - 要求玩家领主达到**中级（2级）或更高君权**。

---

## 🏛️ 政体与 DLC 兼容性 (Compatibility Matrix)

本 Mod 采用**纯追加（Additive）模式**开发，未修改或覆写任何游戏原版文件，保证零冲突：

| 系统 / 政体 | 兼容状态 | 说明 |
| :--- | :---: | :--- |
| **全 DLC 体系** | 兼容 | 原生完美支持《东亚与帝国》（TGP）、《摄政与行政制》（Roads to Power）、《死神与传奇》等所有 DLC |
| **中华天朝政体** | 兼容 | 全面适配节度使、都护府等天朝官僚体系，平衡模式适配天朝政制等级 |
| **拜占庭行政制** | 兼容 | 全面适配总督（Strategos）与总督区（Thema）疆域法理管理 |
| **封建制 / 氏族制 / 部落制 / 游牧制** | 兼容 | 平衡模式已适配全部对应政体的权威法案（王权、部族权威、游牧权威） |
| **中途加入存档** | 兼容 | 随时可在已有存档中启用，不会损坏任何存档数据 |

---

## 📦 安装与启用指引 (Installation Guide)

### 方式一：Steam 创意工坊（推荐）
直接在 Steam 创意工坊订阅本 Mod，并在 Paradox 启动器中将 Mod 加入“播放集（Playset）”并勾选启用。

### 方式二：本地手动安装
1. 下载仓库最新源码 Release 压缩包并解压。
2. 将解压后的文件夹放入 CK3 的本地 Mod 目录：
   - **Windows**: `Documents\Paradox Interactive\Crusader Kings III\mod\ck3realigndejure`
   - **Linux**: `~/.local/share/Paradox Interactive/Crusader Kings III/mod/ck3realigndejure`
   - **macOS**: `~/Documents/Paradox Interactive/Crusader Kings III/mod/ck3realigndejure`
3. 确保该目录下的 `ck3realigndejure.mod` 放置于上一级 `mod/` 目录中。
4. 打开游戏启动器并在播放集中启用。

---

## 🤝 欢迎反馈与贡献 (Contributions Welcome)

如果你在游玩过程中发现任何逻辑异常或希望扩充更多法理勘定规则：

1. **提交 Issue**：在 [GitHub Issues](https://github.com/ShunbaoLi/ck3-realign-dejure/issues) 反馈 Bug、建议与游戏截图。
2. **提交 Pull Request**：
   - Fork 本仓库并基于特性分支修改。
   - 保持所有 `.txt` 和 `.yml` 文件为 **UTF-8 with BOM** 编码。
   - 在 [CHANGELOG.md](CHANGELOG.md) 的 `[Unreleased]` 中同步登记变动内容。

---

## 📜 开源协议

本项目采用 [MIT License](LICENSE) 开源授权。
Copyright (c) 2026 ShunbaoLi.
