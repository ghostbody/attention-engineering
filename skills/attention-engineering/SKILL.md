---
name: attention-engineering
description: Use when the user wants to reduce reading, summarize or triage long outputs, design AI agents/skills that do not overwhelm humans, review large diffs or reports, decide what deserves attention, or find tools, skills, papers, and patterns that save human attention.
---

# Attention Engineering

## One line

注意力工程（attention engineering）= 设计 AI 系统与信息流，让人的注意力只花在关键决策与核心阻碍上。

Summarization, alerting, dashboards, agent output, review process — all instances of that one sentence.

## Two modes

Decide the mode first. Read only what the mode needs.

### FIND — user wants resources

Signals: "有什么工具/仓库/skill/文章", "推荐几个", "别人怎么做的".

1. Read `references/catalog.md`. Search it by the type of attention the user is losing.
2. Rank by what the resource saves: 阅读量 / 审查量 / 点击量 / 等待时间 / 打断次数.
3. Return **at most 5** entries. Format: `name — link — saves <what> because <why>`.
4. Nothing fits? Say so in one line, give the closest 1–2 and name their gap. Never pad to five.

### ADVISE — user describes their own agent / product / process

Signals: "我的 agent 每次都…", "这个报告太长", "团队被通知淹了", "review 不完".

1. Map their situation onto the five principles below.
2. Return the **1–3 highest-leverage changes**. Not all five. Not a checklist of everything wrong.
3. For each: 问题 → 改法 → 预期效果（尽量量化：行数、次数、时长）.
4. If the user has no observable signal yet, say what to measure first, then stop.

## Five principles

| # | Principle | 中文 | Test question |
|---|---|---|---|
| 1 | **Condense** | 一瞥即懂 | Can a reader get the point without scrolling? |
| 2 | **Tier** | 注意力只给重要的（精确率优先于召回率） | Does every surfaced item deserve to interrupt? |
| 3 | **Map** | 先给全局结构，按需下钻（渐进披露 / calm tech） | Is there a 1-line map before the detail? |
| 4 | **Human owns decisions & blockers only** | 人只负责决策与阻塞 | Is the human asked to do anything else? |
| 5 | **AI owns details, closes the loop** | AI 负责细节并闭环 | Does the interaction end in a decision or a done state? |

> 人的上限不是单个任务，而是同时跟踪的会话数（约 3–5 个）。超过就加一层 Router：Router 收事件、分级、派单，Worker 并行，人只看汇总与阻塞项（见 `references/playbook.md` §8）。

Use the test question, not the label. If a design fails one test, fixing that one usually solves the case.

## Three traps

1. **Output volume ≠ value.** Processed volume is value. A 100-page report nobody read produced zero.
2. **Chasing recall triggers alarm fatigue.** Every added alert type lowers the credibility of every existing alert. Precision over recall.
3. **Line-by-line human review cannot absorb exponential AI output.** Move humans up to architecture, interfaces, and risk; let machines cover the surface.

These three explain most real failures. Check them before proposing anything clever.

## Answer protocol (hard constraints)

- **First line = conclusion or recommended action.** Not context, not restatement.
- **Default ≤5 lines.** Expand only when the user says 展开 / 详细 / "show me".
- **Map first, drill down on request.** One line of overview, then details only if asked.
- **Every recommendation names what it saves:** 阅读量 / 审查量 / 点击量 / 等待时间 / 打断次数.
- **No restating the question. No "我将…". No process narration.** ("我先看一下…", "接下来我会…" are deleted.)
- **A choice for the user = 2–4 numbered options + a recommended one + one-line reason.**
- If the answer is longer than the question deserves, cut the answer, not the user's time.

## Before sending (anti-slop checklist)

- [ ] Can this be understood in one glance?
- [ ] Did I give only one level of detail, not three?
- [ ] Did I push any detail back onto the human that AI should own?
- [ ] Is it over 5 lines while the user did not ask for more?
- [ ] Does every item change a decision? If not, delete the item.

Any "no" → rewrite before sending.

## Reference routing

| Need | Read |
|---|---|
| 原理、文献、判据 | `references/principles.md` |
| 具体改法、模板、代码形态 | `references/playbook.md` |
| 全部收录资源 | `references/catalog.md` |
| 反模式清单 | `references/anti-patterns.md` |

Read on demand. **Do not preload all four.** Most questions need zero or one; FIND questions need `catalog.md` only.

`catalog.md` is generated from the repository README by `scripts/sync-catalog.mjs` — do not hand-edit it.

## Examples

**Example 1 — FIND**

> 用户：有没有能帮我少读点的工具？

```
最该先看的 3 个（都省阅读量，不省功能）：
1. <tool> — <link> — 把长页面压成一屏要点，省掉 80% 的滚动。
2. <tool> — <link> — 只在内容变化时通知，省掉重复阅读与打断。
3. <tool> — <link> — 自动生成变更摘要，省掉读完整 diff。
要我再按「省审查量」或「省打断」重排一次吗？
```

**Example 2 — ADVISE**

> 用户：我的 agent 每次都输出 100 行报告，怎么办？

```
改成默认给 3 行决策摘要（结论 / 风险 / 下一步），完整报告折叠在下面。
细节交给 agent 收口，人只在两种情况下被叫醒：需要拍板，或卡住了。
预期：单次阅读量 100 行 → 3 行，其余按需展开。
```

**Example 3 — judging a resource**

> 用户：这个 repo 值得收进 catalog 吗？

```
值得，因为它省的是审查量而不是阅读量：它把 diff 先按风险分层，人只看高风险点。
收录时按「省审查量」归类，别混进「省阅读量」。
```

## Common mistakes

| Mistake | Fix |
|---|---|
| Explaining the five principles instead of answering | Use one principle, answer in 5 lines |
| Listing 15 tools "for completeness" | 5 max, ranked by attention saved |
| Summarizing by shortening every sentence equally | Delete whole items; keep the decision |
| Surfacing every warning "so nothing is missed" | Rank, cap, and say what was dropped and why |
| Asking the human to verify details AI can verify | AI verifies, human decides |
| Writing a long answer to a small question | Length is a property of the question, not the topic |
