---
tags:
  - plateforme/htb
  - status/in-progress
difficulty: 
ip: 
url: 
os: 
creation_date: <% tp.date.now("YYYY-MM-DD") %>
completion_date: 
---
# [[<% tp.file.title %>]]

## 📝 Informations Générales

**OS :** 
**Difficulté :** 
**Points :** 
**Release Date :** 

---

## 🕵️‍♂️ Phase 1 : Reconnaissance & Énumération

### 🗺️ Nmap - Scan Initial
```bash
nmap -sC -sV -oN nmap_initial.txt <IP>
```

**Ports ouverts :**
| Port | Service | Version |
|------|---------|---------|
|      |         |         |

### 🌐 Énumération Web (si applicable)

**Technologies détectées :**
- 

**Directories/Files découverts :**
```bash
gobuster dir -u http://<IP> -w /usr/share/wordlists/dirb/common.txt
```

---

## 🚪 Phase 2 : Foothold (Accès Initial)

### 🔍 Vulnérabilité Identifiée
**CVE/Nom :** [[]]
**Description :** 

### 💥 Exploitation
```bash

```

**Résultat :** 
- [ ] User flag obtenu : `<flag>`

---

## 🚀 Phase 3 : Privilege Escalation

### 🔎 Énumération Post-Exploitation
```bash
# LinPEAS / WinPEAS
# sudo -l
# find / -perm -4000 2>/dev/null
```

**Vecteur identifié :**

### ⚡ Exploitation
```bash

```

**Résultat :**
- [ ] Root flag obtenu : `<flag>`

---

## 💡 Résumé & Leçons Apprises

### Points Clés
1. 
2. 
3. 

### Techniques Utilisées
- 
- 

### Nouvelles Connaissances
- 

---

## 🔗 Références

- Writeup officiel : 
- Outils utilisés : [[]], [[]]
- CVE/Vulnérabilités : [[]]
