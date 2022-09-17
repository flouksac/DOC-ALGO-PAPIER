### LES OPERATEURS ### 
______________________

Le VRAI
  
  Un des deux états possiblent pour un booléen, VRAI étant l'état d'une condition positive

Le FAUX

  Un des deux états possiblent pour un booléen, FAUX étant l'état lorsqu'une condition est négative/fausse


```
Exemple : 

. si ( vrai )          // si (vrai) n'est pas reelement utile ici, mais une variable de 
.   do_something... ; // type booleen pourrait remplacer, vrai, et selon son état
. fsi                // on rentrerai dans la condition et executerai le do_something ou non

Exemple : 

. si ( faux )               // on ne rentrera jamais dans le si a cause du faux 
.   do_something... ;      // on ne fait donc pas ca, et on passe directement au sinon
. sinon
.   do_something_else... ;
. fsi

```

Le VAUT

  Opérateur permettant de verifier si deux valeurs valent la meme chose, compairason d'égalité.

Le NE_VAUT_PAS
  
  Opérateur permettant de verifier l'inégalité, est le contraire du VAUT.

```
Exemple : 

. si ( monEntier vaut 1 ) 
.     afficher ("monEntier vaudrait vraiment 1 !")
.   sinon_si ( monEntier ne_vaut_pas 2 )
.     afficher ("monEntier ne vaudrait donc pas 2 !")
.   sinon 
.     afficher ("monEntier vaudrait donc 2 !")
. fsi

```

Le <

  Opérateur comparatif, signifie plus petit que, le symbole < est encadré par deux valeurs

Le >

  Opérateur comparatif, signifie plus grand que, le symbole > est encadré par deux valeurs

```
Exemple :

. si ( 1 > 2 )                // si 1 est supérieur a 2 (faux)
.     do_something ;         // on fait quelque chose
.   sinon_si (2 < 3) :      // sinon si 2 est inferieur a 3 (vrai)
.     do_something_esle;   // on fait autre chose
. fsi
```

Le <=

   Opérateur comparatif, signifie plus petit ou égal a, le symbole <= est encadré par deux valeurs

Le >=

  Opérateur comparatif, signifie plus grand ou égal a, le symbole > est encadré par deux valeurs

```
Exemple :

. si ( 8 >= 9-3 )            // si 8 est superieur ou égal a 9-3 (vrai)
.     do_something ;        // on fait quelque chose
.   sinon_si (7 <= 120) :  // sinon si 7 est inferieur ou égal a 120 (vrai, mais on n'y rentre pas)
.     do_something_esle;  // on fait autre chose
. fsi
```
