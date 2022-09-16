# DOC-ALGO-PAPIER #

Dans ce repo vous trouverez un manuel détaillé de la syntaxe strict de l'algo papier selon Mr Casali 

afin de pouvoir visualiser la syntaxe particuliere de ce langage voici une super extension pour visual studio code,
developpé par Nils Ponsard ! 
https://github.com/NilsPonsard/algo-papier-iut-aix

______________________ 

### ALGO ? hein ?? ### 
______________________

une algorithme est une séquence d'opérations visant à la résolution d'un problème en un temps fini ( mentionner la condition d'arret )
______________________ 

###  LA  SYNTAXE  ### 
______________________

La sensibilité a la casse 

La sensibilité à la casse (traduction de l'anglais case sensitivity) est une notion informatique signifiant que dans un contexte donné, le sens d'une chaîne de caractères (par exemple un mot, un nom de variable, un nom de fichier)

```
Exemple,
la variable UneVar ne sera pas la meme que la variable uNeVaR 
```

Le camelCase
  
  convention de nommage des variables,
  la regle étant de rajouter une majuscule a chaque nouveau mot dans la variable, (le premier mot commençant par une minuscule)
  par exemple : uneVariableAvecUnNomVraimentBeaucoupTropLongPourPasGrandChoseAuFinal 
  
  PS : Mr Casali preferes le camelCase
  
Le snake_case
  
  convention de nommage des variables,
  la regle étant de mettre un underscore/tiret du bas ( _ ) entre chaque mots composant une variable
  par exemple : une_variable_en_snake_case_c_est_plus_aeree_ahah

Le // 

  le // permet de commenter son algo ( et accessoirement son code )
  il est crucial de commenter son code, afin de concerver une certaine lisibilité et pour pouvoir maintenir a jour son code ( quand on y revient apres un bon moment )

LE ; 

  le ; ou semicolon en anglais est un terminateur, il indique la fin d'une instruction. Il équivaut à un point qui termine une phrase.
  ici le ; permet de séparé les actions unique, il se met a la fin d'une sequence d'action
  
  ```
  Exemple :
  
  . debut
  .   une_action ;
  .   une_autre_action ;
  . fin

  ```
  
L'indentation

  Dans certains langages de programmation (Haskell, Python…), l'indentation a un sens spécifique (p.ex. la délimitation des blocs, 
  rôle tenu par les accolades comme en C, ou en Java par exemple ), 
  alors que dans les autres elle est ignorée et n'a d'utilité que pour les programmeurs humains afin d'apporté plus de lisibilité.
  Ici en Algo, elle nous permettra de mieux structurer et de rendre plus lisibile notre pseudo-code/
  
______________________ 

###  LA STRUCTURE  ### 
______________________

L' ALGORITHME

  premier mot qui devrait apparaitre, permet de donner un nom à l'algorithme 
 
Le DEBUT

  le second mot qui devrait apparaitre, permet de marquer le début de l'algorithme
   
Le FIN

  le dernier mot qui devrait apparaitre, permet de marquer la fin de l'algorithme
 
  ```
  Exemple :
  
  . algorithme afficherBonjour  // toujours la premiere ligne , nom de l'algorithme
  . debut                      // toujours la seconde ligne  , debut de l'algo
  .     do_something... ;     //
  . fin                      // toujours la derniere ligne , fin de l'algo 
  ```
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
  
  ```
  Exemple :
  
  . si ( conditionVrai )     // si la condition est vrai nous
  .     do_something... ;   // faisons quelque chose
  . fsi                    // fin de la condition
  ```
    
Le SINON

  Permet une alternative à la condition SI,
  Le sinon est toujours précédé par une condition SI, 
  
  ```
  Exemple :
  
  . si ( conditionVrai )           // si la condition est vrai nous
  .     do_something... ;         // faisons quelque chose
  . sinon                        // sinon
  .     do_something_else... ;  // on fait quelque chose d'autre
  . fsi                        // fin de la condition
  ```
  
Le SINON_SI

  Permet une alternative a la condition SI, en rajoutant sa propre condition
  de la meme maniere qu'un SI
  
  ```
  Exemple :
  
  . si ( conditionVrai )           // si la condition est vrai nous
  .     do_something... ;         // faisons quelque chose
  .   sinon_si ( condition2Vrai) // sinon si la seconde condition est vrai
  .     do_something_else... ;  // on fait quelque chose d'autre
  . fsi                        // fin de la condition
  ```
  
Le FSI

  Ferme le bloc conditionnel SI. il doit y avoir autant de fsi que de SI
  Le FSI est au meme niveau d'indentation que le SI qui le préccede 
  
  ``` Exemple : voir plus haut ```
  
  
Le OU

  Opérateur logique conditionnel permettant la création d'une deuxieme condition, fonctionne de la meme maniere qu'un ou logique,
  et a donc pour table de vérité ->
  
  ```
  Table de vérité 
  OU / OR
  +-------+---+
  | 0 . 0 | 0 |
  | 0 . 1 | 1 |
  | 1 . 0 | 1 |
  | 1 . 1 | 1 |
  +-------+---+
  ```
  
  ```
  Exemple:
  
  . si ( ( condition1) ou (condition2) ) // si la condition 1 ou (ou+et) la condition 2 est vrai 
  .     do_something... ;               // on fait quelque chose
  . fsi                                // fin du bloc conditionnel
  ```
  
Le OU_SINON

  Opérateur logique conditionnel ayant le meme fonctionnement logique que le OU, mais qui prend en compte l'ordre d'éxecution, et qui convient donc
  mieux dans une succession de contidition
  
  ```
  Exemple:
          //(ici on prend en compte l'ordre d'éxecution, d'abord condition1 puis sinon condition2)
  . si ( ( condition1) ou_sinon (condition2) ) // si la condition 1 ou (ou+et) la condition 2 est vrai 
  .     do_something... ;                     // on fait quelque chose
  . fsi                                      // fin du bloc conditionnel
  ```
  
Le ET

  Opérateur logique condtionnel ET, Permet d'additionner des conditions entre elle, 
  en suivant le fonctionnement du ET logique, et a donc pour table de vérité 
  
  ```
  Table de vérité 
  ET / AND
  +-------+---+
  | 0 . 0 | 0 |
  | 0 . 1 | 0 |
  | 1 . 0 | 0 |
  | 1 . 1 | 1 |
  +-------+---+
  ```

  ```
  Exemple:
      
  . si ( ( condition1) et (condition2) )    // si la condition 1 et la condition 2 est vrai 
  .     do_something... ;                  // on fait quelque chose
  . fsi                                   // fin du bloc conditionnel
  ```


Le ET_ALORS
   
  Opérateur logique condtionnel ET, Permet d'additionner des conditions entre elle tout comme le ET 
  mais qui prend en compte l'ordre d'éxecution, et qui convient donc 
  mieux dans une succession de contidition

  ```
  Exemple:
          //(ici on prend en compte l'ordre d'éxecution, d'abord condition1 et ensuite condition2)
  . si ( ( condition1) et (condition2) )      // si la condition 1 et la condition 2 est vrai 
  .     do_something... ;                    // on fait quelque chose
  . fsi                                     // fin du bloc conditionnel
  ```

Le NON
  
  Opérateur logique conditionnel permettant d'exprimer la negation / l'inverse d'une condition succedant le NON
  
  ```
  Exemple:
  . si ( NON ( condition1 ) )      // si la condition n'est pas vrai
  .     do_something ... ;        // on fait quelque chose
  . fsi                          // fin du bloc conditionnel
  ```
Le CHOIX_SUR x ENTRE

  switch permettant de comparer une variable directement avec different CAS definit a la suite du CHOIX_SUR d_une_variable ENTRE
  similaire a une succession de si, sinon_si dans le but de comparé une seule variable

Le CAS valeur :

  permet de definir un CAS a comparé avec une variable 

Le AUTRE :
  
  permet de definir le CAS execption

Le FCHOIX
  
  ferme le switch CHOIX_SUR, et possede la meme indentation que le CHOIX_SUR qu'il complete
  
  ```
  Exemple : 
  
  . choix_sur une_variable entre
  .   cas reponse1 :
  .     do_something... ;
  .   cas reponse2 :
  .     do_something_else... ;
  .   autre :
  .     do_something_else2... ;
  . fchoix
  ```
PS : les CAS se termine par un : et le CHOIX_SUR precede le mot ENTRE
  
______________________

###  LES  BOUCLES  ### 
______________________ 

La BOUCLE
 
permet l'initiation d'une boucle infinit, ce qui sera contenu entre la BOUCLE et le FBOUCLE sera exécuté a l'infini, 
si il n'y pas de condition d'arret utilisant l'instruction SORTIE

La FBOUCLE

ferme la zone de la boucle, et s'indente au meme niveau, similaire au FSI qui ferme le bloc conditionnel du SI, mais dans le cas de la BOUCLE

```
Exemple :

voici une premiere boucle sans condition d'arret,

. boucle                   //repetition de l'instruction do_something, et do_something_else a l'infini
.   do_something... ;
.   do_something_else... ;
. fboulce

et une deuxieme avec une condition d'arret,

. boucle                        // pourrait se traduire par
.  si (bordDeFalaise) sortie ; // si nous sommes au bord de la falaise, 
.  avancerDUnPas;             // quitter la boucle qui nous fait avancer
. fboucle

```

Le REPETER
  
  permet de rentrer dans une boucle ou nous allons REPETER une suite d'instruction JUSQUA atteindre une condition d'arret/de sortie
  
Le JUSQUA

  exprime la condition de sortie lorsqu'une condition est vrai,
  lorsque le jusqua n'est pas précédé par le mot REPETER il faut délimiter le bloc de la boucle par les instructions FAIRE et FFAIRE

```
Exemple : 

. repeter                             // ici on va repeter l'action commenter_code
.   je_commente_toujours_mon_code ;  // jusqu'a atteindre la condition (mort) -> qui deviendrait vrai (rip...)
. jusqua ( ce_que_mort_s_en_suive ) // et lorsqu'on l'atteint on quitte la boucle

Un autre exemple avec la condition d'arret en premiere ligne ( sans le bloc répéter, dans le cas
ou on aurait besoin de verifier que la condition ne soit pas vrai ) ( au cas ou )

. jusqua ( atteindreLeBut ) //jusqu'a ce qu'on atteigne notre but ( en partant du principe qu'il n'est pas atteint
. faire                    // on fait
.   do_something... ;     // quelque chose (sensé nous rapprocher du but)
. ffaire                 // fin du bloc boucle jusqua (mais ne veut pas dire qu'a la fin de do_something on va necessairement quitté la boucle)
                        // c'est le role de la condition jusqua de nous faire sortir de la boucle

```

Le FAIRE

  permet de délimiter le début d'un bloc de boucle avec TANT_QUE ou JUSQUA (voir exemple plus haut)

Le FFAIRE

  permet de terminer un bloc de boucle

Le TANT_QUE

  boucle tant_que, qui va continuer son execution tant que la condition est vrai, (on remarque d'ailleur qu'elle est l'inverse de la boucle jusqua)
  elle peut commencer par l'instruction REPETER et finir par TANT_QUE ou etre délimité par FAIRE et FFAIRE

```
Exemple : 

. tant_que ( J_ai_la_solution ) // tant que je peux apporter mon aide
. faire                        //
.   je_la_partage ;           // je le fait, mais quand je ne peux pas je passe la main (je sors de la boucle)
. ffaire                     //

```

Le POUR

permet de creer une boucle a compteur, elle se combine au VARIANT_DE x A y, il s'agit d'une boucle qui s'auto incrémente, 
(sauf cas contraite car elle peut aussi décrémenté, voir mot DESCENDANT), 
en programmation comme en pseudo-code, 
on a l'habitude de donner pour nom a notre compteur 'i', puis 'j','k'...

Règles : Dans une boucle pour, la variable de parcours doit prendre
toutes les valeurs entre les bornes minimale et maximale (incluses).
Aucune rupture de séquence utilisant une instruction sortie n’est
permise. 
l'usage de SORTIE, est interdite, mais celle de CONTINUE, est "légal"

Le VARIANT_DE x A y 

cette instruction permet la gestion d'un compteur au sein d'une boucle,
le compteur variant de x a y, le compteur se déclarera directement dans le variant ( initialiser a x)

```
Exemple : 

. pour ( i variant_de 1 a 100 ) // on repete l'affichage de i 
. faire                        // (le compteur qui incrémente de 1 a chaque tour) 
.   afficher ( i )            // avec i variant de 1 a 100
. ffaire

```

Le SORTIE

permet la sortie d'une boucle lors de son execution, souvent couplé a une condition, ( qu'on appelle condition de sortie )

Le CONTINUE

permet de revenir au début de la boucle ( au niveau du faire, ou du repeter ) 

```
Exemple :

. tant_que (NON victoire)                  //tant qu'on a pas gagné
. faire                                   // on repete la phase
.   prendreUnePortion ;                  // de prendre une potion, et si on a pas encore assez de vie
.   si ( Non beaucoupDeVie ) continue ; // on retourne a la ligne tant_que (Non victoire)
.   attaquer ;                        // ou sinon on attaque
. ffaire 
```

Le DESCANDANT

instruction permettant a la boucle POUR de décrémenté son indice,

```
Exemple :
. declarer tabInt : tableau_de entier;                     //génération de tabInt, 
    ...                                                   // on ommet la partie ou on remplis tabInt
. pour (i variant_de taille (tabInt) -1 a 0 descendant ) // pour i variant de la longueur du tableau -1 a 0, avec i décrémentant )
. faire                                                 // faire
.   afficher (tabInt[i]);                              // affichage du tableau a l'indice i
. ffaire                                              // fin bloc faire
```

______________________ 

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

______________________ 

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

______________________ 

###  LES METHODES  ### 
______________________ 


Le AFFICHER

la méthode afficher permet d'afficher le contenu de ses parametres a l'écran, elle ne renvoie rien (ne pas confondre afficher/renvoyer)

Le SAISIR

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


______________________

### LES  FONCTIONS ### 
______________________

La PROCEDURE

La FONCTION

Le RENVOIE

Le IN

Le IN_OUT

Le OUT

```

                   WORK IN PROGRESS...


                                  __________
                                 || .------.|
                                 ||/       [|
                                 |||      /||
                                 |||\    | [|
              _     ________ _   |||.'___| |'---...__
             /o)===|________(o\  ||========|         ``-..
            / /       _.----'\ \ |'=.====.='  ________    \
           / |     .-' ----. / | |  |____|  .'.-------.\   |
           \  \  .'_.----._ \  | _\_|____|.'.'_.----._ \\__|
     /\     \  .'.'   __   `.\ |-_| |____| /.'   __   '.\   |
    // \     \' /   /    \   \\|-_|_|____|//   /    \   \`--'
   //   \    / .|  |      |  |      |____| |  |      |  |
  //     \ .'.' |   \ __ /   |             |   \ __ /   |
 //      /'.'    '.        .'               '.        .'
//_____.'-'        `-.__.-'                   `-.__.-' 
```
