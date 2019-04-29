Utilisation du code python pour le drone dji tello:

Étape 1:
Ecrivez les commandes souhaitées pour la manipulation du drone dans le fichier "command.txt", voici un exemple:

```
command
takeoff
land
```

La commande "command" doit être écrite avant toute autre commande, c'est ce qui va permettre d'indiquer au drone qu'il s'agit bien d'un script de commandes.
Ensuite, la deuxième commande "takeoff" est utilisée pour faire monter automatiquement le drone d'environ 20cm depuis le sol tandis que "land" permettra de le faire atterir.

Étape 2:
Le script enverra directement une commande à la fois, lorsqu'une commande est reçu par le drone, la prochaine commande est envoyée immédiatement.
Pour ajouter un délai entre deux commandes, il suffit d'écrire la commande "delay" suivi du nombre de secondes qui est maximum de "17".

Exemple: "delay 5"
pour 5 secondes

Étape 3:
Démarrer le script en ouvrant un terminal puis avec la commande:

```
python tello_test.py command.txt
```
La fenêtre du terminal indiquera chaque commande du script puis stockera apres l'execution un fichier log dans un dossier log.

Les autres commandes possibles sont indiquées dans le fichier SDK du drone.
