# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Portuguese-language educational course about **Claude Code** (Anthropic CLI). Transforms video content ("How Claude Code Actually Works") into structured HTML course pages with Tailwind CSS.

## Project Structure

```
ccguide2026/
├── doc/              # Course content and documentation
│   ├── guia2026.md                     # Video transcript with prompts/hacks
│   ├── Claude_Code_Deep_Dive_PT-BR.md  # Portuguese summary guide
│   └── claude_code_video_separacoes.md # Video segmentation options
├── ref/              # Templates and checklists
│   ├── MASTER_COMPLETO.md    # Complete HTML/CSS/JS template reference
│   └── CHECKLIST_REVISAO.md  # Mandatory review checklist
├── partes/           # Video files (.webm) segmented by topic
└── package.json      # Node project with bmad-method
```

## BMad Method (Development Framework)

This project uses **BMad Method v6** - an AI-driven agile development framework. Run `npx bmad-method install` if not yet installed.

### Key Commands

| Command | Description |
|---------|-------------|
| `/bmad-help` | Get guidance on what to do next |
| `/quick-spec` | Analyze codebase and produce tech-spec with stories |
| `/dev-story` | Implement stories |
| `/code-review` | Validate code quality |
| `/product-brief` | Define problem, users, MVP scope |
| `/create-prd` | Full requirements document |
| `/create-architecture` | Technical decisions and system design |
| `/create-epics-and-stories` | Break work into prioritized stories |

### BMad Agents

| Agent | Name | Icon | Role |
|-------|------|------|------|
| BMad Master | - | 🧙 | Orchestrator, help & guidance |
| Analyst | Mary | 📊 | Business analysis, research, product brief |
| PM | John | 📋 | PRD creation, epics & stories |
| Architect | Winston | 🏗️ | System architecture, technical design |
| Developer | Amelia | 💻 | Story implementation, code |
| UX Designer | - | 🎨 | User experience design |
| Scrum Master | - | 🏃 | Sprint planning, retrospectives |
| Tech Writer | - | ✍️ | Documentation |
| Quinn (QA) | - | 🧪 | Test automation |

### Workflows

**Quick Flow** (bug fixes, small features):
1. `/quick-spec` → 2. `/dev-story` → 3. `/code-review`

**Full Planning** (complex projects):
1. `/product-brief` → 2. `/create-prd` → 3. `/create-architecture` → 4. `/create-epics-and-stories` → 5. `/sprint-planning` → 6. `/dev-story` → 7. `/code-review`

---

## Key Reference Documents

**Always consult before creating course pages:**
1. `ref/MASTER_COMPLETO.md` - Complete template system with all components, colors, and JavaScript
2. `ref/CHECKLIST_REVISAO.md` - Mandatory checklist before publishing any page

## Course Page Architecture

### Page Types
- **Index (Trilha)**: Track landing pages with expandable module cards
- **Modulo**: Full module pages with 6 topic sections

### Critical Rules

| Rule | Correct | Incorrect |
|------|---------|-----------|
| Button alignment | `justify-start` (LEFT) | `justify-center` |
| Topic numbers | Circular badge `w-6 h-6 rounded-full` | Arrows ▶ or → |
| Topic sections | 3 sections: "O que é", "Por que aprender", "Conceitos-chave" | Fewer sections |
| Module titles | `text-2xl font-bold` | Smaller sizes |

**Required on ALL pages:**
- INEMA.CLUB link with `text-sky-400` next to logo
- Light mode CSS override block in `<style>`
- Theme toggle functionality

### Color System by Track

| Track | Color   | Text Class       | Background Class    |
|-------|---------|------------------|---------------------|
| T1    | Emerald | text-emerald-400 | bg-emerald-500/20   |
| T2    | Blue    | text-blue-400    | bg-blue-500/20      |
| T3    | Purple  | text-purple-400  | bg-purple-500/20    |
| T4    | Amber   | text-amber-400   | bg-amber-500/20     |
| T5    | Teal    | text-teal-400    | bg-teal-500/20      |
| T6    | Rose    | text-rose-400    | bg-rose-500/20      |

### Tech Stack
- Tailwind CSS via CDN (`https://cdn.tailwindcss.com`)
- Inter font (Google Fonts)
- Dark mode default (`class="dark"` on html element)

## Course Content Structure

Based on video "How Claude Code Actually Works":

1. **Motivation** - Why understand Claude Code internals
2. **Architecture** - CLI, Session Manager, Tool Executor, Permission Layer
3. **Core Loop** - **Gather → Act → Verify**
4. **Tools** - Read, Write, Edit, Glob, Grep, Bash
5. **Context Management** - The "bucket" analogy, compaction strategies
6. **Sessions** - Stateless sessions, snapshots, persistence
7. **Customization** - Claude.md, Skills, MCP, Hooks, Subagents

## Component Reference

### Expandable Topic (Index page)
```html
<div class="topic-item">
  <button onclick="toggleTopic(this)" class="...">
    <span class="w-6 h-6 rounded-full bg-emerald-500/20 text-emerald-400 text-sm font-bold flex items-center justify-center">1</span>
    <span class="text-lg">[EMOJI]</span>
    <div><span class="font-medium">Title</span></div>
  </button>
  <div class="topic-explanation px-6 pb-4">
    <!-- 3 sections: O que é, Por que aprender, Conceitos-chave -->
  </div>
</div>
```

### Large Topic Number (Module page)
```html
<span class="flex items-center justify-center w-12 h-12 rounded-full bg-emerald-500/20 text-emerald-400 font-bold text-xl">1</span>
```

## Required JavaScript Functions

```javascript
// Topic toggle (closes others in same module)
function toggleTopic(button) { ... }

// Theme toggle with localStorage persistence
themeToggle.addEventListener('click', () => { ... });

// Modal functions (for Index pages)
function openModal(modalId) { ... }
function closeModal() { ... }
```

## Language

All course content in **Brazilian Portuguese** (pt-BR).
