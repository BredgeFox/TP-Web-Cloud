# TP-Web-Cloud
TP noté du module de web and cloud dans le cadre du master MIAGE première année (2022).
TP réalisé par 

## Projet TinyPet

Dans le cadre du module "Développement d'applications sur le CLOUD", nous avons du réaliser une application web pour la gestion de pétitions en prenant exemple sur des sites tel que https://www.change.org/ et https://secure.avaaz.org/page/en/.

Ce README à pour objectif de vous présenter les fonctions implémenté ainsi que les liens et aperçus de l'application. 

Ce projet a été réalisé par BÉRANGER Grégoire et AUBERT Quentin.
Face au diverses difficultés techniques que notre groupe et nos camarades avons rencontrés pour faire fonctionner la nouvelle API google `accounts.google.com/gsi/client` et au problèmes supplémentaire qu'elle posait (notament par rapport à la communication avec la parti API de l'application) par rapport au temps qu'il nous restait, à partir du moment ou nous avons tous eux connaissance d'un moyen de faire fonctionner l'api `apis.google.com/js/platform.js` (plus simple). Nous avons fait le choix de repartir d'un projet réaliser par un groupe d'étutiant de l'année 2021 (BARRY Boubacar, BOULID Hamza, HADJI Thiziri, NING Binbing) dont le git est accessible avec le lien suivant https://github.com/thiziri-HADJI/petitions. 

##Liens
Lien de l'application
https://gregoire-quentin-wc.ew.r.appspot.com
Lien menant à la création d'un jeu de données pour l'application (30 pétitions)
https://gregoire-quentin-wc.ew.r.appspot.com/petitionInit

## Fonctionnalités implémentées

Permis les fonctionalités existantes sur l'application figure :

<u>Sans réserve de connection</u>
<li>Consulter les pétitions les plus récentes</li>
<li>Consulter les pétitions les plus signées</li>
<li>Rechercher une pétition à partie de mots clé figurant dans le titre ou en tag</li>
<li>Se connecter vie l'api Google `apis.google.com/js/platform.js`</li>

<u>Sous réserve d'être connecté</u>
<li>Créer des pétitions</li>
<li>Consulter les pétitions (créée)<li>
<li>Éditer des pétitions (créée)</li>
<li>Supprimer des pétitions (créée)</li>
<li>Signer des pétitions (non_créée)</li>
<li>Retirer sa signature de pétition (non_créée et signée)</li>
<li>Se connecter</li>



##Performances

Nous n'avons pas eu le temps de réaliser des tests de performance pertinent de le délai qu'il nous restais.
Cependant nous pouvons indiquer que l'affichage des pages est chargé en moins d'une secondes mais que le chargement des données concernant ces pages peuvent prendre nettement plus de temps ce qui induis un problème de performance.

##Entités présentes dans le datastore

Petition

![image](https://user-images.githubusercontent.com/47324056/170892771-eec06d64-0c30-4ecb-b4fa-c6c282b7ba59.png)

Signature

![image](https://user-images.githubusercontent.com/47324056/170892984-a8d86d44-7cf8-4973-bad5-cea93a482462.png)


User : Entité exploité uniquement dans le cadre de la création du jeu de données à l'aide de https://gregoire-quentin-wc.ew.r.appspot.com/petitionInit

![image](https://user-images.githubusercontent.com/47324056/170892638-64efd822-d623-41eb-b9e2-dfd433143645.png)

##Visuels de l'application

Acceuil / Parcourir les pétitions

<li>Les pétitions récentes</li>
![image](https://user-images.githubusercontent.com/47324056/170893269-0372e709-fc5d-4c9b-af7e-94ebdf3522e6.png)
<li>Les pétitions signés</li>
![image](https://user-images.githubusercontent.com/47324056/170893358-c4647182-448d-4f67-be7f-a90f9db78c8d.png)

Mes petitions

<li>Pétition(s) lancée(s)</li>
![image](https://user-images.githubusercontent.com/47324056/170893307-1c828cec-446e-4ac9-8cd5-81091526b1d4.png)
<li>Pétition(s) signée(s)</li>
![image](https://user-images.githubusercontent.com/47324056/170893663-f4fd7618-7593-4797-8926-7bc16b8da16b.png)

Créer une pétition

![image](https://user-images.githubusercontent.com/47324056/170893322-ca3bdc15-5a80-42d3-97ed-ee789ff6c8dc.png)

Recherche de pétitions

![image](https://user-images.githubusercontent.com/47324056/170893689-c4b5b316-118e-41ca-8ff7-36741585052c.png)

##Problèmes

Parmis les problèmes que nous avons relevé figures:

<li>Le temps de chargement de l'ensemble des pétitions</li>
<li>La présence de pétition qui ont été signé mais que ne le sont plus et qui apparaisent parmis les pétitions signé (nottament dans Mes petitions</li>
<li>La présence de pétition qui n'ont jamais été signées parmis les pétitions signées de Parcourir les pétitions</li>
<li>Une recherche très récelcitrante sur les mot clés</li>

##Conclusion 
Ce projet nous a permis de prendre pleinement conscience des difficultés de déploiement d'une 
application web.

En effet les méthodes d'authentification de l'API google nous ont posé problème. Notamment 
avec la mise en place de leurs nouvelles API rendant l'ancienne difficilement exploitable. 
Nous avons perdu un temps considérable à essayer de mettre la mettre en place. 
En effet, les données rendues par la fonction de connexion étant chiffrées, et la documentation en ligne 
relativement rudimentaire.

De plus l'utilisation de mythril nous à également rendu la tache complexe. Il s'agissait de 
notre première expérience de développement avec ce mode de programmation. Cela à rendu la
réalisation du front problématique et la connexion avec l'api PetitionEndpoint extrêmement 
difficile.
