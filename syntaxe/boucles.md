[Retour au sommaire](../README.md)

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
