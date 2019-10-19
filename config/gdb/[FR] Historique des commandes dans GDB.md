# Historique des commandes dans GDB

## Introduction

Par défaut, l'historique des commandes est désactivée. 
On peut l'activer grâce au fichier de configuration de GDB : ``.gdbinit``.

Ce tutoriel vous montre comment réaliser cela rapidement.

## Configuration de GDB

Il faut tous d'abord créer un fichier nommé ``.gdbinit`` dans votre home.
Au démarage, gdb chargera la configuration de ce fichier

Mettez y a ligne suivante dans ce fichier : 
```
set history save on
```

Cette commande active la sauvegarde de votre historique de commande dans un fichier ``.gdb_history`` dans votre répertoire courant.
**Attention**: ce fichier est un trash file. Vous ne devez pas le push

## Eviter de push votre gdb_history

Pour cela, on va configurer git. Git ignore tous les fichiers listés dans les fichiers ``.gitignore``.
Il y a 2 types de  ``.gitignore``:
* Le gitignore global : il est actif sur tous les repositories de votre session (on va utiliser celui la)
* le gitignore local : il est propre à votre repository actuel.

Vous pouvez donc créer un fichier ``.gitignore`` dans votre home et y écrire la ligne suivante: 
```gitignore
.gdb_history
```


Désormais, l'historique de vos commandes dans gdb est sauvegardé et vous pouvez rappelé vos commandes précédentes ; le tout en gardant votre 
repository git propre.

## Liens utiles
* [Ma config GDB](https://github.com/cedricfarinazzo/gdb-config)

#### Authors
* cedric.farinazzo / 2022
