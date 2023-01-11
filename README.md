# 2023H-TP0

*À noter: le tutoriel ci-bas est à réaliser après avoir consulté le jupyter notebook intitulé intro_TP0.ipynb*
La visualisation des jupyter notebook est possible directement via l'environnement PyCharm ou Visual Studio Code que vous avez déjà installé.

## Contenu
- [2023H-TP0](#2023h-tp0)
  - [Contenu](#contenu)
  - [Objectif](#objectif)
  - [:octocat: Qu'est-ce que Git/GitHub?](#octocat-quest-ce-que-gitgithub)
  - [:computer: Commandes les plus utilisées](#computer-commandes-les-plus-utilisées)
    - [Git clone](#git-clone)
    - [Git add](#git-add)
    - [Git commit](#git-commit)
    - [Git push](#git-push)
    - [Git pull](#git-pull)
    - [Git status](#git-status)
  - [Exercice pour se pratiquer](#exercice-pour-se-pratiquer)
  - [:keyboard: Instructions pour l'accès au terminal](#keyboard-instructions-pour-laccès-au-terminal)
    - [Windows](#windows)
    - [Mac](#mac)
    - [Linux](#linux)
  - [Comment naviguer entre des fichiers via le terminal](#comment-naviguer-entre-des-fichiers-via-le-terminal)
  - [Ressources additionnelles](#ressources-additionnelles)

## Objectif
Se familiariser avec les commandes les plus communes que vous allez utiliser sur Git/GitHub via un terminal (voir les [instructions particulières pour l'accès au terminal] pour votre système d'exploitation) en modifiant un fichier à l'[exercice ci-bas](#exercice-pour-se-pratiquer).

## :octocat: Qu'est-ce que Git/GitHub?
Git est un système de gestion de versions, il vous permet de garder un historique de toutes les modifications que vous faites dans un répertoire (lieu où vous sauvegarder un TP/Projet dans votre cas) aux fichiers qui y sont présents. Ainsi, il est plus facile de vous rappeler les divers modifications qui y ont été faites en les associant à un message informatif. Ceci enlève le risque de perdre votre travail puisque tout est inventorié. Également, Git facilite le travail collaboratif puisque deux personnes peuvent avoir une copie locale du même projet auquel ils font des modifications en parallèle. Quant à lui, GitHub est le serveur virtuel qui permet d'entreposer divers projets et d'être à nouveau au courant de leur historique ou de l'utiliser pour y apporter des changements. 

## :computer: Commandes les plus utilisées

### Git clone
Habituellement, tout commence par cloner un répertoire disponible en ligne sur GitHub. Vous pouvez cliquer sur le rectangle vert intitulé '<>Code' puis rendez-vous sur le terminal où vous écrirez la commande suivant:
```bash
    git clone https://github.com/exemple-de-lien/2023H-TP0.git
```
### Git add
Cette commande permet d'ajouter un fichier que vous voulez répertorier les changements que vous y apportez. C'est la première étape à faire après avoir fait un changement à un fichier quelconque:
```bash
    git add nom-du-fichier.py
```
### Git commit
Lorsque vous êtes satisfait des changements apportés, il faut maintenant 's'engager' et ajouter un message (-m) qui explique ce qui a été modifié tel que:
```bash
    git commit -m "Réponse à la question 1 complétée"
```
Qui vous retourne par exemple comme message:
```bash
    [main 1dfd86a] Réponse à la question 1 complétée
 1 file changed, 3 insertions(+), 1 deletion(-)
```
Un moyen de faire un git add sur tous les fichiers modifiés dans un répertoire en même temps est d'ajouter un -a (signifiant 'all') avant d'inscrire votre message informatif. Lorsque cette commande est utilisée, il n'est pas nécessaire de faire un git add auparavant.
```bash
    git commit -a -m "Réponse à la question 1 complétée"
```
### Git push
Ceci est la dernière étape qui rend visible vos modifications à un autre collaborateur potentiel puisque les changements seront maintenant disponibles sur le répertoire GitHub. 
```bash
    git push origin main
```
### Git pull
Lorsque vous commencez à travailler sur un projet d'équipe dont vous savez potentiellement que votre coéquipier a fait des changements, il faut aller 'tirer' les changements vers la version locale du répertoire que vous avez sur votre ordinateur. Ainsi, simplement tapez:
```bash
    git pull origin main
```
### Git status
Cette commande qui est souvent négligée ou oubliée, mais pourtant très utile, permet de vous dire où vous en être rendu dans le 'workflow' de Git. Ainsi, il vous avise à quelle étape vous êtes rendue... Dois-je 'add', 'commit' ou bien suis-je prêt à 'push' ma version locale vers GitHub? Toutes vos questions seront répondues!
Des exemples de statuts sont:
```bash
    nothing to commit, working tree clean
```
Vous êtes donc prêts à push, ou bien:
```bash
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
```
Il vous faut donc faire un 'commit' avant de pouvoir 'push' vos modifications sur le serveur virtuel GitHub!

*À noter qu'il existe beaucoup plus de commandes Git utiles, mais les commandes ci-haut sont celles que vous utiliserez le plus souvent*
## Exercice pour se pratiquer
L'exercice consiste tout simplement à faire des modifications sur le fichier python intitulé --- et disponible sur ce répertoire GitHub en y ajoutant un 'print statement' qui affiche votre nom et prénom. N'oubliez pas d'écrire un message indiquant les modifications que vous avez réalisées! 

## :keyboard: Instructions pour l'accès au terminal

### Windows
Sur Windows, afin de travailler sur le terminal, il est plus simple d'installer Anaconda via [ce lien](https://www.anaconda.com/products/distribution#). Par la suite, aller chercher 'Anaconda Prompt (Anaconda 3)' dans la barre de recherche afin de commencer à l'utiliser!

### Mac

### Linux

## Comment naviguer entre des fichiers via le terminal

Voici les commandes les plus utilisées afin de naviguer sur le terminal pour vous mettre, par exemple, à l'endroit où vous voulez cloner un répertoire GitHub. Le terminal fonctionne selon des chemins vers vos fichiers qui peuvent s'apparenter à une adresse. Initialement le terminal ressemblera à ceci si vous êtes sur Windows:
```bash
    (base) C:\Users\votre-username>
```
Disons que vous voulez aller vers votre dossier Documents puis INF1007, vous allez utiliser la commande 'cd' qui veut dire 'change directory' afin de vous déplacer vers ce nouveau chemin:
```bash
    (base) C:\Users\votre-username> cd Documents/INF1007
```
Dont le résultat sera:
```bash
    (base) C:\Users\votre-username\Documents\INF1007>
```
Ainsi, on est bel et bien à la bonne place maintenant! Il suffit de faire votre git clone à l'endroit voulu.
Pour revenir en arrière si vous vous êtes trompés de chemin, ne paniquez pas la commande est simple, il s'agit de:
```bash
    (base) C:\Users\votre-username\Documents\INF1007>cd ..
```
Qui vous remet donc à:
```bash
    (base) C:\Users\votre-username\Documents>
```
Finalement, pour savoir à tout moment vous vous situez à quel endroit, et bien tapez 'pwd' signifiant 'print working directory' qui vous imprimera le chemin auquel vous êtes présentement. 

Voilà, le tour est joué! :sparkler:

## Ressources additionnelles
1. [Cours d'introduction sur Git et GitHub](https://emdupre.github.io/git-course/)
2. [Un autre tutoriel Git](https://www.w3schools.com/git/)
3. [Lien vers un site montrant/réglant les fautes les plus communes sur Git](https://dangitgit.com/)
4. [Stack Overflow pour répondre à vos problèmes syntaxiques et/ou algorithmiques](https://stackoverflow.com/)