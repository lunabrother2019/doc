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
- `html/papers-reference.html` — 83-paper reference with 3 views (分类手册 / 卡片浏览 / 表格视图), includes "个人补充" category for user-added papers
- `html/architecture-study.html` — 6-tab Agent architecture study (Claude Code source analysis, competitive analysis, implementation plan)
- `html/deep-dive/01-05` — 5 paper deep-dive analyses (01-03 original, 04-05 user-added with "后加" badge)

## Paper Addition Workflow

When the user mentions a paper (by name, link, or description), always perform these three steps:

1. **Deep Dive** — Create a detailed analysis HTML file in `html/deep-dive/` (numbered sequentially, currently up to 05). Include full architecture breakdown, key findings, and connections to Generative Agents concepts. Mark with a pink dashed "后加" badge in the title.

2. **Papers Reference** — Add the paper to `html/papers-reference.html` in all three views:
   - **分类手册**: Add under the "个人补充" section (`cat-personal`, `#cat-personal`), with `personal-badge` ("后加 · 待讨论") marker
   - **卡片浏览**: Add an `rl-card` with `data-cat="personal"` and `rl-personal-badge`
   - Paper number continues from the current max (currently 83)

3. **Concept Map** — Add a node to the "外围方法论启发" subgraph in `html/concepts-map.html` Tab 1's Mermaid diagram. Use pink style (`stroke:#f472b6, color:#f9a8d4`) and append `★后加` to the node label to distinguish from original nodes. Add edges to relevant existing concepts. Also add a paper card with pink dashed border in the cards section below the diagram.

**Marking convention**: All user-added papers use a unified pink dashed-border badge (`personal-badge` class) with text "后加" so they can be instantly identified across all views. In Mermaid diagrams, user-added nodes use pink color and `★后加` suffix.

## Conversation Transcripts

Session logs in `logs/` directory (`conversation-*.txt` and `*-resume.txt`) capture prior research explorations. When resuming work, read these to understand the research trajectory and avoid duplicating prior analysis. The `session-summary-2026-04-05-06.md` file provides a structured overview of all prior work.
