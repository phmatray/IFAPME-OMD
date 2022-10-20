# OMB-05 - Les bases de la ligne de commande

## Introduction

La ligne de commande est un outil puissant qui permet de faire des choses très rapidement. C'est un outil qui peut être intimidant au premier abord, mais qui est très utile une fois qu'on a compris comment il fonctionne.

Dans ce chapitre, nous allons apprendre les bases de la ligne de commande. Nous allons voir comment se déplacer dans l'arborescence de fichiers, comment créer des fichiers et des dossiers, comment copier, déplacer et supprimer des fichiers et des dossiers, et comment afficher le contenu d'un fichier.

## Objectifs

* Comprendre les bases de la ligne de commande
  * Pouvoir utiliser la ligne de commande pour naviguer dans les dossiers
  * Pouvoir utiliser la ligne de commande pour créer des fichiers et des dossiers
  * Pouvoir utiliser la ligne de commande pour afficher le contenu d'un fichier
  * Pouvoir utiliser la ligne de commande pour éditer un fichier
  * Pouvoir utiliser la ligne de commande pour supprimer un fichier ou un dossier
* Créer un script Bash
  * Pouvoir créer un script Bash
  * Pouvoir exécuter un script Bash
  * Pouvoir passer des paramètres à un script Bash
* Créer un script PowerShell
  * Pouvoir créer un script PowerShell
  * Pouvoir exécuter un script PowerShell
  * Pouvoir passer des paramètres à un script PowerShell

## Liens vers les ressources

