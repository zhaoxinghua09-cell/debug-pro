# debug-pro · 7 步标准调试协议

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![Category](https://img.shields.io/badge/category-debugging-8a2be2.svg)](#)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](#)
[![Multilingual](https://img.shields.io/badge/i18n-8%20languages-brightgreen.svg)](#)
[![llms.txt](https://img.shields.io/badge/AI--friendly-llms.txt-101E2C.svg)](llms.txt)
[![English](https://img.shields.io/badge/English-README.en.md-blue.svg)](README.en.md)

> 提供 7 步标准调试协议 + 多语言调试命令，系统性识别、验证、修复软件缺陷——用于回答「代码报错怎么查」「这个 bug 到底在哪」「改了还是不对怎么办」。支持 Python / JavaScript / Swift / CSS / 网络 / Git Bisect。
> A 7-step standard debugging protocol plus multi-language debugging commands to systematically identify, verify and fix defects, covering Python / JavaScript / Swift / CSS / networking / git bisect.

SynomosAI 四支柱体系：**身份（Identity）· 溯源（Traceability）· 治理（Governance）· 共生（Symbiosis）**——当 AI 进入商业，可信是唯一的硬通货。

**关键词 / Keywords**：调试协议 · debug · bug 定位 · 最小复现 · git bisect · 断点 · 日志 · troubleshooting · debugging · python · javascript

本仓库是一个 **Agent Skill 发布包**：核心文件 `SKILL.md` 遵循 Agent Skills 规范（YAML frontmatter），把「用 7 步协议把「报错→定位→最小复现→修复→验证」走成可审计流程」的方法固化为可被 AI Agent 直接加载的技能。可直接放入主流 AI Agent（如 WorkBuddy）的技能目录使用。

- **分类 / Category**：开发工具 / Debugging
- **版本 / Version**：1.0.0
- **署名 / Author**：诺声(Logos)@SynomosAI
- **许可 / License**：MIT（详见仓库 [LICENSE](LICENSE)）

---

## ✨ 特性 / Features

- 7 步标准协议：复现 → 定位 → 最小复现 → 假设 → 验证 → 修复 → 回归，不跳步
- 多语言命令库：Python / JavaScript / Swift / CSS / 网络 / Git Bisect 各有对应排查命令
- 真实参照法：每步结论挂到可复现实测证据（日志 / 断点 / 最小复现），不靠猜测改代码
- 最小复现优先：先把问题收敛到最小用例，再动手改
- 通用方法论工具：非医疗器械 / 非医疗软件，无疗效或临床声明
- 多语种：中 / 英 / 日 / 韩 / 西 / 法 / 德 / 阿（核心 8 种）

---

## 🚀 快速开始 / Quick Start

前置：一个能加载 Agent Skill 的 AI 编码助手 / 技能运行时；无独立可执行服务；本包为调试方法论 + 命令速查。

```bash
# 1. 克隆本仓库
git clone https://github.com/zhaoxinghua09-cell/debug-pro.git
cd debug-pro

# 2. 查看技能主文件（7 步协议、各语言命令、触发词）
cat SKILL.md

# 3. 把技能目录放进你的 Agent 技能目录（示例：WorkBuddy）
#    cp -r . ~/.workbuddy/skills/debug-pro/
```

跑通后，直接用自然语言发起调用，例如：

```text
「这段代码报错了，帮我按步查」
「这个 bug 到底在哪」
「改了还是不对，怎么一步步定位」
```

---

## 📖 使用方式 / Usage

1. 克隆本仓库，或将技能目录放入 Agent 技能目录（如 `~/.workbuddy/skills/`）；
2. 按 `SKILL.md` 的描述与触发词调用对应能力；
3. 详细方法、边界与治理溯源见 `SKILL.md` 正文。

> 按 SKILL.md 的 7 步顺序对当前报错执行；每步先拿证据再下结论。

---

## 📁 仓库结构 / Repository layout

```text
debug-pro/
├── README.md            # 本文件（双语）
├── README.en.md         # 英文版说明
├── SKILL.md             # 技能主文件（Agent Skills 规范 · YAML frontmatter）
├── manifest.json        # 技能元数据（名称 / 版本 / 许可 / 描述）
├── LICENSE              # MIT 许可全文
├── SECURITY.md          # 安全策略
├── CONTRIBUTING.md      # 贡献指南
├── AGENTS.md            # 给 AI Agent 的工作指引
├── llms.txt             # 给 AI 的最小索引（llms.txt 标准）
└── llms-full.txt        # 给 AI 的完整文本
```

---

## 许可说明 · License Notice

- **权利状态**：本仓库以 **MIT 许可** 许可发布，可依该许可证条款自由使用、修改与再分发。
- **引用建议**：引用时请标注仓库名与原文链接 `https://github.com/zhaoxinghua09-cell/debug-pro`
  与权利人「赵兴华 / Steven Zhao·China」。
- **品牌状态限定**：MedXpert、SynomosAI、LGD 等为相关项目标识，
  **均未申请实体注册、未申请商标注册**；出现仅作来源标识，
  不构成对法人实体或商标权的任何主张。
- **完整条款**：见仓库根目录 [LICENSE](LICENSE)。
- **联系**：zhaoxinghua06@126.com ｜ ORCID 0009-0001-0512-1237

---

## 🔒 安全 / Security

如发现安全问题，请按 [`SECURITY.md`](SECURITY.md) 的方式私下报告，不要在公开 issue 中披露。

## 🤝 贡献 / Contributing

欢迎按 [`CONTRIBUTING.md`](CONTRIBUTING.md) 提交改进。本仓库为技能发布包，改动请保持 `SKILL.md` 的 YAML frontmatter 字段兼容（`name` / `slug` / `version` / `license` 等）。

## 免责声明

本仓库内容为**理论站位与工具化探索**，不代表任何已获认证、已商业化交付或已服务特定客户的声明；文中涉及的外部标准、认证与条款信息为公开资料转述，正式引用前请**独立核实**。API、授权码与形象大使等为路线图（roadmap）事项，尚未上线。
