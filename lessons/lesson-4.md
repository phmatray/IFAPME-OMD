# OMB-04 - Git, le meilleur ami du développeur

## Introduction

Git est un outil de gestion de version de code source. Il permet de gérer les modifications de code source de manière efficace et de travailler en équipe sur un même projet. Il est utilisé par de nombreux développeurs et est devenu un standard dans le monde du développement logiciel.

Il a été créé par Linus Torvalds, le créateur du noyau Linux. Il est utilisé par de nombreux projets open source comme le noyau Linux, le logiciel de gestion de version de code source Git, le navigateur web Firefox, le système d'exploitation Android, etc.

Git est un outil puissant et il est possible de faire beaucoup de choses avec. Nous allons voir les commandes de base de Git et nous allons voir comment utiliser Git pour travailler en équipe sur un projet.

## Objectifs

* Savoir utiliser Git pour travailler en équipe sur un projet
* Comprendre les concepts de base de Git
  * Comprendre ce qu'est un commit
  * Comprendre ce qu'est une branche
  * Comprendre ce qu'est un merge
  * ...
* Voir les commandes de base de Git
  * git init
  * git add
  * git commit
  * git status
  * git log

## Liens vers les ressources

* [Git](https://git-scm.com/)
* [Git - Wikipedia](https://en.wikipedia.org/wiki/Git)
* [Git - The Simple Guide](https://rogerdudler.github.io/git-guide/)
* [Learn Git Branching](https://learngitbranching.js.org/?locale=fr_FR)
* [Oh my Git!](https://ohmygit.org/)
* [OpenClassrooms - Git](https://openclassrooms.com/fr/courses/7162856-gerez-du-code-avec-git-et-github)
* [W3Schools - Git](https://www.w3schools.com/git/git_getstarted.asp)

## Comprendre les concepts de base de Git

Lire [Git for Everyone else](https://underbelly.is/writing-about/git-for-everyone-else) de [Zack Sunderland](https://underbelly.is/).

## Commandes de base de Git

### git init

La commande `git init` permet d'initialiser un dépôt Git. Cela crée un dossier `.git` dans le dossier courant. Ce dossier contient toutes les informations sur le dépôt Git.

### git add

La commande `git add` permet d'ajouter des fichiers au dépôt Git. Elle prend en paramètre le nom du fichier à ajouter. Par exemple, pour ajouter le fichier `README.md` au dépôt Git, on utilise la commande suivante:

```bash

git add README.md

```

### git commit

La commande `git commit` permet de créer un commit. Un commit est un point dans l'historique du dépôt Git. Il contient les modifications apportées au dépôt Git depuis le dernier commit. Il prend en paramètre le message du commit. Par exemple, pour créer un commit avec le message "Ajout du fichier README.md", on utilise la commande suivante:

```bash

git commit -m "Ajout du fichier README.md"

```

### git status

La commande `git status` permet d'afficher l'état du dépôt Git. Elle affiche les fichiers qui ont été modifiés, les fichiers qui ont été ajoutés au dépôt Git, etc.

### git log

La commande `git log` permet d'afficher l'historique du dépôt Git. Elle affiche les commits du dépôt Git.

### git branch

La commande `git branch` permet de créer une branche. Une branche est une ligne de développement indépendante. Elle permet de travailler sur un projet sans impacter le code source du projet. Par exemple, pour créer une branche `feature-1`, on utilise la commande suivante:

```bash

git branch feature-1

```

### git checkout

La commande `git checkout` permet de changer de branche. Par exemple, pour changer de branche `master` vers la branche `feature-1`, on utilise la commande suivante:

```bash

git checkout feature-1

```

## Exercices

### Exercice 1

Completer la lise d'exercice sur Learn Git Branching. Vous pouvez utiliser le lien suivant: [Learn Git Branching](https://learngitbranching.js.org/?locale=fr_FR)

### Exercice 2

La W3Schools propose une liste d'exercices sur Git. Vous pouvez utiliser le lien suivant: [W3Schools - Git Exercises](https://www.w3schools.com/git/exercise.asp)