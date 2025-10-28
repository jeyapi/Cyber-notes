# 🏷️ Guide Tags & Liens

## 📋 Système de Tags

### Tags par type de note

**Challenge CTF:**
```yaml
tags:
  - ctf                      # Type de note
  - plateforme/rootme        # Plateforme (rootme, thm, htb...)
  - categorie/web-serveur    # Catégorie du challenge
  - status/in-progress       # Statut (in-progress, completed)
```

**Note de concept:**
```yaml
tags:
  - apprentissage
  - concept
  - categorie/exploitation   # Type de concept (exploitation, enumeration, privesc...)
```

**Outil:**
```yaml
tags:
  - outil
  - ressource
  - categorie/enumeration    # Type d'outil (enumeration, exploitation, post-exploit...)
```

---

## 🏷️ Liste des tags disponibles

### Plateformes
- `plateforme/rootme`
- `plateforme/thm` (TryHackMe)
- `plateforme/htb` (HackTheBox)
- `plateforme/vulnhub`
- `plateforme/autre`

### Statuts (pour CTF)
- `status/in-progress` → Challenge en cours
- `status/completed` → Challenge terminé
- `status/stuck` → Bloqué (optionnel)

### Catégories CTF (RootMe)
- `categorie/web-serveur`
- `categorie/web-client`
- `categorie/app-script`
- `categorie/cracking`
- `categorie/cryptanalyse`
- `categorie/forensic`
- `categorie/steganographie`
- `categorie/reseau`
- `categorie/programmation`
- `categorie/realiste`

### Catégories Concepts
- `categorie/exploitation`
- `categorie/enumeration`
- `categorie/privesc`
- `categorie/web`
- `categorie/network`
- `categorie/crypto`

### Catégories Outils
- `categorie/enumeration`
- `categorie/exploitation`
- `categorie/post-exploit`
- `categorie/web`
- `categorie/network`

### Difficultés
- `difficulty/facile`
- `difficulty/moyen`
- `difficulty/difficile`

---

## 🔗 Système de Liens

### Pourquoi créer des liens ?

Les liens `[[Nom du fichier]]` permettent de :
- ✅ **Connecter tes notes** dans la vue graphique
- ✅ **Naviguer rapidement** entre concepts/outils/challenges
- ✅ **Voir les relations** entre ce que tu apprends

### Comment créer des liens

**Dans un challenge :**
```markdown
**Outils utilisés:** [[Nmap]] [[Burp Suite]]
**Concepts liés:** [[SQL Injection]] [[XSS]]
```

**Dans un concept :**
```markdown
**Outils liés:** [[sqlmap]] [[Burp Suite]]
**Challenges liés:** [[RootMe - SQL Injection]] [[THM - OWASP Top 10]]
```

**Dans un outil :**
```markdown
**Challenges utilisant cet outil:** [[RootMe - Port Scan]] [[THM - Nmap]]
**Concepts liés:** [[Enumeration]] [[Port Scanning]]
```

---

## 💡 Exemples concrets

### Exemple 1 : Challenge RootMe "SQL Injection"

```yaml
---
tags:
  - ctf
  - plateforme/rootme
  - categorie/web-serveur
  - status/completed
difficulty: Facile
points: 40
date: 2025-10-28
completion_date: 2025-10-28
---

# RootMe - SQL Injection

## 🎯 Challenge
**Catégorie:** Web - Serveur
**Points:** 40
**Difficulté:** Facile

## 🔍 Ce que j'ai trouvé
...

## 💡 La solution
**Outils utilisés:** [[sqlmap]] [[Burp Suite]]
**Concepts liés:** [[SQL Injection]] [[Union-Based SQLi]]
```

### Exemple 2 : Concept "SQL Injection"

```yaml
---
tags:
  - apprentissage
  - concept
  - categorie/web
difficulty: Moyen
date: 2025-10-28
---

# SQL Injection

## 📖 C'est quoi ?
...

## 🔗 Liens
**Outils liés:** [[sqlmap]] [[Burp Suite]]
**Challenges liés:** [[RootMe - SQL Injection]] [[THM - SQL Injection Lab]]
```

### Exemple 3 : Outil "sqlmap"

```yaml
---
tags:
  - outil
  - ressource
  - categorie/web
date: 2025-10-28
---

# sqlmap

## 📦 Installation
...

## 🔗 Liens
**Challenges utilisant cet outil:** [[RootMe - SQL Injection]] [[THM - OWASP Top 10]]
**Concepts liés:** [[SQL Injection]] [[Database Enumeration]]
```

---

## 🎯 Résultat dans la vue graphique

Avec ce système, tu auras un **graphique connecté** :

```
[RootMe - SQL Injection] ←→ [SQL Injection (concept)]
         ↓                            ↓
    [sqlmap]         ←→         [Burp Suite]
         ↓                            ↓
[THM - OWASP Top 10] ←→ [Database Enumeration]
```

---

## ✅ Checklist après chaque challenge

Après avoir terminé un challenge :

1. ✅ Tag `status/completed` + `completion_date`
2. ✅ Déplacer dans `CTF/Terminés/`
3. ✅ Ajouter liens vers **outils utilisés**
4. ✅ Ajouter liens vers **concepts appliqués**
5. ✅ Si nouveau concept appris → Créer note de concept
6. ✅ Si nouvel outil utilisé → Créer doc d'outil

