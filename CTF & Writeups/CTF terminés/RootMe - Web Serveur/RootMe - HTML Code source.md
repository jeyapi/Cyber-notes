---
tags:
  - plateforme/rootme
  - categorie/web-serveur
  - status/completed
difficulty: Très facile
points: 5
url: https://www.root-me.org/fr/Challenges/Web-Serveur/HTML-code-source
creation_date: 2025-10-27
completion_date: 2025-10-27
---
# RootMe - HTML - Code source

## 📝 Informations du Challenge

**Catégorie :** [X] Web [ ] Réseau [ ] App-Script [ ] Cryptanalyse [ ] Steganographie [ ] Forensic [ ] Cracking [ ] Réaliste [ ] Programmation
**Difficulté :** Très facile
**Points :** 5
**URL :** https://www.root-me.org/fr/Challenges/Web-Serveur/HTML-code-source
**Validations :** 50000+

---

## 🎯 Objectif

> Trouver le mot de passe caché dans le code source HTML de la page

---

## 🔍 Phase 1 : Analyse & Reconnaissance

### Informations Initiales
- Challenge de catégorie "Web - Serveur"
- Niveau très facile (introduction)
- Le titre suggère que la solution est dans le code source HTML

### Premier Examen
Accès à la page web du challenge

**Observations :**
- Page simple avec un message
- Formulaire de validation du password
- Suggestion d'examiner le code source

---

## 💡 Phase 2 : Recherche de la Vulnérabilité

### Hypothèses
1. Le mot de passe est visible directement dans le code HTML
2. Le mot de passe est dans un commentaire HTML
3. Le mot de passe est dans un attribut caché

### Tests Effectués
```bash
# Afficher le code source de la page
Ctrl+U (Firefox/Chrome)
# ou
Clic droit → Afficher le code source de la page
```

**Découverte :**
- Commentaire HTML contenant le mot de passe
- Format : `<!-- password: XXXXXXX -->`

---

## 💥 Phase 3 : Exploitation

### Méthode Utilisée
**Vulnérabilité exploitée :** [[Information Disclosure - HTML Comments]]

### Exploitation Détaillée
```html
<!-- Extrait du code source -->
<!-- password: nZ^&@q5&sjJHev0 -->
```

**Étapes :**
1. Ouvrir le code source de la page (Ctrl+U)
2. Chercher les commentaires HTML (<!-- -->)
3. Trouver le password dans un commentaire
4. Copier le password

---

## 🏁 Phase 4 : Validation

### Flag Obtenu
```
nZ^&@q5&sjJHev0
```

### Preuve
- Challenge validé
- Points obtenus : 5

---

## 💡 Résumé & Leçons Apprises

### Concepts Clés
1. **Information Disclosure** - Ne jamais laisser d'informations sensibles dans le code source
2. **Commentaires HTML** - Visibles par tous les utilisateurs
3. **Reconnaissance basique** - Toujours commencer par examiner le code source

### Techniques Appliquées
- Inspection du code source HTML
- Recherche de commentaires
- Analyse statique de page web

### Nouvelles Connaissances
- Les commentaires HTML (`<!-- -->`) sont envoyés au navigateur
- Le code source client-side est toujours accessible
- Raccourcis navigateur : Ctrl+U, F12, Clic droit → Inspecter

### Ressources Utiles
- MDN Web Docs : Commentaires HTML
- OWASP : Information Disclosure

---

## 🔗 Liens

**Outils utilisés :** Navigateur web uniquement
**Vulnérabilités :** [[Information Disclosure - HTML Comments]]
**Concepts liés :** [[Reconnaissance Web]], [[Client-Side Security]]
