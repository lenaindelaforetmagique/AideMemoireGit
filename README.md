# Aide mémoire git
_X. Morin_

## Lancer la console Git Bash

Démarrer > Tous les programmes > Git > Git Bash

## Fonctions courantes console

    pwd :   Print Working Directory
    cd :    Change Directory
    ls :    List Segments (liste du contenu d'un répertoire)
    mkdir : Make Directory
    touch :

## Principe de fonctionnement

Git permet de faire de gérer les versions d'un projet.

## Vocabulaire
### Commit
Un commit est une sauvegarde du projet à un instant T. Chaque commit est identifié par :
    * une clef _SHA_ (Secure Hash Algorithm) qui permet d'identifier de manière unique un commit
    * un auteur
    * une date
    * un message de description

### Index

### commit

SHA : clef d'identification d'un commit

## Lignes de commandes courantes
https://git-scm.com/docs

### Paramétrage
    git config --global user.name "Nom/Pseudo"
    git config --global user.email "email"

### Commandes générales sur un repository
    git init :                  activer le répertoire courant
    git clone _lienGitHub_ :    copie dans le répertoire courant le repository pointé par le _lienGitHub_

    git log :                   affiche l'historique des commits du répertoire
    git status :                affiche le statut du répertoire courant

    git add _filename_ :        ajoute le fichier à l'index
    git add . :                 ajoute TOUS les fichiers du répertoire à l'index
    git commit :                commit de l'index
    git commit -m "message" :   commit de l'index + message (très fortement recommandé)
    git commit -a :             commit de tous les fichiers modifiés qui existent déjà dans l'index (add + commit)

    git checkout _SHA_ :        rend courrant le commit identifié par _SHA_
    git checkout master :       rend courant le dernier commit de la branche principale
    git revert _SHA_ :          crée un nouveau commit annulant le dernier commit
    git reset --hard :          annuler tous les changements effectués depuis le dernier commit


    git push origin master :    envoie le commit sur le remote origin dans la branche master
    git pull origin master :    récupère le dernier commit présent