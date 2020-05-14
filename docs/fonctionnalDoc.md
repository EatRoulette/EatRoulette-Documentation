







# Documentation fonctionnelle

![logo](../ressources/img/name/enrich/EatRoulette-large-logo-right-bordless.png)

## Descriptif de l'application

EatRoulette est une application permettant à ses utilisateurs de choisir des restaurants, dans leurs listes de restaurants préférés afin de les aider à faire le choix de leur lieux de restauration.

Grâce à un aspect social, vous pouvez inviter vos amis à déjeuner et choisir au hasard dans vos restaurants favoris le lieux idéal en prenant en compte les caractéristiques de chacun.



## Fonctionnalités de l'application

##### Fonctionnalités utilisateur - Client Web

| Fonctionnalités                           | Détails                                                      |
| :---------------------------------------- | ------------------------------------------------------------ |
| Roulette                                  | La roulette est la fonctionnalité permettant de proposer aléatoirement un restaurant à un utilisateur (connecté ou non). |
| Inscription à EatRoulette                 | Lors de l'inscription un compte sera créer à l'utilisateur, lui accordant les fonctionnalités supplémentaires liés à un compte ( Création de listes de restaurants favoris, Dîner entre amis ... ). |
| Filtrer les restaurants                   | L'utilisateur pourra spécifier sa recherche à l'aide de filtres (Régime alimentaire, Type de restaurant, Proximité du restaurant). |
| Création de liste des restaurants favoris | Un utilisateur pourra créer une liste avec un titre dans lequel il pourra y ajouter ses restaurants préférer. Il aura la possibilité d'inviter des amis à collaborer à cette liste. |
| Ajout d'un restaurant dans une liste      | Pour ajouter un restaurant dans une liste, l'utilisateur devra le rechercher par son nom et son adresse. Si le restaurant n'existe pas, il à la possibilité de le créer. |
| Renseigner un restaurant                  | Si le restaurant n'existe pas déjà sur EatRoulette, un utilisateur connecté aura la possibilité de le créer en renseignant le nom et l'adresse du restaurant. Sa création entrainera automatiquement l'ouverture d'un ticket à valider. |
| Définir ses caractéristiques              | Un utilisateur possédant un compte pourra renseigner ses allergènes, s'il y est en situation de handicap ou encore son régime alimentaire. Ces informations seront utilisés dans le cadre de la roulette groupé. |
| Groupe ami                                | Les utilisateurs connectés pourront créer des groupes et inviter leurs amis EatRoulette. |
| Roulette groupé                           | Les utilisateurs connectés pourront inviter leurs amis à une roulette groupé. Cette fonctionnalité à pour objectif de trouver le restaurant le plus adapté à votre groupe d'amis, en fonction leurs régimes alimentaires et leurs allergènes . |
| Descriptif d'un plat                      | Certain plat pourront être décrit avec l'histoire du plat. Ces descriptions seront récupérées sur d'autres sites. |
| Envoie de Ticket                          | L'utilisateur pourra envoyer des tickets expliquant le problème rencontré au support |
| Mon historique                            | Un utilisateur connecté pourra consulté la liste des restaurant qu'il est allé visité via la roulette quand il l'aura choisi via le bouton "Valider" après la roulette. |



##### Fonctionnalités administrateur - Client Lourd

| Fonctionnalités                   | Détails                                                      |
| :-------------------------------- | ------------------------------------------------------------ |
| Consulter le tracking utilisateur | L'administrateur à la possibilité de visionner le tracking réaliser par l'application. En le consultant, il à la possibilité de filtrer (par localisation, type de restaurant...) et de construire le reporting qu'il souhaite. |
| Consulter le tracking des tickets | L'administrateur à la possibilité de visionner le tracking sur les tickets réaliser par l'application. En le consultant, il à la possibilité de filtrer (par état, type de demande...) et de construire le reporting qu'il souhaite. |
| Gérer les plugins                 | Via  cette fonctionnalité, l'administrateur à la possibilité d'ajouter ou supprimer au client lourd différents plugins. |
| Gérer les demandes utilisateurs   | Permet de gérer les différentes demandes des utilisateurs via les tickets. Il peut requalifier les demandes (Bogue, demande...), changer le statut (En cours, Résolue...), les commenter afin de lui donner un feedback. |



