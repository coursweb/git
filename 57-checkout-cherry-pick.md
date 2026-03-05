---
layout: page
title: Checkout et Cherry-pick
permalink: checkout-cherry-pick.html
---

La situation suivante peut se présenter: des erreurs ont été introduites dans le projet, et on veut revenir en arrière vers un commit plus ancien (uniquement pour deux fichiers). 

Tentative: on choisit le commit dans l'historique, et on choisit l'action "Checkout Commit".

Problème: on se retrouve en 'detached HEAD' et on ne sait pas quoi faire.

## Qu'est-ce qui s'est passé ?

Quand vous avez fait un checkout vers un ancien commit, Git a placé votre espace de travail "dans le passé" de l'historique. Git appelle ça un **detached HEAD** car vous n'êtes plus sur une branche (´main´), mais sur un commit flottant. Tout ce que vous auriez commité là aurait pu être perdu.

## Comment s'en sortir

Si vous vouliez juste consulter l'ancien état (sans modifier) → Il suffit de revenir sur `main` :

```
git checkout main
```

Si vous vouliez vraiment restaurer 2 fichiers spécifiques vers une ancienne version → La bonne commande à utiliser n'est pas checkout sur le commit entier, mais :

```
git checkout <hash-du-commit> -- fichier.html fichier.css
```

Le `--` suivi des noms de fichiers indique à Git de ne restaurer **que ces fichiers-là**, sans toucher au reste ni entrer en detached HEAD. Les fichiers restaurés apparaissent alors directement dans la zone de staging, prêts à être commités.

C'est un des cas où le terminal reste incontournable, même avec GitHub Desktop. 

## Checkout avec tous les fichiers ?

**Question:** Avec la commande `git checkout <hash> -- fichiers` est-ce qu'il y a un moyen simple de dire "tous les fichiers qui étaient dans ce commit" ?

**Réponse:** Oui, très simplement ! Il suffit de ne pas spécifier de fichiers du tout :

```
git checkout a3f5c2d -- .
```

Le `.` signifie "tous les fichiers" — Git restaure alors l'ensemble des fichiers du commit dans leur état d'époque.

### En résumé

-----|-----:
**Objectif**|**Commande**
Consulter un ancien commit | `git checkout <hash>` → puis `git checkout main` pour revenir
Restaurer des fichiers spécifiques | `git checkout <hash> -- fichier1 fichier2`

Le hash du commit (ex: a3f5c2d) est visible dans l'historique de GitHub Desktop en cliquant sur le commit concerné.

### Méthode dans Github Desktop

La combinaison la plus simple :

1. Dans GitHub Desktop, aller dans l'onglet **History**
2. Cliquer sur le commit ancien pour voir les fichiers modifiés
3. **Noter le hash** du commit (affiché en haut à droite, ex: a3f5c2d)
4. Ouvrir le terminal via **Repository → Open in Terminal**
5. Taper la commande : `git checkout a3f5c2d -- fichier.html fichier.css`
6. Retourner dans GitHub Desktop → les fichiers restaurés apparaissent automatiquement dans **Changes**, prêts à être commités

## Différence avec Cherry-pick Commit

**Question:** Quelle est la différence de cela avec l'action Cherry-pick Commit ?

Très bonne question ! Les deux permettent de récupérer des choses du passé, mais ils opèrent à des niveaux différents.

-----|-----:
`git checkout <hash> -- fichiers` | Récupère uniquement le **contenu de fichiers** spécifiques depuis un ancien commit. Ça ne crée pas de commit automatiquement — les fichiers restaurés atterrissent dans ta zone de staging, et tu commites quand tu veux.
**Cherry-pick** | Récupère un **commit entier** (avec toutes ses modifications) et le rejoue sur la branche actuelle. Ça crée automatiquement un nouveau commit.

En résumé:

**Cherry-pick** → tu veux récupérer tout un commit du passé. 
**checkout fichiers** → tu veux récupérer des fichiers précis d'un commit. 