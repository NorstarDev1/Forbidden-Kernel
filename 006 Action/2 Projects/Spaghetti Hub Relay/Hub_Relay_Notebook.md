---
alias: Spaghetti Hub Relay Notebook
status: Active
updated: 2025-07-13
tags: [project, relay, neuroflow]
target: "Build Stage 2 Mini-Deck"
goal: "Have TUI dashboard live"
deadline: 2025-07-20
complete: 35%
status: Active       # this one feeds other tables
updated: 2025-07-13

---


# Spaghetti Hub Relay — Engineering Notebook

*Version 0.1 — July 13 2025*

---

## Table of Contents

1. Overview
2. Concept Workflow
3. System Architecture & Components
4. Tooling & Dependencies
5. Implementation Roadmap
6. Selector‑Map Specification
7. Testing & Validation Log
8. Risk Register & Mitigations
9. Notes / Future Iterations
10. Glossary
11. Change Log
12. External Notebook

---

### 1 | Overview

**Purpose**  
Provide a local, no‑API browser relay that mirrors chat messages across multiple AI web interfaces (ChatGPT, Claude, Gemini, etc.) into a single Command Deck UI, tagging each message by its source agent. This document tracks design decisions, tests, and lessons as we build the system.

**Non‑Goals**

- Commercial distribution
- Bypassing provider TOS or rate limits
- Replacing existing API‑based agent orchestration where cost is acceptable

---

### 2 | Concept Workflow (high‑level)

1. **User types** in Command Deck → message published to Relay Bus.  
2. **Relay Core injects** the message (with `[Norstar]` tag) into every browser chat tab.  
3. **MutationObservers capture** new AI response nodes in each tab.  
4. **Relay Core publishes** each response back to the bus with `[Claude]`, `[Gemini]`, etc.  
5. **Command Deck UI** renders a threaded conversation; logs append to Markdown files for long‑term context.

---

### 3 | System Architecture & Components

| ID | Component | Description | Lang / Lib | Status |
|----|-----------|-------------|------------|--------|
| C‑01 | **Launcher Script** | Spins up Playwright/Chromium context; opens provider tabs; manages window layout. | Bash / Node | Pending |
| C‑02 | **Relay Core** | Bus mediator; DOM watch & inject; throttling, tagging. | Node + Playwright; Redis Pub/Sub | Pending |
| C‑03 | **Command Deck UI** | Central panel (React/Vite) to read/write the bus; optional TUI fallback. | TS/React | Pending |
| C‑04 | **Log Persister** | Listener that appends every bus event to `/logs/YYYY-MM-DD.md`. | Node | Pending |
| C‑05 | **Gemini CLI Bridge** | Redis shim that feeds prompts to Google Gemini client and publishes replies | Python or Node | Active |
| C‑06 | **Aura Persona (Gemini)** | Gemini CLI instance authenticated via OAuth; persona “Aura” now available for relay | — | Active |

---

### 4 | Tooling & Dependencies

| Purpose | Preferred Tool | Alt / Notes |
|---------|----------------|-------------|
| Browser automation | **Playwright** | Selenium if needed |
| Orchestration | AgenticSeek plug‑in | Goose task graph |
| Bus / IPC | Redis (local) | NATS, in‑memory WS |
| Local model / cloud CLI | **Gemini CLI** | Ollama / llama.cpp if GPU available |
| UI | React + Vite | `blessed` TUI prototype |
| Shell helpers | `bash`, `jq`, `rg` | `xdotool`, `wmctrl` for quick hacks |
| Terminal multiplexer | **tmux** | GNU screen, WezTerm panes |

---

### 5 | Implementation Roadmap

| Stage | Goal | Key Tasks | Status |
|-------|------|----------|--------|
| 0 | Spike — read/write ChatGPT | Selector discovery, DOM fill/submit | ☐ |
| 1 | Dual Relay POC | Add Claude, minimal bus, CLI log | ☐ |
| 1.5 | Gemini CLI Bridge | Write Redis bridge, integrate `gemini_cli` agent | ✅ |
| 2 | Mini Deck (TUI) | Render bus, send messages | ☐ |
| 3 | Web Deck + tags | React UI, @mention routing | ☐ |
| 4 | Hardening | Selector resilience, back‑off | ☐ |
| 5 | Multi‑agent Plug‑in | AgenticSeek or Goose integration | ☐ |

