---
banner: "https://preview.redd.it/arqa352ph7x61.jpg?width=960&crop=smart&auto=webp&s=84f9245d607b029667d5bfc4abf36547fc6213de"
tags:
  - template
  - siverse
  - periodic/weekly-note
template_type: "periodic-weekly-note"
template_description: "A template for a weekly note."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "Draft"
week: <% tp.date.now("ww") %>
month: <% tp.date.now("YYYY - MM-MMMM") %>
year: <% tp.date.now("YYYY") %>
---

###### [[<% tp.date.now("gggg-[W]ww", -7, tp.file.title, "gggg-[W]ww") %>|↶ PREVIOUS WEEK]] ⁝ [[<% tp.date.now("gggg-[W]ww", 7, tp.file.title, "gggg-[W]ww") %>|FOLLOWING WEEK ↷]]
# ◌ <% tp.file.title %>
```dataview
TABLE
week as "Week"
FROM "600 Periodic/610 Daily"
WHERE week = "<% tp.file.title %>"
```