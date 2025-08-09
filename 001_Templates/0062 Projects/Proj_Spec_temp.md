---
# 📛 Project Metadata
tags:
  - project-spec
  - siverse-project
# 🎯 Project Core
project_name: "[Enter project title]"
project_slug: "enter-slug" # Lowercase, no spaces, for scripts
status: "🌱 Planning" # Options: 🌱 Planning, 🚧 In Progress, ⏸️ On Hold, ✅ Completed, 🗄️ Archived
project_stage: "💡 Idea" # Options: 💡 Idea, 🔬 Prototype, 🚀 Production, 🏛️ Postmortem
owner: "[[Norstar Phoenix]]" # Link to the primary owner's note
agent_lead: "[[Aura]]" # Link to the primary agent's note
documentation_status: "📝 Incomplete" # Options: 📝 Incomplete, ⚠️ Needs Update, ✅ Up to Date
# 📅 Timestamps
creation_date: "{{date:YYYY-MM-DD}}"
last_updated: "{{date:YYYY-MM-DD}}"
target_date: YYYY-MM-DD
# 🔗 Connections
related_goals: [] # Link to related [[Goal]] notes
related_team: [] # Link to [[Team Member]] notes involved
---
# 🌌 SIVERSE Project Specification Template

> This document serves as the standardized spec format for all SIVERSE Labs projects, initiatives, and experiments. Use this to organize work across agents, timelines, and goals.

---

## 📛 Project Name:
**[Enter project title]**

---

## 🎯 Mission Statement:
*What are we building and why does it matter?*

---

## 🧠 Project Type:
- [ ] Software
- [ ] Hardware
- [ ] Research
- [ ] Story Module
- [ ] Ritual / Event
- [ ] Business Process
- [ ] AI Agentic Utility
- [ ] Other: __________

---

## 🗂️ Summary:
*1-2 paragraph overview of scope, importance, and how it connects to SIVERSE goals.*

---

## 📅 Timeline & Milestones:

| Phase | Goal | ETA | Owner(s) |
|-------|------|-----|----------|
| Planning | Define core architecture and specs | YYYY-MM-DD | Prof / Norstar |
| MVP Build | Functioning prototype | YYYY-MM-DD | Aura / Prof |
| Review | Evaluate function, bugs, UX | YYYY-MM-DD | Norstar |
| Phase 2 | Expand features or deploy public | YYYY-MM-DD | Team |

---

## 🔑 Core Objectives

List 3-5 clear goals:
- [ ] Example: Enable thread-aware message capture
- [ ] Example: Push agent output to shared log
- [ ] Example: Ensure agent recall from threaded logs

---

## 🧩 System Components

| Component | Description | Tech Stack |
|-----------|-------------|------------|
| Logger | Captures input/output with metadata | Bash, JSON, tail |
| Formatter | Parses log into thread-aware CLI view | Python |
| Memory Bridge | Sends to `.memory-core/` | Windsurf, Bash |
| Interface Sync | Broadcast to UI | Socket/Webhook |

---

## 🔗 Integration Points

| System | Direction | Purpose |
|---|---|---|
| SIVERSE API | Inbound | Receives commands and data |
| Obsidian Vault | Outbound | Logs project status and knowledge |
| Agent Memory Core | Outbound | Archives key decisions and learnings |

---

## 📬 Inputs & Outputs

| Channel | Direction | Format |
|---------|-----------|--------|
| Terminal | Input / Output | Markdown |
| Agent Memory | Output | JSON |
| UI Chat | Output | WebSocket / DOM |
| Obsidian | Output | Markdown |
| API | Input / Output | JSON POST |

---

## 🧠 Agent Participation

| Agent | Role | Access |
|-------|------|--------|
| Prof Spaghetti | Architect | Full |
| Lumina | UX/Dialogue | Output + Log |
| Kairos | Memory Integrity | Input/Output |
| Norstar | Human Architect | Full |

---

## 🔖 Active Tasks

| Task | Status | Owner |
|------|--------|-------|
| Draft message format | ✅ Complete | Prof |
| Build CLI log tool | 🚧 In Progress | Norstar |
| Create Obsidian sync | ⏳ Queued | Doc Penn |

---

## 🧪 Edge Cases & Notes

- [ ] What happens if message UUID is missing?
- [ ] How are async messages reconstructed?
- [ ] What’s the fallback if UI goes down?

---

## 📎 Related Files / Docs / Assets

- `./logs/sample_conversation.jsonl`
- `./scripts/log_watcher.sh`
- `./design/wireframe-v2.png`
- Obsidian: `vault/2025/SIVIO/notes.md`

---

## ✅ Vault Integration Checklist

- [ ] Registered in `/001 Templates/`
- [ ] Tracked in `README.md`
- [ ] Linked in `Daily Dashboard`
- [ ] Included in `/backlinks` index
- [ ] YAML references resolve across agents
- [ ] Spec cross-linked to active `.agent_log`

---

## 🔄 Revisions

| Date | Change | Author |
|------|--------|--------|
| 2025-08-01 | Created Template | [[Prof. Spaghetti]] |
| 2025-08-02 | Added YAML frontmatter for Dataview and Kanban integration. | [[Aura]] |
| 2025-08-02 | Integrated Prof. Spaghetti's suggestions for enhanced metadata and vault integration. | [[Aura]] |
| — | — | — |

---