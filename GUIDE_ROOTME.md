#  Guide RootMe

---

##  Catégories RootMe

| Catégorie | Tag |
|-----------|-----|
| Web - Serveur | `categorie/web-serveur` |
| Web - Client | `categorie/web-client` |
| Cracking | `categorie/cracking` |
| Cryptanalyse | `categorie/cryptanalyse` |
| Programmation | `categorie/programmation` |
| Steganographie | `categorie/steganographie` |
| Forensic | `categorie/forensic` |
| Réseau | `categorie/reseau` |
| App - Script | `categorie/app-script` |
| Réaliste | `categorie/realiste` |

---

##  Template RootMe

```yaml
---
tags:
  - plateforme/rootme
  - categorie/web-serveur
  - status/completed
difficulty: Très facile
points: 5
url: https://www.root-me.org/...
creation_date: 2025-10-27
completion_date: 2025-10-27
---
```

---

##  Organisation

**Option 1 : Par catégorie (recommandé)**
```
CTF terminés/
 RootMe - Web Serveur/
 RootMe - Web Client/
 RootMe - Cracking/
 ...
```

**Option 2 : Tout dans un dossier**
Utiliser tags + Dataview pour filtrer

---

##  Dashboard Stats

```dataview
TABLE WITHOUT ID
  sum(rows.points) as "Points RootMe"
FROM "CTF & Writeups"
WHERE contains(tags, "plateforme/rootme")
  AND contains(tags, "status/completed")
GROUP BY true
```

---

##  Workflow

1. Créer note  Template RootMe
2. Nommer : `RootMe - [Nom du challenge]`
3. Documenter solution
4. Flag  Marquer `completed`
5. Dashboard auto-update

---

##  Tips

**Naming :**
- `RootMe - HTML - Code source`
- `RootMe - SQL injection`

**Points :**
- Notés automatiquement
- Total dans Dashboard

**Catégories :**
- Toujours ajouter tag `categorie/xxx`
- Facilite stats et recherche

---

*Profil RootMe : https://www.root-me.org/[username]*