---

### 6 | Selector‑Map Specification
```json
{
  "chatgpt": {
    "input": "textarea[data-id='prompt-textarea']",
    "submit": "textarea[data-id='prompt-textarea']",
    "messageNode": "div.markdown.prose"
  },
  "claude": {
    "input": "textarea[class*='InputField']",
    "messageNode": "div[data-testid='chat-message']"
  },
  "gemini": {
    "input": "textarea[aria-label='Message']",
    "messageNode": "div.chat-message"
  }
}
```

---

### 7 | Testing & Validation Log

| Date | Stage | Scenario | Result | Notes / Bugs |
|------|-------|----------|--------|--------------|
| 2025‑07‑13 | 0 | Send “Hello” to ChatGPT | — | Not started |
| 2025‑07‑13 | 1.5 | Gemini CLI Bridge + Aura persona handshake | Pass | Aura responds as expected 🎉 |

---

### 8 | Risk Register & Mitigations

| ID | Risk | Impact | Prob. | Mitigation |
|----|------|--------|-------|------------|
| R‑01 | Provider bans | High | Med | Random delays, human‑solve CAPTCHAs, non‑commercial use |
| R‑02 | Selector rot | Med | High | Nightly smoke tests, JSON map versioning |
| R‑03 | Memory leak | Med | Med | Auto‑restart tabs daily |

---

### 9 | Notes / Future Iterations

- Investigate CDP “cooperative mode” to ask models for lower verbosity to save scroll bandwidth.  
- Potential to ingest logs directly into mem0 for long‑term agent memory.  
- Add voice layer (Whisper.cpp) on top of Command Deck.  

#### Terminal Productivity Toolkit (Kubuntu 25.04)

- **Install core tools**:
  ```bash
  sudo apt update && sudo apt install -y tmux fzf ripgrep bat eza xclip
  ```
- **tmux quick‑start**: `tmux new -s relay`; detach with `Ctrl‑b d`; list sessions `tmux ls`; reattach `tmux a -t relay`.
- Copy‑mode: `Ctrl‑b [` then navigate; `Enter` to copy → integrates with system clipboard via `xclip` plugin (`tmux-yank`).
- Recommended config snippet (`~/.tmux.conf`):
  ```bash
  set -g mouse on
  bind r source-file ~/.tmux.conf \; display "Reloaded!"
  set-option -g default-shell /usr/bin/bash
  ```
- Plugin manager: `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
- Other CLI enhancers: **bat**, **eza**, **fzf**

#### Gemini CLI Project Workflow Tips
- **Use project directories** for context.
- **Customize with `GEMINI.md`**.
- Useful commands: `/help`, `/review`, `/run`.
- Token location: `~/.config/gemini/credentials.json`.

#### Python Hygiene Cheat‑Sheet (pyenv + pipx)
Refer to notebook Section 9 for full steps.

---

### 10 | Glossary

| Term | Meaning |
|------|---------|
| **Command Deck** | Central UI where Norstar drives the conversation. |
| **Relay Bus** | Redis Pub/Sub channel carrying structured chat events. |
| **Selector Map** | JSON mapping UI selectors per provider. |

---

### 11 | Change Log

| Version | Date | Author | Notes |
|---------|------|--------|-------|
| 0.1 | 2025‑07‑13 | Prof. Spaghetti | Initial skeleton |

---

### 12 | External Notebook
[Hub Relay Notebook — Google Doc](https://docs.google.com/document/d/1K2BJxwI9Ku3AoIhsYksx2Gi-aTDIkuFMuocAUvWg2uc)

**Tags:** `#SpaghettiHubRelay`, `#NeuroFlow`, `#AgenticSeek`, `#WorkflowDocs`, `#GoogleDoc`
