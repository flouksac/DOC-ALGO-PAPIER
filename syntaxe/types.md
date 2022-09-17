### LES  VARIABLES ### 
______________________ 


La porté des variables

une variable déclaré dans un bloc indenté ( par exemple un bloc debut/fin, si/fsi , faire/ffaire ... ) n'existe qu'a l'interieur de ce bloc
une variable déclaré a l'interieur d'une condition n'existera plus hors de cette meme condition

Le DECLARER

Permet de déclarer une variable,
Il est important de déclarer chaque variables avant de leur attribuer des valeurs
Le mot DECLARER est toujour suivis par un le nom d'une variable, puis ':' et enfin un type primitif

```
Exemple : 

voir ci-dessous :
```

Le <-

Le symbole <- permet d'affecter une valeur a une variable, attention a affecté une valeur du même type que la variable initial

```
Exemple : 

voir ci-dessous :
```

Le CARACTERE

Type primitif concernant tout type de caractère unique, il est toujours entre guillemets simple (simple quote) 
Les lettres, les chiffres, les caractères spéciaux tel que \n sont du type primitif 

```
Exemple : 

. declarer unCaractere : caractere ; // déclaration d'une variable de type caractere 
. unCaractere <- 'e' ;              // on assigne la valeur 'e' dans la variable

```

Le TABLEAU_DE

Type primitif fonctionnant de la meme maniere qu'une liste, 
c'est a dire qu'un tableau peut contenir une suite de valeur, d'un meme type prédéfinis lors de sa déclaration, 
on accede aux elements d'un tableau grace a son indice, les élements d'un tableau sont compris entre 0 et n-1 (avec n qui correspond a la longueur du tableau)
il est important de spécifier la taille du tableau lors de sa création ( avec le mot DECLARER )
Un tableau ne contient que des élements d'un seul type. 

```
Exemple : 

. declarer  tableauEntier  :  tableau_de 3 entier ; // création d'un tableau de longueur 3, contenant exclusivement des entiers
. tableauEntier[0]  <- 6  ;                        // on assigne a l'emplacement 1 du tableau la valeur 6
. tableauEntier[1]  <- 6  ;                       //
. tableauEntier[2]  <- 6  ;                      //
. afficher ( tableauEntier ) ;                  // envoie a l'écran [6,6,6]
```
Le STRING 

Type primitif similaire au tableau, il est la concaténation de plusieurs caractères, 
un STRING peut donc être une phrase,
Un mot ou encore une suite de lettres et de chiffres. 
Sa valeur s'ecrit entre double guillemets (double quotes)
on peut acceder aux élément d'un string de la meme maniere qu'on accederai aux element d'une liste (TABLEAU_DE)

```
Exemple : 

. declarer uneChaine : string ; // déclaration d'une variable de type chaine de caracteres
. uneChaine <- "un mot" ;      // on assigne la valeur 'e' dans la variable

```

Le TABLEAU_DE CARACTERE

  le tableau_de caractere est appellé STRING, voir reference ci-dessus

Le BOOLEEN
  
  Le booleen est un type primitif, qui a seulement deux états; VRAI ou FAUX , il est souvent utilisé pour verifier et tester des égalités lors de conditions
  un booleen peut se trouver seul dans une condition, on rentrera donc dans le bloc conditionnel lorsque le booleen est dans l'état VRAI
  Il est possible d'inverser un booleen avec l'instruction NON ( booleen )
  
```
Exemple : 

. declarer toBe : booleen ;
. declarer notToBe : booleen ;
. declarer question : booleen ;
. toBe <- faux ;                  // on donne comme a toBe l'état faux
. notToBe <- NON toBe ;          // vrai
. question <- toBe OU notToBe ; // toujours vrai !

```

L' ENTIER
  
  le type primitif entier désigne tout les entier positif et negatif, il ne possede pas de partie décimale
  
```
Exemple : 

. declarer unEntier : entier ;
. unEntier <- -5 ;

```

L' ENTIER_NATUREL 

  similaire a l'ENTIER mais strictement positif

```
Exemple : 

. declarer unEntierNaturel : entier_naturel ;
. unEntierNaturel <-  5 ;

```

Le REEL

  Un nombre positif ou négatif, pouvant contenir une partie décimale

```
Exemple : 

. declarer unReel : reel ;
. unReel <- 5.61 ;

```

La KONSTANTE
  
  une constante est de n'importe quel type primitif mais possede la propriété de ne jamais changer,
  de son initiation a la fin de l'algorithme la valeur attribué a la constante restera toujours la meme.
  On rajoutera la lettre K devant le nom de la variable afin de pouvoir les idenditifiés plus facilement.

```
Exemple : 

. declarer KapproximationPi : constante  reel <- 3.14 ;     //on notera qu'on ne peut plus changer KapproximationPi apres cela

```

