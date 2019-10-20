# Contributions à ce repository

Pour rajouter ou modifier des tutoriels, vous devez utiliser github.
Voici toutes les étapes permettant votre contribution à ce repository.

Vous avez besoin d'un compte Gihub.

## Forkez ce repository

Il suffit de cliquer sur le bouton de ``fork`` en haut de la page.
Cela va créer une copie du répertoire sur votre compte.

## Clonez ce répertoire

Maintenant, clonez ce répertoire sur votre ordinateur. 
Cliquez sur le bouton ``clone``. Selectionez ``SSH`` ou ``HTTPS``.
Puis cliquez sur l'icone *copier dans le presse-papier*.

Ouvrez une invite de commande et exécutez les commandes git suivantes :

```
git clone "l'url que vous venez de copier"
```
où "l'url que vous venez de copier" (sans les guillemets) est l'url du repository. 


## Créez votre branche

Déplacez-vous dans le repository cloné (si vous n'y êtes pas encore) :

```
cd Epituto
```
Maintenant vous pouvez créer une branche avec le commande `git checkout` :
```
git checkout -b <nom-de-votre-branche>
```
Le nom de votre branche doit avoir un rapport avec ce que vous voulez apporter.


## Effectuez vos modifications

Faites vos modifications: ajoutez, mettez à jour des fichiers.

Faites des commits de temps en temps pour sauvegarder vos modifications :

```
git commit -m "message-de-votre-commit"
```

## Pushez (Poussez) vos modifications vers GitHub

Poussez vos modifications avec la commande `git push` :
```
git push origin <nom-de-votre-branche>
```
en remplaçant ``<nom-de-votre-branche>`` avec le nom de la branche précédemment créée.

## Soumettez vos changements via une Pull Request

Si vous visitez votre répertoire sur Github, vous verrez un bouton  `Compare & pull request`.  Cliquez sur ce bouton.

Mettez un titre explicite, décrivez ce que vous avez fait.

Un modérateur fusionnera vos modifications avec la branche master de ce projet si elles sont acceptés.


## Gardez votre repository synchronisé après la fusion de vos modifications

Si vous souhaitez recontribuer à Epituto dans le futur, vous devez suivre les étapes suivantes afin de synchroniser votre repository
avec celui-ci.

D'abord, basculez sur la branche master
 ```
 git checkout master
 ```

Et ajouter l'url de ce repository comme  `upstream remote url` :
```
git remote add upstream https://github.com/NicolasWent/Epituto.git
```
Ceci est une manière de dire à git qu'une autre version de ce repository existe à l'adresse spécifiée et que nous l'appelons  `upstream`.

Pour récupérer les modifications : 
```
git pull upstream master
```

Ensuite vous pourrez appliquer les modfications sur votre repository Github : 
```
git push origin master
```

## Authors
* cedric.farinazzo / 2022
