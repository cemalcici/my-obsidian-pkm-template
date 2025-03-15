
## Görevler
```tasks
```


## Gelen Kutusu
```dataview
TABLE WITHOUT ID file.link AS "Ad", file.folder AS "Nesne Türü", file.cday AS "Oluşturma Tarihi"
FROM #status/inbox 
WHERE file.folder != "Vault/_templates"
SORT file.mtime desc
LIMIT 20
```

## Aktif Olanlar
```dataview
TABLE WITHOUT ID file.link AS "Ad", file.folder AS "Nesne Türü", file.cday AS "Oluşturma Tarihi"
FROM #status/inprogress
SORT file.mtime desc
LIMIT 20
```

## Yakalananlar

```dataview
TABLE WITHOUT ID file.link AS "Günlük Not", Idea AS "Fikir"
FROM #dailynote 
WHERE nonnull(Idea)
SORT file.mtime desc
LIMIT 10
```

```dataview
TABLE WITHOUT ID file.link AS "Günlük Not", Capture AS "Yakalanan"
FROM #dailynote 
WHERE nonnull(Capture)
SORT file.mtime desc
LIMIT 10
```
