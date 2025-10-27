# 🔐 Cyber Notes - Portfolio Cybersécurité

> **Vault Obsidian professionnel** pour documenter mes apprentissages en cybersécurité, writeups CTF et techniques de pentesting.

[![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat&logo=obsidian&logoColor=white)](https://obsidian.md/)
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-red?style=flat&logo=tryhackme)](https://tryhackme.com/)
[![HackTheBox](https://img.shields.io/badge/HackTheBox-Profile-9FEF00?style=flat&logo=hackthebox&logoColor=white)](https://hackthebox.com/)

> 🎯 **Recruteurs ?** Consultez [[POUR_RECRUTEURS.md]] | **Débutant ?** Voir [[GUIDE_DEMARRAGE.md]]

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
│   ├── TPL - Machine HTB.md        # Template HackTheBox
│   ├── TPL - Room THM-HTB.md       # Template TryHackMe
│   ├── TPL - Outil & Commande.md   # Template outils
│   ├── TPL - Vulnérabilité.md      # Template CVE/vulns
│   └── TPL - Concept.md            # Template apprentissage
└── 🖼️ _MEDIA/                    # Captures, schémas, preuves
```

---

## 🎯 Méthodologie & Templates

### 🏆 Template CTF Challenge
Documentation complète d'un CTF avec méthodologie professionnelle :
- Reconnaissance & Énumération (Nmap, Gobuster)
- Exploitation & Foothold
- Privilege Escalation
- Lessons learned & Takeaways

### 🖥️ Template Machine HTB
Spécifique aux machines HackTheBox avec :
- Informations machine (OS, difficulté, points)
- Flags user & root
- Writeup structuré

### 📖 Template Room THM
Pour les rooms TryHackMe guidées

### 🔧 Template Outil & Commande
Cheatsheets personnalisées avec :
- Installation & Configuration
- Commandes essentielles
- Exemples pratiques issus de CTF

### 🐛 Template Vulnérabilité
Documentation de CVE et exploits :
- CVSS score & impact
- PoC et exploitation
- Mitigation

### 📚 Template Concept
Pour la théorie et les fondamentaux

---

## 🏷️ Système de Tags (Dataview-Ready)

### Plateformes
- `plateforme/thm` - TryHackMe
- `plateforme/htb` - HackTheBox
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

## 📊 Dashboard & Dataview

Le fichier `Dashboard.md` offre :
- ✅ Statistiques globales (nombre de CTF, réussite par difficulté)
- 🎯 CTF en cours avec progression
- 🏆 Derniers CTF terminés
- 📈 Graphiques de progression
- 🛠️ Outils documentés

**Nécessite le plugin Dataview** pour fonctionner.

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

## 🎓 Workflow Recommandé

### 1. Démarrer un nouveau CTF
- Utiliser le template approprié (CTF, HTB, THM)
- Remplir les métadonnées (IP, difficulté, tags)
- Documenter en temps réel

### 2. Pendant le CTF
- Noter chaque commande utilisée
- Capturer les flags et preuves dans `_MEDIA/`
- Lier les outils et vulnérabilités

### 3. Après résolution
- Compléter les "Lessons Learned"
- Mettre à jour le statut → `completed`
- Ajouter la completion_date
- Créer des notes d'outils si nouveaux outils utilisés

### 4. Apprentissage continu
- Créer des notes de concepts pour approfondir
- Documenter les nouvelles vulnérabilités rencontrées
- Maintenir les cheatsheets à jour

---

## 📈 Pourquoi ce vault est professionnel ?

✅ **Structure claire** - Organisation logique par type de contenu  
✅ **Méthodologie cohérente** - Templates basés sur PTES/OSSTMM  
✅ **Traçabilité complète** - Dates, tags, statuts, liens  
✅ **Automatisation** - Dataview pour statistiques automatiques  
✅ **Portfolio-ready** - Parfait pour montrer aux recruteurs  
✅ **Scalable** - Peut contenir des centaines de CTF  
✅ **Knowledge base** - Liens entre concepts, outils, vulns  

---

## 🚀 Utilisation pour Portfolio

### Pour les recruteurs
1. **Montrez le Dashboard** - Statistiques impressionnantes
2. **Sélectionnez 5-10 meilleurs writeups** - Variés en difficulté
3. **Exportez en PDF** via Obsidian ou Markdown
4. **Ajoutez sur GitHub** - Vault complet ou writeups sélectionnés

### Bonus points
- Schémas d'attaque avec Excalidraw
- Notes propres et bien formatées
- Cheatsheets d'outils personnalisés
- Documentation de CVE découvertes

---

## 📝 Maintenance

- **Hebdomadaire** : Compléter les CTF en cours
- **Mensuel** : Réviser le Dashboard et statistiques
- **Backup** : Git push régulier (penser à exclure les fichiers sensibles)

---

## 📞 Contact & Profils

- TryHackMe : [Votre profil]
- HackTheBox : [Votre profil]
- GitHub : [Votre repo]
- LinkedIn : [Votre profil]

---

*Dernière mise à jour : 27 octobre 2025*  
*Version : 2.0 - Professional Edition*
