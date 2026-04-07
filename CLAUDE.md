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

## Conversation Transcripts

Session logs in `conversation-*.txt` and `*-resume.txt` capture prior research explorations. When resuming work, read these to understand the research trajectory and avoid duplicating prior analysis.