* [Bash - Wikipedia](https://en.wikipedia.org/wiki/Bash_(Unix_shell))
* [Bash - Learn Shell](https://www.learnshell.org/)
* [CMD - Wikipedia](https://fr.wikipedia.org/wiki/Cmd)
* [Liste des commandes CMD](https://www.ionos.fr/digitalguide/serveur/know-how/commande-cmd/)

## Définitions

### Terminal

Le terminal est un programme qui permet d'interagir avec l'ordinateur en tapant des commandes. Il est disponible sur tous les systèmes d'exploitation.

* Sur Windows, le terminal est appelé `cmd.exe`.
* Sur Mac, il est appelé `Terminal.app`.
* Sur Linux, il est appelé `Terminal`.

Avec le terminal, on peut naviguer dans les dossiers de l'ordinateur, créer des fichiers et des dossiers, exécuter des programmes, etc.

![Terminal](/media/terminal.png)

Autrefois, le terminal était la seule façon d'interagir avec l'ordinateur. Aujourd'hui, il est utilisé pour automatiser des tâches répétitives.

Chaque système d'exploitation a son propre terminal. Par exemple, le terminal de Windows est différent du terminal de Mac. Cependant, la plupart des commandes sont les mêmes ou du moins très similaires.

### Commande

Une commande est une instruction que l'on donne à un ordinateur. Par exemple, pour afficher le contenu d'un fichier, on utilise la commande `cat` sur Mac et Linux, et la commande `type` sur Windows.

Liste des commandes les plus utilisées sur Mac et Linux:

* `ls` - Affiche le contenu d'un dossier.
* `cd` - Change le dossier courant.
* `mkdir` - Crée un dossier.
* `touch` - Crée un fichier.
* `cat` - Affiche le contenu d'un fichier.
* `rm` - Supprime un fichier ou un dossier.
* `open` - Ouvre un fichier ou un dossier.
* `clear` - Efface l'écran.

Liste des commandes les plus utilisées sur Windows:

* `dir` - Affiche le contenu d'un dossier.
* `cd` - Change le dossier courant.
* `mkdir` - Crée un dossier.
* `type nul >` - Crée un fichier.
* `type` - Affiche le contenu d'un fichier.
* `del` - Supprime un fichier ou un dossier.
* `explorer` - Ouvre un fichier ou un dossier.
* `cls` - Efface l'écran.

### Paramètre

Un paramètre est une information supplémentaire que l'on donne à une commande. Par exemple, pour afficher le contenu d'un fichier, on utilise la commande `cat` sur Mac et Linux, et la commande `type` sur Windows. Ces commandes prennent un paramètre, qui est le nom du fichier à afficher.

```bash
cat fichier.txt
type fichier.txt
```

### Script (Bash)

Un script est un programme écrit dans un fichier texte. Il est exécuté par un terminal. Par exemple, on peut écrire un script qui contient une suite de commandes pour automatiser une tâche répétitive.

Par exemple, on peut écrire un script qui affiche des informations sur l'ordinateur et qui les enregistre dans un fichier texte avec la date et l'heure.

```bash
#!/bin/bash

date=$(date)
hostname=$(hostname)
uptime=$(uptime)

echo "Date: $date" > info.txt
echo "Hostname: $hostname" >> info.txt
echo "Uptime: $uptime" >> info.txt
```

Une fois le script enregistré dans un fichier texte, il est nécessaire de le rendre exécutable avec la commande `chmod`:

```bash
chmod +x script.sh
```

Ensuite, on peut l'exécuter:

```bash
./script.sh
```

## Dans quel cas utiliser la ligne de commande?

La ligne de commande est utile pour automatiser des tâches répétitives. Par exemple, on peut écrire un script qui crée un dossier pour chaque projet, et qui crée des fichiers de base pour chaque projet.

Nous pouvons également utiliser la ligne de commande pour automatiser des tâches qui ne sont pas possibles avec l'interface graphique. Par exemple, on peut écrire un script qui télécharge des fichiers depuis un serveur distant.

Un dernier exemple: on peut écrire un script qui affiche des informations sur l'ordinateur, les enregistre dans un fichier texte avec la date et l'heure et l'envoie par courriel à un administrateur pour du diagnostic...

Les possibilités sont infinies!

## Comment ouvrir le terminal?

### Windows

Pour ouvrir le terminal sur Windows, il faut appuyer sur la touche `Windows` et taper `cmd`. On peut aussi ouvrir le terminal en appuyant sur la touche `Windows` et en tapant `cmd.exe`.

### Mac

Pour ouvrir le terminal sur Mac, il faut appuyer sur la touche `Command` et taper `Terminal`. On peut aussi ouvrir le terminal en appuyant sur la touche `Command` et en tapant `Terminal.app`.

### Linux

Pour ouvrir le terminal sur Linux, il faut appuyer sur la touche `Ctrl` et taper `Alt` et `T`. On peut aussi ouvrir le terminal en appuyant sur la touche `Ctrl` et en tapant `Alt` et `T`.

> **Note**
> Selon la distribution Linux, il est possible que ce raccourci ne fonctionne pas. Dans ce cas, il faut ouvrir le terminal en appuyant sur la touche `Windows` et en tapant `Terminal`.

## WSL (Windows Subsystem for Linux)

Si vous utilisez Windows, vous pouvez installer un système d'exploitation Linux en utilisant WSL. Cela vous permet d'utiliser le terminal de Linux sur Windows.

C'est une sorte de machine virtuelle qui exécute Linux. C'est un peu comme si on avait un ordinateur virtuel qui exécute Linux.

WSL est inclus dans Windows 10 et Windows 11. Pour l'activer, il faut ouvrir le menu Démarrer, taper `Activer ou désactiver les fonctionnalités Windows` et cocher la case `Sous-système Windows pour Linux`.

![Activer WSL](/media/enable-wsl.png)

Une fois WSL activé, il faut installer une distribution Linux. Pour ce faire, il faut ouvrir le menu Démarrer, taper `Microsoft Store` et chercher une distribution Linux. Par exemple, on peut installer Ubuntu.

Une fois la distribution Linux installée, il faut lancer le terminal Linux. Pour ce faire, il faut ouvrir le menu Démarrer, taper `Ubuntu` et cliquer sur l'application Ubuntu.

## Exemples

### Afficher le contenu d'un fichier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `cat fichier.txt` | Affiche le contenu du fichier `fichier.txt` |
| Windows | `type fichier.txt` | Affiche le contenu du fichier `fichier.txt` |

### Créer un fichier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `touch fichier.txt` | Crée un fichier `fichier.txt` |
| Windows | `type nul > fichier.txt` | Crée un fichier `fichier.txt` |

> **Note**
> Si la commande `type nul > fichier.txt` ne fonctionne pas, il faut utiliser la commande `notepad fichier.txt`. L'éditeur de texte Notepad va s'ouvrir, et il vous suffit de sauvegarder le fichier.

### Créer un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `mkdir dossier` | Crée un dossier `dossier` |
| Windows | `mkdir dossier` | Crée un dossier `dossier` |

### Supprimer un fichier ou un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `rm fichier.txt` | Supprime le fichier `fichier.txt` |
| Mac et Linux | `rm -r dossier` | Supprime le dossier `dossier` |
| Windows | `del fichier.txt` | Supprime le fichier `fichier.txt` |
| Windows | `rmdir /s dossier` | Supprime le dossier `dossier` |

### Ouvrir un fichier ou un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `open fichier.txt` | Ouvre le fichier `fichier.txt` |
| Mac et Linux | `open dossier` | Ouvre le dossier `dossier` |
| Windows | `explorer fichier.txt` | Ouvre le fichier `fichier.txt` |
| Windows | `explorer dossier` | Ouvre le dossier `dossier` |

### Effacer l'écran

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `clear` | Efface l'écran |
| Windows | `cls` | Efface l'écran |

### Afficher le dossier courant

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `pwd` | Affiche le dossier courant |
| Windows | `cd` | Affiche le dossier courant |

### Changer le dossier courant

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `cd dossier` | Change le dossier courant en `dossier` |
| Windows | `cd dossier` | Change le dossier courant en `dossier` |

### Afficher le contenu d'un dossier

Cette commande affiche le contenu d'un dossier, c'est-à-dire les fichiers et les dossiers qui se trouvent dans ce dossier. Elle est très utile pour savoir si un fichier ou un dossier existe.

De nombreux paramètres peuvent être ajoutés à cette commande pour afficher plus d'informations. Par exemple, le paramètre `-l` affiche les fichiers et les dossiers avec plus de détails.

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `ls` | Affiche le contenu du dossier courant |
| Mac et Linux | `ls dossier` | Affiche le contenu du dossier `dossier` |
| Mac et Linux | `ls -l` | Affiche le contenu du dossier courant avec plus de détails |
| Mac et Linux | `ls -l dossier` | Affiche le contenu du dossier `dossier` avec plus de détails |
| Windows | `dir` | Affiche le contenu du dossier courant |
| Windows | `dir dossier` | Affiche le contenu du dossier `dossier` |
| Windows | `dir /w` | Affiche le contenu du dossier courant avec plus de détails |
| Windows | `dir /w dossier` | Affiche le contenu du dossier `dossier` avec plus de détails |

### Copier un fichier ou un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `cp fichier.txt dossier` | Copie le fichier `fichier.txt` dans le dossier `dossier` |
| Mac et Linux | `cp -r dossier1 dossier2` | Copie le dossier `dossier1` dans le dossier `dossier2` |
| Windows | `copy fichier.txt dossier` | Copie le fichier `fichier.txt` dans le dossier `dossier` |
| Windows | `xcopy /e dossier1 dossier2` | Copie le dossier `dossier1` dans le dossier `dossier2` |

### Déplacer un fichier ou un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `mv fichier.txt dossier` | Déplace le fichier `fichier.txt` dans le dossier `dossier` |
| Mac et Linux | `mv dossier1 dossier2` | Déplace le dossier `dossier1` dans le dossier `dossier2` |
| Windows | `move fichier.txt dossier` | Déplace le fichier `fichier.txt` dans le dossier `dossier` |
| Windows | `move /e dossier1 dossier2` | Déplace le dossier `dossier1` dans le dossier `dossier2` |

### Renommer un fichier ou un dossier

| OS | Commande | Description |
| --- | --- | --- |
| Mac et Linux | `mv fichier.txt nouveau_nom.txt` | Renomme le fichier `fichier.txt` en `nouveau_nom.txt` |
| Mac et Linux | `mv dossier nouveau_dossier` | Renomme le dossier `dossier` en `nouveau_dossier` |
| Windows | `ren fichier.txt nouveau_nom.txt` | Renomme le fichier `fichier.txt` en `nouveau_nom.txt` |
| Windows | `ren dossier nouveau_dossier` | Renomme le dossier `dossier` en `nouveau_dossier` |

## Trouver de l'aide

Pour trouver de l'aide sur une commande, on utilise la commande `man` sur Mac et Linux, et la commande `help` sur Windows.

## Exercices Linux

Voici quelques exercices pour vous entraîner à utiliser la ligne de commande sur Linux. Pour les faire, vous pouvez utiliser un terminal en ligne comme [repl.it](https://repl.it/languages/bash) ou [CodeSandbox](https://codesandbox.io/s/terminal-lesson-5-5xq7o).

### Exercice 1-A (joe, less, ls)

1. Créez un fichier `premiertexte` contenant une ou deux phrases.
2. Visualisez le contenu de `premiertexte` sans l'éditer.
3. Quelle est la taille de `premiertexte` ?
4. Éditez `PREMIERTEXTE`. Que constatez-vous ?

### Exercice 1-B (cp, ls, mv)

1. Faites une copie de `premiertexte` appelée `double`.
2. Comparez leurs tailles.
3. Renommez `double` en `introduction`.
4. Quelle différence y a-t-il entre `mv double introduction` et `cp double introduction`

### Exercice 1-C (mkdir, mv, cp, ls, cd)

1. Créez un répertoire `essai/`.
2. Déplacez `introduction` dans `essai/`.
3. Faites une copie de `premiertexte` appelée `copie`, et placez-la également dans `essai/`.
4. Affichez une liste de ce que contient `essai/`.

### Exercice 1-D (rmdir, cd, rm)

1. Essayez de détruire `essai/`. Que se passe-t-il ? Que faut-il faire pour détruire un répertoire ?
2. Détruisez tout ce que contient `essai/`.
3. Détruisez `essai/`.

## Exercices Windows

Il s'agit d'une version des exercices précédents pour Windows. Pour les faire, vous pouvez utiliser le terminal sur votre ordinateur tournant sous Windows.

### Exercice 2-A (type, notepad, dir)

1. Créez un fichier `premiertexte` contenant une ou deux phrases.
2. Visualisez le contenu de `premiertexte` sans l'éditer.
3. Quelle est la taille de `premiertexte` ?
4. Éditez `PREMIERTEXTE`. Que constatez-vous ?

### Exercice 2-B (copy, dir, rename)

1. Faites une copie de `premiertexte` appelée `double`.
2. Comparez leurs tailles.
3. Renommez `double` en `introduction`.
4. Quelle différence y a-t-il entre `rename double introduction` et `copy double introduction`

### Exercice 2-C (mkdir, move, copy, dir, cd)

1. Créez un répertoire `essai/`.
2. Déplacez `introduction` dans `essai/`.
3. Faites une copie de `premiertexte` appelée `copie`, et placez-la également dans `essai/`.
4. Affichez une liste de ce que contient `essai/`.

### Exercice 2-D (rmdir, cd, del)

1. Essayez de détruire `essai/`. Que se passe-t-il ? Que faut-il faire pour détruire un répertoire ?
2. Détruisez tout ce que contient `essai/`.
3. Détruisez `essai/`.

## Conclusion

La ligne de commande est un outil puissant qui permet de faire beaucoup de choses. Elle est utilisée par les développeurs pour automatiser des tâches répétitives, et par les administrateurs système pour gérer des serveurs. Elle est également utilisée par les hackers pour pirater des systèmes.

Il s'agit d'un outil très puissant, mais qui peut être dangereux si on ne sait pas ce qu'on fait. Il est donc important de bien comprendre ce qu'on fait avant de l'utiliser.

Rappelez-vous que vous pouvez toujours utiliser l'aide pour trouver des informations sur une commande. Par exemple, pour trouver de l'aide sur la commande `cat`, on utilise la commande `man cat` sur Mac et Linux, et la commande `help cat` sur Windows.

