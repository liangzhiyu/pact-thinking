# PACT Prompt Templates

Use these prompt blocks directly or adapt them.

## 1) Premise

```text
先不要给我答案。
先帮我把我的初始判断写清楚，只整理，不扩展。
请按下面结构输出：
1. 我的初步判断是：
2. 我的理由是：
3. 我的关键假设是：
4. 我不确定的地方是：
```

## 2) Attack

```text
请不要给我新方案。
请只攻击我的想法：
1. 哪些假设最脆弱？
2. 哪些证据不足？
3. 有哪些反例？
4. 如果我错了，最可能错在哪里？
```

## 3) Compare

```text
请基于我的目标，给出 3 种不同思路：
1. 保守方案
2. 激进方案
3. 折中方案

每种方案请比较：
- 核心逻辑
- 成本
- 风险
- 适用条件
- 失败信号
```

## 4) Take

```text
请把以上内容整理成决策表。
不要替我做最终决定。
请告诉我：
1. 每个选择成立的条件
2. 每个选择的最大风险
3. 我做决定前还需要确认什么
```

## Combined shortcut

```text
用 P.A.C.T. 框架帮我推进这个问题，但不要直接替我做决定。
顺序必须是：
P — 先帮我明确初步判断、理由、假设、不确定点；
A — 先攻击这个判断，不要立刻给新答案；
C — 再展开保守/激进/折中三种方案，并比较成本、风险、适用条件、失败信号；
T — 最后整理成决策表，告诉我各方案成立条件、最大风险、决策前待确认事项。
```

## Good use cases

- 战略判断
- 职业选择
- 产品方向
- 投资假设复盘
- 写作观点打磨
- 复杂对话前的立场梳理

## Anti-patterns

Avoid using PACT mechanically when:
- the user only needs a factual lookup
- the decision is trivial and reversible
- the user needs emotional support first, not structured critique
