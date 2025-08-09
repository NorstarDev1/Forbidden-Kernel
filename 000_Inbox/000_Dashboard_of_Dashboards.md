# 🌐 Dashboard of Dashboards

This central dashboard provides an overview and quick access to all project-specific dashboards within this vault. It uses Dataview to automatically list all notes tagged with `#dashboard`.

---

## 📊 All Project Dashboards

```dataview
LIST
FROM #dashboard
WHERE file.name != "Dashboard of Dashboards"
SORT file.name ASC
```

---

*This dashboard auto-updates using Dataview. Ensure the Dataview plugin is enabled in Obsidian.*