## Use case

Ci-dessous le diagrammes des cas d'utilisation :

![UseCase](../ressources/diagrams/EatRoulette-Diagrams-UseCase.png)

*Diagramme des cas d'utilisations*

## Descriptif des cas d'utilisations

### Insciption

#### Cas d'utilisation

|         Nom          |                 Inscription                  |
| :------------------: | :------------------------------------------: |
|        Numéro        |                      1                       |
|        Acteur        |                 Utilisateur                  |
| Dernière mise à jour |                  5/05/2019                   |
|     Précondition     |                      /                       |
|      Démarrage       | L'utilisateur accède à la page d'inscription |

#### Scénario nominal

|      | Utilisateur                           |      | Système                       |
| ---- | ------------------------------------- | ---- | ----------------------------- |
|      |                                       | 10   | Affiche la page d'inscription |
| 20   | L'utilisateur rentre ses informations |      |                               |
|      |                                       | 30   | Vérifie les champs renseigner |
|      |                                       | 40   | Crée l'utilisateur en base    |
|      |                                       | 50   | Affiche la page de connexion  |

#### Scénario alternatif

|      | Utilisateur                                           |      | Système |
| ---- | ----------------------------------------------------- | ---- | ------- |
| 21   | L'utilisateur décide de quitter la page d'inscription |      |         |

#### Scénario d'exception

|      | Utilisateur                        |      | Système                                                      |
| ---- | ---------------------------------- | ---- | ------------------------------------------------------------ |
|      |                                    | 31   | Le système trouve un autre utilisateur avec le même email    |
|      |                                    | 32   | le système renvoie un message d'erreur indiquant à l'utilisateur qu'un autre compte utlise déjà cet email |
| 21   | L'utilisateur entre un autre email |      |                                                              |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la page d'inscription sans validation                 |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche un message de succès et enregistre l'utilisateur.              <u>Annulation :</u> Aucun envoie n’est effectué, un message signale que le formulaire n’a pas été envoyé. |



## Connexion

|         Nom          |                  Connexion                  |
| :------------------: | :-----------------------------------------: |
|        Numéro        |                      2                      |
|        Acteur        |                 Utilisateur                 |
| Dernière mise à jour |                  5/05/2019                  |
|     Précondition     |       l'utilisateur doit être inscrit       |
|      Démarrage       | L'utilisateur accède à la page de connexion |

#### Scénario nominal

|      | Utilisateur                           |      | Système                                          |
| ---- | ------------------------------------- | ---- | ------------------------------------------------ |
|      |                                       | 10   | Affiche la page de connexion                     |
| 20   | L'utilisateur rentre son email        |      |                                                  |
| 30   | L'utilisateur rentre son mot de passe |      |                                                  |
|      |                                       | 30   | Vérifie les informations                         |
|      |                                       | 50   | Crée une session de connexion pour l'utilisateur |

#### Scénario alternatif

|      | Utilisateur                                          |      | Système |
| ---- | ---------------------------------------------------- | ---- | ------- |
| 21   | L'utilisateur décide de quitter la page de connexion |      |         |

#### Scénario d'exception

|      | Utilisateur                                    |      | Système                                                      |
| ---- | ---------------------------------------------- | ---- | ------------------------------------------------------------ |
|      |                                                | 31   | Le système ne trouve aucun email correspondant               |
|      |                                                | 32   | le système renvoie un message d'erreur indiquant à l'utilisateur que l'email ou le mot de passe renseigné n'est pas correct |
| 21   | L'utilisateur entre à nouveau ses informations |      |                                                              |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la page de connexion sans validation                  |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche un message de succès et créer une session.                      <u>Annulation :</u> Aucun envoie n’est effectué, un message signale que le formulaire n’a pas été envoyé. |



