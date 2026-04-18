# 夜间自主补全 · 问题记录

> 用户 2026-04-18 晚委托：按年份补齐 papers-reference 和 concepts-map 中缺失的 deep-dive，次晨回看。
> 这里记录过程中遇到的模糊点、判断权衡、需用户确认的事项。

---

## 夜间工作总结（2026-04-18 晚 → 2026-04-19 晨）

### 数量变化

| 指标 | 开工前 | 目前 | 增量 |
|---|---:|---:|---:|
| Deep-dive 数 | 26 | **42** | **+16** |
| Papers-reference 中已链 deep-dive 的条目 | ~14 | **48** | +34（含孤儿链接修复） |
| Papers-reference 总条目数 | 95 | 96 | +1（MetaGPT 补录） |
| Commits 推送 | 2 | **8** | +6 |

### 新增 deep-dive 清单（按顺序）

| # | 标题 | 来源提示 |
|---|---|---|
| 25 | ExpeL + AutoGuide + ERL — 跨轨迹经验反思三代演化 | 用户点名 ExpeL / ERL 后扩展 AutoGuide |
| 26 | Cross-Attention Retrieval — ACAN 替代小镇公式 | 用户从概念图注意到 |
| 27 | MAD + MAR/A-HMAD — 辩论式反思两代 | 用户点名 MAD / MAR / A-HMAD |
| 28 | LLMs Cannot Self-Correct — 反思转向论文 | 概念图侦察识别为关键缺失 |
| 29 | GEA — 通用具身 Agent (CVPR 2025) | 用户点名 具身智能 CVPR 2025 |
| 30 | Mem0 — 生产级长期记忆框架 | 自主选择，高优先级 |
| 31 | RMM — 前瞻+回顾反思记忆管理 | 自主选择 |
| 32 | Memory POMDP 形式化 | 自主选择，理论类 |
| 33 | SocioVerse — 千万用户池 | 自主选择，大规模仿真 |
| 34 | Generative Agent Simulations of 1,000 People (Park 2024) | 自主选择，斯坦福小镇 followup |
| 35 | OpenCity — 万级开源城市仿真 (ACL 2025) | 自主选择 |
| 36 | Critical Perspectives on Generative Social Simulation | 自主选择，批判视角 |
| 37 | Concordia — Google DeepMind 仿真库 | 自主选择 |
| 38 | Sotopia — CMU 社交智能评估 | 自主选择 |
| 39 | Sweet&Sour — 正向经验反思 (NeurIPS 2024) | 自主选择 |
| 40 | Hallucination Survey — Agent 幻觉综述 | 自主选择 |
| 41 | Mitigating Hallucination — RAG+推理+Agentic 三路径 | 40 号的配套解药 |
| 42 | MegaAgent — 590 Agent 自动生成 | 自主选择 |

### 批量维护操作

- **35 个 orphan 链接修复**：早期的 deep-dive 01-24 有多个未在 papers-reference 里补"深度解读"链接的遗留问题，用 Python 批量修复 3 个视图
- **arxiv ID 错误修复**：papers-reference 和 concepts-map 之前把 Huang et al. "LLMs Cannot Self-Correct" 的 arxiv ID 写成 `2310.01848`，WebSearch 确认真实为 `2310.01798`，已批量替换（papers-reference 3 处 + concepts-map 6 处）
- **concepts-map 链接**：Self-Correct / MAD / MAR / ChatDev / MetaGPT / GEA 的概念图卡片之前缺 `deep-dive/` 链接，补齐

### 剩余未 deep-dive 的论文（48 篇）

按年份排序 top 15：

| 年份 | 标题 | 建议 |
|---|---|---|
| 2026 | Evaluating Memory Structure in LLM Agents | 可做（记忆基准，但略窄） |
| 2026 | ALCS: Laplace Collapsed Sampling | 跨领域，可选 |
| 2025.09 | Soul Machines Workforce Connect | **商业产品**，不建议做 deep-dive |
| 2025.06 | TalkingMachines: Real-Time Video (Character.AI) | **商业产品** |
| 2025.04 | AvatarFX (Character.AI) | **商业产品** |
| 2025 | Autonomous Memory Augmentation | 可做 |
| 2025 | OPTIMA — MAS 优化 | 可做 |
| 2025 | AgentTorch — 微分仿真 | 可做 |
| 2025 | Multi-Agent Autonomous Driving Survey | 应用域，可选 |
| 2025 | DriveMLM | 应用域，可选 |
| 2025 | Multi-Agent Swarm Intelligence | 应用域，可选 |
| 2025 | Ubisoft Teammates | **商业原型** |
| 2025 | LLM-Driven NPCs: Cross-Platform Dialogue | 应用域 |
| 2025 | Empowering Economic Simulation MMO | 应用域 |
| 2025 | Beyond Playtesting: Generative Multi-Agent MMO | 应用域 |

