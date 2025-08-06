```dataview
TASK
FROM #project-spec
WHERE !completed
GROUP BY file.link
```