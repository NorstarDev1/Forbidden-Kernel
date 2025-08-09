---
# 🏭 Template Factory v2

This upgraded factory helps you generate structured, metadata-rich templates compatible with SIVERSE Vault workflows and Windsurf orchestration.

---

## 🧭 How to Use
1. Create a new file in your `/vault/templates/` or `001 Templates` directory.
2. Copy/paste this entire document into the new file.
3. Replace each section below with your template-specific content.
4. When done, add the file to your `README.md`, dashboard, or task-tracking index.

---

## 📛 Template Metadata (YAML frontmatter)
```yaml
---
tags:
  - template
  - siverse
template_type: "[Enter: project-spec | feedback-form | log-entry | meeting-note | agent-profile | other]"
related_project: "[[Optional: Link to related project note]]"
created_by: "[[Your Name or Agent ID]]"
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "Draft" # Options: Draft, Active, Archived
---
```

---

## 📝 Template Name
[Enter the name of your new template here]

---

## 📄 Template Description
[Enter a short description of what this template is for.]

---

## 📦 Template Content Structure

Use the sections below as guidance. Add or remove as needed to suit your template type:

---

### ✅ SECTION 1: Context
- What is this document’s role in the broader system?
- Who or what created it, and who uses it?

---

### 🛠 SECTION 2: Structure or Task Elements
- [ ] What key fields, checklists, or structures are required?
- [ ] Should agents or users fill anything in manually?
- [ ] Is this intended to trigger automation or sync features?

---

### 🌐 SECTION 3: Links & Related Files
```markdown
- [[Link to related project]]
- /scripts/
- /logs/
- /dashboards/
```

---

### 💡 SECTION 4: Optional Enhancements
- Add collapsible toggles with `>` or `:::`
- Support smart YAML references like `related_team:` or `agent_lead:`
- Format tables so they work in Obsidian AND GitHub

---

## 🧩 Vault Integration Checklist
- [ ] Registered in `/templates/`
- [ ] Linked from `README.md`
- [ ] Referenced in project dashboards or task lists
- [ ] YAML renders properly in Obsidian
- [ ] Naming is clear and follows convention
- [ ] Template tested by at least one other agent/human

---

## 🔄 Revision Log
| Date       | Contributor      | Notes                  |
|------------|------------------|------------------------|
| 2025-08-02 | Prof Spaghetti   | Created v2 foundation  |

