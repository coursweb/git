---
layout: page
title: Troubleshooting
permalink: /git/troubleshooting/
---

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
Se rendre dans l'historique de Github Desktop, et retourner dans une version antérieure avec un double click.

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

***

Pour sa présentation *"[Changing History, or How to Git pretty](http://justinhileman.info/article/changing-history/)"*, Justin Hileman a créé le graphe "escape a git mess, step-by-step" - visuel qui explique les différentes manières de résoudre des problèmes dans Git:

![escape a git mess, step-by-step](/cours-divers/img/git-pretty.png)

