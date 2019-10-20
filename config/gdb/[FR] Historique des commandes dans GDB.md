# Historique des commandes dans GDB

## Introduction

Par défaut, l'historique des commandes est désactivée. 
On peut l'activer grâce au fichier de configuration de GDB : ``.gdbinit``.

Ce tutoriel vous montre comment réaliser cela rapidement.

## Configuration de GDB

Il faut tous d'abord créer un fichier nommé ``.gdbinit`` dans votre home.
Au démarage, gdb chargera la configuration de ce fichier

Mettez-y à la ligne suivante dans le fichier en question : 
```
set history save on
```

Cette commande active la sauvegarde de votre historique de commande dans un fichier ``.gdb_history`` dans votre répertoire courant.
**Attention**: ce fichier est un trash file. Vous ne devez donc pas le push.

## Eviter de push votre gdb_history

Pour cela, on va configurer git. Git ignore tous les fichiers listés dans les fichiers ``.gitignore``.
Il y a 2 types de  ``.gitignore``:
* Le gitignore global : il est actif sur tous les répértoires (repersitories en anglais) de votre session (on va se servir de celui là).
* le gitignore local : il est propre à votre repository actuel.

Vous pouvez donc créer un fichier ``.gitignore`` dans votre home et y écrire la ligne suivante: 
```gitignore
.gdb_history
```

Désormais, l'historique de vos commandes dans gdb est sauvegardé et vous pourrez rappelé vos commandes précédentes ; le tout en gardant votre repository git propre.

## Liens utiles
* [Ma config GDB](https://github.com/cedricfarinazzo/gdb-config)

#### Author
* cedric.farinazzo / 2022
