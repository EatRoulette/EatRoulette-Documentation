# Manuel d'utilisation de EatRoulette Front Angular

## Utilisation sans compte utilisateur

EatRoulette propose certaines fonctionnalités sans que l'utilisateur ait besoin d'un compte.

### <u>Tirage au sort d'un restaurant</u>  

### ![Rand](../ressources\img\angular\roulette-user-not-connected.png)

On accède à cette page en cliquant sur l'icone **EatRoulette** en haut de la page.

Sur cette page l'utilisateur à la possibilité de tirer au sort un restaurant présent dans la base de données en appuyant sur le bouton **Roulette**.

L'utilisateur peut filtrer ces restaurants en fonction de la ville, du type de restaurant, de ses allergènes et ses caractéristiques (Végan, PRM, ...) pour que le système affine le résultat de la recherche et donc le restaurant proposé.

L'utilisateur peut aussi relancer le tirage au sort en appuyant de nouveau sur le bouton **Roulette** ou accéder aux informations du restaurant en appuyant sur le bouton **Voir**.

### <u>Détails du restaurant</u>

### ![Details](..\ressources\img\angular\details-restaurant-user-not-connected.png)

Sur cette page l'utilisateur a accès aux informations du restaurant ainsi qu'à un plan indiquant la position du restaurant.

### <u>Recherche d'un restaurant</u>

Dans la sidebar, un bouton **recherche** permet d'accéder à la page de recherche d'un restaurant.

![Search](..\ressources\img\angular\search-restaurant.PNG)

Sur cette page, l'utilisateur peut rechercher des restaurants en renseignant un nom, une ville ou un code postal.

Le bouton **Voir** lui permet également accéder à la page de détails du restaurant.

## Utilisation avec compte utilisateur

### <u>Situation de l'utilisateur</u>

Lors de sa première connexion l'utilisateur est redirigé sur sa page de situation, il lui sera obligatoire de la valider avant de pouvoir lancer un tirage au sort.

Il peut y accéder a tout moment afin de modifier sa situation en cliquant dans la sidebar sur le bouton **Ma situation**.

![Situation](..\ressources\img\angular\situation.PNG)

### <u>Roulette</u> 

En cliquant sur l'icone **EatRoulette** on accède à la page de tirage au sort d'un restaurant.

Cette fonctionnalité est différente de la version non connecté. Le tirage se fera sur les restaurants contenus dans la liste des restaurants sélectionnée et la liste d'amie choisie si une liste a été sélectionnée, lui proposant un restaurant qui correspond le plus possible à sa situation et à celle de ses amis.

Si aucune liste d'ami n'est renseignée la situation sera celle de l'utilisateur connecté.

Si une liste d'ami est renseignée, une situation globale des amis et de l'utilisateur est prise en compte. 

![Roulette](..\ressources\img\angular\roulette.PNG)

On lance le tirage en cliquant sur le bouton **Roulette**. Si le restaurant proposé n'est pas souhaité, il est possible de relancer le tirage en réappuyant sur ce même bouton.

En appuyant sur le bouton **Valider**, le système considère qu'on souhaite s'y rendre et le restaurant ainsi que les amis apparaitront dans la rubrique **Mon historique**.

En cliquant sur le bouton **Voir** on accède à la page de détails du restaurant, en provenant de la Roulette cette page permet aussi de **Valider** le restaurant

![Roulette Details](..\ressources\img\angular\roulette-details-restaurant.PNG)



### <u>Demande d'ajout d'un restaurant</u>

Lors de la recherche d'un restaurant, si le restaurant n'existe pas, l'utilisateur à la possibilité de l'ajouter au catalogue des restaurants EatRoulette en appuyant sur le bouton **L'ajouter**.

Il sera redirigé sur un formulaire d'ajout

![Add Restaurant](..\ressources\img\angular\form-add-restaurant.PNG)

Une fois le restaurant ajouté, un ticket sera automatiquement envoyé et  devra être validé par l'équipe EatRoulette avant d'apparaitre lors d'une recherche et ainsi être rajouté à une liste.

### <u>Gestion du compte utilisateur</u>

EatRoulette propose à ses utilisateurs de modifier leurs informations entrées lors de l'inscription. En cliquant dans la sidebar sur le bouton **Mon Compte** , il accède a ses informations et peut les modifier en cliquant sur le bouton **Modifier**

![Account](..\ressources\img\angular\account.PNG)

### <u>Gestion des listes de Restaurants</u>

Avant de lancer une roulette, un utilisateur doit créer au moins une liste de restaurants.  Pour se faire, il doit se rendre sur la page permettant de gérer ses listes, en cliquant sur le bouton **Mes listes**.



#### <u>**Création d'une liste**</u>

![Create List](..\ressources\img\angular\create-list.PNG)

En cliquant sur le bouton **+** une popup apparait, permettant la création d'une nouvelle liste de restaurants.



![Popup list](..\ressources\img\angular\popup-create-list.PNG)



#### <u>Ajout et suppression d'un restaurant dans une liste</u>

Pour ajouter ou supprimer un restaurant d'une liste il faut d'abord sélectionner une liste de restaurants dans le menu déroulant.

En appuyant sur le bouton **Ajouter un nouveau restaurant à cette liste** un formulaire apparait dans lequel on peut rechercher un restaurant à ajouter, il suffira ensuite d'appuyer sur le bouton **Ajouter** sur le restaurant désiré.

![Add](..\ressources\img\angular\add-restaurant-list.PNG)

Une fois des restaurants dans la liste on peut les supprimer en appuyant sur le bouton **Supprimer**.

![Remove](..\ressources\img\angular\remove-restaurant.PNG)

En Appuyant sur le bouton **Supprimer la liste** la liste des restaurants est définitivement supprimée.

### <u>Gestion des listes d'amis</u>

De la même façon que pour les listes de restaurants il est possible de gérer ses listes d'amis.

![Friendlist](..\ressources\img\angular\friendlist.PNG)

### <u>Historique de l'utilisateur</u>

Un utilisateur EatRoulette peut visualiser l'historique des restaurants visités.

![Historic](..\ressources\img\angular\historique.PNG)

Le buton **Restaurant** nous redirige sur la page des informations du restaurant et le bouton **Historique** sur les détails de l'historique.

![Historic Details](..\ressources\img\angular\historique-details.PNG)

 

### <u>Demande de support</u>

Eatroulette propose un support à ses utilisateurs, ils peuvent faire une demande ou reporter un bug sur l'application à l'équipe EatRoulette.

Pour accéder à cette page l'utilisateur doit cliquer sur le **Demande de support** situé en bas à droite de l'écran.

![Support](..\ressources\img\angular\support.PNG)



### <u>Les tickets de l'utilisateur</u>

L'utilisateur peut accéder à ses tickets en cliquant sur le bouton **Mes tickets** situé dans la sidebar.

![Tickets](..\ressources\img\angular\my-tickets.PNG)

Il peut accéder aux détails d'un ticket en appuyant sur le bouton **Details** du ticket concerné, sur cette page il peut visualiser l'avancée du ticket ainsi que répondre à l'équipe EatRoulette via les commentaires.

![Details Ticket](..\ressources\img\angular\details-ticket.PNG)

