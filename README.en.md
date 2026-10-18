# debug-pro · 7-Step Debugging Protocol

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-SKILL.md-blue.svg)](SKILL.md)
[![Category](https://img.shields.io/badge/category-debugging-8a2be2.svg)](#)
[![Version](https://img.shields.io/badge/version-1.0.0-informational.svg)](#)
[![llms.txt](https://img.shields.io/badge/AI--friendly-llms.txt-101E2C.svg)](llms.txt)
[![中文](https://img.shields.io/badge/%E4%B8%AD%E6%96%87-README.md-blue.svg)](README.md)

> A 7-step standard debugging protocol plus multi-language debugging commands to systematically identify, verify and fix defects, covering Python / JavaScript / Swift / CSS / networking / git bisect.

**Keywords**: 调试协议 · debug · bug 定位 · 最小复现 · git bisect · 断点 · 日志 · troubleshooting · debugging · python · javascript

This repository is an **Agent Skill distribution package**. The core file `SKILL.md` follows the Agent Skills spec (YAML frontmatter) and packages the method of "用 7 步协议把「报错→定位→最小复现→修复→验证」走成可审计流程" into a skill an AI agent can load directly. Drop it into your agent's skills directory (e.g. `~/.workbuddy/skills/`).

- **Category**: 开发工具 / Debugging
- **Version**: 1.0.0
- **Author**: 诺声(Logos)@SynomosAI
- **License**: MIT (see [LICENSE](LICENSE))

---

## Features

- 7 步标准协议：复现 → 定位 → 最小复现 → 假设 → 验证 → 修复 → 回归，不跳步
- 多语言命令库：Python / JavaScript / Swift / CSS / 网络 / Git Bisect 各有对应排查命令
- 真实参照法：每步结论挂到可复现实测证据（日志 / 断点 / 最小复现），不靠猜测改代码
- 最小复现优先：先把问题收敛到最小用例，再动手改
- 通用方法论工具：非医疗器械 / 非医疗软件，无疗效或临床声明
- 多语种：中 / 英 / 日 / 韩 / 西 / 法 / 德 / 阿（核心 8 种）

---

## Quick Start

Prerequisite: an AI coding assistant / skill runtime that can load Agent Skills. 无独立可执行服务；本包为调试方法论 + 命令速查.

```bash
# 1. 克隆本仓库
git clone https://github.com/zhaoxinghua09-cell/debug-pro.git
cd debug-pro

# 2. 查看技能主文件（7 步协议、各语言命令、触发词）
cat SKILL.md

# 3. 把技能目录放进你的 Agent 技能目录（示例：WorkBuddy）
#    cp -r . ~/.workbuddy/skills/debug-pro/
```

Then invoke it in natural language, e.g.:

```text
「这段代码报错了，帮我按步查」
「这个 bug 到底在哪」
「改了还是不对，怎么一步步定位」
```

---

## Usage

1. Clone this repo, or copy the skill directory into your agent's skills folder.
2. Call the capability via the trigger keywords described in `SKILL.md`.
3. See `SKILL.md` for the full method, boundaries and provenance.

---

## Repository layout

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

## License

Released under the **MIT** license. See [LICENSE](LICENSE) for the full text. Attribution: cite this repository `https://github.com/zhaoxinghua09-cell/debug-pro` and the rights holder "赵兴华 / Steven Zhao·China". Contact: zhaoxinghua06@126.com ｜ ORCID 0009-0001-0512-1237.

---

## Security

If you find a security issue, report it privately per [SECURITY.md](SECURITY.md); do not disclose it in a public issue.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Keep the `SKILL.md` YAML frontmatter fields compatible when changing this skill.

## Disclaimer

This repository content is a **theoretical stance and tooling exploration**. It does not represent any certified, commercially delivered, or client-served claim. External standards, certifications and clause information are restatements of public sources; independently verify before formal citation. APIs, authorization codes and ambassadors are roadmap items, not yet live.
