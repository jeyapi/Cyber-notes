**Point d'entrée principal du vault**

---
##  EN COURS

```dataview
TABLE WITHOUT ID
  file.link as "Challenge",
  difficulty as "Difficulté",
  tags as "Plateforme"
FROM "CTF/En cours"
SORT file.mtime DESC
```

---
##  MES DERNIERS WINS

```dataview
TABLE WITHOUT ID
  file.link as "Challenge",
  difficulty as "Diff",
  choice(points, "+" + points + " pts", "") as "Points"
FROM "CTF/Terminés"
SORT file.mtime DESC
LIMIT 10
```

---
##  MA PROGRESSION

**RootMe**
```dataview
TABLE WITHOUT ID
  sum(rows.points) + " points" as "Total"
FROM "CTF"
WHERE contains(tags, "plateforme/rootme") AND contains(tags, "status/completed")
GROUP BY true
```

**TryHackMe**
```dataview
TABLE WITHOUT ID
  length(rows) + " rooms" as "Total"
FROM "CTF"
WHERE contains(tags, "plateforme/thm") AND contains(tags, "status/completed")
GROUP BY true
```

---
##  MES NOTES
```dataview
TABLE WITHOUT ID
  file.link as "Concept",
  difficulty as "Niveau"
FROM "Notes/Concepts"
SORT file.mtime DESC
LIMIT 10
```

---
##  MES OUTILS
```dataview
TABLE WITHOUT ID
  file.link as "Outil"
FROM "Ressources/Outils"
SORT file.name
```
