# Epituto présentation

### The english part is written bellow

## Introduction

Bonjour, l'objectif de ce repo git est de permettre aux élèves d'écrire des tutoriels pour d'autres élèves d'Epita afin que ceux qui ont du mal avec l'interface proposer à Epita (Arch linux, i3 et afs) puissent trouver quelques petits tutoriaux afin de les aidez.

Vous trouverez sur ce depo :
* Des guides sur comment configurer votre session Epita (fond d'écrant, configurations de bases et avancer).
* Des tutoriels écrit par des élèves sur les languages de programmations vu a épita

## Comment écrire un tutoriel

Ce dépo git vas fonctionner avec des commits. Ces commits seront ensuite valider par une équipe de modérateurs.

Pour que votre tutoriel soit valide il faut respecter quelques règles afin d'éviter les problèmes :
* Ne pas faire de confloose (ou de tutoriaux sur les confloose), ce git doit rester propre afin que les personnes ne s'y connaissant pas bien ne risquent pas de tomber sur un truc qui va au final casser leur architecture.
* Lorsque dans vos tutoriaux il est nécéssaire de faire un curl (pour installer un programme ou autre), la source du lien vers votre curl doit être vérifier et viable (pas de site yolo.com ou autre).
* Si vous réaliser un script d'automatisation d'installation, ne mettez pas un lien de "curl" vers ce script mais mettez le dans le dossier scripts de ce depo.
* Vous devez signer votre tutoriel voir :
* Si vous souhaitez contribuer à un tutoriel voir :


### Signer son tutoriel :

Lorsque vous écrivez un tutoriel, celui-ci doit être signer avec un header author suivi d'au minimum votre login et vous devez préciser l'année de votre promo, voici un exemple de signature :

#### Authors
* nicolas.went / 2022

Pour reproduire le format ci-dessus, il vous suffit de mettre 4 \# devant "Authors" puis ensuite de mettre une étoile '\*' devant votre login.

Je vous invite également à lire la page suivante : [Markdown](https://guides.github.com/features/mastering-markdown/), sur cette page vous trouverez des bonnes astuces pour écrire un beau tutoriel.

Vous pouvez également, si vous le souhaitez ajouter des informations à votre signature en précisant par exemple votre adresse e-mail ainsi que votre psuedo discord, ce qui donnerais :

#### Authors
* nicolas.went / 2022 / nicolas.went@epita.fr 

## Comment contribuer à un tutoriel

Vous pouvez contribuer aux tutoriaux des autres notament en corrigeant les fautes d'orthographes, ou encore en faisant une traduction en anglais du tutoriel voir encore ajouter des précisions.

Pour ce faire, vous pouvez modifier directement le fichier sur github en aillant un compte. Il vous suffit de directement modifier le fichier et ensuite de proposer un commit, dans ce commit vous devez écrire en quoi vos modifications sont judicieuse. Ensuite ce commit devra être valider par l'équipe de modérateurs avant d'être mis en ligne.

Git étant un outil qui nous permet de faire du "versionning", si un commit ne plait pas à l'auteur du post ou casse tout, on peut toujours revenir en arrière.

Après avoir contribuer au tutoriel de quelqu'un, vous pouvez vous ajouter dans la liste des Contributeurs. Cette liste est juste en dessous des autheurs, à la fin du fichier. Cette liste doit avoir le format suivant :

#### Contributors
* nicolas.went / 2022

La signature doit avoir le même format que pour les autheurs.
