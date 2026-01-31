# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Portuguese-language educational course project about **Claude Code** (the Anthropic CLI tool). The project transforms video content ("How Claude Code Actually Works") into structured course materials with HTML pages using Tailwind CSS.

## Project Structure

```
ccguide2026/
├── doc/           # Main documentation and course content
│   ├── guia2026.md                    # Video timestamps and transcript
│   ├── Claude_Code_Deep_Dive_PT-BR.md # Portuguese deep-dive guide
│   └── claude_code_video_separacoes.md # Video segmentation options
├── ref/           # Reference templates and checklists
│   ├── MASTER_COMPLETO.md  # Complete HTML/CSS template reference
│   └── CHECKLIST_REVISAO.md # Review checklist for pages
├── partes/        # Video files (.webm) segmented by topic
└── package.json   # Node project (uses bmad-method dev dependency)
```

## Key Reference Documents

When creating course pages, consult these in order:
1. **ref/MASTER_COMPLETO.md** - Complete template system with all components
2. **ref/CHECKLIST_REVISAO.md** - Mandatory review checklist before publishing

## Course Page Architecture

### Page Types
- **Index (Trilha)**: Track landing pages with expandable module cards
- **Modulo**: Full module pages with 6 topic sections

### Critical Rules (from MASTER_COMPLETO.md)

1. **Buttons always LEFT-aligned**: Use `justify-start`, never `justify-center`
2. **Topic numbers in circles**: Never use arrows (▶), always circular number badges
3. **Three sections per topic**: Each expandable topic must have "O que é", "Por que aprender", "Conceitos-chave"
4. **INEMA.CLUB link**: Required on all pages with `text-sky-400`
5. **Light mode CSS**: Required override block in every page
6. **Module titles**: Use `text-2xl font-bold`

### Color System by Track (Trilha)

| Track | Color   | text-*          | bg-*/20           |
|-------|---------|-----------------|-------------------|
| T1    | Emerald | text-emerald-400| bg-emerald-500/20 |
| T2    | Blue    | text-blue-400   | bg-blue-500/20    |
| T3    | Purple  | text-purple-400 | bg-purple-500/20  |
| T4    | Amber   | text-amber-400  | bg-amber-500/20   |
| T5    | Teal    | text-teal-400   | bg-teal-500/20    |
| T6    | Rose    | text-rose-400   | bg-rose-500/20    |

### Required Technologies
- Tailwind CSS (via CDN)
- Inter font (Google Fonts)
- Dark mode as default (`class="dark"` on html)

## Content Structure

The course covers Claude Code internals based on video segmentation:
1. Motivation and learning approach
2. Architecture (CLI, Session Manager, Tool Executor, Permission Layer)
3. Core loop: **Gather → Act → Verify**
4. Tools: Read, Write, Edit, Glob, Grep, Bash
5. Context management and compaction
6. Sessions and persistence
7. Customization: Claude.md, Skills, MCP, Hooks

## Language

All course content is in **Brazilian Portuguese** (pt-BR).