**商业产品类（Soul Machines / Character.AI / Ubisoft）** 通常在本库里只做 papers-reference 条目不做 deep-dive，保持现状即可。

**应用域（驾驶 / NPC / MMO / 医疗）** 如果要做可再加一轮，但和斯坦福小镇核心主题稍远。

**理论/方法类（Evaluating Memory / Autonomous Memory Aug / OPTIMA / AgentTorch）** 可做，但优先级明显低于已完成的 16 篇。

---

## 待用户确认的事项

### 1. Self-Correct 论文 arXiv ID 已修正

- papers-reference.html 和 concepts-map.html 之前写的是 **2310.01848**（错误）
- 通过 WebSearch 确认真实 arXiv ID 是 **2310.01798**（https://arxiv.org/abs/2310.01798）
- ICLR 2024, Huang, Chen, Mishra, Zheng, Yu, Song, Zhou
- 已批量替换，deep-dive/28 用的本就是 2310.01798（正确）

### 2. MAD 论文作者归属冲突

Agent 在写 27 号时发现 papers-reference 的**作者归属错误**：
- papers-reference.html 行 816 把 arXiv:2305.14325 归给 Liang et al.
- 但 WebFetch 确认该 arXiv ID 实际是 **Du, Li, Torralba, Tenenbaum, Mordatch** 的 "Improving Factuality and Reasoning in Language Models through Multiagent Debate" (MIT/Google Brain, 2023.05)
- Liang et al. 的 "Encouraging Divergent Thinking" 真实 arXiv 是 **2305.19118**
- 27 号 deep-dive 按 WebFetch 真实作者写，并在"诚实声明"章节指出该偏差
- **已在 papers-reference 条目旁加橙色⚠提示**指向 deep-dive 27

**需要你决定**：
- 方案 A：把 papers-reference.html 的 MAD 条目作者改成 Du et al.（保持 arXiv ID 不变）
- 方案 B：把 arXiv ID 改成 2305.19118（保持 Liang et al. 署名），增补一个 Du et al. 条目

### 3. MAR 论文的实际标题与摘要数据差异

- papers-reference 原描述：A-HMAD 变体 GSM-8K 91%
- 实际 MAR 论文（arXiv:2512.20845）标题是 **"MAR: Multi-Agent Reflexion Improves Reasoning Abilities in LLMs"**
- 实际报告指标：HotpotQA 47% EM + HumanEval 82.7%
- **GSM-8K 91% 数字在论文中无对应**
- A-HMAD 缩写在 MAR 论文中不存在

**需要你决定**：可能是 papers-reference 条目描述本身混合了多篇论文的信息。需 fact-check。

### 4. Autoguide 和 Concordia 开源 / 代码状态

- AutoGuide（25 号内）未找到官方 GitHub，标 "📄 暂无开源"
- Concordia：有官方 GitHub（google-deepmind/concordia）
- 其他所有 deep-dive 的代码状态已就位

### 5. MAR 论文 arXiv 2512.20845 的有效性

2025.12 发表的 arxiv 编号，WebFetch 可获取。deep-dive 27 写入时依据摘要；如果后续更新 v3+ 可能需回访。

---

## 过程日志（按时间）

### 2026-04-18 晚（checkpoint commits）

- `de3fbbd` Expand README and archive session logs（早前）
- `7ca58bd` Archive 04-08 through 04-18 research（早前）
- `c3db291` Track logs/ directory（早前）
- `d3cdb0a` Add ExpeL + ERL paired deep-dive (25)
- `17b7bfb` Add deep-dive 26 Cross-Attention (ACAN)
- `903e4b9` Expand deep-dive 25 to trilogy (add AutoGuide)
- `653da6d` **Add deep-dives 27/28/29: MAD+MAR, Self-Correct, GEA**
- `943562c` Fix 35 orphan deep-dive links
- `a898667` Add deep-dives 30/31/32 + arxiv ID fix
- `4047d77` Add deep-dives 33/34/35 (social simulation cluster)
- `9de3087` Add deep-dives 36/37/38 (evaluation & critique cluster)
- `873b3ac` Add deep-dives 39/40 (Sweet&Sour + Hallucination Survey)
- `(pending)` Batch 5: deep-dives 41/42 (Mitigating Hallucination + MegaAgent)

---

## 方法论备忘

- 每篇 deep-dive 通过 subagent 写作，先 WebFetch 获取真实数据，不确定处严格标 `<待实证>` 或类似 visual marker，拒绝编造数字
- 每个 3-4 篇 deep-dive commit 一次，保证增量可回滚
- 索引更新用 Python 脚本批量处理（papers-reference 3 视图 + index1 + CLAUDE.md），避免手工遗漏
- concepts-map 的卡片级链接在写入新 deep-dive 时同步更新（适用于 25/26/27/28/29），40+ 号因为多属较新论文，部分尚未在 concepts-map 中有对应卡片；视你的需要后续补上
