---
tags:
  - outil/recon
related_tools:
  - "[[Masscan]]"
  - "[[Rustscan]]"
creation_date: 2025-10-27
---
# Nmap

## 📝 Description
> **À quoi ça sert ?** Scanner de ports et détection de services/versions. L'outil de reconnaissance #1 en pentesting.
> 
> **Quand l'utiliser ?** Première étape de reconnaissance sur une cible pour identifier les ports ouverts et les services exposés.

---

## 🛠️ Installation & Configuration
```bash
# Debian/Ubuntu
sudo apt install nmap

# Mise à jour des scripts NSE
sudo nmap --script-updatedb
```

---

## ✨ Cheatsheet : Commandes Essentielles

| Commande | Description de l'action |
| -------- | ----------------------- |
| `nmap <IP>` | Scan basique des 1000 ports les plus communs |
| `nmap -p- <IP>` | Scan TOUS les ports (1-65535) |
| `nmap -sV <IP>` | Détection de version des services |
| `nmap -sC <IP>` | Lancement des scripts NSE par défaut |
| `nmap -sC -sV -oN scan.txt <IP>` | **Scan standard CTF** - Scripts + Versions + Sauvegarde |
| `nmap -p 22,80,443 <IP>` | Scan de ports spécifiques |
| `nmap -sU <IP>` | Scan UDP (lent mais important) |
| `nmap -Pn <IP>` | Désactive le ping (si le host semble down) |
| `nmap -A <IP>` | Scan agressif (OS, version, scripts, traceroute) |
| `nmap --script vuln <IP>` | Scripts de détection de vulnérabilités |

---

## 🧠 Exemples d'Utilisation Pratique

**Challenge :** [[THM - Basic Pentesting]]

**Contexte :** Première reconnaissance d'une machine Linux

**Utilisation :**
```bash
# Scan initial rapide
nmap -sV -sC -oN nmap_initial.txt 10.10.10.25

# Résultat : SSH, HTTP, SMB identifiés
# Scan complet pour ne rien manquer
nmap -p- --min-rate 5000 -oN nmap_full.txt 10.10.10.25

# Scan UDP sur les ports communs
nmap -sU -p 53,67,68,161,162 10.10.10.25
```

---

## 🎯 Scans Avancés

### Éviter la détection
```bash
# Scan furtif SYN
nmap -sS <IP>

# Fragmentation des paquets
nmap -f <IP>

# Timing lent (évite IDS)
nmap -T2 <IP>
```

### Scripts NSE utiles
```bash
# Énumération SMB
nmap --script smb-enum-shares,smb-enum-users -p 445 <IP>

# Vulns HTTP
nmap --script http-vuln* -p 80,443 <IP>

# Brute force
nmap --script ssh-brute --script-args userdb=users.txt -p 22 <IP>
```

---

## 💡 Tips & Tricks

**Optimisation vitesse :**
- `--min-rate 5000` : Force un minimum de paquets/sec
- `-T4` : Timing agressif (bon compromis)
- `--open` : Affiche uniquement les ports ouverts

**Pour CTF :**
1. **Toujours** faire `-sV -sC` pour les infos de version
2. Sauvegarder avec `-oN` ou `-oA` (tous formats)
3. Si le scan normal ne trouve rien : essayer `-Pn` et `-p-`
4. Ne pas oublier UDP si rien en TCP

**Erreurs courantes :**
- ❌ Oublier de scanner tous les ports (`-p-`)
- ❌ Ne pas sauvegarder les résultats
- ❌ Ignorer les services sur ports non-standards
