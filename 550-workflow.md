---
layout: page
title: Workflow
permalink: /git/workflow/
---

Un workflow Git
===

Une méthodologie Git pour projets de design, proposée par [Mathieu Dutour](https://mathieudutour.github.io/git-sketch-plugin/), auteur du *Git Sketch Plugin*:

* Créez une nouvelle *branche* quand vous commencez à travailler sur une nouvelle fonctionalité.
* Travaillez normalement sur votre design.
* Enregistrez le fichier.
* Faites un "Commit" de vos modifications, avec un message les décrivant.
* Faites un "Push" de vos modifications.
* Faites une "pull request" de votre branche vers la branche principale ("master").
* Voilà! Vos collaborateurs peuvent voir vos modifications, faire des commentaires, et les approuver. Une fois approuvés, faire un "merge" de votre "pull request".

<h3>Liens sur les workflows Git:</h3>

* [A successful Git branching model](http://nvie.com/posts/a-successful-git-branching-model/), article de Vincent Driessen, 2010, définissant la méthodologie "Git Flow". Propose un système de branches.
* [Using git-flow to automate your git branching workflow](http://jeffkreeftmeijer.com/2010/why-arent-you-using-git-flow/), par Jeff Kreeftmeijer - donne des informations techniques sur la manière d'appliquer le modèle "Git Flow" (et l'utilitaire [git-flow](https://github.com/nvie/gitflow), qui est "a wrapper around existing git commands").
* [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html), article de  Scott Chacon, 2011, qui décrit une méthode plus simple et fluide (pratiquée par l'entreprise GitHub, d'où son nom).
* [A simple git branching model](https://gist.github.com/jbenet/ee6c9ac48068889b0912), par Juan Benet, 2013.
* [Simple Git workflow is simple](http://blogs.atlassian.com/2014/01/simple-git-workflow-simple/), article de Nicola Paolucci, 2014.
* [GitLab Flow](https://about.gitlab.com/2014/09/29/gitlab-flow/), article de Sytse Sijbrandij, 2014 - une méthode qui vise à prévenir la complexité de Git Flow: "git flow is too complex for most of the use cases".
* [Comparing Workflows](https://www.atlassian.com/git/tutorials/comparing-workflows), documentation d'Atlassian (la société produisant Bitbucket et Sourcetree)

Quelques autres articles sur l'utilisation de Git:

- [Bien utiliser Git merge et rebase](http://www.git-attitude.fr/2014/05/04/bien-utiliser-git-merge-et-rebase/), par Christophe Porteneuve (git-attitude), 2014

Difficile?
===

Git n'est certainement pas un outil simple. Voici quelques citations qui le confirment:

> Git isn’t difficult because you’re not smart enough, or because you missed an important meeting. Git is difficult because Git is difficult.

David Demaree, auteur de *Git for Humans*

> I’m not good with Git, and still don’t fully understand how rebasing works. I messed up my commits a couple of times. Not a big deal, but I got different error messages no matter which workflow I tried. I realized that I need to know more about Git, and be more patient.

Sami Keijonen, développeur, [dans un article](https://poststatus.com/contributing-to-twenty-seventeen-theme/) où il relate sa contribution au thème WordPress TwentySeventeen.

Il est important de réaliser que le plus important, avec Git, c'est d'adopter la pratique du "versionnement" dans son processus de travail. Ce n'est pas seulement un outil, un logiciel - c'est un ensemble de méthodes pour mieux organiser le travail collaboratif.

