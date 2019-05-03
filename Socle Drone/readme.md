# I-Première réflexion sur la charge sans fil:

Pour automatiser le  drone, nous avions penser à un socle, possédant une recharge sans fil, je me suis donc consacré à cette partie.

# II-Etapes:
 
 ###  Etape 1:
 J'ai d'abord réfléchi à faire mes bobines moi-même, mais face à la difficultés d'une tel idée et le temps que nous avions j'ai préféré me rabbatre sur un modèle déja existant.

Le principe de base de la recharge sans fil est décrit ci-dessous:
![Le principe de base de la recharge sans fil est décrit ci-dessous:](https://cdn57.androidauthority.net/wp-content/uploads/2013/04/magnetic-fields.png)

 ### Etape 2:
 J'ai donc recherché un modèle de charge sans fil dans le commerce, nous nous sommes dirigé vers la carte suivante: 
Wireless Charging Module 5V/1A-DFRobot (https://www.dfrobot.com/product-1284.html?search=wireless%20charging&description=true), malgré le fait que ce module n'avait pas le bon ampérage, nous avons ddéécidé que cela ralentirait uniquement le temps de recharge.

 ### Etape  3:
 Nous avons reçu le drone, et nous avons commencé à réfléchir au câblage et à comment adapter les 4 pins utiliser par le drone pour la recharge avec le module de charge sans fil, et avec la gateway.
 
 ## Etape 4:
 La modélisation 3D du socle passa par plusieurs étapes, il y a eu un soucis lié au proportion pour designer la pièce, et j'ai ensuite choisi de  remplacé les tunnels pour les cables par des gouttière nous donnant alors un accès plus façile au câble. Puis nous l'avons imprimer sur l'imprimante 3D.
 
 ## Etape 5:
 Plusieurs difficultés sont apparus pour la cablage, ma première idée était de retirer le module caméra pour câbler dans l'espace que ça aurait laisser, mais retirer ce module est impossible sans le découper. Nous avons donc réfléchi sur comment creuser la coque pour faire passer les câbles sans géné tout le reste. (


# III-Difficultés rencontrés:

Les premières difficultés on été pour la création de nos propres bobines de charge sans fil, ce qui à été vite abbandonné, j'ai ensuite recherché des bobines parfaitement identique à nos besoins, ce qui fut impossible, nous sommes rabbatu sur le module 5V1A par DFRobot.
Ensuite des soucis sont apparu pour la modélisation 3D, sur des tout petits modèles, j'ai trouvé une solution en modélisant sur TinkerCad en 10 fois plus gros et creusant les tunnels, puis en diminuant les proportions par 10.
Pour faciliter l'accès  au câble j'ai décidé de passer d'un tunnel à une gouttière.
Un dernier problème est apparu car la pièce faisait réagir le drone qui la considère comme un obstacle.
Avec plus de temps nous aurions fais les cablages pour combiner les 3 modules (Gateway/Drone/Recharge), (voir Etape 5).

# IV-Possible dévellopement:

Sur le cours terme, il faudrait reimprimer le socle de tel sorte à ce qu'il ne soit pas considérer comme un obstacle.
Ainsi que de faire les branchements, creuser deux trou assez fin dans le dessous du drone.

Sur le long terme, il faudrait améliorer le socle, pour par exemple inclure une batterie avec une manière de la recharger comme un panneau solaire, ainsi qu'une carte Rasberry-Pi pour gérer la commande du drone.