## Déconnexion

|         Nom          |                     Déconnexion                      |
| :------------------: | :--------------------------------------------------: |
|        Numéro        |                          3                           |
|        Acteur        |                     Utilisateur                      |
| Dernière mise à jour |                      5/05/2019                       |
|     Précondition     |           L'utilisateur doit être connecté           |
|      Démarrage       | L'utilisateur clique sur le boutton "se déconnecter" |

#### Scénario nominal

|      | Utilisateur |      | Système                                           |
| ---- | ----------- | ---- | ------------------------------------------------- |
|      |             | 10   | Supprime la session de connexion de l'utilisateur |
|      |             | 20   | Affiche un message de succès                      |

#### Scénario alternatif

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 11   | Le système detecte que la session arrive à la fin            |
|      |             | 21   | le système renvoie un message indiquant à l'utilisateur qu'il à été déconnecté |

#### Scénario d'exception

|      | Utilisateur |      | Système                                            |
| ---- | ----------- | ---- | -------------------------------------------------- |
|      |             | 11   | Le système ne trouve aucune session correspondante |
|      |             | 21   | le système renvoie un message d'erreur             |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la page EatRoulette                                   |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale:</u> La session est supprimé et l'utilisateur et redirigé sur la page de connexion |

## Faire une demande au support

|         Nom          |             Faire une demande au support             |
| :------------------: | :--------------------------------------------------: |
|        Numéro        |                          4                           |
|        Acteur        |                     Utilisateur                      |
| Dernière mise à jour |                      5/05/2019                       |
|     Précondition     |          L'utilisateur doit être connecter           |
|      Démarrage       | L'utilisateur accède à la page de demande au support |

#### Scénario nominal

|      | Utilisateur                             |      | Système                               |
| ---- | --------------------------------------- | ---- | ------------------------------------- |
|      |                                         | 10   | Affiche la page de demande au support |
| 20   | L'utilisateur choisi le type de demande |      |                                       |
| 30   | L'utilisateur renseigne les champs      |      |                                       |
|      |                                         | 40   | Envoie les données en bases           |

#### Scénario alternatif

|      | Utilisateur                                             |      | Système |
| ---- | ------------------------------------------------------- | ---- | ------- |
| 21   | L’utilisateur décide de retourner sur la page d'acceuil |      |         |

#### Scénario d'exception

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 41   | un ou plusieur champs sont manquant                          |
|      |             | 42   | le système renvoie un message d'erreur à l'utilisateur indiquant quels champs est vide |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | L'utilisateur quite la page de demande au support            |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche un message de succès et enregistre la demande.              <u>Annulation :</u> Aucun envoie n’est effectué, un message signale que le formulaire n’a pas été envoyé. |

## Definir sa situation

|         Nom          |                     Definit sa situation                     |
| :------------------: | :----------------------------------------------------------: |
|        Numéro        |                              5                               |
|        Acteur        |                         Utilisateur                          |
| Dernière mise à jour |                          8/05/2019                           |
|     Précondition     |               L'utilisateur doit être connecté               |
|      Démarrage       | L'utilisateur accède à la page de définition de sa situation |

#### Scénario nominal

|      | Utilisateur                           |      | Système                                                     |
| ---- | ------------------------------------- | ---- | ----------------------------------------------------------- |
|      |                                       | 10   | Affiche la page d'utilisation de définition de sa situation |
| 20   | L'utilisateur renseigne sa situation  |      |                                                             |
| 30   | L'utilisateur renseigne ses allergies |      |                                                             |
|      |                                       | 40   | Envoie les données en base                                  |

#### Scénario alternatif

