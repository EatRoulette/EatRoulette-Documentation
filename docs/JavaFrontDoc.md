## Utilisation Graphique : 

**Utilisation des plugins :** 

- Ajout de nouveau plugin : 

  - Cliquer sur le bouton "new plugin" : ![](../ressources/img/FrontJava/CliqueAjoutDePlugins.png)

  - Retrouver le fichier Jar du plugin :![](..\ressources\img\FrontJava\SelectPlugin.png)

    

    

    

- Actualisation des plugins :

  - cliquez sur le bouton Refresh :![](../ressources/img/FrontJava/RefreshPlugin.png)

  - Après avoir cliqué,  des boutons seront disponible pour lancer les plugins : ![](..\ressources\img\FrontJava\RenderPlugin.png)



**Espace d'administration des restaurants :** 

- Afficher tous les restaurants : 

- Cliquer sur le button View All Restaurant :![](..\ressources\img\FrontJava\CliqueViewAllRestaurants.png)
  
- Affichage de tous les restaurants : ![](..\ressources\img\FrontJava\ViewAllRestaurants.png)
  - Cliquez sur un bouton du restaurant :![](..\ressources\img\FrontJava\cliqueBouttonRestaurantData.png)
  - Affichage des informations du restaurant : ![](..\ressources\img\FrontJava\RestaurantInfo.png)
  
- Creer un restaurant :

  - Cliquez sur le bouton "Create new Restaurant" : ![](..\ressources\img\FrontJava\CreateRestaurantFeature.png)

  - Cliquez sur submit pour créer le Restaurant après avoir remplis tous les champs du formulaire :![](..\ressources\img\FrontJava\CreateRestaurantFormFill.png)

  

- Ajouter un type à un restaurant déjà créer :

  - Cliquez sur le bouton "Add type to restaurant" et appuyer sur "Load | Refresh" : ![](..\ressources\img\FrontJava\AddTypeStart.png)
  - Cliquez sur le restaurant pour ajouter le type souhaité :![](..\ressources\img\FrontJava\AddType.png)
  - Cliquez sur le type souhaitez : ![](..\ressources\img\FrontJava\TypeAddSelected.png)

  - Cliquez sur submit pour créer le nouveau type dans le restaurant :![](..\ressources\img\FrontJava\Submit addTypeRestaurant.png)

- Retirer un type à un restaurant déjà créer :

  - Charger toutes les infos des Restaurant et des Types : ![](..\ressources\img\FrontJava\DelTypeRestaurant.png)
  - Sélectionner le Restaurant : 
    ![](..\ressources\img\FrontJava\DeleteTypeSelectedRestaurant.png)

  - Sélectionner le type du restaurant à supprimer : ![](..\ressources\img\FrontJava\DeleteTypeSelect.png)
  - Retirer un type du restaurant : ![](..\ressources\img\FrontJava\SubmitDeleteType.png)

- Pour les Caractéristiques et les Allergènes il s'agit du même fonctionnement que les type du restaurant.

- Créer un nouvelle Allergène : 

  - Cliquer sur le button "Create new Allergen" & ecrit le nom du nouvelle allergène :

    ![](..\ressources\img\FrontJava\CreateAllergen.png)

  - Cliquer sur le bouton submit pour confirmer l'ajout du nouvelle allergène : ![](..\ressources\img\FrontJava\CreateAllergenSubmit.png)

  - Annuler la création de allergène :![](..\ressources\img\FrontJava\CreateAllergenCancel.PNG)

    

## Application en mode CLI

L'application Java est aussi utilisable en ligne de commande. Pour cela il suffit de lancer l'application avec l'argument `-cli`. Exemple :

```sh
java - jar EatRoulette-admin-<VERSION> -cli
```

Ce mode offre des fonctionalités *"super-admin"* qui sont notament la supression de restaurant, de types, d'allergènes ou encore de caractéristiques.



### Commandes disponibles

Les commandes disponibles sont les suivantes :

```
EatRoulette-cli commands ...
*	add [restaurant | type | allergen | characteristic] [data]
*	upd [type | allergen | characteristic] id [data]
*	dell [restaurant | type | allergen | characteristic] id
*	run [plugin-name]
*	show [restaurants | types | allergens | characteristics | plugins]
*	help #To get this panel
*	exit #To quit the application
```

Vous pouvez entrer à  tout moment la commande `help` pour avoir ces informations.

![](../ressources/img/FrontJava/CliHelp.png)



Les commandes `add` permettent d'ajouter des restaurants, des types, des allergènes ou encore des caractéristiques. Exemple pour ajouter un nouveau type de restaurant:

```
add type NomDeType
```

Une fois ajouté, nous avons un retour nous confirmant l'ajout:

![](../ressources/img/FrontJava/CliAddType.png)



Les commandes `upd` permettent de mettre à jour des types, des allergènes ou encore des caractéristiques. Exemple pour mettre à jour un type :

```
upd type <ID_TYPE> NouveauNom
```

Une fois mis à jour, nous avons la confirmation:

![](../ressources/img/FrontJava/CliUpdType.png)



Les commandes `del` permettent de supprimer des restaurants, des types, des allergènes ou encore des caractéristiques. Exemple supprimer un type :

```
del type <ID_TYPE>
```

Une fois mis à jour, nous avons la confirmation:

![](../ressources/img/FrontJava/CliDelType.png)



La commande `run` permet e lancer les plugins. Il est necessaire de la coupler à la commande `show plugins` pour connaitre le nom des différents plugins exécutables:

![](../ressources/img/FrontJava/CliPlugins.png)



La commande `show` permet de d'afficher les restaurants, les types, les allergènes, les caractéristiques ou encore les plugins. Example d'affichage des types :

![](../ressources/img/FrontJava/CliShowType.png)



En cas de command invalid un message vous avertis que la saisie est incorrect :

![](../ressources/img/FrontJava/CliError.png)
