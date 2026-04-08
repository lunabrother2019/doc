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

- `html/generative-agents-concept-map.html` — Mermaid-based diagram showing concept evolution from original paper to modern agentic AI
- `html/papers-table.html` — categorized table of 39 papers across 17 categories (memory, reflection, planning, multi-agent, scaling, embodied AI, training, survey, patent, game, medical, framework, benchmark, hallucination, protocol)
- `html/reading-list.html` — 64-card filterable bibliography with color-coded categories and clickable URLs

## Paper Addition Workflow

When the user mentions a paper (by name, link, or description), always perform these three steps:

1. **Deep Dive** — Create a detailed analysis HTML file in `html/deep-dive/` (numbered sequentially, currently up to 09). Include full architecture breakdown, key findings, and connections to Generative Agents concepts. Mark with a pink dashed "后加" badge in the title.

2. **Papers Reference** — Add the paper to `html/papers-reference.html` in all three views:
   - **分类手册**: Add under the "个人补充" section (`cat-personal`, `#cat-personal`), with `personal-badge` ("后加 · 待讨论") marker
   - **卡片浏览**: Add an `rl-card` with `data-cat="personal"` and `rl-personal-badge`
   - Paper number continues from the current max (currently 78)

3. **Concept Map** — Add a node and edges in `html/concepts-map.html` linking the paper to relevant existing concepts. Use a distinct style to mark it as a personal addition.

**Marking convention**: All user-added papers use a unified pink dashed-border badge (`personal-badge` class) with text "后加" so they can be instantly identified across all views.

## Conversation Transcripts

Session logs in `conversation-*.txt` and `*-resume.txt` capture prior research explorations. When resuming work, read these to understand the research trajectory and avoid duplicating prior analysis.
