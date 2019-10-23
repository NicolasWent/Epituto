# Tutoriel raccoursis clavier pour Vim

## Introduction

Le but de ce tutoriel est de vous apprendre les bases pour que vous puissiez
faire vos propres raccoursis clavier avec vim.

Par exemple pour ma part, j'ai fait un raccoursis clavier pour sauvegarder et
sauvegarder quitter en cliquand respectivement sur <F2> et <F1> et ces
raccoursis fonctionnent même en mode insertion. Je vous apprendrais comment
faire ça dans ce tutoriel.

N'hésitez pas à le compléter ou faire un autre tuturiel si vous connaisser
d'autres raccoursis utiles.

## Exemple détailler de la création d'un raccoursi clavier

Alors déjà avant de faire un raccoursis clavier, il faut savoir ce que nous
souhaitons faire.

Par exemple pour sauvegarder lorsque nous sommes en mode insertion, nous
cliquont sur les touches <ESC> puis nous tapons ':w' puis <entre> puis nous
recliquon sur i pour se remettre en mode insertion.

Ce qui est asser long en soit.

Du coup pour ajouter le raccoursis clavier permettant de faire ça il faut se
rendre dans son .vimrc qui se trouve dans : ~/.vimrc.

Pour y acceder vous pouvez soit faire `cd` puis `vim .vimrc`. Ou directement
`vim ~/.vimrc`.

Une fois dans le .vimrc qui est le fichier qui gère toutes les configs de vim,
il vous suffit d'ajouter la lignes suivante :

`imap <F2> <ESC>:w<CR>i`

Sauvegarder puis ensuite ouvrer n'importe quelle fichier avec vim (pas un
fichier binaire hein -\_-). Puis écriver un truc et cliquer sur la touche <F2>
et vous aurrez l'impression que rien ne c'est passer, mais sa a sauvegarder ce
que vous avez modifier.

Alors décortiquons la ligne du dessus.

* `imap` : permet de définir un raccoursi lorsqu'on est en mode insertion

`Mais si on peut définir un raccoursi en mode insertion comment on défini un
raccoursi lorsqu'on est en dehord du mode insertion ?`

-> Je vais aborder ce point plus tard, laisser-moi finir les explications sur la
ligne svp.

* `<F2>` : c'est la touche que nous utilisons pour lancer le 'map'.

* `<ESC>:w<CR>i` : est la combinaison de touche que nous exécutons après avoir
cliquer sur la touche du map. Elle est séparer d'un espace de la définition de
la touche.

Les caractères un peut bizares sont : `<ESC>` qui veux dire tout simplement
"clique sur la touche echap". Et `<CR>` qui veux dire "Clique sur la touche
entré".

Ainsi lorque nous cliquons sur la touche `<F2>`. Cela exécute la séquence de
touche défini en brut.

## Quels autres type de raccoursis existent ?

Dans ce tutoriel je vais également aborder, en plus de imap, les deux suivants :
`nmap` et `map`. Il en existe beaucoup d'autres, je vous laisse voir ce
[lien](https://vim.fandom.com/wiki/Mapping_keys_in_Vim_-_Tutorial_(Part_1)) si
vous souhaitez plus d'informations.

* `nmap` : map pour le mode normal. C'est à dire lorsque vous ouvrez vim vous
ètes en mode normal ou que vous ètes en mode insertion puis cliquer sur `Echap`
vous revenez au mode normal.

* `map` : map pour tous les modes.

Il n'y a pas que les modes insert et normal dans vim, ce sont juste eux que nous
utilisons principalement. Il y a également le mode `(insert) VISUAL` et ainsi
que les modes ~~bizares~~ dont nous sortons en spammant la touche `Echap`.

`map` fonctionne pour TOUS les modes.

## Mes raccoursis de sauvegarde

```
nmap <F2> :w<CR>
imap <F2> <ESC>:w<CR>i<right>

map <F1> :wq<CR>
imap <F1> <ESC>:wq<CR>
```

* Vous pouvez remarquer que pour le map de <F2> (pour sauvegarder sans quitter)
est défini dans le mode insert et mode normal.

C'est normal, j'ai fait ça afin de différencier lorsque je suis en mode insert
et en mode normal afin que lorsque je suis en mode insert alors apres avoir
cliquer sur <F2>, je reste en mode insert. Et même chose pour le mode normal.

C'est pour sa qu'il est conseiller de définir les 2 séparément.

* Vous pouvez également remarquer que j'ai ajouter un `<right>` à la fin du
imap, c'est afin que je puisse revenir à l'endroit où j'était avant de cliquer
sur `<F2>`, le meilleur moyen de comprendre ce que je veux dire, c'est d'essayer
avec et sans le 'right', vous verrez la différence si vous spammer <F2> sans et
si vous le faite avec (lorsque vous ètes en bout de ligne).

* `Pourquoi tu map <F1> deux fois, genre avec map et imap, map ne définit-il pas
déjà dans tous les modes ?`

-> Très bonne question, c'est le cas. Du coup essayer de voir ce qu'il se passe
lorsque vous commenter (en ajoutant le charactere " devant la ligne) la ligne
`imap <F1> <ESC>:wq<CR>` et cliquer sur <F1> en mode insert.

Vous allez remarquer que la fenêtre du tutoriel s'ouvre. Ainsi pour éviter que
cette fenêtre s'ouvre et que sa face bien le ':wq' (sauvegarder et quitter), on
doit ajouter explicitement le imap sur cette touche.

## Conclusion

* `nmap <TOUCHE> une_suite_de_touche` : permet d'ajouter un raccoursi clavier à
la touche <TOUCHE> lorsqu'on est en mode normal.

* `imap <TOUCHE> une_suite_de_touche` : permet d'ajouter un raccoursi clavier en
mode insert.

* `map <TOUCHE> une_suite_de_touche` : permet d'ajouter un raccoursi clavier
dans TOUS les modes.

* Il est conseiler de crée le même raccoursi 2 fois (en mode nmap et en mode
imap) afin de différencier le comportement lorsqu'on est en insert mode et en
normal mode.

#### Authors
* nicolas.went / 2022 / nicolas.went@epita.fr / Lockface77#8305 / délegué GRB1

