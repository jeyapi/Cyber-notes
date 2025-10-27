# 💻 Exemple de Projet - Lab VulnHub Local

> Exemple de documentation d'un projet perso

---
tags:
  - projet/lab
  - status/completed
technologies:
  - VirtualBox
  - Kali Linux
  - Metasploitable
creation_date: 2025-10-27
completion_date: 2025-10-27
---
# Lab VulnHub - Environnement de Test Local

## 🎯 Objectifs du Projet

> Créer un environnement de test local avec plusieurs machines vulnérables pour pratiquer le pentesting sans dépendre d'Internet

**Motivation :**
- Pratiquer offline
- Tester des exploits sans limite de temps
- Comprendre la configuration réseau virtuel
- Préparer certifications (eJPT, OSCP)

**Objectifs d'apprentissage :**
1. Configuration de VMs avec VirtualBox
2. Réseau virtuel (NAT, Host-Only, Bridged)
3. Pratique exploitation sur environnement contrôlé

---

## 🛠️ Technologies & Outils

**Stack :**
- VirtualBox 7.0
- Kali Linux (machine attaquante)
- Metasploitable 2 (cible Linux)
- DVWA (Damn Vulnerable Web App)

**Environnement :**
- OS : Windows 11
- RAM : 16GB (4GB pour Kali, 2GB pour cibles)
- Storage : 50GB alloués

---

## 📋 Plan de Réalisation

### Phase 1 : Préparation
- [x] Télécharger VirtualBox
- [x] Télécharger ISO Kali Linux
- [x] Télécharger Metasploitable 2
- [x] Télécharger DVWA

### Phase 2 : Implémentation
- [x] Installer VirtualBox
- [x] Créer VM Kali Linux
- [x] Importer Metasploitable 2
- [x] Configurer réseau Host-Only

### Phase 3 : Tests & Validation
- [x] Vérifier connectivité réseau
- [x] Scanner Metasploitable depuis Kali
- [x] Tester exploitation basique

---

## 💻 Réalisation

### Configuration Réseau
```bash
# Dans VirtualBox : Fichier → Gestionnaire de réseau hôte
# Créer nouveau réseau vboxnet0
# IP : 192.168.56.1/24
# DHCP désactivé
```

**Adresses IP assignées :**
- Kali Linux : 192.168.56.10
- Metasploitable 2 : 192.168.56.20
- DVWA : 192.168.56.30

### Étape 1 : Installation Kali Linux
```bash
# Télécharger depuis kali.org
# Créer nouvelle VM :
# - Type : Linux, Debian 64-bit
# - RAM : 4096 MB
# - Disque : 40 GB dynamique

# Configuration réseau :
# Adaptateur 1 : NAT (pour Internet)
# Adaptateur 2 : Host-Only (vboxnet0)
```

**Résultat :**
- Kali installé et fonctionnel
- Accès Internet via NAT
- Accès réseau local via Host-Only

### Étape 2 : Import Metasploitable
```bash
# Télécharger depuis SourceForge
# VirtualBox → Nouvelle → Utiliser fichier existant
# Sélectionner metasploitable.vmdk

# Configuration réseau :
# Adaptateur 1 : Host-Only (vboxnet0)
```

**Résultat :**
- Metasploitable démarre correctement
- IP 192.168.56.20 configurée
- Accessible depuis Kali

### Étape 3 : Premier Scan
```bash
# Depuis Kali
nmap -sV 192.168.56.20

# Résultat : 20+ services vulnérables détectés
# FTP, SSH, HTTP, SMB, MySQL, etc.
```

---

## 🐛 Problèmes Rencontrés

### Problème 1 : VMs ne communiquent pas
**Description :** Kali et Metasploitable ne se voient pas sur le réseau

**Solution :** 
- Vérifier que les deux VMs sont sur le même réseau Host-Only
- Désactiver le pare-feu Windows temporairement pour tester
- Vérifier configuration IP avec `ip addr` (Kali) et `ifconfig` (Metasploitable)

### Problème 2 : Metasploitable boot loop
**Description :** VM reboot en boucle

**Solution :**
- Augmenter RAM allouée de 512MB à 1024MB
- Désactiver l'accélération 3D
- Vérifier intégrité du fichier téléchargé

---

## ✅ Résultats

**Ce qui fonctionne :**
- ✅ Lab 100% fonctionnel offline
- ✅ 3 VMs opérationnelles
- ✅ Réseau Host-Only stable
- ✅ Peut pratiquer tous les jours

**Ce qui reste à faire :**
- [ ] Ajouter plus de cibles (VulnHub)
- [ ] Documenter configuration Windows cible
- [ ] Créer snapshots pour reset rapide

**Captures d'écran/Preuves :**
- Voir `_MEDIA/lab-vulnhub/`
- Schéma réseau créé avec Excalidraw

---

## 💡 Ce Que J'ai Appris

### Compétences Techniques
1. **Virtualisation** - Configuration avancée VirtualBox
2. **Réseau** - Différence NAT/Bridged/Host-Only
3. **Troubleshooting** - Résolution problèmes réseau virtuel

### Concepts Clés
- Isolation réseau pour sécurité
- Snapshots pour préserver états
- Resource allocation (RAM/CPU)

### Pour Aller Plus Loin
- Essayer VMware pour comparer
- Créer mon propre lab Active Directory
- Automatiser déploiement avec Vagrant

---

## 🔗 Liens & Ressources

**Documentation :**
- VirtualBox Manual : https://www.virtualbox.org/manual/
- Metasploitable Guide : https://docs.rapid7.com/metasploit/

**Outils utilisés :** [[VirtualBox]], [[Kali Linux]], [[Nmap]]
**Concepts liés :** [[Virtualisation]], [[Réseau]]

**Code Source :**
- Pas applicable (configuration manuelle)
- Screenshots dans `_MEDIA/lab-vulnhub/`

---

## 🎯 Utilisation du Lab

**Scénarios pratiques :**
- Tester nouveaux exploits Metasploit
- Pratiquer commandes Nmap
- Apprendre web exploitation (DVWA)
- Simuler pentest complet

**Maintenance :**
- Backup snapshots hebdomadaire
- Reset Metasploitable après exploitation
- Update Kali mensuelle
