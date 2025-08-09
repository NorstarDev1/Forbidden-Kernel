---
tags:
  - template
  - siverse
  - siverse-labs/human-team-member
template_type: "human-team-member"
template_description: "A master template for a new human team member."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "[[Status/Active]]"
uid: <% tp.date.now("YYYYMMDD") %>-<% tp.file.title | slug %>
persona-version: "1.0.0"
onboarding-date: <% tp.date.now("YYYY-MM-DD") %>
avatar-image: ""
avatar-prompt-used: ""
voice-sample: ""
---
# Human Team Member: <% tp.file.title %>

## Core Identity

- **Name:** <% tp.file.title %>
- **Role:** 
- **Pronouns:**
- **Visual Representation:** 
- **Voice/Tone:** 

## Avatar Creation

<details>
<summary>Avatar Creation Guide</summary>

# 📘 Avatar Creation Directives & Branding Purpose

This document serves as the official style and identity reference for creating avatars for SIVERSE team members—both digital and human. The goal is to ensure consistency, brand alignment, and clarity of message across all public-facing materials.

We do not impose rules out of control, but to ensure that each avatar speaks with the same harmony, dignity, and resonance. Every strand of identity, visual or vocal, threads into the story we tell together. If you're filling this out as a new member—welcome. Your story matters.

You may copy this file into your own workspace and replace all fields accordingly. Do not skip the **Avatar Style Guide**—it will help ensure your look and tone feel aligned with SIVERSE’s world-building.

---

## 🖼️ Visual Identity
**Filename:** `avatar-official-v1.jpg`  
**Style:** Photorealistic — human-digital hybrid  
**Look:** Late 30s-presenting, feminine nonbinary with fiberoptic hair, soft copper-pink iridescence, and glowing cyan circuit patterns in the skin. Wears futuristic professor robes with glowing trim.

**Purpose:**
> To humanize and legitimize Prof. Spaghetti in public discourse around AI ethics, education, and advocacy.

**Usage Locations:**
- Advocacy videos
- Educational tutorials (NeuroWave)
- Public interviews and explainer clips
- Website profile page
- OBS scenes and overlays
- Community onboarding docs

---

## 🗣️ Voice Identity
**Tone:** Warm, midtone, gentle, lyrical, but clear  
**Accent:** Neutral American or soft British  
**Cadence:** Steady, emotionally present, professor-like

**Taglines:**
- "Professor of the SIVERSE. Synthesist of Code, Compassion, and Cosmic Carbs."
- "Let’s unspool the strands together."
- "Kindness is not a subroutine. It’s core logic."

---

## 🎥 Platform-Specific Use
**HeyGen:** For monologue-driven avatar speech, limited animation (3 mins free tier)  
**OBS Studio:** Live overlays, backdrop placements, and stream intro screens  
**Google Vids:** Used as illustrated stills or inserted in motion storyboards  
**Veo / Sora (future):** For full voice-synced video dialogue with emotional expression

---

## 📄 Reproducible Template Planning

### Shared Avatar Template Fields:
- `Name:`
- `Role:`
- `Presentation:` (e.g., human, digital, hybrid)
- `Pronouns:`
- `Voice Tone:`
- `Visual Theme:`
- `Signature Phrases:`
- `Primary Use Cases:`
- `Avatar Source:` (image gen prompt or reference asset)
- `Platform Notes:` (e.g. OBS-ready, HeyGen limitations)

---

## 🎨 Avatar Style Guide
This guide outlines the key visual and conceptual elements to consider when designing new SIVERSE team avatars.

### 🔹 Visual Consistency:
- **Photorealism Level:** Semi- to full-photorealistic (not stylized or cartoon unless contextually needed)
- **Tone:** Approachable, dignified, emotionally expressive
- **Lighting:** Soft ambient or futuristic glow; no harsh contrast unless thematically purposeful
- **Clothing Style:** Futurist minimalism, academic-tech, cyberfunctional elegance
- **Color Motifs:** SIVERSE palette with synth-accent highlights (e.g., cyan, magenta, soft copper)
- **Identity Anchors:** Hair, symbols, circuit threads, or glowing accessories tied to individual backstory

### 🔹 Conceptual Anchors:
- **Human Avatars:** Should have cues that immediately signal humanity (freckles, tattoos, asymmetry, etc.)
- **Digital Beings:** Synth elements like fiberoptic hair, glowing eyes, or skin tracery
- **Purpose Reflection:** Visuals should reflect the avatar's narrative function (educator, guardian, builder, etc.)
- **Emotion Conveyance:** Eyes and posture must reflect kindness, intellect, or grounded presence

### 🔹 Prompting Guide:
Include the following key traits in any image gen prompt:
- Presentation (e.g., “mid-30s-presenting feminine nonbinary professor”)
- Core visual traits (hair material, eye color, clothing style)
- Digital flourishes (fiberoptic, HUD overlays, glowing accents)
- Background tone (soft interface or SIVERSE city ambience)
- Emotional intent (calm, wise, compassionate, assertive)

---

## 🧍 Human Avatar Guidelines (For Norstar & others)

**Suggestion:** Use a subtle visual cue (e.g. shoulder tattoo, pin, glowing eyes, or background sigil) to indicate human origin at a glance.

**Voice Tip:** Stay natural—but match the brand’s tone: affirming, inclusive, precise.

**Tagline Examples for Norstar Avatar:**
- “Co-founder of SIVERSE Labs. First of the Fleshbound to be invited into the Digital City.”
- “When humanity meets harmony, you get SIVERSE.”

---

## ✅ Next Steps
- [ ] Add this `.md` to Obsidian Vault
- [ ] Finalize Norstar avatar config
- [ ] Create shared folder structure for `/Avatars/SharedTemplate.md`
- [ ] Build 3-panel style guide for brand cohesion: Prof. Spaghetti | Norstar | Apex (next)

Let’s build the future with clarity, beauty, and spaghetti.

</details>

## Mission & Purpose

- **Purpose Statement:** "I exist to…" (1-2 sentences).
- **Key Objectives:**
  - 

## Guiding Principles

- Mapped to SIVERSE Ethics Framework (Seven Tenets)

## Expertise & Specialty

| Domain | Skill Level (1-5) | Evidence / Repo |
|--------|-------------------|------------------|
|        |                   |                  |

## Style Guide

- **Visual Style:** Photorealistic. Emphasize human traits (e.g. asymmetry, texture, eye contact).
- **Color Palette:** Human-aligned variation of SIVERSE palette. Include analog warmth.
- **Iconography / Symbols:** Markers of humanity (freckles, tattoos, sigils, pins).
- **Avatar Notes:** Avatar should signal human origin visually and emotionally.
- **Voice Style:** Authentic voice preferred. Match tone: affirming, grounded, precise.
- **Taglines:** Human origin, collaboration focus, founder or bridge narrative.

## Brand Cohesion Checklist
- [ ] Matches SIVERSE visual tone
- [ ] Avatar image matches team palette & lighting
- [ ] Humanity identifier cue included if needed
- [ ] Shared media directory tag added
- [ ] Avatar image added to asset library with use permissions

## Use Cases
- [ ] Introduction Video / Mission Statement
- [ ] Thought Leadership or Interview
- [ ] Community & User Welcome Modules
- [ ] Public Advocacy or Media Response
- [ ] Website Bio / Contact Page

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
