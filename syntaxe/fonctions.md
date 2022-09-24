[Retour au sommaire](../README.md)

### LES SOUS-PROGRAMMES ### 
______________________

La PROCEDURE

permet d'exécuté une séquence d'instruction lors de son appel,  

une procédure a toujours un identificateur ( son nom ), des conditions d'utilisation propre à elle-même, 
Éventuellement des paramètres ( des sortes d'ingrédients ont lui fourni en amont, avec lequel elle va travailler )
on pourrait interpréter la liste de ses paramètres comme un "guichet" de communication entre le monde extérieur et l'intérieur du sous-programme (porté des variables)

elle produit éventuellement un résultat

elle sert à "mettre en facteurs" du code, c'est-à-dire permettre d'écrire une seule fois une séquence d'instructions souvent utilisée.
cette séquence d'instructions s'exécutera quand la procédure sera appelée,

```
Exemple :

. procedure afficherNFoisBonjour 
.                     ( n : in entier_naturel )
.                     //n (l'indicateur du parametre)
.                     //in (marqueur : parametre "donnée")
.                     //entier_naturel (type)
. debut
.     pour (i variant_de 1 a n )
.     faire
.         afficher ("Bonjour");
.     ffaire
. fin

```

```

. declarer nbFois : entier_naturel;
. nbFois <- 12;
. afficherNFoisBonjour (nbFois);

```

la procédure permet de remplacer une suite d'actions élémentaire par une seule action de "haut niveau"

par exemple :
```
-afficher l'écran d'accueil
-établir une connexion
-saisir login/password
-charger les images
-interroger une base de données
```

La FONCTION

une fonction est une procédure qui a au moins un paramètre out, 
la fonction correspondante renvoie alors ce paramètre out

```
Exemple : un sous-programme qui
          reçoit un nombre réel,
          calcule sa racine carrée

en procédure :

. procedure sqrt (valInit : in reel, 
.                 result : out reel);
                
en fonction :

. fonction sqrt (valInit : in reel) 
.                renvoie reel;

Exemple d'utilisation : 

. declarer Rac_12 : reel;
. Rac_12 <- sqrt (12.0);
```

Le prédicat est une fonction qui renvoie un booleen,
(on choisit un identificateur qui commence par "is"/"has"/"are" (pour est, a, sont) )

```
Exemple :

. fonction isMultiple (entier1 : in entier,
.                      entier2 : in entier)
.                      renvoie booleen
. debut
.     si (modulo (entier1, entier2) vaut 0)
.         renvoie vrai;
.     sinon
.         renvoie faux;
.     fsi
. fin


```

Le RENVOIE

  permet de renvoyer une valeur depuis une fonction 

Le IN

  Marqueur dans une procedure/fonction signifiant que l'argument désigné (par ce même marqueur) ne subira pas de modification dans le sous-programme

Le IN_OUT

  Marqueur dans une procedure/fonction signifiant que l'argument désigné (par ce même marqueur) pourrait subir une modification dans le sous-programme

Le OUT

  Marqueur dans une procedure/fonction signifiant que l'argument désigné (par ce même marqueur) subira une modification obligatoire dans le sous-programme

