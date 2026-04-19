# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Workspace Purpose

This is a research documentation workspace focused on Generative Agents, LLM-driven multi-agent simulations, and related AI systems. It contains:
- CLI session transcripts from interactive research sessions
- Generated HTML reference materials (concept maps, paper tables, reading lists)

There is no build system, test suite, or executable code.

## Permissions

WebSearch is enabled (see `.claude/settings.local.json`). Use it freely to fetch papers, look up citations, and research AI agent topics.

## Research Focus Areas

**Core topic:** Stanford Smallville (arXiv:2304.03442) — the foundational Generative Agents paper by Park et al. (2023)

**Key conceptual components:**
- **Memory Stream** — chronological experience storage with recency, importance, and relevance scoring
- **Reflection** — periodic synthesis of memories into higher-level insights when importance threshold is exceeded
- **Planning** — long-horizon scheduling decomposed into short-term action sequences
- **Action & Interaction** — multi-agent dynamics and environment execution

**Applied implementations covered:** Inworld AI (game NPCs), Character.AI (conversational agents), Soul Machines (animated digital humans)

## HTML Reference Files (`html/`)

- `html/index1.html` — navigation hub with learning path (concepts → study guide → papers → deep dives)
- `html/concepts-map.html` — 3-tab interactive concept maps (5 pillars, Top 15 concepts, full evolution)
- `html/study-guide.html` — 3-track unified learning center (core architecture, multi-agent frontier, MetaGPT vs ChatDev)
- `html/papers-reference.html` — 96-paper reference with 3 views (分类手册 / 卡片浏览 / 表格视图), includes "个人补充" category for user-added papers
- `html/architecture-study.html` — 6-tab Agent architecture study (Claude Code source analysis, competitive analysis, implementation plan)
- `html/cot-reflexion-map.html` — CoT × Reflexion relationship concept map (Mermaid graph, timeline, 4-layer architecture, Smallville mapping)
- `html/deep-dive/01-06` — 6 paper deep-dive analyses (01-03 original, 04-06 user-added with "后加" badge)
- `html/deep-dive/07-17` — 11 CoT/Reflexion series deep-dives (all with "后加" badge): CoT, ReAct, Inner Monologue, Reflexion, ToT, Plan-and-Solve, LATS, Voyager, CAMEL, Multi-Agent ToT Validator, AgentSociety
- `html/deep-dive/18-21` — 4 memory-focused deep-dives (HiAgent, Generative Agents 原始论文, A-MEM, MemoryOS)
- `html/deep-dive/22-24` — 3 multi-agent & memory-survey deep-dives (all "后加"): MetaGPT SOP 流水线, ChatDev Waterfall 瀑布, Memory in the Age of AI Agents 综述
- `html/deep-dive/25-expel-erl.html` — trilogy deep-dive (all "后加"): ExpeL insights pool (AAAI 2024) + AutoGuide context-aware guidelines (NeurIPS 2024) + ERL heuristics pool (arXiv 2026.03), three-gen evolution of 跨轨迹经验反思: 聚合→条件→检索
- `html/deep-dive/26-cross-attention-retrieval.html` — Cross-Attention 检索 (Hong & He, Frontiers in Psychology 2025): trainable ACAN network replaces Smallville's hand-tuned Recency×Importance×Relevance scoring formula
- `html/deep-dive/27-mad-mar.html` — paired (both "后加"): MAD Multi-Agent Debate (Du et al. 2023) + MAR Persona Diversity (2024), debate-style reflection evolution
- `html/deep-dive/28-self-correct-limits.html` — "后加": LLMs Cannot Self-Correct Reasoning Yet (Huang et al., ICLR 2024) — the pivotal paper that turned the reflection field toward external critique
- `html/deep-dive/29-gea-embodied.html` — "后加": GEA Generalist Embodied Agent (Szot et al., CVPR 2025, Apple + Georgia Tech) — unified multi-embodiment action tokenizer
- `html/deep-dive/30-mem0.html` — "后加": Mem0 Production-Ready AI Agents with Scalable Long-Term Memory (2025, arXiv:2504.19413)
- `html/deep-dive/31-rmm.html` — "后加": In Prospect and Retrospect: Reflective Memory Management (RMM, 2025, arXiv:2503.08026) — prospective + retrospective dual-axis reflection
- `html/deep-dive/32-memory-pomdp.html` — "后加": Memory for Autonomous LLM Agents: A POMDP Formalization (2026, arXiv:2603.07670) — theoretical formalization complementing empirical memory papers
- `html/deep-dive/33-socioverse.html` — "后加": SocioVerse (arXiv:2504.10157, Fudan DISC): 10M real-user pool world model for social simulation, 2024 election 92.2% accuracy
- `html/deep-dive/34-1000-people.html` — "后加": Generative Agent Simulations of 1,000 People (arXiv:2411.10109, Park et al. 2024) — Stanford followup using deep interviews of 1052 people, 85% attitude prediction
- `html/deep-dive/35-opencity.html` — "后加": OpenCity (ACL 2025, Tsinghua FIB Lab) — 10K-agent urban simulation framework with epoll LLM scheduler and group-and-distill
- `html/deep-dive/36-critical-perspectives.html` — "后加": Critical Perspectives on Generative Social Simulation with LLMs (Larooij & Törnberg, Springer AI Review 2025) — 35-paper critical review covering prior pollution, diversity collapse, LLM-as-Judge loops
- `html/deep-dive/37-concordia.html` — "后加": Concordia (Google DeepMind, arXiv:2312.03664) — Entity × Component × Engine library for generative social simulation
- `html/deep-dive/38-sotopia.html` — "后加": SOTOPIA (CMU LTI, arXiv:2310.11667, ICLR 2024) + SOTOPIA-S4 (arXiv:2504.16122) — 7-dimension social intelligence evaluation framework
- `html/deep-dive/39-sweet-sour.html` — "后加": Sweet&Sour (arXiv:2411.02223, NeurIPS 2024) — positive-experience reflection complements Reflexion's failure-only focus; ScienceWorld benchmark
- `html/deep-dive/40-hallucination-survey.html` — "后加": LLM-based Agents Suffer from Hallucinations: A Survey (arXiv:2509.18970, 2025) — 5-stage hallucination taxonomy, agent-specific failure modes, mitigation pathways
- `html/deep-dive/41-mitigating-hallucination.html` — "后加": Mitigating Hallucination: RAG, Reasoning, and Agentic Systems (arXiv:2510.24476, 2025) — three pragmatic paths complementing survey 40
- `html/deep-dive/42-megaagent.html` — "后加": MegaAgent (arXiv:2408.09955, ACL Findings 2025) — 590 auto-generated agents with dynamic task allocation, contrasts fixed-pipeline approaches (MetaGPT/ChatDev)
- `html/deep-dive/43-evaluating-memory.html` — "后加": Evaluating Memory Structure (arXiv:2602.11243, 2026) — StructMemEval benchmark comparing Linear/Tree/Graph memory structures
- `html/deep-dive/44-autonomous-memory-aug.html` — "后加": MemInsight: Autonomous Memory Augmentation (arXiv:2503.21760, EMNLP 2025, AWS AI Labs) — LLM-driven attribute mining across entity×conversation perspectives
- `html/deep-dive/45-optima.html` — "后加": OPTIMA (arXiv:2410.08115, ACL Findings 2025, Tsinghua THUNLP) — MCTS-inspired DPO for MAS communication, 2.8× performance + <10% token
- `html/deep-dive/46-agenttorch.html` — "后加": AgentTorch (arXiv:2409.10568, MIT Media Lab, AAMAS 2024 Oral) — differentiable million-scale agent simulation
- `html/deep-dive/47-aipatient.html` — "后加": AIPatient (arXiv:2409.18924, Nature Comm Medicine 2025) — 6-agent medical simulation with MIMIC-III + Reasoning RAG, 94.15% QA accuracy
- `html/deep-dive/48-embodied-hallucinations.html` — "后加": Empirical Study on Hallucinations in Embodied Agents (EMNLP Findings 2025) — HEAL dataset, perception-action loop hallucinations (40/41/48 form hallucination trilogy)
- `html/deep-dive/49-swarm-intelligence.html` — "后加": LLM × Swarm Intelligence (Jimenez-Romero et al., Frontiers AI 2025, DOI 10.3389/frai.2025.1593017) — ant/bird flock LLM-ification experiments

