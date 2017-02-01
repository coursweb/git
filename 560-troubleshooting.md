---
layout: page
title: Troubleshooting
permalink: /git/troubleshooting/
---

Git n'est certainement pas un outil simple. Voici quelques citations qui le confirment:

> Git isn’t difficult because you’re not smart enough, or because you missed an important meeting. Git is difficult because Git is difficult.

David Demaree, auteur de *Git for Humans*

> I’m not good with Git, and still don’t fully understand how rebasing works. I messed up my commits a couple of times. Not a big deal, but I got different error messages no matter which workflow I tried. I realized that I need to know more about Git, and be more patient.

Sami Keijonen, développeur, [dans un article](https://poststatus.com/contributing-to-twenty-seventeen-theme/) où il relate sa contribution au thème WordPress TwentySeventeen.

Il est important de réaliser que le plus important, avec Git, c'est d'adopter la pratique du "versionnement" dans son processus de travail. Ce n'est pas seulement un outil, un logiciel - c'est un ensemble de méthodes pour mieux organiser le travail collaboratif.

![Un message encourageant quand on ne comprend plus rien](/cours-git/img/git-homeomorphic.png)



Résolution de problèmes typiques:
==

**Problème:** Lors de la synchronisation, Git dit: *Sync Failed - There are both local and remote commits. Please commit all your changes and then sync again*.

**Tentative:** 

- Cocher toutes les modifications ("Uncommited changes").
- Faire un "Commit".
- Refaire un "Sync". Message : *Sync Conflicts: Please resolve all conflicted files, commit, then try syncing again*.
- Faire un click-droit sur les fichiers affichés, faire "Discard Changes"...

**Résultat:**  

Le résultat n'est pas celui escompté...

```
error: failed to push some refs to 'https://github.com/monprojet.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

**Solution:** 

- Comme le dit l'explicatif, il faut intégrer tout d'abord les modifications du serveur (avec un pull).
- Si des "Merge conflicts" apparaissent... les résoudre.

***

**Problème:**  
On se trouve avec des modifications non voulues. Comment revenir d'une version en arrière?

**Solution:**  
Se rendre dans l'historique de Github Desktop, et retourner dans une version antérieure... tout simplement avec un double click.

***

**Problème:** on a des caractères étranges dans un document, comme ceci: 

```
<<<<<<< HEAD
    Une version de mon projet
=======
    Une autre version de mon projet
>>>>>>> master
```

**Solution:** Ces symboles sont des délimiteurs nommés "conflict markers", ils indiquent un conflit non-résolu entre deux versions d'un même fichier, que Git n'a pas pu résoudre automatiquement.

Vous devez les corriger soit en effaçant l'une des versions, soit en utilisant une fonction "Resolve a Merge" dans votre logiciel Git.

C'est plus simple avec un graphe
===

Pour sa présentation *"[Changing History, or How to Git pretty](http://justinhileman.info/article/changing-history/)"*, Justin Hileman a créé le graphe "escape a git mess, step-by-step" - un visuel qui vous montre les différents cheminements pour résoudre un problème dans Git:

![escape a git mess, step-by-step](/cours-divers/img/git-pretty.png)