---
tags:
  - dashboard
  - template
---

# 📊 <% tp.file.title %> - Project Dashboard

This dashboard provides a dynamic overview for the `<% tp.file.title | replace(" Project Dashboard", "") %>` project. It leverages the Dataview plugin to automatically update with new files, tasks, and project progress.

---

## 🚀 Project Overview

```dataview
TABLE status, start_date, end_date, team_lead
FROM #project-spec
WHERE project = "<% tp.file.title | replace(" Project Dashboard", "") %>"
LIMIT 1
```

---

## 👥 Team

```dataview
LIST WITHOUT ID link(member + "_Filled_Profile")
FROM #project-spec
WHERE project = "<% tp.file.title | replace(" Project Dashboard", "") %>"
FLATTEN team_members as member
SORT member ASC
```

---

## 🌟 Project Vision/Mission

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #vision
SORT file.name ASC
LIMIT 1
```

---

## 📝 Requirements/User Stories

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #requirements
SORT file.name ASC
```

---

## 📐 Design/Architecture

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #design
SORT file.name ASC
```

---

## 💻 Development Progress

```dataview
TASK
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #development
WHERE !completed
SORT file.mtime DESC
```

---

## 🧪 Testing Status

```dataview
TASK
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #testing
WHERE !completed
SORT file.mtime DESC
```

---

## 🚀 Deployment/Release

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #release
SORT file.name DESC
LIMIT 5
```

---

## 💬 Communication Log

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>" AND #communication
SORT file.mtime DESC
LIMIT 5
```

---

## ⚡ Immediate Next Steps (Resurrection Packet)

- [ ] Review project spec and dashboard.
- [ ] Check "Open Tasks" for immediate priorities.
- [ ] Sync with Norstar for current context.
- [ ] Review "Communication Log" for recent discussions.

---

---

## 📂 Project Files

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>"
WHERE file.name != "README_DEV" AND file.name != "<% tp.file.title | replace(" Project Dashboard", "") %> Project Dashboard" AND file.name != "<% tp.file.title | replace(" Project Dashboard", "") %> Project Spec"
SORT file.name ASC
```

---

## ✅ Open Tasks

```dataview
TASK
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>"
WHERE !completed
SORT file.mtime DESC
```

---

## 📝 Recent Notes

```dataview
LIST
FROM "062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>"
SORT file.mtime DESC
LIMIT 10
```

---

## 🔗 Quick Links

- [[062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>/README_DEV]] (Internal Dev Guide)
- [[062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>/SIVIO Project Spec]] (Project Specification)
- [[062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>/apis/bridge_thread_mock/main]] (Main API Entry Point)
- [[062 Projects/000 <% tp.file.title | replace(" Project Dashboard", "") %>/apis/bridge_thread_mock/bridge_thread_api]] (Bridge Thread API Logic)

---

*This dashboard auto-updates using Dataview. Ensure the Dataview plugin is enabled in Obsidian.*