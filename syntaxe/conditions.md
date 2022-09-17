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

  Opérateur logique conditionnel permettant la création d'une deuxieme condition alternative a la premiere, 
  fonctionne de la meme maniere qu'un ou logique, et a donc pour table de vérité ->
  
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
  
  Nous nous servons du OU logique seulement pour la comparaison de booleen , préférez le OU_SINON dans les conditions (SI, SINON_SI ...)
  
  ```
  Exemple:
  
  . si ( (condition1) ou (condition2) ) // si la condition 1 ou (ou+et) la condition 2 est/sont vrai (si sont, en meme temps) 
  .     do_something... ;               // on fait quelque chose
  . fsi                                // fin du bloc conditionnel
  ```
  
Le OU_SINON

  Opérateur logique conditionnel ayant le meme fonctionnement logique que le OU, mais qui prend en compte l'ordre d'éxecution, et qui convient donc
  mieux dans une succession de condition
  
  ```
  Exemple:
          //(ici on prend en compte l'ordre d'éxecution, d'abord condition1 puis sinon condition2)
  . si ( (condition1) ou_sinon (condition2) ) // si la condition 1 ou (ou+et) la condition 2 est vrai 
  .     do_something... ;                     // on fait quelque chose
  . fsi                                      // fin du bloc conditionnel
  ```
  
Le ET

  Opérateur logique condtionnel ET, Permet d'additionner des booleen entre eux, 
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
  
  Nous nous servons du ET logique seulement pour la comparaison de booleen , préférez le et_alors dans les conditions (SI, SINON_SI ...)

  ```
  Exemple:
      
  . si ( ( condition1) et (condition2) )    // si la condition 1 et la condition 2 sont vrai en meme temps
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
  . si ( ( condition1) et_alors (condition2) )      // si la condition 1 et la condition 2 est vrai 
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
  
