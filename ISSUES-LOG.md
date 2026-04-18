# 夜间自主补全 · 问题记录

> 用户 2026-04-18 晚间委托：按年份补齐 papers-reference 和 concepts-map 中缺失的 deep-dive，次晨回看。
> 这里记录过程中遇到的模糊点、判断权衡、需用户确认的事项。

## 状态概览（动态更新）

- **起始 deep-dive 数**：26（commits: 17b7bfb)
- **夜间新增目标**：自主优先级排序，按年份新的先补
- **已完成**：见下方日志
- **提交节奏**：每 3-4 篇一次 commit，避免丢失

---

## 待用户确认的事项

（空：过程中遇到判断模糊处会写入此处）

---

## 过程日志

### 2026-04-18 夜间开工

- 已完成 deep-dive 25 (ExpeL+AutoGuide+ERL trilogy)、26 (Cross-Attention ACAN)
- deep-dive 27/28/29 已写完，待索引 + 提交
  - 27: MAD + MAR/A-HMAD（辩论式反思两代）
  - 28: LLMs Cannot Self-Correct (ICLR 2024)
  - 29: GEA Generalist Embodied Agent (CVPR 2025)

### 27 号需注意的事项

Agent 在写 27 号时发现了现有 papers-reference 的**作者归属错误**：
- papers-reference.html 行 816 把 arXiv:2305.14325 归给 Liang et al.
- 但 WebFetch 确认该 arXiv ID 实际是 **Du, Li, Torralba, Tenenbaum, Mordatch** 的 "Improving Factuality and Reasoning in Language Models through Multiagent Debate" (MIT/Google Brain, 2023.05)
- Liang et al. 的 "Encouraging Divergent Thinking" 真实 arXiv 是 **2305.19118**
- 27 号 deep-dive 按 WebFetch 真实作者写，并在"诚实声明"章节指出该偏差

**建议用户决定**：
- 方案 A：把 papers-reference.html 的 MAD 条目作者改成 Du et al.（保持 arXiv ID 不变）
- 方案 B：把 arXiv ID 改成 2305.19118（保持 Liang et al. 署名），增补一个 Du et al. 条目

### Self-Correct 论文 arXiv ID 已修正

- papers-reference.html 和 concepts-map.html 之前写的是 **2310.01848**（错误）
- 通过 WebSearch 确认真实 arXiv ID 是 **2310.01798**（https://arxiv.org/abs/2310.01798）
- ICLR 2024, Huang, Chen, Mishra, Zheng, Yu, Song, Zhou
- 已批量替换，deep-dive/28 用的本就是 2310.01798（正确）

### MAR 论文的实际标题与摘要数据差异

- papers-reference 原描述：A-HMAD 变体 GSM-8K 91%
- 实际 MAR 论文（arXiv:2512.20845）标题是 "MAR: Multi-Agent Reflexion Improves Reasoning Abilities in LLMs"
- 实际报告指标：HotpotQA 47% EM + HumanEval 82.7%
- **GSM-8K 91% 数字在论文中无对应**
- A-HMAD 缩写在 MAR 论文中不存在

**建议用户决定**：可能是 papers-reference 条目描述本身混合了多篇论文的信息。需 fact-check。
