# 📖 Guide d'utilisation

## 📝 Prendre des notes sur un challenge

### Nouveau challenge RootMe

1. **Créer la note**
   - `Ctrl + N` (nouvelle note)
   - Choisir template **Challenge**
   - Nommer : `RootMe - Nom du challenge`

2. **Placer dans le bon dossier**
   - Déplacer dans `CTF/En cours/RootMe/`

3. **Remplir pendant que tu résous**
   - Section **Challenge** : Infos du challenge
   - Section **Ce que j'ai trouvé** : Tes découvertes
   - Section **La solution** : Comment tu as réussi
   - Section **Flag** : Le flag obtenu
   - Section **Notes rapides** : Takeaways

4. **Marquer comme terminé**
   - Déplacer le fichier dans `CTF/Terminés/RootMe/`
   - Changer tag : `status/in-progress` → `status/completed`
   - Ajouter `completion_date: 2025-10-27`
   - **Ajouter liens** vers outils/concepts utilisés (voir `TAGS_ET_LIENS.md`)

### Nouveau challenge THM/HTB/autre

Même process, mais utiliser `CTF/En cours/Autres/` et `CTF/Terminés/Autres/`

---

## 📚 Prendre une note de concept

1. **Créer la note**
   - `Ctrl + N`
   - Template **Concept**
   - Nommer : `Buffer Overflow`, `SQL Injection`, etc.

2. **Placer dans**
   - `Notes/Concepts/`

3. **Remplir**
   - **C'est quoi ?** → Définition simple
   - **Comment ça marche ?** → Explication technique
   - **Exemple pratique** → Commandes/code
   - **À retenir** → Points clés

---

## 🛠️ Documenter un outil

1. **Créer la note**
   - `Ctrl + N`
   - Template **Outil**
   - Nommer : `Nmap`, `Burp Suite`, etc.

2. **Placer dans**
   - `Ressources/Outils/`

3. **Remplir**
   - **Installation** → Comment installer
   - **Commandes essentielles** → Les commandes de base
   - **Exemples** → Cas d'usage concrets
   - **Notes** → Astuces perso

---

## 📊 Utiliser le Dashboard

### Voir ta progression

Ouvre `Dashboard.md` pour voir :
- 🔥 **EN COURS** → Tes challenges actifs
- ✅ **MES DERNIERS WINS** → Tes 10 derniers challenges terminés
- 📊 **MA PROGRESSION** → Points RootMe + Rooms TryHackMe
- 🎯 **OBJECTIFS** → Check-list du mois

### Mettre à jour les stats

Les stats se mettent à jour **automatiquement** quand tu :
- Ajoutes un fichier dans `CTF/Terminés/`
- Tags avec `status/completed`
- Ajoutes `points: X` dans le frontmatter (pour RootMe)

---

## ⚡ Raccourcis utiles

| Raccourci | Action |
|-----------|--------|
| `Ctrl + N` | Nouvelle note |
| `Ctrl + O` | Recherche rapide |
| `Ctrl + E` | Mode édition/lecture |
| `Ctrl + P` | Palette de commandes |
| `[[` | Créer un lien |

---

## 💡 Bonnes pratiques

### Pendant un challenge
✅ **Note en direct** → Écris pendant que tu cherches, pas après  
✅ **Screenshots** → Mets-les dans `_MEDIA/`  
✅ **Liens** → Utilise `[[Nom outil]]` pour lier vers tes docs d'outils

### Organisation
✅ **Nommage clair** → `RootMe - Nom`, `THM - Nom`  
✅ **Tags cohérents** → `plateforme/rootme`, `plateforme/thm`, `status/completed`  
✅ **Déplacer quand terminé** → De `En cours/` vers `Terminés/`

### Productivité
✅ **Dashboard tous les jours** → Pour voir où tu en es  
✅ **Objectifs du mois** → Coche-les dans le Dashboard  
✅ **Concepts après CTF** → Note ce que tu as appris  
✅ **Crée des liens** → `[[Nom]]` pour connecter tes notes (vue graphique)  
✅ **Tags complets** → Utilise tous les tags (voir `TAGS_ET_LIENS.md`)

---

## 🎯 Workflow complet (exemple)

1. **Lundi matin** → Ouvre Dashboard, regarde tes objectifs
2. **Nouveau challenge RootMe** → `Ctrl+N` → Template → `CTF/En cours/RootMe/`
3. **Pendant le challenge** → Note commandes, découvertes, flag
4. **Challenge terminé** → Déplace dans `CTF/Terminés/RootMe/` + tag completed
5. **Concept appris** → Crée note dans `Notes/Concepts/`
6. **Fin de journée** → Dashboard pour voir progression
7. **Fin de mois** → Vérifie objectifs atteints

---

