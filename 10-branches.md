---
layout: page
title: Les branches
permalink: /git/branches/
---

# Les branches

Le système des **branches** est une fonctionnalité puissante, qui permet de sortir d'un processus d'avancement linéaire, et de créer au sein d'un projet des "bifurcations", voire une arborescence.

Cela permet par exemple de créer une version alternative et expérimentale, pour tester de nouvelles fonctionalités.

Ces ajouts, qui peuvent introduire des dysfonctionnements, ne vont pas perturber la version de base (généralement nommée "master"), qui reste ainsi stable.

Une fois qu'un développement expérimental arrive à maturité, on peut l'intégrer dans la version de base. On fera cela en fusionnant la branche expérimentale avec la branche "master", en faisant appel à la fonction "merge".

Voir à ce sujet: 

* explicatif des branches dans l'interface SourceTree: [Use SourceTree branches to merge an update](https://confluence.atlassian.com/bitbucket/use-sourcetree-branches-to-merge-an-update-732268925.html)