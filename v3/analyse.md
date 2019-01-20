# Analysez le besoin pour votre client pour son goupe de pizzerias

## Contexte

« OC Pizza » est un jeune groupe de pizzeria en plein essor et spécialisé dans les pizzas **livrées** ou à **emporter**. Il compte déjà 5 points de vente et prévoit d’en ouvrir au moins 3 de plus d’ici la fin de l’année. Un des responsables du groupe a pris contact avec vous afin de mettre en place un système informatique, déployé dans toutes ses pizzerias et qui lui permettrait notamment :

* d’être plus efficace dans la gestion des commandes, de leur réception à leur livraison en passant par leur préparation ;
* de suivre en temps réel les commandes passées et en préparation ;
* de suivre en temps réel le stock d’ingrédients restants pour savoir quelles pizzas sont encore réalisables ;
* de proposer un site Internet pour que les clients puissent :
    * passer leurs commandes, en plus de la prise de commande par téléphone ou sur place,
    * payer en ligne leur commande s’ils le souhaitent – sinon, ils paieront directement à la livraison
    * modifier ou annuler leur commande tant que celle-ci n’a pas été préparée
* de proposer un aide mémoire aux pizzaiolos indiquant la recette de chaque pizza

## 1 - Les acteurs du système

* d’être plus efficace dans la gestion des **commandes**, de leur **réception** à leur **livraison** en passant par leur **préparation** ; **=> Gestionnaire de commandes, Livreur**
* de suivre en temps réel les **commandes passées** et en **préparation** ; **=> Gestionnaire de commande**
* de suivre en temps réel le **stock d’ingrédients restants** pour savoir quelles pizzas sont **encore réalisables** ;** => Gestionnaire de stock**
* de proposer un site Internet pour que les **clients** puissent :
    * **passer leurs commandes**, en plus de la prise de commande par **téléphone** ou **sur place**,** => Gestionnaire de commande**
    * **payer en ligne** leur commande s’ils le souhaitent – sinon, ils paieront directement **à la livraison**** => Banque**
    * **modifier** ou **annuler** leur commande tant que celle-ci n’a **pas été préparée**
* de proposer un aide mémoire aux **pizzaiolos** indiquant la **recette** de chaque pizza

![Les acteurs](img/01_actors.png)

Nous considérons que le livreur n'a pas d'intération directe avec le système, la gestion des commandes faisant appel à ses services sera géré par le Gestionnaire de commandes.

![Diagramme de contexte](img/01_contexte.png)

## 2 - Décomposition du système

* d’être plus efficace dans la **gestion des commandes**, de leur **réception** à leur **livraison** en passant par leur **préparation** ;
* de suivre en temps réel les **commandes passées et en préparation** ;
* de suivre en temps réel le **stock d’ingrédients** restants pour savoir quelles pizzas sont encore réalisables ;
* de proposer un site Internet pour que les clients puissent :
    * **passer leurs commandes**, en plus de la prise de commande par **téléphone ou sur place**,
    * **payer en ligne** leur commande s’ils le souhaitent – sinon, ils paieront directement **à la livraison
    * **modifier ou annuler** leur commande tant que celle-ci n’a pas été préparée
* de proposer un aide mémoire aux pizzaiolos indiquant la **recette** de chaque pizza

On distingue 2 grandes familles:
* La gestion du cycle de vie des commandes
* La gestion du produit

Un 3ème package ressort:
* l'authentification: va servir à connaitre le role de chaque utilisateur et également la boutique avec laquelle il intéragit

![Diagramme de packages](img/02_packages.png)

## 3 - Les cas d'utilisation

![Diagramme de cas d'utilisation Produit](img/03_produit.png)

![Diagramme de cas d'utilisation Commande](img/03_commande.png)

![Diagramme de cas d'utilisation Authentification](img/03_authentification.png)

## 4 - Fiche Descriptives

## Package Produit
* [P01 : Gérer le stock](fiches/P01.md)
* [P02 : Consulter une recette](fiches/P02.md)

## Package Commande
* [C01 : Livrer une commande](fiches/C01.md)
* [C02 : Passer une commande](fiches/C02.md)
* [C03 : Modifier une commande](fiches/C03.md)
* [C04 : Annuler une commande](fiches/C04.md)
* [C05 : Suivre l'état d'une commande](fiches/C05.md)
* [C06 : Payer une commande](fiches/C06.md)
* [C07 : Préparer une commande](fiches/C07.md)

## Package Authentification
* [A01 : S'identifier](fiches/A01.md)
* [A02 : Créer un compte](fiches/A01.md)
* [A03 : Choisir une boutique](fiches/A01.md)

## 5 - Solution technique

Une solution en ligne qui permet d'avoir une interface commune entre les clients et le personnel. Cette solution permet de s'affranchir d'un matériel particulier car accessible par un navigateur WEB.

* Amazon Web Service : Hébergeur qui s'adapte au trafique et permet de s'affranchir des problèmes matériel, la garantie de toujours avoir le service en ligne.
* Django : La partie Admin intégrée à Django va permettre d'avoir une gestion des commandes efficace et permet une modularité de l'application afin de prévoir de futures évolutions.
* Nginx/Gunicorn/Postgres : Une combinaison robuste qui permettra à l'application de supporter la croissance de la société.
* HTML5/CSS3/JQuery/Bootstrap : Des technologies WEB qui permettent d'avoir une application répondant aux standards graphique actuels et de s'adapter à l'utilisation mobile.
* Facebook authentification: Permettre au client de se connecter grace à son compte facebook afin de simplifier l'identification et de se laisser la possibilité d'utiliser les réseaux sociaux pour faire de la publicité.

![Solution Technique](img/05_DeployementDiagram.png)
