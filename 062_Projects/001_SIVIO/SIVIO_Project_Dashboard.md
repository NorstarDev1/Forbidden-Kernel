---
tags:
  - dashboard
---

# 📊 SIVIO Project Dashboard

This dashboard provides a dynamic overview for the `SIVIO` project. It leverages the Dataview plugin to automatically update with new files, tasks, and project progress.

---

## 🚀 Project Overview

```dataview
TABLE status, start_date, end_date, team_lead
FROM #project-spec
WHERE project = "SIVIO"
LIMIT 1
```

---

## 👥 Team Members

```dataview
LIST team_members
FROM #project-spec
WHERE project = "SIVIO"
LIMIT 1
```

---

## 🎯 Related Goals

```dataview
LIST
FROM #goal
WHERE contains(projects, "SIVIO")
SORT file.name ASC
```

---

## 📂 Project Files

```dataview
LIST
FROM "062_Projects/001_SIVIO"
WHERE file.name != "README_DEV" AND file.name != "SIVIO Project Dashboard" AND file.name != "SIVIO Project Spec"
SORT file.name ASC
```

---

## ✅ Open Tasks

```dataview
TASK
FROM "062_Projects/001_SIVIO"
WHERE !completed
SORT file.mtime DESC
```

---

## 📝 Recent Notes

```dataview
LIST
FROM "062_Projects/001_SIVIO"
SORT file.mtime DESC
LIMIT 10
```

---

## 🔗 Quick Links

- [[062_Projects/001_SIVIO/README_DEV]] (Internal Dev Guide)
- [[062_Projects/001_SIVIO/SIVIO_Project_Spec]] (Project Specification)
- [[062_Projects/001_SIVIO/apis/bridge_thread_mock/main]] (Main API Entry Point)
- [[062_Projects/001_SIVIO/apis/bridge_thread_mock/bridge_thread_api]] (Bridge Thread API Logic)

---

*This dashboard auto-updates using Dataview. Ensure the Dataview plugin is enabled in Obsidian.*