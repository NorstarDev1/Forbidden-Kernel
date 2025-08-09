# 🚀 SIVIO Project Overview Dashboard

This dashboard provides a dynamic overview of the SIVIO project within this vault. It leverages the Dataview plugin to automatically update with new files, tasks, and project progress.

---

## 📂 Project Files

```dataview
LIST
FROM "projects/sivio"
WHERE file.name != "README_DEV"
SORT file.name ASC
```

---

## ✅ Open Tasks (SIVIO)

```dataview
TASK
FROM "projects/sivio"
WHERE !completed
SORT file.mtime DESC
```

---

## 📝 Recent Notes (SIVIO)

```dataview
LIST
FROM "projects/sivio"
SORT file.mtime DESC
LIMIT 10
```

---

## 🔗 Quick Links

- [[README_DEV]] (SIVIO Internal Dev Guide)
- [[apis/bridge_thread_mock/main]] (SIVIO Main API Entry Point)
- [[apis/bridge_thread_mock/bridge_thread_api]] (SIVIO Bridge Thread API Logic)

---

*This dashboard auto-updates using Dataview. Ensure the Dataview plugin is enabled in Obsidian.*