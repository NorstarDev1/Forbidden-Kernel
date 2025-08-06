---
tags:
  - template
  - siverse
  - travel-journal/travel
template_type: "travel-journal-travel"
template_description: "A template for a travel entry in the travel journal."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "Draft"
from: {{VDATE: From, YYYY-MM-DD}}
to: {{VDATE: To, YYYY-MM-DD}}
place: {{VALUE: Place}}
why: {{VALUE: Why}}
---
# <%tp.file.title%>
---

```dataviewjs  

const startDate = new Date("{{VDATE: From, YYYY-MM-DD}}")
const endDate = new Date("{{VDATE: To, YYYY-MM-DD}}")

const dvData = dv.pages('"600 Periodic/610 Daily"').filter(row => row.file.path != "600 Periodic/610 Daily/610 Daily.md")

const notes = dvData.filter(value => startDate <= value['full-date'] && value['full-date'] <= endDate)

const headers = ['Notes', 'Notable']
const data = notes.map(note => ["[["+note.file.name+"]]", note.notable])
dv.table(headers, data)
```