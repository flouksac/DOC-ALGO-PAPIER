[Retour au sommaire](../README.md)

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
  
  PS : Mr Casali preferes le camelCase, on utilisera d'ailleur le camel case uniquement pour les mots non syntaxique tel que les noms des variables, des procedures,
  des fonctions ...
  
Le snake_case
  
  convention de nommage des variables,
  la regle étant de mettre un underscore/tiret du bas ( _ ) entre chaque mots composant une variable
  par exemple : une_variable_en_snake_case_c_est_plus_aeree_ah_ah
  
  on se sert du snake case uniquement pour les mots syntaxique dans l'algo papier de Mr Casali ( ex: sinon_si,tant_que)

Le // 

  le // permet de commenter son algo ( et accessoirement son code )
  il est crucial de commenter son code, afin de conserver une certaine lisibilité et pour pouvoir maintenir a jour son code ( quand on y revient apres un bon moment )

LE ; 

  le ; ou semicolon en anglais est un terminateur, il indique la fin d'une instruction. Il équivaut à un point qui termine une phrase.
  ici le ; permet de séparé les actions unique, il se met a la fin d'une sequence d'action (ne se met pas a la fin d'une condition, ou d'une boucle)
  
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
  
