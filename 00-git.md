---
layout: page
title: Git
permalink: /git/
---

> Ce chapitre propose une introduction au logiciel Git et à la gestion de versions.

**Git** est un logiciel de *gestion de versions* décentralisé, créé en 2005 par Linus Torvalds (le créateur de Linux). C'est un logiciel libre, sous licence GPL. Il existe des versions pour toutes les plateformes, y compris MacOS. Le site officiel de documentation est [git-scm.com](https://git-scm.com).

Voici quelques-uns des avantages que Git apporte: 

- Permet à un grand nombre de collaborateurs de travailler sur un même projet, en offrant une bonne gestion des modifications.
- Permet de synchroniser un projet entre plusieurs collaborateurs, en ayant l'assurance que tous les fichiers soient à jour.
- Permet d'avoir un historique précis de tous les changements et modifications d'un projet. Cela permet de clarifier les questions récurrentes: "Où est la dernière version du fichier X?" et "Qu'est-ce qui a été changé entre les révisions 41 et 42"?.

Git est à la base un outil "en ligne de commande". Afin d'avoir un meilleur confort d'utilisation, il existe divers logiciels offrant une interface graphique. Il existe également des services en ligne permettant d'héberger des projets Git, afin de faciliter la collaboration et d'avoir une sauvegarde en ligne.

**[GitHub](https://github.com/)** est un service web offrant l'hébergement de projets utilisant Git, lancé en 2008 (cf. [cet article](http://tom.preston-werner.com/2011/03/29/ten-lessons-from-githubs-first-year.html) sur les débuts de cette startup californienne). Devenu extrêmement populaire (plus de 14 millions d'utilisateurs en 2016), GitHub offre de nombreuses fonctionnalités facilitant la communication et la collaboration. En 2018, GitHub a été acheté par Microsoft.

![Une publication marketing de GitHub](/cours-divers/img/github-activity-book.jpg)

Si GitHub est le plus populaire, il existe cependant d'autres services d'hébergement Git. Notamment: 

* [BitBucket](https://bitbucket.org), un service freemium, acquis par la société australienne Atlassian en 2010. Contrairement à Github, il permet d'avoir des projets privés même dans la version gratuite. Le service devient payant à partir de 5 personnes dans une équipe.
* [GitLab](https://about.gitlab.com/gitlab-com/), à la fois un service en ligne comparable à GitHub, et un outil serveur open-source.
* [Framagit](https://framagit.org), un service maintenu par l'association Framasoft, reposant sur GitLab.

Il est aussi possible d'installer Git sur votre serveur, comme le fait par exemple le collectif de graphistes OSP (Open Source Publishing). Voici leur serveur Git public: [https://gitlab.constantvzw.org/osp](https://gitlab.constantvzw.org/osp)

## Concept du versionnage

Le principe fondamental de Git est d'offrir un système de **versionnage** (gestion des versions), permettant de suivre de manière extrêmement précise chaque étape dans évolution d'un projet.

Pour illustrer cela, voici la visualisation du développement d'une fonte typographique, *[Steps Mono](https://velvetyne.fr/fonts/steps-mono/)*, créée par Raphaël Bastide et Jean-Baptiste Morizot pour le magazine *étapes*:

![Visualisation linéaire du développement de Steps Mono.](/cours-git/img/timeline-dev-fonte.jpg)

### Versionnage vs. déploiement

Dans le domaine du développement web, Git est souvent utilisé pour la collaboration et le versionnage du code d'un site. Il n'est pour autant pas forcément utilisé comme **outil de déploiement** (envoi du code finalisé vers le serveur public), car les services d'hébergement web ne supportent pas toujours les protocoles nécessaires (SSH+Git).

On peut donc très bien avoir des processus hybrides:

* **Git** est utilisé pour la collaboration et l'archivage du code (versionnage).
* **FTP ou SFTP** est utilisé pour publier le code vers le serveur public (déploiement).

![Versionnage / dépoiement](/cours-git/img/versionnage-deploiement.jpg)



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



