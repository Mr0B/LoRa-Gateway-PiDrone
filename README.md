# LoRa-Gateway-PiDrone

Ce projet est réalisé dans le cadre du module Communication Sans Fil en License 1 à l'Université Nice Sophia Antipolis.

# Description:

Le projet que nous réalisons est un Drone pouvant se déplacer automatiquement à partir d'un code (python) disposant d'une carte ESP32 utilisant le protocole de communication LoRa. Il doit aussi posséder la technologie de recharge sans fil (wireless charging).

# Matériel:
- Wireless Charging Module 5V/1A-DFRobot
- Drone Ryze Tello (DJI) full pack avec chargeur,3 batteries et cable mini-usb
- SX1276 ESP32 TTGO board
- Socle imprimé en 3D pour le module de la charge sans fil.

# Logiciel:
- Software Development Kit du drone
- Langage Python (pour les commandes du drone)
- Arduino IDE (pour la carte ESP32)
- Éditeur de texte (pour les commandes du drone)
- Terminal (sur mac (pour éxecuter les commandes du drone))

# Résumé du projet:

Le drone utilise des capteurs infrarouge pointés vers le bas permettant d'évaluer la distance depuis le sol, il se pose automatiquement si le pourcentage de batterie est trop faible et se lève si un élement vient gêner en dessous.
Et enfin, grâce aux capteurs, le drone essaye de se stabiliser toujours à la même position, même si on le fait bouger pendant qu'il vole, mais les capteurs fonctionnent réellement que quand le drone a terminé son décollage, soit environ à 20 cm du sol.
La caméra n'est pas utilisée pour ce projet.

Le drone possédant déjà un kit de developpement (SDK), le code écrit en langage python permet alors la communication avec le drone depuis l'ordinateur simplement avec une liste de commandes du SDK dans un fichier .txt, le terminal (sur mac) est utilisé pour éxecuter le code et débuter la communication des commandes. Biensur, tout cela est impossible si l'ordinateur n'est pas connecté à la wifi du drone.
Le terminal va afficher les commandes utilisés et reçus par le drone, toutes les erreurs (si il y en a) et pourra également montrer le pourcentage de batterie par exemple.

La carte ESP32 est utilisé comme une Gateway LoRa ce qui permettra pour d'autres projets d'utiliser le protocole de communication LoRA. Elle doit pouvoir voler avec le drone et alimentée depuis la même batterie.

Et enfin, pour la recharge sans fil, le drone doit pouvoir se recharger automatiquement avec du 5V pour 1A tout en se posant voir même en étant légerement au dessus. Une partie doit être directement relié à la batterie du drone et pouvoir s'alimenter avec la deuxième partie posé sur le socle imprimé au sol.
