---
tags:
  - template
  - siverse
  - mcp/project
template_type: "project"
template_description: "A template for managing Master Control Program (MCP) projects."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "Active"
owner: "[[Norstar]]"
linked-tools: ""
start-date: <% tp.date.now("YYYY-MM-DD") %>
end-date:
---
# MCP Project: <% tp.file.title %>

## Goals

## Mission Status

## Active Tasks
```dataview
TASK
FROM #mcp/project/<% tp.file.title %>
WHERE !completed
```

## Lore Logs

## Team Members
