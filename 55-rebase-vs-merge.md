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

La solution : le *Rebase* au lieu du *Merge*. Au lieu de fusionner les deux historiques, le **rebase** replace les commits de l'élève après ceux déjà sur "main" — comme s'il avait travaillé après les autres. L'historique reste propre et linéaire.

### Comment appliquer pull.rebase ?

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

## Comment vérifier si le réglage a été appliqué ?

Il faut vérifier le contenu du dossier caché `.git/config`, en faisant cette commande de terminale:

```
cat .git/config
```

## Avantages et désavantages

Certains utilisateurs de Git sont réticents à activer le mode `pull.rebase true` : 

> Le *rebase* automatique m'effraie un peu, et je me demande si je ne suis pas simplement paranoïaque. Le fait de définir le comportement de *pull* sur *rebase* par défaut comporte-t-il des risques ?

Les utilisateurs expérimentés indiquent : 

> Utiliser *rebase* comme stratégie de *pull* par défaut est une excellente idée si vous comprenez ce qu'est *rebase*. Le *merge* est une bonne stratégie pour les débutants, au détriment d'un graphique de commit plus complexe. ([source](https://www.reddit.com/r/git/comments/1p9zdul/does_rebase_as_the_default_pull_behavior_have_any/
))

> La plupart des développeurs s'en tiennent aux workflows de *merge* traditionnels simplement parce qu'ils ne savent pas qu'il existe une meilleure solution. GitHub vous fournit les outils nécessaires pour garder votre historique propre, alors pourquoi ne pas les utiliser ? ([source](https://medium.com/@akhilvp/why-you-should-enable-rebase-as-true-in-github-e82620ff8866
))
