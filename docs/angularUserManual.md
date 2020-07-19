# Manuel d'utilisation de EatRoulette Front Angular

## Utilisation sans compte utilisateur

EatRoulette propose certaine fonctionnalités sans que l'utilisateur nécessite un compte.

### <u>Tirage au sort d'un restaurant</u>  

### ![Rand](../ressources\img\angular\roulette-user-not-connected.PNG)

On accède à cette page en cliquant sur l'icone **EatRoulette** en haut de la page.

Sur cette page l'utilisateur à la possibilité de tirer au sort un restaurant présent dans la base de données en appuyant sur le bouton **Roulette**.

L'utilisateur peut filtrer ces restaurants en fonction de la ville, du type de restaurant, de ses allergènes et sa caractéristique pour que le système affine le restaurant proposé.

L'utilisateur peut aussi relancer le tirage au sort en appuyant de nouveau sur le bouton **Roulette** ou accéder au information du restaurant en appuyant sur le bouton **Voir**.

### <u>Détails du restaurant</u>

### ![Details](..\ressources\img\angular\details-restaurant-user-not-connected.PNG)

sur cette page l'utilisateur à accès aux information du restaurant ainsi qu'un plan indiquant sa position.

### <u>Recherche d'un restaurant</u>

Dans la sidebar un bouton "recherche" permet d'accéder à la page de recherche d'un restaurant.

![Search](..\ressources\img\angular\search-restaurant.PNG)

Sur cette page, l'utilisateur peut recherche des restaurant en renseignant un nom, une ville ou un code postale.

Le bouton **Voir** lui permet également accéder à la page de détails du restaurant.

## Utilisation avec compte utilisateur

### <u>Situation de l'utilisateur</u>

Lors de la première connexion l'utilisateur est redirigé sur sa page de situation, il lui sera obligatoire de la valider avant de pouvoir lancer un tirage au sort.

Il peut y accéder a tout moment afin de modifier sa situation en cliquant dans la sidebar sur le bouton **Ma situation**.

![Situation](..\ressources\img\angular\situation.PNG)

### <u>Roulette</u> 

En cliquant sur l'icone **EatRoulette** on accède à la page de tirage au sort d'un restaurant.

Cette fonctionnalité est différente de la version non connecté. Le tirage se fera sur les restaurants contenue dans la liste des restaurants, lui proposant un restaurant qui correspond le plus possible à sa situation et de celle de ses amis.

Si aucune liste d'ami n'est renseigner la situation sera celle de l'utilisateur connecté.

Si une liste d'ami est renseigné, une situation globale des amis et de l'utilisateur est prise en compte. 



On lance le tirage en cliquant sur le bouton **Roulette**. Si le restaurant proposé n'est pas souhaité, il est possible de relancer le tirage en réappuyant sur ce même bouton.

En appuyant sur le bouton Valider, le système considère qu'on souhaite si rendre et le restaurant ainsi que les amis apparaitront dans la rubrique **Mon historique**.

### <u>Gestion du compte utilisateur</u>

EatRoulette propose à ses utilisateur de modifier leur information entrer lors de l'inscription. En cliquant dans la sidebar sur le bouton **Mon Compte** , il accède a ses informations et peut les modifier ne cliquant sur le bouton **Modifier**

![Account](..\ressources\img\angular\account.PNG)

### <u>Gestion des listes de Restaurants</u>

Avant de lancer une roulette un utilisateur doit créer au moins une liste de restaurants.  Pour se faire il doit se rendre sur la page permettant de gérer ses listes, en cliquant sur le bouton **Mes listes**.



#### <u>**Création d'une liste**</u>

![Create List](..\ressources\img\angular\create-list.PNG)

En cliquant sur le bouton **+** une popup apparait, permettant la création d'une nouvelle liste de restaurant.



![Popup list](..\ressources\img\angular\popup-create-list.PNG)



#### <u>Ajout et suppression d'un restaurant dans une liste</u>

Pour ajouter ou supprimer un restaurant d'une liste il faut d'abord sélectionner une liste de restaurant dans le menu déroulant.

En appuyant sur le bouton **Ajouter un nouveau restaurant à cette liste** un formulaire apparait dans lequel on peut rechercher un restaurant à ajouter, il suffira ensuite d'appuyer sur le bouton **Ajouter** sur le restaurant désiré.

![Add](..\ressources\img\angular\add-restaurant-list.PNG)

Une fois des restaurants dans la liste on peut les supprimer en appuyant sur le bouton **Supprimer**.

![Remove](..\ressources\img\angular\remove-restaurant.PNG)

En Appuyant sur le bouton **Supprimer la liste** la liste des restaurant est définitivement supprimer.

### <u>Gestion des listes d'amis</u>

De la même façon que pour les listes de restaurant il est possible de gérer ses listes d'amis.

![Friendlist](..\ressources\img\angular\friendlist.PNG)

### <u>Historique de l'utilisateur</u>

Un utilisateur EatRoulette peut visualiser l'historique des restaurants où.



### <u>Demande de support</u>

Eatroulette propose un support à ses utilisateurs, ils peuvent faire une demande ou reporter un bug sur application à l'équipe EatRoulette.

Pour accéder à cette page l'utilisateur doit cliquer sur le **Demande de support** situé en bas à droite de l'écran.

![Support](..\ressources\img\angular\support.PNG)



### <u>Les tickets de l'utilisateur</u>

L'utilisateur peut accéder à ses tickets en cliquant sur le bouton **Mes tickets** situé dans la sidebar.

![Tickets](..\ressources\img\angular\my-tickets.PNG)

Il peut accéder au détails d'un ticket en appuyant sur le bouton **Details** du ticket concerné, sur cette page il peut visualisé l'avancé du ticket ainsi que répondre à l'équipe EatRoulette.

![Details Ticket](..\ressources\img\angular\details-ticket.PNG)