## Paper Addition Workflow

When the user mentions a paper (by name, link, or description), always perform these three steps:

1. **Deep Dive** — Create a detailed analysis HTML file in `html/deep-dive/` (numbered sequentially, currently up to 49). Include full architecture breakdown, key findings, and connections to Generative Agents concepts. Mark with a pink dashed "后加" badge in the title.

2. **Papers Reference** — Add the paper to `html/papers-reference.html` in all three views:
   - **分类手册**: Add under the "个人补充" section (`cat-personal`, `#cat-personal`), with `personal-badge` ("后加 · 待讨论") marker
   - **卡片浏览**: Add an `rl-card` with `data-cat="personal"` and `rl-personal-badge`
   - Paper number continues from the current max (currently 96)

3. **Concept Map** — Add a node to the "外围方法论启发" subgraph in `html/concepts-map.html` Tab 1's Mermaid diagram. Use pink style (`stroke:#f472b6, color:#f9a8d4`) and append `★后加` to the node label to distinguish from original nodes. Add edges to relevant existing concepts. Also add a paper card with pink dashed border in the cards section below the diagram.

**Marking convention**: All user-added papers use a unified pink dashed-border badge (`personal-badge` class) with text "后加" so they can be instantly identified across all views. In Mermaid diagrams, user-added nodes use pink color and `★后加` suffix.

## Conversation Transcripts

Session logs in `logs/` directory (`conversation-*.txt` and `*-resume.txt`) capture prior research explorations. When resuming work, read these to understand the research trajectory and avoid duplicating prior analysis. The `session-summary-2026-04-05-06.md` file provides a structured overview of all prior work.
