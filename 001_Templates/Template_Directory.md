# 🏭 Template Directory

This is a dynamic directory of all templates in the SIVERSE Vault. It automatically updates as new templates are created and tagged with `#template`.

---

## All Templates

```dataview
TABLE template_description as "Description", file.link as "Template Name"
FROM #template
SORT file.name ASC
```
