---
layout: page
title: Versionnage
permalink: /git/versionnage/
---


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



