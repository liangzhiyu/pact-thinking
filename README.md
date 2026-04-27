# pact-thinking

An OpenClaw skill for structured thinking with the **P.A.C.T.** framework.

PACT helps an agent improve the user's thinking **without taking over the decision**.

- **P — Premise**: surface the current view first
- **A — Attack**: stress-test that view before proposing alternatives
- **C — Compare**: compare multiple paths with explicit trade-offs
- **T — Take**: organize the decision while leaving the final choice to the user

## What this skill is for

Use this skill when the user wants help with:

- clearer judgment
- deeper analysis
- structured debate
- assumption testing
- option comparison
- decision framing
- reusable reasoning workflows

Typical prompts:

- 帮我想清楚这个判断
- 挑战一下我的想法
- 给我一个思考框架
- 做个决策表
- 我该不该继续做这个项目？

## Repository structure

```text
pact-thinking/
├── SKILL.md
└── references/
    └── prompts.md
```

- `SKILL.md` — trigger description, workflow, output format, and operating rules
- `references/prompts.md` — reusable prompt blocks for Premise / Attack / Compare / Take

## How it works

The skill enforces a deliberate sequence:

1. **Premise** — clarify the user's current view
2. **Attack** — criticize the current view before proposing alternatives
3. **Compare** — compare conservative / aggressive / balanced paths
4. **Take** — return the final judgment to the user

Short version:

> 先立场 → 再攻击 → 后比较 → 最终自己取舍

## Example output shape

```markdown
## P — 前提
- 初步判断：
- 理由：
- 关键假设：
- 不确定点：

## A — 攻击
- 最脆弱假设：
- 证据缺口：
- 关键反例：
- 最可能错点：

## C — 比较
| 方案 | 核心逻辑 | 成本 | 风险 | 适用条件 | 失败信号 |
|---|---|---|---|---|---|

## T — 取舍
- 方案成立条件：
- 最大风险：
- 决策前待确认：
```

## Installation

Copy this directory into your OpenClaw skills path, for example:

```bash
cp -R pact-thinking ~/.openclaw/skills/
```

Then make sure your agent can discover and load the skill from that path.

## Packaging

To package the skill into a distributable `.skill` file, use OpenClaw's packaging script:

```bash
python /root/.nvm/versions/node/v22.22.1/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py ./pact-thinking
```

## Notes

This repo intentionally keeps the skill small:

- core behavior stays in `SKILL.md`
- reusable prompt text lives in `references/prompts.md`
- no extra framework code is required

## License

MIT
