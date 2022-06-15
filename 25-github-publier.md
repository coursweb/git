---
layout: page
title: Créer un projet
permalink: github-publier.html
---

## Comment créer un projet sur GitHub ?

Voici la méthode avec l'application GitHub Desktop:

- Lancez l'application Github Desktop
- Faites *File > Add Local Repository* et choisissez votre dossier de travail

GitHub va vous dire "This directory is not a Git repository" ... c'est normal!

- Cliquer *Create a repository*
- GitHub va ajouter votre dossier, c'est désormais un dossier de travail Git.
- Vous devez faire "Publish repository" pour le publier sur GitHub.
- Vous devez indiquer le nom du repository, choisir s'il sera public ou privé, choisir s'il se trouve dans une organisation.

La même chose en vidéo:

<video width="100%" controls>
  <source src="videos/publier-sur-github.mp4" type="video/mp4">
</video>


### Le .gitignore

**Attention:** avant votre premier commit, il est sage de vérifier que vous n'avez pas des formats de fichier non-désirés (qui risquent de rendre votre projet inutilement lourd):

- Inspectez la liste des "Uncommited Changes". Si vous voyez des fichiers qui ne devraient pas être mis en ligne - des images TIFF, PSD, des fichiers InDesign... - c'est le moment de créer un **GitIgnore**.

Pour cela, faites un clic-droit sur l'un de ces fichiers. Dans le menu contextuel, choisissez "Ignore all .indd files" (pour ne pas prendre en compte les fichiers InDesign, par exemple).

Le fichier `.gitignore` est un fichier optionnel, situé à la racine de votre projet, qui permet de désigner tout ce que Git doit "ignorer". 

Cela comprend généralement des fichiers temporaires créés par certains logiciels, ou des fichiers système comme [.DS_Store](https://fr.wikipedia.org/wiki/.DS_Store) (sur MacOS), [Thumbs.db](https://fr.wikipedia.org/wiki/Thumbs.db) ou Desktop.ini (systèmes Windows).

Exemple, [le .gitignore du Repository de Space Grotesk](https://github.com/floriankarsten/space-grotesk/blob/master/.gitignore):

```
# file manager empty files
.DS_Store
.empty
.sparkleshare
# temporary files
*(Autosaved).glyphs
*.vfbak
# minisite files
/docs/node_modules
/docs/package-lock.json
```

### Le premier commit

- Une fois cela fait, effectuez votre premier **commit**. Indiquez un message de Commit (champ *Summary*), obligatoire.
- Une fois le commit fait, cliquez le bouton **Publish**.
- Définissez le titre du projet, sous "Name"
- Vérifiez que le compte Github est correct.
- Cliquez sur **Publish Repository**.

**Bravo, votre projet est désormais en ligne!**

Si vous souhaitez qu'il soit accessible par une adresse personalisée, voir [Github Pages](github-pages.html).

## Explications en vidéo

### Cloner un projet existant

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/jf3zZNoYDYA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>