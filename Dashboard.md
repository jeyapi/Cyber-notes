# 🎯 Dashboard - Vue d'ensemble

> **Dernière mise à jour :** `= date(today)`

---

## 📊 Statistiques Globales

```dataview
TABLE WITHOUT ID
  length(rows) as "Total"
FROM ""
WHERE file.folder != "_TEMPLATES"
GROUP BY true
```

### Par Plateforme
```dataview
TABLE WITHOUT ID
  plateforme as "Plateforme",
  length(rows) as "Nombre"
FROM ""
WHERE contains(tags, "plateforme/")
GROUP BY tags[0] as plateforme
```

### Par Statut
```dataview
TABLE WITHOUT ID
  status as "Statut",
  length(rows) as "Nombre"
FROM ""
WHERE contains(tags, "status/")
GROUP BY tags[1] as status
```

---

## 🚀 CTF en Cours

```dataview
TABLE 
  difficulty as "Difficulté",
  ip as "IP",
  creation_date as "Commencé le"
FROM "CTF & Writeups/CTF en cours"
WHERE contains(tags, "status/in-progress")
SORT creation_date DESC
```

---

## ✅ CTF Récemment Terminés

```dataview
TABLE 
  difficulty as "Difficulté",
  completion_date as "Terminé le"
FROM "CTF & Writeups/CTF terminés"
WHERE contains(tags, "status/completed")
SORT completion_date DESC
LIMIT 10
```

---

## 📚 Apprentissages Récents

```dataview
TABLE 
  creation_date as "Date"
FROM "Apprentissage & Concepts"
SORT creation_date DESC
LIMIT 5
```

---

## 🛠️ Outils Documentés

```dataview
TABLE WITHOUT ID
  file.link as "Outil",
  creation_date as "Ajouté le"
FROM "Ressources/Outils"
SORT creation_date DESC
```

---

## 🎓 Progression par Difficulté

### Easy
```dataview
LIST
FROM ""
WHERE difficulty = "easy" AND contains(tags, "status/completed")
```

### Medium
```dataview
LIST
FROM ""
WHERE difficulty = "medium" AND contains(tags, "status/completed")
```

### Hard
```dataview
LIST
FROM ""
WHERE difficulty = "hard" AND contains(tags, "status/completed")
```

---

## 📌 À Réviser

```dataview
TASK
FROM ""
WHERE !completed
LIMIT 10
```
