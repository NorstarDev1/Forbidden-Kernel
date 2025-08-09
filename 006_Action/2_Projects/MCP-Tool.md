---
tags:
  - template
  - siverse
  - mcp/tool
template_type: "tool"
template_description: "A template for documenting Master Control Program (MCP) tools."
related_project: ""
created_by: ""
created_date: {{date:YYYY-MM-DD}}
last_updated: {{date:YYYY-MM-DD}}
status: "Planning"
owner: "[[Aura]]"
type: "[[Tool Type/CLI]]"
dependencies: ""
---
# MCP Tool: <% tp.file.title %>

## Description

## Capabilities

## Usage

## Active Tasks
```dataview
TASK
FROM #mcp/tool/<% tp.file.title %>
WHERE !completed
```

## Related Projects
```dataview
TABLE WITHOUT ID file.link as Project, status, owner
FROM #mcp/project
WHERE contains(linked-tools, [[<% tp.file.title %>]])
```

## Troubleshooting/Notes
