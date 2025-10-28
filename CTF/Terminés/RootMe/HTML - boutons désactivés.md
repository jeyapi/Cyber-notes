---
tags:
difficulty: Très facile
points: "5"
date: 2025-10-28
---
## Ce que j'ai trouvé

![[Pasted image 20251028094901.png]]

On observe qu'on ne peut rien écrire et ni cliquer sur le bouton "Member access". 
##  La solution

**L'idée:**
On fait une inspection des éléments.
![[Pasted image 20251028095238.png]]

On peut voir que les lignes de codes pour la zone de texte et du bouton sont les suivantes :
```
<input disabled="" type="text" name="auth-login" value=""> # il faut enlever "disabled"
<input disabled="" type="submit" value="Member access" name="authbutton"> #idem
```

On doit juste enlever les "disabled" pour pouvoir utiliser le bouton et la zone de texte.

![[Pasted image 20251028095635.png]]
---
On voit qu'on peut utiliser la zone de texte et le bouton. On essaie d'accéder avec "admin".
On obtient ceci. 
![[Pasted image 20251028095758.png]]

On a donc le flag.
##  Flag
```
HTMLCantStopYou
```

