---
layout: page
title: Créer un projet
permalink: /git/github-creer/
---

**Comment créer un projet sur GitHub?**

Voici la méthode avec l'application GitHub Desktop:

- Lancez l'application Github Desktop
- Faites *File > Add Local Repository* et choisissez votre dossier de travail

Github va vous dire "This folder is not a repository" ... c'est normal!

- Cliquer *Create and Add*
- Github va ajouter votre dossier, c'est désormais un dossier de travail Git.

**Attention:** avant votre premier commit, il est sage de vérifier que vous n'avez pas des formats de fichier non-désirés (qui risquent de rendre votre projet inutilement lourd):

- Inspectez la liste des "Uncommited Changes". Si vous voyez des fichiers qui ne devraient pas être mis en ligne - des images TIFF, PSD, des fichiers InDesign... - c'est le moment de créer un **GitIgnore**.

Pour cela, faites un clic-droit sur l'un de ces fichiers. Dans le menu contextuel, choisissez "Ignore all .indd files" (pour ne pas prendre en compte les fichiers InDesign, par exemple).

- Une fois cela fait, effectuez votre premier **commit**. Indiquez un message de Commit (champ *Summary*), obligatoire.
- Une fois le commit fait, cliquez le bouton **Publish**.
- Définissez le titre du projet, sous "Name"
- Vérifiez que le compte Github est correct.
- Cliquez sur **Publish Repository**.

**Bravo, votre projet est désormais en ligne!**

Si vous souhaitez qu'il soit accessible par une adresse personalisée, voir [Github Pages](/git/github-pages/).

