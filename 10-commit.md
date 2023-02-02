---
layout: page
title: Commit
permalink: commit.html
---

> **Commit** : C’est la commande qui donne à Git toute sa puissance. Quand vous « committez », vous prenez un « instantané », une « photo » de votre dépôt à ce stade, vous donnant un point de contrôle que vous pouvez ensuite réévaluer ou restaurer votre projet à un état précédent. – Christophe Ducamp, *[Github pour les nuls](https://www.christopheducamp.com/2013/12/15/github-pour-nuls-partie-1/)*

![Ce designer vient de commiter un changement de couleur](img/abstract/commit-changes.jpg)

### Ecriture de messages de Commit

"En règle générale, les messages doivent débuter par une ligne unique d’au plus 50 caractères décrivant concisément la modification, suivie d’une ligne vide, suivie d’une explication plus détaillée. Le projet Git exige que l’explication détaillée inclue la motivation de la modification en contrastant le nouveau comportement par rapport à l’ancien — c’est une bonne règle de rédaction."

Source: [The Git Book](https://git-scm.com/book/fr/v2/Git-distribu%C3%A9-Contribution-%C3%A0-un-projet)

![Messages de Commit](img/git-commit-messages.png)

Source: *[Git for Humans](https://speakerdeck.com/alicebartlett/git-for-humans)*, conférence par Alice Bartlett, développeuse au *Financial Times* - aussi disponible [en vidéo](https://www.youtube.com/watch?v=eWxxfttcMts).

"Un message de commit bien conçu doit clarifier la raison d'une modification. Git permet de voir facilement *ce qui* a changé, mais seul un bon message de commit peut expliquer *pourquoi*."


### Conventions d'écriture

Il existe des "conventions d'écriture" qui visent à harmoniser les manières d'écrire les messages.

L'une de ces conventions se nomme, de manière très originale, "Commits Conventionnels": [https://www.conventionalcommits.org/fr/v1.0.0/](https://www.conventionalcommits.org/fr/v1.0.0/)

Voici le modèle proposé: 

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

### Autres bonnes pratiques

L'écriture de messages de commit est l'une des méthodes permettant d'avoir un historique lisible et structuré. Ces bonnes pratiques, qui tout d'abord apparaissent comme une perte de temps, deviendront une habitude, et augmenteront la productivité de toutes les parties prenantes.

### Les règles du bon commit

En 2014, Chris Beams définit quelques règles pour l'écriture d'un bon commit, dans son article "*[How to Write a Git Commit Message](https://cbea.ms/git-commit/)*":

- Le sujet doit être limité à 50 caractères.
- La première lettre prend une majuscule.
- Ne pas terminer le sujet par un point.
- Utiliser une même forme verbale pour tous les commits.
- Le message doit expliquer le *pourquoi*.

Quelle forme verbale utiliser? En anglais, le message du commit devrait compléter la phrase *"If applied, this commit will..."*.

- If applied, this commit will... *Update getting started documentation*
- If applied, this commit will... *Remove deprecated methods*

En français, le message doit compléter la phrase *"Ce commit..."*. Exemples:

- Ce commit... *Complète la documentation*
- Ce commit... *Simplifie la structure du CSS*
- Ce commit... *Supprime des images non-utilisées*

### Ce qu'il ne faut pas faire

Cette bande-dessinée de xkcd montre un exemple de commentaires Git mal utilisés: ils expriment l'état d'esprit de l'auteur, mais n'indiquent pas *le sens des modifications*, et n'ont donc aucune utilité.

![Plus le projet avance, moins les messages de commit sont informatifs...](img/git-folklore/xkcd_git_commits.png)

Source: [https://xkcd.com/1296/](https://xkcd.com/1296/)
