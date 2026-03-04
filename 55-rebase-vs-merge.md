---
layout: page
title: Rebase vs. Merge
permalink: rebase-vs-merge.html
---

## Rebase ou Merge

Quand on travaille à plusieurs sur un même Repository, dans une même branche, on peut se trouver avec un grand nombre de commits "Merge".

Voici le scénario typique :

1. Élève A et Élève B partent du même point
2. Élève A pousse en premier.
3. Élève B essaie de pousser, mais GitHub lui dit "attends, il y a du nouveau"
4. GitHub Desktop fait un pull automatique + crée un commit de merge pour réconcilier

Résultat : un commit inutile «Merge branch 'main'»

La solution : le Rebase au lieu du Merge. Au lieu de fusionner les deux historiques, le **rebase** replace les commits de l'élève après ceux déjà sur "main" — comme s'il avait travaillé après les autres. L'historique reste propre et linéaire.

Il faut faire ce réglage, dans le terminal: 

```
git config pull.rebase true
```

Cela écrit la config dans le fichier `.git/config` du projet, plutôt que dans le fichier global `~/.gitconfig` de l'utilisateur.

ou globalement sur la machine:

```
git config --global pull.rebase true
```

Avec ce réglage, quand un élève fait Fetch + Pull, Git rebase automatiquement au lieu de créer un commit de merge.

Cela est équivalent à faire la commande suivante: 

```
git pull --rebase origin main
```