#geo-health #genie-logiciel 


# Structure of the backlog

- Epic ➞ User story ➞ Task

## Epic 

- An "epic" is a large functional area or a major objective of the product
- It is a user story about a more complex feature
- It is too vast to be implemented in 1 sprint
- Example : "As a system manager, I need a way to backup the system and restore either individual applications, files, directories or the whole system."

## User story 

- User stories follow this structure : "As a [user role], I want to [action] so that [goal/reason]"

## Feature/ Task

- More precise than user stories, increased granularity
- Should be implemented in 1 sprint
- Features must follow the CRI principles :
	- **Coherence** : Features should be linked to a single item of functionality. They should not do more than one thing and they should never have side-effects. 
	- **Relevance** : Features should reflect the way that users normally carry out some task. They should not provide obscure functionality that is hardly ever required.
	- **Independence** : Features should not depend on how other system features are implemented and should not be affected by the order of activation of other features. 


## User roles 

- Admin
- Expert
- Decider (décisionnaire politique)
- User (englobe tous les rôles)

# Actual backlog 

## EPIC 1 - Authentification et gestion des rôles 

### User stories : 

1. "En tant qu'utilisateur, je veux pouvoir me connecter à ma session via une interface sécurisée afin d'accéder aux fonctionnalités liées à mon rôle"

2. "En tant qu'admin, je veux une interface dédiée qui me permet de consulter la liste des utilisateurs, en supprimer, modifier les rôles,... (? à définir) afin d'assurer le bon fonctionnement de l'application et d'avoir le pouvoir de pénaliser une personne qui trouble l'ordre en son sein"



## EPIC 2 - WebGIS interactif

### User stories : 

1. "En tant qu'*utilisateur*, je veux consulter des cartes multicouches (risque, facteurs, OSM, Google Maps) de manière optimale afin d'explorer les données de risque épidémiologique sur le territoire du Cameroun"

### Features : 

- Stockage organisé de cartes (utilisation de rasters, 1 pixel = 1km²)
- Visualisation des cartes
- Possibilité de cliquer sur un pixel afin de voir la valeur exacte pour cette zone
- Zoom et pan
- Recherche par département/district (voir différents niveaux de division du pays)
- Superposer deux cartes (risques + facteurs) pour voir clairement les liens
- Visualisation 3d des cartes
- Affichage ou non (checkbox) des valeurs par département par exemple directement sur la carte
- Ajouter un quadrillage gradué personnalisable 
- Filtrer les facteurs de risque ?
- 1 pixel = 1km x 1km


## EPIC 3 - Annotations par les experts

### User stories : 

1. "En tant qu'expert, je veux annoter une carte de manière intuitive afin de partager mon expertise au sujet des risques épidémiologiques, de leurs causes et des liens entre ces derniers directement sur une carte du Cameroun, en ayant la possibilité de sélectionner le niveau de division (régions, départements, districts,...)"

2. "En tant qu’admin, je veux consulter les annotations + auteur, mais sans pouvoir les modifier, car il est important que les annotations des experts restent inchangées (ni corrigées ni modifiées, ni corrompies,...)"

3. "En tant qu’expert, je veux voir les annotations des autres experts de façon **anonyme**, classées par **profil d'annotations** afin d'avoir un oeil sur la qualité des annotations produites par les experts."

4. "En tant qu'expert A, je ne peux pas voir qui est expert B, mais je peux voir quelles autres cartes expert B a annotées, afin de maintenir l'anonymat des experts entre eux."

5. "En tant qu'admin, j'ai accès aux différentes versions des annotations produites par chaque expert (elles ne sont pas écrasées)."



### Features : 

- Implémenter l'éditeur graphique, il devrait offrir les possibilités suivantes : 
    - Choisir quelle carte annoter
    - Superposer deux cartes (ou plus ?), en général risque/facteur de risque
    - Ajouter flèches, zones, formes, couleurs, notes textuelles avec une variété de libertés (forme des flèches, épaisseur, opacité des couleurs, police texte,...)
    - Revenir en arrière et en avant (undo/redo)
    - Copier/Coller les éléments
    - (Ajouter un quadrillage gradué personnalisable comme lors de la lecture de la carte)

- Gestionnaire de permissions (édition/ lecture) en fonction du rôle de l'utilisateur/trice

- Historique lié à un(e) utilisateur/trice (identié(e) par identifiant unique)

- Stockage des annotations

- Interface de consultation dédiée à l'admin

- (Système d'allias ou de pseudos générés automatiquement afin que les experts soient reconnaissables tout en restant anonymes ?)