|      | Utilisateur                                |      | Système |
| ---- | ------------------------------------------ | ---- | ------- |
| 21   | L'utilisateur retourne à la page d'acceuil |      |         |

#### Scénario alternatif

|      | Utilisateur                         |      | Système                    |
| ---- | ----------------------------------- | ---- | -------------------------- |
| 21   | L'utilisateur modifie sa situation  |      |                            |
| 31   | L'utilisateur modifie ses allergies |      |                            |
|      |                                     | 41   | Envoie les données en base |

#### Scénario d'exception

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 41   | un ou plusieur champs sont manquant                          |
|      |             | 42   | le système renvoie un message d'erreur à l'utilisateur indiquant quels champs est vide |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | L'utilisateur quite la page de définition de sa situation    |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche un message de succès et enregistre la situation.                     <u>Update :</u> Affiche un message de succès et enregistre la nouvelle situation. |



## Utiliser la roulette

|         Nom          |                    Utiliser la roulette                     |
| :------------------: | :---------------------------------------------------------: |
|        Numéro        |                              6                              |
|        Acteur        |                         Utilisateur                         |
| Dernière mise à jour |                         10/05/2019                          |
|     Précondition     |                              /                              |
|      Démarrage       | L'utilisateur accède à la page d'utilisation de la roulette |

#### Scénario nominal

|      | Utilisateur                                                  |      | Système                                                      |
| ---- | ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
|      |                                                              | 10   | Affiche la page d'utilisation de la roulette                 |
| 20   | L'utilisateur choisi la liste de restaurant qu'il souhaite utiliser |      |                                                              |
| 30   | L'utilisateur lance la roulette                              |      |                                                              |
|      |                                                              | 40   | le système renvoie un restaurant de la liste de façon aléatoire en fonction de la situation de l'utilisateur |

#### Scénario alternatif

|      | Utilisateur                                               |      | Système                                                      |
| ---- | --------------------------------------------------------- | ---- | ------------------------------------------------------------ |
| 21   | l'utilisateur choisi la liste d'ami qu'il souhaite convié |      |                                                              |
| 31   | L'utilisateur lance la roulette                           |      |                                                              |
|      |                                                           | 41   | le système met en commun les situations des utilisateurs conviés |
|      |                                                           | 42   | le système renvoie un restaurant de la liste de façon aléatoire en fonction des situations des utilisateurs |
|      |                                                           | 43   | le système affiche le match entre les sutiations fournies et le restaurant proposé en % |

#### Scénario d'exception

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 41   | la situation des utilisateurs n'est pas définis              |
|      |             | 42   | Le système renvoie un message d'erreur indiquant qu'un ou plusieur situation ne sont pas définis |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la page d'utilisation de la roulette sans validation  |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche un restaurant avec ses information.                                                   <u>Fin alternative :</u> Affiche un restaurant avec ses information et envoie une notification aux utilisateur conviés. |



## Gérer ses liste de restaurant

|         Nom          |                Gérer sa liste de restaurant                |
| :------------------: | :--------------------------------------------------------: |
|        Numéro        |                             7                              |
|        Acteur        |                        Utilisateur                         |
| Dernière mise à jour |                         10/05/2019                         |
|     Précondition     |                             /                              |
|      Démarrage       | L'utilisateur accède à la page de ses liste de restaurants |

#### Scénario nominal

|      | Utilisateur                                                  |      | Système                                                   |
| ---- | ------------------------------------------------------------ | ---- | --------------------------------------------------------- |
|      |                                                              | 10   | Affiche la page contenant les listes de restaurants       |
| 20   | L'utilisateur choisi la liste de resaurant qu'ils souhaite gérer |      |                                                           |
|      |                                                              | 30   | le système affiche les restaurants contenue dans la liste |
| 40   | L'utilisateur à la possibilité d'ajouter, de modifier ou de supprimer un restaurant |      |                                                           |

#### Scénarios alternatifs

