#  Guide de Démarrage

---

##  Setup (5 min)

### Plugins Requis
1. **Templater** (OBLIGATOIRE)
   - Settings  Community Plugins  "Templater"
   - Template folder  `_TEMPLATES`
   -  Activer "Trigger on new file"

2. **Dataview** (pour Dashboard)
   - Community Plugins  "Dataview"
   -  Enable JavaScript Queries

---

##  Créer un Writeup

**Méthode rapide :**
1. Clic droit sur dossier  "New note from template"
2. Choisir template (RootMe, THM, CTF)
3. Documenter en temps réel
4. Marquer `completed` quand fini

---

##  Tags Essentiels

```yaml
tags:
  - plateforme/rootme    # ou thm, ctftime
  - status/in-progress   # ou completed
  - categorie/web-serveur # pour RootMe
```

**Pourquoi ?** Le Dashboard utilise les tags pour les stats.

---

##  Dashboard

Ouvrir `Dashboard.md`  Stats auto :
- CTF complétés
- Points RootMe
- Progression

---

##  Liens entre Notes

```markdown
J'ai utilisé [[Nmap]] pour scanner
Vulnérabilité [[SQLi]] trouvée
```

Les backlinks se créent automatiquement.

---

##  Cheatsheet Outil

1. Créer note dans `Ressources/Outils/`
2. Template "Outil & Commande"
3. Remplir commandes + exemples

---

##  Tips

**Raccourcis :**
- `Ctrl+P` : Commande palette
- `Ctrl+O` : Chercher note
- `Ctrl+K` : Insérer lien

**Backup :**
- Installer plugin "Git"
- Auto-commit toutes les heures

---

*C'est tout ! Commence à documenter tes CTF. *
