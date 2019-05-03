# LoRa-Gateway-PiDrone

Ce projet est réalisé dans le cadre du module Communication Sans Fil en License 1 à l'Université Nice Sophia Antipolis.

# Description:

Le projet que nous réalisons est un Drone pouvant se déplacer automatiquement à partir d'un code (python) disposant d'une carte ESP32 utilisant le protocole de communication LoRa. Il doit aussi posséder la technologie de recharge sans fil (wireless charging).

# Matériel:
- Wireless Charging Module 5V/1A
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

Le drone possédant déjà un kit de developpement (SDK), le code écrit en langage python permet alors d'éxecuter simplement une liste de commandes du SDK dans un fichier .txt à partir d'un terminal sur Mac. Le langage Python est utilisé pour la communication wifi avec le drone.
La carte ESP32 est utilisé comme une Gateway LoRa ce qui permettra pour d'autres projets la communication en LoRa.
