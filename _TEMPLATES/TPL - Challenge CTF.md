---

---
---
tags:
  - platform/<% tp.prompt("Platform (thm/rootme/other)","thm") %>
  - os/<% tp.prompt("OS (linux/windows/other)","linux") %>
  - status/in-progress
platform: <% tp.prompt("Platform (TryHackMe/RootMe/Autre)","TryHackMe") %>
type: challenge
difficulty: <% tp.prompt("Difficulté (easy/medium/hard/expert)","easy") %>
ip: <% tp.prompt("IP (si applicable)","") %>
url: <% tp.prompt("URL (si applicable)","") %>
creation_date: <% tp.date.now("YYYY-MM-DD") %>
completion_date:
time_spent:
points:
author: <% tp.user %>
--- 
# [[<% tp.file.title %>]]

> **Résumé (1 phrase)** : <% tp.prompt("Résumé rapide (1 phrase)","") %>

---

## 🎯 Objectifs & Contexte
- Objectif principal :
- Contexte / scoring / remarques :

---

## 🕵️‍♂️ Phase 1 — Reconnaissance & Énumération

### 🗺️ Nmap — Scan initial
```bash
nmap -sC -sV -oN nmap_initial.txt <% tp.frontmatter.ip %>
# ou : nmap -p- -T4 <IP>

