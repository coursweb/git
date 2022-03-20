---
layout: page
title: Terminologie
permalink: terminologie.html
---

Voici quelques-uns des termes fondamentaux du système Git:

**Repository** (parfois abrégé en "Repo") : c'est un "dépôt" (de code ou de fichiers). C'est le dossier de travail, contenant les fichiers d'un projet.

**Commit** (valider) : l'action d'enregistrer vos modifications dans l'historique du projet. Un commit est un instantané de votre projet. Il faut l'accompagner d'un "commit message".

**Push** (pousser) : permet d'envoyer vos commits vers un dépôt distant (remote repository) sur un serveur git, p.ex. Github.

**Pull** (tirer) : *get commits from a remote*.

**Checkout** : permet de "voyager dans le temps", en ramenant votre espace de travail à un commit précis.

**Stash** (en français: remise) : *save modified and staged changes*. Permet de "mettre de côté" vos modifications, sans pour autant faire un commit. C'est une façon de ranger dans un tiroir (ou sous le tapis...) des modifications un peu hasardeuses, que vous n'êtes pas certain de vouloir conserver.

**Merge** (fusionner) : *combining two branches*. Une action critique: le "merge" est le fusionnement de deux versions d'un projet (branche alternative vers branche principale). Si cela se passe bien, les modifications de la branche A seront proprement intégrées par la branche B. Si cela se passe mal, vous pouvez rencontrer un "merge conflict" (voir [Troubleshooting]()).

![](img/memes/git-Merge.gif)

**Rebase** (rembobiner) : *apply any commits of current branch ahead of specified one*.

**Branch** (branche) : *create a new branch at the current commit (a movable label that points to a commit)*.

**index** (aussi nommé "staging area") : Il s’agit de la zone de validation désignant les travaux que vous souhaitez voir apparaître dans votre prochain commit. La commande "git add" permet d'y ajouter des fichiers.

**HEAD** : HEAD est un pointeur, une référence sur notre position actuelle dans notre répertoire de travail Git. "The current HEAD is local to each repository, and is therefore individual for each developer."