---
layout: page
title: Utiliser Github Pages
permalink: /git/github-pages/
---

Comment créer un site hébergé dans Github Pages:

<h3>Réglages à faire dans l'administration DNS de votre hébergeur</h3>

- Réfléchissez au type de domaine que vous souhaitez utiliser. 
- Rendez-vous dans la gestion des zones DNS de votre domaine (chez Infomaniak ou autre).
- Pour trouver cet endroit chez Infomaniak, connectez-vous à [admin2.infomaniak.com](https://admin2.infomaniak.com/), allez dans : *Nom de domaine > Nom de votre domaine > Gestion des DNS*, puis cliquez le bouton "Gérer les zones DNS".

**Option sous-domaine:**

- Si le domaine comporte un sous-domaine, comme portfolio.example.com, ou www.example.com, vous devrez créer une entrée de type CNAME.
- Renseignez "Champ/Field" (entrer le sous-domaine choisi), et "Cible/Target" (username.github.io). Si votre utilisateur est p.ex. Gandalf69, vous entrerez : gandalf69.github.io (tout en minuscules).
- Vous pouvez laisser le champ TTL avec sa valeur par défaut.

![Ajout de CNAME chez Infomaniak](/cours-divers/img/github-dns-cname.png)

![Ajout de CNAME chez O2Switch](/cours-divers/img/git-cname-o2switch.png)

**Option "apex domain":**

- Si le domaine est dépourvu de sous-domaine, comme **cours-web.ch** (un "apex domain"), la procédure est différente. Il faudra créer deux entrées de type A.
- Renseignez "Cible" et entrez les adresses IP [fournies par GitHub dans leur documentation](https://help.github.com/articles/setting-up-an-apex-domain/), à savoir 192.30.252.153 et 192.30.252.154 (une pour chaque entrée A).
- Vous pouvez laisser le champ TTL avec sa valeur par défaut.

![Ajout de zone A chez Infomaniak](/cours-divers/img/git-apex-infomaniak.png)

![Même réglage, chez Hostpoint](/cours-divers/img/git-apex-hostpoint.png)

<h3>Réglages à faire dans GitHub</h3>

- Premièrement, votre projet doit être publié sur GitHub.
- Aller dans les "Settings" de votre projet, dans la partie "Github Pages"
- Sous "Source", choisir la branche à utiliser.
- Sous "Custom domain", renseigner le domaine, p.ex. portfolio.example.com
- Enregistrer ("Save") - ça y est, votre site fonctionne!

Note: initialement il était nécessaire de créer une branche nommée "gh-pages", mais ce [n'est plus nécessaire depuis août 2016](https://github.com/blog/2228-simpler-github-pages-publishing).

![Saisie du domaine pour GitHub Pages](/cours-divers/img/github-custom-pages.png)

Références GitHub: 

* [Using a custom domain with GitHub Pages](https://help.github.com/articles/using-a-custom-domain-with-github-pages/)
* [About supported custom domains](https://help.github.com/articles/about-supported-custom-domains/)
* [Setting up an apex domain](https://help.github.com/articles/setting-up-an-apex-domain-and-www-subdomain/)
