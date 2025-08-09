---
tags:
  - dashboard
  - template
---

# 📊 Standardized Project Dashboard System Project Dashboard

This dashboard provides a dynamic overview for the `Standardized Project Dashboard System` project. It leverages the Dataview plugin to automatically update with new files, tasks, and project progress.

---

## 🚀 Project Overview

```dataview
TABLE status, start_date, end_date, team_lead
FROM #project-spec
WHERE project = "Standardized Project Dashboard System"
LIMIT 1
```

---

## 👥 Team

```dataview
LIST WITHOUT ID link(member + "_Filled_Profile")
FROM #project-spec
WHERE project = "Standardized Project Dashboard System"
FLATTEN team_members as member
SORT member ASC
```

---

## 🌟 Project Vision/Mission

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System" AND #vision
SORT file.name ASC
LIMIT 1
```

---

## 📝 Requirements/User Stories

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System" AND #requirements
SORT file.name ASC
```

---

## 📐 Design/Architecture

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System" AND #design
SORT file.name ASC
```

---

## 💻 Development Progress

```dataview
TASK
FROM "062_Projects/000_Standardized_Dashboard_System" AND #development
WHERE !completed
SORT file.mtime DESC
```

---

## 🧪 Testing Status

```dataview
TASK
FROM "062_Projects/000_Standardized_Dashboard_System" AND #testing
WHERE !completed
SORT file.mtime DESC
```

---

## 🚀 Deployment/Release

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System" AND #release
SORT file.name DESC
LIMIT 5
```

---

## 💬 Communication Log

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System" AND #communication
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
FROM "062_Projects/000_Standardized_Dashboard_System"
WHERE file.name != "README_DEV" AND file.name != "Standardized Project Dashboard System Project Dashboard" AND file.name != "Standardized Project Dashboard System Project Spec"
SORT file.name ASC
```

---

## ✅ Open Tasks

- [ ] Review Existing Dashboard Template.md
- [ ] Integrate Team Member Links
- [ ] Add SDLC Sections
- [ ] Define Standardized Metadata
- [ ] Create Standardized Project Dashboard System Project Spec.md
- [ ] Generate Meta-Project Dashboard
- [ ] Populate Meta-Project Dashboard with Plan Tasks
- [ ] Verify & Refine
- [ ] Update README_DEV.md (or similar)
- [ ] Final Review

---

## 📝 Recent Notes

```dataview
LIST
FROM "062_Projects/000_Standardized_Dashboard_System"
SORT file.mtime DESC
LIMIT 10
```

---

## 🔗 Quick Links

- [[062_Projects/000_Standardized_Dashboard_System/README_DEV]] (Internal Dev Guide)
- [[062_Projects/000_Standardized_Dashboard_System/SIVIO Project Spec]] (Project Specification)
- [[062_Projects/000_Standardized_Dashboard_System/apis/bridge_thread_mock/main]] (Main API Entry Point)
- [[062_Projects/000_Standardized_Dashboard_System/apis/bridge_thread_mock/bridge_thread_api]] (Bridge Thread API Logic)

---

*This dashboard auto-updates using Dataview. Ensure the Dataview plugin is enabled in Obsidian.*