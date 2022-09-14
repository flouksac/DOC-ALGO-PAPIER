# DOC-ALGO-PAPIER

Dans ce repo vous trouverez un manuel détaillé de la synthaxe strict de l'algo papier selon Mr Casali 

afin de pouvoir visualiser la synthaxe particuliere de se langage voici une super extension ! 
https://marketplace.visualstudio.com/items?itemName=nilsponsard.algo-papier-iut-aix&ssr=false#review-details 

______________________ 

### ALGO ? hein ?? ### 
______________________

  Séquence d'opérations visant à la résolution d'un probl-me en un temps fini ( mentionner la condition d'arret )
______________________ 

###  LA  SYNTHAXE  ### 
______________________

La sensibilité a la casse
  


Le CamelCase

Le snake_case

Le // 

LE ;

L'indentation



______________________ 

###  LA STRUCTURE  ### 
______________________

L' ALGORITHME
  premier mot qui devrait apparaitre, permet de donner un nom à l'algorithme 
 
Le DEBUT
  le second mot qui devrait apparaitre, permet de marquer le début de l'algorithme
   
Le FIN
  le dernier mot qui devrait apparaitre, permet de marquer la fin de l'algorithme

Exemple : 

  . algorithme afficherBonjour // toujours la premiere ligne , nom de l'algorithme
  
  . debut                      // toujours la seconde ligne  , debut de l'algo
  
  .     do_something... ;     
  
  . fin                        // toujours la derniere ligne , fin de l'algo 

PS : ces 3 mots n'apparaissent qu'une seule fois par algorithme

______________________ 

### LES CONDITIONS ### 
______________________ 

Le SI

  l'opérateur conditionnel SI permet d'exprimer la condition, 
  il contient une condition entre parantheses , 
  la condition est soit vrai, soit fausse,
  il n'exite pas d'autre état, l'operateur SI est suivi d'instructions et peut etre succédé par d'autres conditions 
  lorsque nous quittons le bloc conditionnel le mot FSI ferme le test
  
  exemple :
  . si ( conditionVrai )    // si la condition est vrai nous
  .     do_something... ;   // faisons quelque chose
  . fsi                     // fin de la condition
  
    
Le SINON

  Permet une alternative à la condition SI,
  Le sinon est toujours précédé par une condition SI, 
  
  exemple :
  
  . si ( conditionVrai )        // si la condition est vrai nous
  .     do_something... ;       // faisons quelque chose
  . sinon                       // sinon
  .     do_something_else... ;  // on fait quelque chose d'autre
  . fsi                         // fin de la condition
  
  
Le SINON_SI

  Permet une alternative a la condition SI, en rajoutant sa propre condition
  de la meme maniere qu'un si
  
  exemple :
  
  . si ( conditionVrai )         // si la condition est vrai nous
  .     do_something... ;        // faisons quelque chose
  . sinon_si ( condition2Vrai)   // sinon si la seconde condition est vrai
  .     do_something_else... ;   // on fait quelque chose d'autre
  . fsi                          // fin de la condition
  
Le FSI
  Ferme le bloc conditionnel SI. il doit y avoir autant de fsi que de SI
  Le FSI est au meme niveau d'indentation que le SI qui le préccede 
  
  exemple : voir plus haut 
  
  
Le OU

Le OU_SINON

Le ET

Le ET_ALORS

Le NON

______________________

###  LES  BOUCLES  ### 
______________________ 

Le TANT_QUE

Le POUR

Le JUSQUA

Le REPETER

Le SORTIE

Le CONTINUE

Le BOUCLE

Le FBOUCLE

______________________

### LES  FONCTIONS ### 
______________________

La PROCEDURE

La FONCTION

Le RENVOIE

______________________ 

### LES OPERATEURS ### 
______________________

Le VRAI

Le FAUX

Le VAUT

Le NE_VAUT_PAS

Le <

Le >

Le <=

Le >=

______________________ 

###  LES   TYPES   ### 
______________________ 

Le DECLARER

Le <-

Le CARACTERE

Le STRING 

Le TABLEAU_DE

Le TABLEAU_DE CARACTERE

Le BOOLEEN

L' ENTIER

L' ENTIER_NATUREL

Le REEL

La KONSTANTE

______________________ 

###  LES METHODES  ### 
______________________ 


Le AFFICHER

Le SAISIR

Le LIGNE_SUIVANTE

Le TAILLE

Le TOUPPER

Le TOLOWER

Le SUCC

Le PRED

L' ALLONGER

Le REDIMENSIONNER





Le FAIRE

Le FFAIRE

Le IN

Le IN_OUT

Le OUT





































































