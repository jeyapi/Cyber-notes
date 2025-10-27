# 🔐 Cyber Notes

> Mes notes de cybersécurité : CTF, projets et certifications

[![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat&logo=obsidian&logoColor=white)](https://obsidian.md/)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-red?style=flat&logo=tryhackme)](https://tryhackme.com/)
[![RootMe](https://img.shields.io/badge/RootMe-Profile-FF6C37?style=flat)](https://www.root-me.org/)

**Quick Start :** [[START.md]] | **Guides :** [[GUIDE_DEMARRAGE]] [[GUIDE_ROOTME]]

---

## 📁 Structure

```
Cyber-notes/
├── 📊 Dashboard.md
├── 📚 Apprentissage & Concepts/
├── 🎯 CTF & Writeups/
├── 💻 Projets/
├── 🛠️ Ressources/
└── 📝 _TEMPLATES/
```

---

## 🎯 Templates

- **Challenge CTF** - CTF générique
- **Challenge RootMe** - RootMe (catégories, points)
- **Room THM** - TryHackMe
- **Projet** - Labs et scripts perso
- **Outil** - Cheatsheets
- **Vulnérabilité** - CVE/exploits
- **Concept** - Théorie

---

## 🏷️ Tags

```yaml
# Plateformes
plateforme/thm | rootme | ctftime

# Statut
status/in-progress | completed

# Difficulté
difficulty/easy | medium | hard

# Catégories RootMe
categorie/web-serveur | web-client | cracking | crypto | etc.
```

---

## 📊 Dashboard

Stats auto avec Dataview :
- Points RootMe
- CTF par plateforme
- Projets en cours
- Progression certifications

---

## 🎓 Workflow

1. **Nouveau challenge** → Template → Documenter en temps réel
2. **Terminer** → Marquer `completed` + date
3. **Apprendre** → Créer notes outils/concepts
4. **Dashboard** → Voir progression

---

## 🎯 Objectifs

### Court terme (1-3 mois)
- 50+ challenges RootMe
- 10+ rooms TryHackMe
- 1-2 projets perso

### Long terme (6-12 mois)
- Certification (eJPT/OSCP)
- 100+ challenges
- Portfolio GitHub

---

## 🔧 Setup

**Plugins requis :**
- Templater (obligatoire)
- Dataview (pour Dashboard)

---

## 🔗 Profils

- TryHackMe : [Mon profil]
- RootMe : [Mon profil]
- GitHub : [Mon repo]

---

*Guides détaillés : [[GUIDE_DEMARRAGE.md]] | [[GUIDE_ROOTME.md]]*

---

## 📁 Structure du Vault

```
Cyber-notes/
├── � Dashboard.md              # Vue d'ensemble et statistiques
├── �📚 Apprentissage & Concepts/
│   ├── Concepts Fondamentaux/   # Théorie et fondamentaux
│   └── TryHackMe/              # Rooms et parcours THM
├── 🎯 CTF & Writeups/
│   ├── CTF en cours/           # Challenges actifs
│   └── CTF terminés/           # Writeups complets
├── 🛠️ Ressources/
│   ├── Outils/                 # Cheatsheets d'outils
│   └── Vulnérabilités/         # Base de CVE et exploits
├── 📝 _TEMPLATES/
│   ├── TPL - Challenge CTF.md      # Template CTF générique
│   ├── TPL - Challenge RootMe.md   # Template RootMe
│   ├── TPL - Room THM.md           # Template TryHackMe
│   ├── TPL - Outil & Commande.md   # Template outils
│   ├── TPL - Vulnérabilité.md      # Template CVE/vulns
│   └── TPL - Concept.md            # Template apprentissage
└── 🖼️ _MEDIA/                    # Captures, schémas, preuves
```

---

## 🎯 Templates Disponibles

### 🏆 Template CTF Challenge
Documentation complète d'un CTF :
- Reconnaissance & Énumération
- Exploitation & Foothold
- Privilege Escalation
- Ce que j'ai appris

### 🎯 Template Challenge RootMe
Pour challenges RootMe :
- Catégorie (Web, Réseau, Crypto, etc.)
- Points et difficulté
- Solution étape par étape
- Flag et validation

### 📖 Template Room THM
Pour rooms TryHackMe guidées

### � Template Projet
Pour vos projets perso :
- Description et objectifs
- Technologies utilisées
- Étapes de réalisation
- Résultats et apprentissages

### 🔧 Template Outil & Commande
Cheatsheets perso :
- Commandes essentielles
- Exemples d'utilisation
- Tips & tricks

### 🐛 Template Vulnérabilité
Documentation de CVE/exploits

### 📚 Template Concept
Pour la théorie et fondamentaux

---

## 🏷️ Système de Tags (Dataview-Ready)

### Plateformes
- `plateforme/thm` - TryHackMe
- `plateforme/rootme` - RootMe
- `plateforme/ctftime` - CTFTime
- `plateforme/vulnhub` - VulnHub

### Statut
- `status/in-progress` - En cours
- `status/completed` - Terminé
- `status/stuck` - Bloqué (à réviser)

### Systèmes
- `os/linux` - Linux
- `os/windows` - Windows
- `os/other` - Autres

### Difficulté
- `difficulty/easy`
- `difficulty/medium`
- `difficulty/hard`
- `difficulty/insane`

### Types
- `outil/recon` - Reconnaissance
- `outil/exploit` - Exploitation
- `outil/privesc` - Privilege Escalation
- `vuln/` - Vulnérabilités
- `concept/` - Apprentissage théorique

---

## 📊 Dashboard

Le fichier `Dashboard.md` affiche :
- 📊 **Statistiques** - Nombre de CTF, points RootMe, etc.
- 🎯 **En cours** - CTF et projets actifs
- 🏆 **Terminés** - Derniers challenges complétés
- � **Apprentissage** - Progression certifications
- 🛠️ **Ressources** - Outils documentés

**Nécessite le plugin Dataview**

---

## � Configuration Obsidian

### Plugins Essentiels

| Plugin | Usage | Priorité |
|--------|-------|----------|
| **Templater** | Templates dynamiques avec dates auto | ⭐⭐⭐ Obligatoire |
| **Dataview** | Dashboard et statistiques | ⭐⭐⭐ Obligatoire |
| **Excalidraw** | Schémas d'attaque et diagrammes | ⭐⭐ Recommandé |
| **Calendar** | Vue calendrier des CTF | ⭐⭐ Recommandé |
| **Git** | Versioning et backup | ⭐⭐ Recommandé |
| **Advanced Tables** | Édition facile de tableaux | ⭐ Optionnel |

### Configuration Templater
1. Settings → Templater → Template folder location → `_TEMPLATES`
2. Activer "Trigger Templater on new file creation"

---

## 🎓 Mon Workflow

### 1️⃣ Démarrer un Challenge
- Choisir le bon template (RootMe, THM, CTF)
- Remplir les infos de base (difficulté, tags)
- Documenter en temps réel pendant la résolution

### 2️⃣ Pendant le Challenge
- Noter TOUTES les commandes testées
- Capturer les preuves (flags, screenshots)
- Lier vers mes cheatsheets d'outils

### 3️⃣ Après Validation
- Compléter "Ce que j'ai appris"
- Marquer comme `completed`
- Créer/mettre à jour les notes d'outils utilisés

### 4️⃣ Apprentissage Continu
- Documenter nouveaux concepts découverts
- Enrichir mes cheatsheets
- Faire des liens entre les challenges similaires

---

## 📈 Pourquoi ce vault est génial ?

✅ **Organisation claire** - Facile de retrouver mes notes  
✅ **Templates prêts** - Gain de temps énorme  
✅ **Tout tracé** - Dates, tags, progression visible  
✅ **Statistiques auto** - Dashboard avec Dataview  
✅ **Évolutif** - Grandit avec mon apprentissage  
✅ **Knowledge base** - Liens entre concepts, outils, CTF  
✅ **Offline** - Mes notes, sur mon PC, pour toujours  

---

## 🎯 Objectifs d'Apprentissage

### Court Terme (1-3 mois)
- [ ] 50+ challenges RootMe (toutes catégories)
- [ ] 10+ rooms TryHackMe
- [ ] Documenter 20+ outils essentiels
- [ ] 1-2 projets perso (lab, script, etc.)

### Moyen Terme (3-6 mois)
- [ ] 100+ challenges RootMe
- [ ] Path TryHackMe complété
- [ ] Préparation certification (eJPT/OSCP)
- [ ] Contribution open-source

### Long Terme (6-12 mois)
- [ ] Certification obtenue
- [ ] Portfolio solide (GitHub)
- [ ] Participation CTF en équipe
- [ ] Blog ou partage de connaissances

---

## 📝 Maintenance

- **Hebdomadaire** : Compléter les CTF en cours
- **Mensuel** : Réviser le Dashboard et statistiques
- **Backup** : Git push régulier (penser à exclure les fichiers sensibles)

---

## � Mes Profils

- 🎯 TryHackMe : [Mon profil]
- 🎯 RootMe : [Mon profil]
- 💻 GitHub : [Mon repo]

---

## 📚 Ressources & Communautés

- Discord TryHackMe
- Discord RootMe
- Reddit : r/netsec, r/homelab
- YouTube : IppSec, John Hammond, LiveOverflow

---

*Dernière mise à jour : 27 octobre 2025*  
*Version : 2.0 - Student Edition*
