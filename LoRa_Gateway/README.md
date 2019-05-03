# LoRa Gateway - TTGO ESP32 SX1276 

### Introduction : 

Pour faire d'un drone une gateway LoRa mobile, il faut bien sûr une gateway qui peut être transportée par le drone. Notre drone est le DJI Tello, ayant une charge utile maximale de 59 grammes, or qu'il faut transporter la gateway, l'antenne, et le module de rechargement sans fils. Ainsi, il faut choisir une carte 'lightweight' avec la capacité de gateway LoRa. D'où notre choix de carte: [TTGO ESP32 SX1276](https://www.ebay.com/itm/152827874001?ul_noapp=true)

### Mise en place de la gateway :

Après avoir cherché pendant un moment, j'ai trouvé le github par [things4u - ESP-1ch-Gateway-v5.0](https://github.com/things4u/ESP-1ch-Gateway-v5.0), et les tutoriels ([1](https://learn.sparkfun.com/tutorials/esp32-lora-1-ch-gateway-lorawan-and-the-things-network/all) et [2](https://www.hackster.io/Arn/single-channel-ttn-lora-gateway-and-nodes-with-esp32-sx1276-709612)). Ceux-ci m'ont permis d'avoir les fichiers nécessaires pour programmer notre carte, avec quelques modifications nécessaires. Dans le github on trouve les libraries nécessaires pour tout mettre en place. Les deux fichiers les plus importants à modifier pour la configuration de notre carte esp32 sont ESP-sc-gway.h et loramodem.h

(*NB: dans le fichier ESP-sc-gway.h il faut entrer le SSID et mot de passe du réseau wifi qu'on utilise dans le deuxième pair de guillemets)

![Capture écran du code:](https://imgur.com/a/mOP9O7Y)

### Difficultés rencontrés :

Comme je suis un novice sur Arduino IDE, il m'a fallu beaucoup de temps pour avoir un code qui marche et qui upload correctement. De plus, Arduino IDE sur Linux a posé quelques soucis aussi avec des listes incomplets. Cette carte manque de documentation facilement accessible aussi.

### Ouverture sur le projet :

Notre carte ne s'agit que d'une demi gateway, car elle n'est que capable de faire 1 channel/une fréquence. Si l'on avait un drone doté d'une charge utile bien supérieur, on aurait pu avoir une vraie gateway avec un raspberry pi, avec plus de fréqueces disponibles.
