###  LES METHODES  ### 
______________________ 


Le AFFICHER

la méthode afficher permet d'afficher le contenu de ses parametres a l'écran, elle ne renvoie rien (ne pas confondre afficher/renvoyer)

Le SAISIR
--

la méthode saisir permet de récupérer une entrée clavier afin d'affecter la valeur rentrée par l'utilisateur dans une variable,
saisir prend en parametre, une variable a modifié, et ne renvoi rien en sortie, elle modifie seulement la variable fourni en entrée

```
Exemple : 

. definir unEntier : entier ;
. saisir ( unEntier );
. afficher ( unEntier );    // >> affiche la valeur attribué a unEntier par la saisie

```

Le LIGNE_SUIVANTE

l'instruction ligne_suivante ne prend rien en parametre, elle permet seulement d'afficher un saut de ligne imaginaire, apres un afficher()

```
Exemple : 

. afficher ( " tada " );
. ligne_suivante ;

```
L' ALLONGER ( t , nb )

permet d'ajouter a un tableau t, nb cases a la fin du tableau

```
Exemple : 

. declarer  unTab  :  tableau_de 8 entier ; // on passe d'un tableau de longueur 8
. allonger ( unTab, 2 );                   // a une liste de longueur 10

```

Le REDIMENSIONNER ( t , nb )

Fixe la taille du tableau t à une longueur nb .
On peut soit :
- Allonger le tableau, auquel cas les nouvelles cases ne sont pas initialisées
- Tronquer (raccourcir) le tableau.

```
Exemple : 
. declarer  unTab  :  tableau_de 3 entier ; // on passe d'un tableau de longueur 3
. redimensionner ( unTab, 10 );            // a une liste de longueur 10

```

Le TAILLE ( t )

renvoie le nombre d'éléments du tableau  t ( renvoie son nombre de cases/ la longueur du tableau)

```
Exemple : 

. declarer  tabReel  :  tableau_de 10 entier ;
. afficher ( taille ( tabReel ) ); // >> 10

```

Le TOUPPER ( c )

renvoie le caractère c en majuscule (uniquement si c’est une minuscule)

Le TOLOWER ( c )

renvoie le caractère c en minuscule (uniquement si c’est une majuscule)

Le SUCC ( c )

renvoie le caractère c suivant dans l’ordre prédéfinit

Le PRED ( c )

renvoie le caractère c précédant dans l’ordre prédéfinit

```

Exemple :

. declarer caract : caractere;
. caract <- nImporteQuelCaractere;
...
. afficher (tolower (caract)); // caract en minuscule
. afficher (toupper (caract)); // caract en majuscule
. afficher (succ (caract)); // suivant de caract
. afficher (pred (caract)); // précédent de caract

```



Le MODULO ( x , y )

Retourne le reste de la division entière de y par x
/!\ l'ordre des parametres est assez étrange, on a naturellement tendance a inversé x et y
```
Exemple : 

. declarer x : entier_naturel;
. x <-10;
. declarer y : entier_naturel;
. y <- modulo (2, 10);          // y <- modulo (2, x)
. afficher (y) ; //2

```

Le RAND ( x , y )

Retourne un entier aléatoire dans l’intervalle [ x , y ]

