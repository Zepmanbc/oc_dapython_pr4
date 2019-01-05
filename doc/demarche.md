J'ai commencé par lister les différents acteurs dans l'énoncé puis imaginé des secnarios pour voir si il en existe d'autres

![0_ListActors](img/0_ListActors.png)

J'ai imaginé le processus de commande d'une pizza d'un client et en ai listé différentes actions

J'ai étoffé cette liste en imaginant les actions de chaque acteur identifié

j'ai pu faire des regroupements dans les actions et je me suis basé sur "CRUD" pour définir toutes les actions

* Commande
* Recette
* Ingrédient

![0_ListUseCases](img/0_ListUseCases.png)

A partir de la je peux faire le diagramme de contexte

![1_contextDiagram](img/1_contextDiagram.png)

Je fais ensuite le diagramme de cas d'utilisation pour chaque acteur

![2_Accueil_UseCaseDiagram](img/2_Accueil_UseCaseDiagram.png)

![2_ Banque_UserCaseDiagram](img/2_ Banque_UserCaseDiagram.png)

![2_Client_UseCaseDiagram](img/2_Client_UseCaseDiagram.png)

![2_GestionnaireStock_UseCaseDiagram](img/2_GestionnaireStock_UseCaseDiagram.png)

![2_Pizzaiolo_UseCaseDiagram](img/2_Pizzaiolo_UseCaseDiagram.png)

![2_Responsable_UseCaseDiagram](img/2_Responsable_UseCaseDiagram.png)

Puis j'ai fais des diagrames de packages

![3_Commande_PackageDiagram](img/3_Commande_PackageDiagram.png)

![3_Ingredient_PackageDiagram](img/3_Ingredient_PackageDiagram.png)

![3_Recette_PackageDiagram](img/3_Recette_PackageDiagram.png)

penser a rajouter :
* la notion de prix de pizza, 
* de prix d'ingrédients, 
* de temps de préparation pour prévoir un temps d'attente, 
* définir le prix de revient de chaque pizza avec la somme d'ingrédients
* on ne peux pas modifier une commande (la liste des pizza) car si ca a été payé c'est le bordel, une commande payé c'est une commande livré. il est possible d'annuler une commande uniquement dans le cas d'une commande a distance non payé.
* quand une commande est lancé le stock d'ingrédients diminu en fonction de la recette
* les différents moyens de paiement en ligne ou en live
* il y a différents comptes utilisateur en fonction du profil avec différents accès
* il est possible de consulter pour commander par téléphone
* il faut aussi penser qu'il y a 5 boutiques et bientot 8 pour savoir où est le stock, les commandes etc...

# Solution technique
* Django: il y a une partie admin qui ira très bien pour gerer les recettes et les ingrédients, les commandes (en même temps si j'avais dit PHP avec Symphony je me serais tiré une balle dans le pied...)
* Postgresql: parceque c'est classe
* permettre la creation d'un compte et la connection avec facebook, ca permettra d'avoir + facilent des like et de la pub etc...
