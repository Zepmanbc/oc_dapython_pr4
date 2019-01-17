# Fiche descriptive du cas d'utilisation "Commander une pizza sur le site web"

## Identification
----

**Numéro** : 1

**Nom**: Commander (package commander)

**Auteur(s)**: Client

**Description succinte**: Le client effectue une commande par le site internet

**Auteur**: moi

**Date(s)**: 16/01/2019 (première rédaction)

**Pré-conditions**: Le client doit avoir accès à un terminal disposant d'un accès à internet (ordinateur, smartphone)

**Démarrage**: l'utilisateur se rend sur l'adresse du site de la pizzéria

----
## Le dialogue: le scénario nominal
----

    1. Système affiche la page d'accueil du site
    2. Client clique sur passer une commande
    3. Systéme demande à Client de se connecter
    4. Client renseigne son identifiant, son mot de passe et valide
    5. Système affiche la liste des pizzas disponible dans la pizzéria par défaut du Client
    6. Client sélectionne une pizza
    7. Client ajoute la pizza dans son panier
    8. Client valide la commande
    9. Système demande le mode de paiement à Client
    10. Client Sélectionne le paiement en ligne
    11. Système redirige vers la banque
    12. Client fournis ses coordonnés bancaire et valide
    13. Système confirme la validation de la commande
    14. Système donne un temps estimatif pour la préparation de la commande

## Le dialogue: les scénarios alternatifs
----
    2a. Le Client souhaite consulter la liste des pizzas
    2b. Le client souhaite avoir des renseignements sur boutiques
    5a. Le Client doit créer un compte
    5b. Le Client ne veut pas créér de compte
    5c. le Client n'a pas de pizzeria par défaut et doit donc en choisir une
    5d. le Client souhaite passer sa commande dans un autre pizzeria
    7a. Le Client souhaite modifier sa pizza
    8a. Le client ferme son navigateur
    8b. Le Client souhaite ajouter une autre pizza
    8c. Le Client souhaite retirer un élément de son panier
    8d. Le Client souhaite modifier les ingrédient d'un pizza du panier
    10a. Le Client ferme son navigateur
    10b. Le Client  Selecstèmetionne le paiement au retrait
    11a. Le serveur de la banque ne répond pas
    12a. Le Client ferme son navigateur
    13a. Le paiement est refusé

----
## Fin
----
**Scénario nominal**: après le point 14 (affichage du temps de préparation)

**Scénario d'exception**: apres les points 8a, 10a, 12a

----
## Post condition
----
**Scénario nominal**: la commande est enregistré dans le système

**Scénario d'exception**: la commande est enregistré dans le système si le Client a sélectionné le paiement au retrait

La commande reste dans le panier du client si il souhaite la reprendre plus tard

----
## Compléments
----

**Ergonomie**: le client doit pouvoir être identifié automatiquement si il a accepté les cookies

L'ajout de plusieurs pizza dans le panier doit se faire dynamiquement sur la même page

La modification des ingrédients d'une pizza doit pouvoir se faire dans un cadre qui s'affiche au premier plan.

Il doit être possible de rajouter plusieurs pizza avec une base identique mais des ingrédients modifiés différents.

Si le paiement est refusé, proposer au client de payer au retrait

Si le Client ne souhaites pas s'identifier (créér un compte) lui indiquer les coordonnés de la boutique et le numéro de téléphone lui indiquent qu'il peut effectuer une commande par téléphone ou directement en boutique

**Problèmes non résolus**: Est ce qu'il faut prévoir un système de livraison à domicile?


