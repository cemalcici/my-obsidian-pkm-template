---
aliases: 
Title: <% tp.file.title %>
tags:
  - "#topic"
Areas: 
Created: <% tp.file.creation_date() %>
---
## Kısa Açıklama


## İlgili Konular
```dataview
LIST
FROM "Vault/02-Areas"
WHERE Areas = [[<% tp.file.title %>]]
SORT file.mtime desc
LIMIT 10
```

## Projeler
```dataview
LIST
FROM #Project 
WHERE Areas = [[<% tp.file.title %>]]
SORT file.mtime desc
LIMIT 10
```

## Notlar
```dataview
LIST
FROM #note 
WHERE Areas = [[<% tp.file.title %>]]
SORT file.mtime desc
LIMIT 10
```
