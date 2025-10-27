# 🎯 Dashboard - Mon Apprentissage Cyber

> **Dernière mise à jour :** `= date(today)`

---

## 📊 Statistiques Globales

```dataview
TABLE WITHOUT ID
  length(rows) as "Total Notes"
FROM ""
WHERE file.folder != "_TEMPLATES"
GROUP BY true
```

---

## 🎯 CTF & Challenges

### 🏆 RootMe - Progression
```dataview
TABLE WITHOUT ID
  sum(rows.points) as "Points Totaux RootMe"
FROM "CTF & Writeups"
WHERE contains(tags, "plateforme/rootme") AND contains(tags, "status/completed")
GROUP BY true
```

### Par Plateforme
```dataview
TABLE WITHOUT ID
  plateforme as "Plateforme",
  length(rows) as "Complétés"
FROM "CTF & Writeups"
WHERE contains(tags, "plateforme/")
GROUP BY tags[0] as plateforme
```

### Par Statut
```dataview
TABLE WITHOUT ID
  status as "Statut",
  length(rows) as "Nombre"
FROM "CTF & Writeups"
WHERE contains(tags, "status/")
GROUP BY tags[1] as status
```

---

## 🚀 En Cours Actuellement

### CTF Actifs
```dataview
TABLE 
  difficulty as "Difficulté",
  creation_date as "Commencé"
FROM "CTF & Writeups/CTF en cours"
WHERE contains(tags, "status/in-progress")
SORT creation_date DESC
```

### Projets Actifs
```dataview
TABLE 
  technologies as "Tech",
  creation_date as "Démarré"
FROM "Projets"
WHERE contains(tags, "status/in-progress")
SORT creation_date DESC
```

---

## ✅ Récemment Terminés

### CTF
```dataview
TABLE 
  difficulty as "Difficulté",
  completion_date as "Terminé le"
FROM "CTF & Writeups"
WHERE contains(tags, "status/completed")
SORT completion_date DESC
LIMIT 10
```

### Projets
```dataview
TABLE 
  completion_date as "Terminé le"
FROM "Projets"
WHERE contains(tags, "status/completed")
SORT completion_date DESC
LIMIT 5
```

---

## 📚 Apprentissage

### Derniers Concepts Étudiés
```dataview
TABLE 
  difficulty as "Niveau",
  creation_date as "Date"
FROM "Apprentissage & Concepts"
WHERE file.name != "Suivi Certifications"
SORT creation_date DESC
LIMIT 5
```

### Certifications
- Voir [[Suivi Certifications]] pour le détail

---

## 🛠️ Ressources

### Outils Documentés
```dataview
TABLE WITHOUT ID
  file.link as "Outil",
  creation_date as "Ajouté"
FROM "Ressources/Outils"
SORT creation_date DESC
```

### Vulnérabilités Documentées
```dataview
TABLE WITHOUT ID
  file.link as "Vulnérabilité",
  cvss as "CVSS"
FROM "Ressources/Vulnérabilités"
SORT cvss DESC
```

---

## � Objectifs du Mois

- [ ] 20+ challenges RootMe
- [ ] 5+ rooms TryHackMe
- [ ] 1 projet perso
- [ ] 5 nouveaux outils documentés

---

## 📈 Progression par Difficulté

### Easy
```dataview
LIST
FROM "CTF & Writeups"
WHERE difficulty = "easy" OR difficulty = "Très facile" OR difficulty = "Facile"
AND contains(tags, "status/completed")
LIMIT 10
```

### Medium
```dataview
LIST
FROM "CTF & Writeups"
WHERE difficulty = "medium" OR difficulty = "Moyen"
AND contains(tags, "status/completed")
LIMIT 10
```

### Hard
```dataview
LIST
FROM "CTF & Writeups"
WHERE difficulty = "hard" OR difficulty = "Difficile"
AND contains(tags, "status/completed")
LIMIT 10
```
