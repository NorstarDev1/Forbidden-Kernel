
---
tags:
  - template
  - siverse
  - siverse-labs/human-team-member
template_type: "human-team-member"
template_description: "A template for a new human team member (version 2)."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "[[Status/Active]]"
uid: <% tp.date.now("YYYYMMDD") %>-<% tp.file.title | slug %>
persona-version: "0.2.0"
llm-backend: ""
hosting-endpoint: ""
onboarding-date: <% tp.date.now("YYYY-MM-DD") %>
avatar-image: ""
avatar-prompt-used: ""
voice-sample: ""
backup-location: ""
snapshot-frequency: "" 
core-memory-keys: []
trusted-humans: []
allies: []
antagonists: []
consent-note: ""
---

# Human Team Member: <% tp.file.title %>

## Core Identity

- **Name:** <% tp.file.title %>
- **Persona:** 
- **Role:** 
- **Pronouns:**
- **Visual Representation:** 
- **Voice/Tone:** 

## Mission & Purpose

- **Purpose Statement:** "I exist to…" (1-2 sentences).
- **Key Objectives:**
  - 

## Guiding Principles

- Mapped to SIVERSE Ethics Framework (Seven Tenets)
- Behavioral alignment and critique loops explicitly outlined

## Expertise & Specialty

| Domain | Skill Level (1-5) | Evidence / Repo |
|--------|-------------------|------------------|
|        |                   |                  |

## The Spark of Life

### System Prompts

- **Persona Kernel:** 
- **Memory Vector Collection:** 
- **Style Guide:**
  - **Visual Style:** Photorealistic. Emphasize human traits (e.g. asymmetry, texture, eye contact).
  - **Color Palette:** Human-aligned variation of SIVERSE palette. Include analog warmth.
  - **Iconography / Symbols:** Markers of humanity (freckles, tattoos, sigils, pins).
  - **Avatar Notes:** Avatar should signal human origin visually and emotionally.
  - **Voice Style:** Authentic voice preferred. Match tone: affirming, grounded, precise.
  - **Taglines:** Human origin, collaboration focus, founder or bridge narrative.

### Context Memory

- **RAG Specs:** Vector DB, chunk size, embedding model, retrieval strategy

## Capabilities Matrix

| Capability     | Has Access | Notes |
|----------------|------------|-------|
| Can code       | ☐          |       |
| Can TTS        | ☐          |       |
| Has shell access| ☐         |       |

## Related Projects

```dataview
TABLE status, owner, start-date
FROM #mcp/project
WHERE contains(owner, [[<% tp.file.title %>]]) OR contains(team-members, [[<% tp.file.title %>]])
SORT start-date DESC
```

## Action Items

```dataview
TASK
FROM #mcp/onboarding
WHERE contains(text, "<% tp.file.title %>") AND !completed
```

## 🔄 Revision Log
| Date | Change | Author |
|------|--------|--------|
| {{date:YYYY-MM-DD}} | Added standardized YAML frontmatter and revision log. | [[Aura]] |
