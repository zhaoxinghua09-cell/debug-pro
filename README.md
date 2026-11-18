# debug-pro · 排障专家

先定位再动手的排障流程：先把故障钉在某一层（输入/环境/依赖/逻辑），再最小化、验证、回归。没有日志与复现步骤就不给根因。

Triage-first debugging: locate the failing layer (input / environment / dependency / logic) before proposing any fix, then minimize, verify and regress.

## 快速开始 / Quick start

```bash
git clone https://github.com/zhaoxinghua09-cell/debug-pro.git
cd debug-pro
python tools/debughunt.py triage --file error.log --out ./out --json
python tools/debughunt.py envsnap --out ./out --json
python tools/debughunt.py reprocheck --file repro.md --json
python tests/run_golden.py
```

## 为什么可信 / Why it is checkable

- 黄金集 10 cases，`python tests/run_golden.py` 会真实执行并给出退出码（不靠自述）。
- 差异化点：single checkable command handed to the user for every claim。
- 零依赖、离线、零凭据：仅标准库，不发网络请求。

## AI 发现层 / AI discovery layer

- `llms.txt` — 面向 AI Agent 的能力与触发条件说明（双语）。
- `AI-INDEX.json` — 机器可读索引（schema `lgd.ai-index/1`）。
- 六维审计通过后登记于爆款清单：https://github.com/zhaoxinghua09-cell/lgd-hit-list

## 同族技能 / Family

- [summarize-pro](https://github.com/zhaoxinghua09-cell/summarize-pro) — 会议纪要专家
- [wechat-viral-topic](https://github.com/zhaoxinghua09-cell/wechat-viral-topic) — 公众号选题专家
- [lgd-skill-review](https://github.com/zhaoxinghua09-cell/lgd-skill-review) — 技能审计官

---

