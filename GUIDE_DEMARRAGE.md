# 🚀 Guide de Démarrage Rapide

Bienvenue dans votre vault Cyber-notes ! Voici comment bien démarrer.

---

## ⚡ Setup Initial (5 minutes)

### 1️⃣ Installer les Plugins Essentiels

#### Templater (OBLIGATOIRE)
1. Settings → Community Plugins → Browse
2. Chercher "Templater" → Install → Enable
3. Settings → Templater → Template folder location → `_TEMPLATES`
4. ✅ Cocher "Trigger Templater on new file creation"

#### Dataview (OBLIGATOIRE pour le Dashboard)
1. Community Plugins → Browse → "Dataview"
2. Install → Enable
3. Settings → Dataview → ✅ Enable JavaScript Queries

#### Recommandés
- **Excalidraw** : Pour dessiner des schémas d'attaque
- **Calendar** : Vue calendrier des CTF
- **Advanced Tables** : Édition facile de tableaux

---

## 📝 Créer votre Premier Writeup

### Méthode 1 : Via Templater (Recommandé)
1. Clic droit sur `CTF & Writeups/CTF en cours/`
2. "New note from template"
3. Choisir le template approprié :
   - `TPL - Challenge CTF` pour CTF générique
   - `TPL - Machine HTB` pour HackTheBox
   - `TPL - Room THM-HTB` pour TryHackMe

### Méthode 2 : Hotkey
1. Configurer dans Settings → Templater → Hotkeys
2. Assigner une touche à "Templater: Insert Template"
3. Créer un nouveau fichier
4. Appuyer sur le hotkey → Choisir le template

---

## 🎯 Workflow Pendant un CTF

### 📋 Checklist

**Avant de commencer :**
- [ ] Créer une note depuis le template
- [ ] Remplir IP, difficulté, URL
- [ ] Ajouter les bons tags (plateforme, OS)
- [ ] Mettre status à `in-progress`

**Pendant :**
- [ ] Copier-coller TOUTES vos commandes
- [ ] Noter les résultats importants
- [ ] Faire des captures d'écran → `_MEDIA/`
- [ ] Créer des liens vers outils/vulns : `[[Nmap]]`

**Après résolution :**
- [ ] Compléter la section "Leçons apprises"
- [ ] Changer status → `completed`
- [ ] Ajouter `completion_date`
- [ ] Déplacer vers `CTF terminés/` si souhaité

---

## 🏷️ Bien Utiliser les Tags

### Format Standard
```yaml
tags:
  - plateforme/thm    # ou htb, ctftime, vulnhub
  - os/linux          # ou windows, other
  - status/in-progress # ou completed, stuck
```

### Tags Optionnels Utiles
```yaml
tags:
  - technique/sqli
  - technique/xss
  - technique/privesc
  - web
  - pwn
  - crypto
```

**Pourquoi c'est important ?**
→ Le Dashboard utilise ces tags pour générer les statistiques !

---

## 📊 Utiliser le Dashboard

1. Ouvrir `Dashboard.md`
2. Attendre que Dataview génère les tableaux (quelques secondes)
3. Voir vos stats en temps réel :
   - Nombre total de CTF
   - CTF en cours
   - Derniers terminés
   - Progression par difficulté

**Astuce :** Épingler le Dashboard en panel latéral pour toujours le voir !

---

## 🔗 Créer des Liens entre Notes

### Liens simples
```markdown
J'ai utilisé [[Nmap]] pour scanner
La vulnérabilité [[SQLi]] était présente
```

### Liens avec alias
```markdown
Voir mon writeup de [[THM - Basic Pentesting|Basic Pentesting]]
```

### Backlinks
Obsidian crée automatiquement les backlinks.
→ Dans une note, regardez le panel "Backlinks" pour voir qui référence cette note.

**Cas d'usage :**
- Lier vos CTF aux outils utilisés
- Lier vos CTF aux vulnérabilités rencontrées
- Créer un graphe de connaissances

---

## 🛠️ Créer une Cheatsheet d'Outil

1. Créer une note dans `Ressources/Outils/`
2. Utiliser `TPL - Outil & Commande`
3. Remplir :
   - Description de l'outil
   - Commandes essentielles (tableau)
   - Exemples d'utilisation de vos CTF
4. Tagger avec `outil/recon` ou `outil/exploit` ou `outil/privesc`

**Exemple :** Voir `[[Nmap]]`

---

## 📚 Documenter une Vulnérabilité

1. Créer une note dans `Ressources/Vulnérabilités/`
2. Utiliser `TPL - Vulnérabilité`
3. Remplir :
   - CVE si applicable
   - CVSS score
   - PoC/exploitation
   - Comment l'avez-vous rencontrée
4. Lier depuis vos writeups : `[[Nom de la Vuln]]`

---

## 🎨 Ajouter des Schémas

### Avec Excalidraw
1. Créer un nouveau dessin : Commande palette → "Excalidraw: Create new drawing"
2. Dessiner l'architecture réseau, le flow d'attaque
3. Sauvegarder dans `_MEDIA/`
4. Insérer dans la note : `![[schema.excalidraw]]`

### Captures d'écran
1. Prendre la capture (Windows+Shift+S)
2. Coller directement dans Obsidian (Ctrl+V)
3. Obsidian la sauvegarde automatiquement

---

## 💡 Tips Pro

### Raccourcis Clavier Utiles
- `Ctrl+P` : Commande palette
- `Ctrl+O` : Quick switcher (chercher une note)
- `Ctrl+Click` : Ouvrir lien dans nouveau panel
- `Ctrl+K` : Insérer un lien
- `Ctrl+E` : Basculer éditeur/preview

### Templates Personnalisés
Vous pouvez modifier les templates existants ou en créer de nouveaux dans `_TEMPLATES/` !

### Backup Automatique
1. Installer le plugin "Git"
2. Configurer pour auto-commit toutes les heures
3. Push vers votre GitHub privé

### Recherche Avancée
- Chercher dans tout le vault : `Ctrl+Shift+F`
- Chercher par tag : `tag:#plateforme/thm`
- Chercher dans les propriétés : `difficulty:easy`

---

## 🎓 Ressources Supplémentaires

**Documentation Obsidian :**
- https://help.obsidian.md/

**Plugins utilisés :**
- Templater : https://github.com/SilentVoid13/Templater
- Dataview : https://blacksmithgu.github.io/obsidian-dataview/

**Inspiration pour writeups :**
- 0xdf writeups : https://0xdf.gitlab.io/
- IppSec videos : https://ippsec.rocks/

---

## ❓ Problèmes Fréquents

### Le Dashboard n'affiche rien
→ Vérifier que Dataview est installé et activé
→ Vérifier que vos notes ont bien les tags `tags:` dans le frontmatter

### Les templates ne fonctionnent pas
→ Vérifier Templater settings → Template folder = `_TEMPLATES`
→ Vérifier que le template a bien l'extension `.md`

### Les émojis ne s'affichent pas
→ Normal selon le thème Obsidian utilisé
→ Fonctionnent mieux sur mobile et avec certains thèmes

---

## 🚀 Vous êtes prêt !

Commencez dès maintenant :
1. ✅ Ouvrir le Dashboard
2. ✅ Créer votre premier writeup
3. ✅ Documenter en temps réel
4. ✅ Construire votre base de connaissances

**Bon hacking ! 🔐**
