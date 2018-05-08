---
layout: page
title: Git
permalink: /git/
---

Explication concernant Git et la gestion de versions.

**Git** est un logiciel de *gestion de versions* décentralisé, créé en 2005 par Linus Torvalds (le créateur de Linux). C'est un logiciel libre, sous licence GPL. Il existe des versions pour toutes les plateformes, y compris MacOS. Le site officiel de documentation est [git-scm.com](https://git-scm.com).

Voici quelques-uns des avantages que Git apporte: 

- Permet à un grand nombre de collaborateurs de travailler sur un même projet, en offrant une bonne gestion des modifications.
- Permet de synchroniser un projet entre plusieurs collaborateurs, en ayant l'assurance que tous les fichiers soient à jour.
- Permet d'avoir un historique précis de tous les changements et modifications d'un projet. Cela permet de clarifier les questions récurrentes: "Où est la dernière version du fichier X?" et "Qu'est-ce qui a été changé entre les révisions 41 et 42"?.

Git est à la base un outil "en ligne de commande". Afin d'avoir un meilleurs confort d'utilisation, il existe divers logiciels offrant une interface graphique. Il existe également des services en ligne permettant d'héberger des projets Git, afin de faciliter la collaboration et d'avoir une sauvegarde en ligne.

**[GitHub](https://github.com/)** est un service web offrant l'hébergement de projets utilisant Git, lancé en 2008 (cf. [cet article](http://tom.preston-werner.com/2011/03/29/ten-lessons-from-githubs-first-year.html) sur les débuts de cette startup californienne). Devenu extrêmement populaire (plus de 14 millions d'utilisateurs en 2016), GitHub offre de nombreuses fonctionnalités facilitant la communication et la collaboration. 

![Une publication marketing de GitHub](/cours-divers/img/github-activity-book.jpg)

Il existe cependant d'autres services d'hébergement Git: 

* [BitBucket](https://bitbucket.org), un service freemium, acquis par la société australienne Atlassian en 2010. Contrairement à Github, il permet d'avoir des projets privés même dans la version gratuite. Le service devient payant à partir de 5 personnes dans une équipe.
* [GitLab](https://about.gitlab.com/gitlab-com/), à la fois un service en ligne comparable à GitHub, et un outil serveur open-source.
* [Framagit](https://framagit.org), un service maintenu par l'association Framasoft, reposant sur GitLab.

## Concept du versionnage

Le principe fondamental de Git est d'offrir un système de **versionnage** (gestion des versions), permettant de suivre de manière extrêmement précise chaque étape dans évolution d'un projet.

Pour illustrer cela, voici la visualisation du développement d'une fonte typographique, *Steps Mono*, créée par Raphaël Bastide et Jean-Baptiste Morizot pour le magazine *étapes*:

![Visualisation linéaire du développement de Steps Mono.](/cours-git/img/timeline-dev-fonte.jpg)

### Versionnage vs. déploiement

Dans le domaine du développement web, Git est souvent utilisé pour la collaboration et le versionnage du code d'un site. Il n'est pour autant pas forcément utilisé comme **outil de déploiement** (envoi du code finalisé vers le serveur public), car les services d'hébergement web ne supportent pas toujours les protocoles nécessaires (SSH+Git).

On peut donc très bien avoir des processus hybrides:

* **Git** est utilisé pour la collaboration et l'archivage du code (versionnage).
* **FTP ou SFTP** est utilisé pour publier le code vers le serveur public (déploiement).

![Versionnage / dépoiement](/cours-git/img/versionnage-deploiement.jpg)

## Terminologie Git

Voici quelques-uns des termes fondamentaux du système Git:

**Repository** (parfois abrégé en "Repo") : c'est un "dépôt" (de code ou de fichiers). C'est le dossier de travail, contenant les fichiers d'un projet.

**Commit** (commettre) : l'action d'enregistrer vos modifications dans l'historique du projet. Un commit est un instantané de votre projet. Il faut l'accompagner d'un "commit message".

**Push** (pousser) : permet d'envoyer vos commits vers un "remote" (un serveur git, p.ex. Github).

**Pull** (tirer) : get commits from a remote.

**Checkout** : permet de voyager dans le temps, en retournant à un commit précis.

**Stash** (ranger) : save modified and staged changes (en français: remise). Permet de "mettre de côté" vos modifications, sans pour autant faire un commit. C'est une façon de ranger dans un tiroir (ou sous le tapis...) des modifications un peu hasardeuses, que vous n'êtes pas certain de vouloir conserver.

**Merge** (fusionner) : combining two branches. Une action critique: le "merge" est le fusionnement de deux versions d'un projet (branche alternative vers branche principale). Si cela se passe bien, les modifications de la branche A seront proprement intégrées par la branche B. Si cela se passe mal, vous pouvez rencontrer un "merge conflict".

**Rebase** (rembobiner) : apply any commits of current branch ahead of specified one.

**Branch** (branche) : create a new branch at the current commit (a movable label that points to a commit).

**index** : aussi "stage", "staging area": Il s’agit de la zone de validation désignant les travaux que vous souhaitez voir apparaître dans votre prochain commit.

**HEAD** : HEAD est un pointeur, une référence sur notre position actuelle dans notre répertoire de travail Git. "The current HEAD is local to each repository, and is therefore individual for each developer."

![](/cours-divers/img/Strip-Bon-daccord-650-final.jpg)

## Guide d'utilisation GitHub:

(Documentation à compléter)

- Créer un compte sur [Github.com](https://github.com/).
- Télécharger l'application [Github Desktop](https://desktop.github.com/).
- Créer un repository.
- Synchroniser ses modifications
- Faire un correctif sur un projet existant.

### Ecriture de messages de Commit

"En règle générale, les messages doivent débuter par une ligne unique d’au plus 50 caractères décrivant concisément la modification, suivie d’une ligne vide, suivie d’une explication plus détaillée. Le projet Git exige que l’explication détaillée inclue la motivation de la modification en contrastant le nouveau comportement par rapport à l’ancien — c’est une bonne règle de rédaction."

Source: [The Git Book](https://git-scm.com/book/fr/v2/Git-distribu%C3%A9-Contribution-%C3%A0-un-projet)

![Messages de Commit](/cours-divers/img/git-commit-messages.png)

Source: *[Git for Humans](https://speakerdeck.com/alicebartlett/git-for-humans)*, conférence par Alice Bartlett, développeuse au *Financial Times* - aussi disponible [en vidéo](https://www.youtube.com/watch?v=eWxxfttcMts).

### Les branches

Le système des **branches** est une fonctionnalité puissante, qui permet de sortir d'un processus d'avancement linéaire, et de créer au sein d'un projet des "bifurcations", voire une arborescence.

Cela permet par exemple de créer une version alternative et expérimentale, pour tester de nouvelles fonctionalités.

Ces ajouts, qui peuvent introduire des dysfonctionnements, ne vont pas perturber la version de base (généralement nommée "master"), qui reste ainsi stable.

Une fois qu'un développement expérimental arrive à maturité, on peut l'intégrer dans la version de base. On fera cela en fusionnant la branche expérimentale avec la branche "master", en faisant appel à la fonction "merge".

Voir à ce sujet: 

* explicatif des branches dans l'interface SourceTree: [Use SourceTree branches to merge an update](https://confluence.atlassian.com/bitbucket/use-sourcetree-branches-to-merge-an-update-732268925.html)

