# Analysez le besoin pour votre client pour son goupe de pizzerias

## Contexte

« OC Pizza » est un jeune groupe de pizzeria en plein essor et spécialisé dans les pizzas **livrées** ou à **emporter**. Il compte déjà 5 points de vente et prévoit d’en ouvrir au moins 3 de plus d’ici la fin de l’année. Un des responsables du groupe a pris contact avec vous afin de mettre en place un système informatique, déployé dans toutes ses pizzerias et qui lui permettrait notamment :

* d’être plus efficace dans la gestion des **commandes**, de leur **réception** à leur **livraison** en passant par leur **préparation** ;
* de suivre en temps réel les **commandes passées** et en **préparation** ;
* de suivre en temps réel le **stock d’ingrédients restants** pour savoir quelles pizzas sont **encore réalisables** ;
* de proposer un site Internet pour que les clients puissent :
    * **passer leurs commandes**, en plus de la prise de commande par **téléphone** ou **sur place**,
    * **payer en ligne** leur commande s’ils le souhaitent – sinon, ils paieront directement **à la livraison**
    * **modifier** ou **annuler** leur commande tant que celle-ci n’a **pas été préparée**
* de proposer un aide mémoire aux pizzaiolos indiquant la **recette** de chaque pizza

## 1 - Les acteurs du système

* d’être plus efficace dans la gestion des **commandes**, de leur **réception** à leur **livraison** en passant par leur **préparation** ; <span style="background-color: red;">=> Gestionnaire de commandes, Livreur</span>
* de suivre en temps réel les **commandes passées** et en **préparation** ; <span style="background-color: red;">=> Gestionnaire de commande</span>
* de suivre en temps réel le **stock d’ingrédients restants** pour savoir quelles pizzas sont **encore réalisables** ;<span style="background-color: red;"> => Gestionnaire de stock</span>
* de proposer un site Internet pour que les <span style="background-color: red;">clients</span> puissent :
    * **passer leurs commandes**, en plus de la prise de commande par **téléphone** ou **sur place**,<span style="background-color: red;"> => Gestionnaire de commande</span>
    * **payer en ligne** leur commande s’ils le souhaitent – sinon, ils paieront directement **à la livraison**<span style="background-color: red;"> => Banque</span>
    * **modifier** ou **annuler** leur commande tant que celle-ci n’a **pas été préparée**
* de proposer un aide mémoire aux <span style="background-color: red;">pizzaiolos</span> indiquant la **recette** de chaque pizza

![Les acteurs](img/01_actors.png)

Nous considérons que le livreur n'a pas d'intération directe avec le système, la gestion des commandes faisant appel à ses services sera géré par le Gestionnaire de commandes.

![Diagramme de contexte](img/01_contexte.png)

## 2 - Décomposition du système

* d’être plus efficace dans la <span style="background-color: yellow;">gestion des commandes</span>, de leur <span style="background-color: yellow;">réception</span> à leur <span style="background-color: yellow;">livraison</span> en passant par leur <span style="background-color: yellow;">préparation</span> ;
* de suivre en temps réel les <span style="background-color: yellow;">commandes passées et en préparation</span> ;
* de suivre en temps réel le <span style="background-color: green;">stock d’ingrédients</span> restants pour savoir quelles pizzas sont encore réalisables ;
* de proposer un site Internet pour que les clients puissent :
    * <span style="background-color: yellow;">passer leurs commandes</span>, en plus de la prise de commande par <span style="background-color: yellow;">téléphone ou sur place</span>,
    * <span style="background-color: yellow;">payer en ligne</span> leur commande s’ils le souhaitent – sinon, ils paieront directement <span style="background-color: yellow;">à la livraison
    * <span style="background-color: yellow;">modifier ou annuler</span> leur commande tant que celle-ci n’a pas été préparée
* de proposer un aide mémoire aux pizzaiolos indiquant la <span style="background-color: green;">recette</span> de chaque pizza

On distingue 2 grandes familles:
* La gestion du cycle de vie des commandes
* La gestion du produit

Un 3ème package ressort:
* l'authentification: va servir à connaitre le role de chaque utilisateur et également la boutique avec laquelle il intéragit
![Diagramme de packages](img/02_packages.png)

## 3 - Les cas d'utilisation


