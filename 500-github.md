---
layout: page
title: Git
permalink: /git/
---

Explication concernant le système de versionnement Git.

**Git** est un logiciel de *gestion de versions* décentralisé, créé en 2005 par Linus Torvalds (le créateur de Linux). C'est un logiciel libre, sous licence GPL. Le site officiel de documentation est [git-scm.com](https://git-scm.com).

**GitHub** est un service web offrant l'hébergement de projets utilisant Git, lancé en 2008 (cf. [cet article](http://tom.preston-werner.com/2011/03/29/ten-lessons-from-githubs-first-year.html) sur les débuts de cette startup californienne). Devenu extrêmement populaire, GitHub offre de nombreuses fonctionnalités facilitant la communication et la collaboration. 



Quelques services d'hébergement Git: 

* [GitHub](https://github.com/), le plus utilisé avec plus de 14 millions d'utilisateurs (état 2016). 
* [BitBucket](https://bitbucket.org), un service freemium, acquis par la société australienne Atlassian en 2010.
* [GitLab](https://about.gitlab.com/gitlab-com/), à la fois un service en ligne comparable à GitHub, et un outil serveur open-source.
* [Framagit](https://framagit.org), un service reposant sur Gitlab, maintenu par l'association Framasoft.

![publication marketing de GitHub](/cours-divers/img/github-activity-book.jpg)

Terminologie Git
==

Voici quelques-unes des actions fondamentales de Git:

**Commit** (commettre) : Valider vos modifications (a snapshot of your repo)

**Push** (pousser) : send commits to a remote

**Pull** (tirer) : get commits from a remote

**Checkout** : time travel to a specific commit

**Stash** (ranger) : save modified and staged changes (en français: remise)

**Merge** (fusionner) : combining two branches

**Rebase** (rembobiner) : apply any commits of current branch ahead of specified one

**Branch** (branche) : create a new branch at the current commit (a movable label that points to a commit)

**index** : aussi "stage", "staging area": Il s’agit de la zone de validation désignant les travaux que vous souhaitez voir apparaître dans votre prochain commit.

**HEAD** : HEAD est un pointeur, une référence sur notre position actuelle dans notre répertoire de travail Git. "The current HEAD is local to each repository, and is therefore individual for each developer."

![](/cours-divers/img/Strip-Bon-daccord-650-final.jpg)

Guide d'utilisation GitHub:
==

(Documentation à compléter)

- Créer un compte sur [Github.com](https://github.com/).
- Télécharger l'application [Github Desktop](https://desktop.github.com/).
- Créer un repository.
- Synchroniser ses modifications
- Faire un correctif sur un projet existant.


Ecriture de messages de Commit
===

"En règle générale, les messages doivent débuter par une ligne unique d’au plus 50 caractères décrivant concisément la modification, suivie d’une ligne vide, suivie d’une explication plus détaillée. Le projet Git exige que l’explication détaillée inclue la motivation de la modification en contrastant le nouveau comportement par rapport à l’ancien — c’est une bonne règle de rédaction."

Source: [The Git Book](https://git-scm.com/book/fr/v2/Git-distribu%C3%A9-Contribution-%C3%A0-un-projet)

![Messages de Commit](/cours-divers/img/git-commit-messages.png)

Source: *[Git for Humans](https://speakerdeck.com/alicebartlett/git-for-humans)*, présentation par Alice Bartlett, développeuse au Financial Times

Les branches
===

Le système des **branches** est une fonctionalité puissante, qui permet de sortir d'un processus d'avancement linéaire, et de créer au sein d'un projet des "bifurcations".

Cela permet par exemple de créer une version alternative et expérimentale, pour tester de nouvelles fonctionalités.

Ces ajouts, qui peuvent introduire des dysfonctionnements, ne vont pas perturber la version de base (généralement la branche "master"), qui reste ainsi stable.

Une fois qu'un développement expérimental arrive à maturité, on peut l'intégrer dans la version de base. On fera cela en fusionnant la branche expérimentale avec la branche "master", en faisant appel à la fonction "merge".

Un explicatif des branches dans l'interface SourceTree: [Use SourceTree branches to merge an update](https://confluence.atlassian.com/bitbucket/use-sourcetree-branches-to-merge-an-update-732268925.html)

