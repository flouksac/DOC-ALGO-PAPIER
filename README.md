# DOC-ALGO-PAPIER

Dans ce repo vous trouverez un manuel détaillé de la syntaxe strict de l'algo papier selon Mr Casali 

afin de pouvoir visualiser la syntaxe particuliere de ce langage voici une super extension pour visual studio code,
developpé par Nils Ponsard (sautax#9170) ! 
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
  .   sinon                      // sinon
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
(sauf cas contraite car elle peut aussi décrémenté), en programmation comme pseudo code, on a l'habitude de donner pour nom a notre compteur 'i', puis 'j','k'...

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
.   attauquer ;                        // ou sinon on attaque
. ffaire 
```


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

### LES  VARIABLES ### 
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

### LES  FONCTIONS ### 
______________________

La PROCEDURE

La FONCTION

Le RENVOIE

Le IN

Le IN_OUT

Le OUT


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

Le MODULO 







































































