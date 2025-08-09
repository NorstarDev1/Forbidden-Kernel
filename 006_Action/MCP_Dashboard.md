---
tags: dashboard
---
# MCP Dashboard

## MCP Tools Overview
```dataview
TABLE status, owner, type, last-updated
FROM #mcp/tool
SORT file.name ASC
```

## MCP Projects Overview
```dataview
TABLE status, owner, start-date, end-date
FROM #mcp/project
SORT file.name ASC
```

## Upcoming MCP Tasks
```dataview
TASK
FROM #mcp
WHERE !completed
SORT due ASC
```

## Recently Modified MCP Notes
```dataview
TABLE file.mtime as "Last Modified"
FROM #mcp
SORT file.mtime DESC
LIMIT 10
```
