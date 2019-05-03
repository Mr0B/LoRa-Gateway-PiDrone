# Comment utiliser le code python pour la communication avec le drone ?

# Github utilisé: https://github.com/dji-sdk/Tello-Python

# Introduction
Le drone pèse environ 80g, possède une wifi, une bluetoothl, une caméra et des capteurs infrarouge permettant d'évaluer la distance avec le sol. J'utilise pour ce projet le langage python qui va permettre de communiquer depuis l'ordinateur en faisant executer un fichier .txt avec un terminal.

# Étape 1:
Ecrivez les commandes souhaitées pour la manipulation du drone dans le fichier "command.txt", voici un exemple:

```
command
takeoff
land
```

La commande "command" doit être écrite avant toute autre commande, c'est ce qui va permettre d'indiquer au drone qu'il s'agit bien d'un script de commandes.
Ensuite, la deuxième commande "takeoff" est utilisée pour faire monter automatiquement le drone d'environ 20cm depuis le sol tandis que "land" permettra de le faire atterir.

# Étape 2:
Le script enverra directement une commande à la fois, lorsqu'une commande est reçu par le drone, la prochaine commande est envoyée immédiatement.
Pour ajouter un délai entre deux commandes, il suffit d'écrire la commande "delay" suivi du nombre de secondes qui est maximum de "17".

Exemple: "delay 5"
pour 5 secondes

# Étape 3:
Démarrer le script en ouvrant un terminal puis avec la commande:

```
python tello_test.py command.txt
```
La fenêtre du terminal indiquera chaque commande du script puis stockera apres l'execution un fichier log dans un dossier log.

Les autres commandes possibles sont indiquées dans le fichier SDK du dossier drone.

# Difficultés rencontrées

La première difficulté rencontrée à été de trouver un code parfait pour notre projet, j'avais tout d'abord essayé d'utiliser le logiciel 3D unity pour tenter la communication en faisant imaginer un environnement en 3d autours du drone mais cela s'est avéré être trop gourmand et bien trop compliqué, demandant beaucoup d'installations de fichiers.

Au final, j'avais trouvé exactement le code qu'on recherchait permettant simplement une communication en python par la wifi du drone. Il fallait ensuite construire son propre code en utilisant les commandes du SDK.

La deuxième difficulté rencontrée été le fait que le SDK avait certaines limites, comme par exemple une hauteur maximale de vol et il ne pouvait pas rester plusieurs minutes à exactement la même position en hauteur, soit maximum 17 secondes environ.
Pour contourner cela, il a fallut modifier les commandes pour permettre de rester plusieurs minutes, pour cela, il a fallu d'abord envoyer le drone a une position puis répéter plusieurs commandes à la fois, c'est à dire le faire monter tout le temps de 1cm puis de redescendre de 1cm, ce qui au final ne pouvait même pas se remarquer à l'oeil nu.

# En conclusion,
le code marche très bien, le drone peut au moins rester stable pendant 10 min au vol avec une batterie, il n'y a pas besoin de compléter le code à moins pour des projets plus précis.