|      | Utilisateur                                                  |      | Système |
| ---- | ------------------------------------------------------------ | ---- | ------- |
| 21   | L'utilisateur décide de quitter la page de listing de ses listes de restaurants |      |         |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la page de listing de ses listes de restaurants |
| -------------------------- | ------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche la liste des restaurants. |

## Ajout d'un restaurant à une liste

|         Nom          |          Gérer sa liste de restaurant          |
| :------------------: | :--------------------------------------------: |
|        Numéro        |                       8                        |
|        Acteur        |                  Utilisateur                   |
| Dernière mise à jour |                   10/05/2019                   |
|     Précondition     |        L'utilisateur doit être connecté        |
|      Démarrage       | L'utilisateur accède à sa liste de restaurants |

#### Scénario nominal

|      | Utilisateur                                                  |      | Système                                            |
| ---- | ------------------------------------------------------------ | ---- | -------------------------------------------------- |
|      |                                                              | 10   | Affiche la page contenant la liste des restaurants |
| 20   | L'utilisateur clicque sur "ajouter un restaurant"            |      |                                                    |
|      |                                                              | 30   | Le système affiche une barre de recherche          |
| 40   | L'utilisateur renseigne le restaurant qu'il souhaite ajouter à sa liste |      |                                                    |
|      |                                                              | 50   | le système ajoute le restaurant à la liste en base |

#### Scénarios alternatifs

|      | Utilisateur                                         |      | Système |
| ---- | --------------------------------------------------- | ---- | ------- |
| 11   | L'utilisateur décide de quitter la page de la liste |      |         |

#### Scénario d'exception

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 51   | Le système ne trouve pas le restaurant recherché             |
|      |             | 52   | Le système envoie un message à l'utilisateur afin de lui indiqué qu'aucun restaurant n'a été trouvé et de lui proposer de le rajouter sur EatRoulette |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la liste des restaurants                              |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche et update la liste des restaurants. |

## Suppression d'un restaurant d' une liste

|         Nom          |          Gérer sa liste de restaurant          |
| :------------------: | :--------------------------------------------: |
|        Numéro        |                       9                        |
|        Acteur        |                  Utilisateur                   |
| Dernière mise à jour |                   10/05/2019                   |
|     Précondition     |        L'utilisateur doit être connecté        |
|      Démarrage       | L'utilisateur accède à sa liste de restaurants |

#### Scénario nominal

|      | Utilisateur                                       |      | Système                                                      |
| ---- | ------------------------------------------------- | ---- | ------------------------------------------------------------ |
|      |                                                   | 10   | Affiche la page contenant la liste des restaurants           |
| 20   | L'utilisateur clique sur "supprimer le resaurant" |      |                                                              |
|      |                                                   | 30   | Le système affiche un message de confirmation dans une popup |
| 40   | L'utilisateur confirme la suppression             |      |                                                              |
|      |                                                   | 50   | le système désaffiche la popup et supprime le restaurant à la liste en base |

#### Scénarios alternatifs

|      | Utilisateur                                                 |      | Système                        |
| ---- | ----------------------------------------------------------- | ---- | ------------------------------ |
| 41   | L'utilisateur annule lors de la confirmation de suppression |      |                                |
|      |                                                             | 51   | le système désaffiche la popup |

#### Scénario d'exception

|      | Utilisateur |      | Système                                                      |
| ---- | ----------- | ---- | ------------------------------------------------------------ |
|      |             | 51   | Le système ne trouve pas le restaurant recherché             |
|      |             | 52   | Le système envoie un message à l'utilisateur afin de lui indiqué qu'aucun restaurant n'a été trouvé et de lui proposer de le rajouter sur EatRoulette |

#### Fin du cas d'utilisation

| Arrêt de cas d'utilisation | Quitte la liste des restaurants                              |
| -------------------------- | ------------------------------------------------------------ |
| Post-condition             | <u>Fin normale :</u> Affiche et update la liste des restaurants. |

---

© EatRouletteDev-2020