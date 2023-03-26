# Matrice Led Animation (base)
## Materiel necesaire
voici un liste du materiels minimum necesaire pour ce montage
* ESP32 (par exemple, ESP32-DevKitC ou NodeMCU-32S)
* Matrice de LED RGB (Adafruit NeoPixel ou compatible)
* Alimentation électrique adaptée pour la matrice de LED (5V, avec un courant suffisant)
* Câbles de connexion (pour relier l'ESP32 et la matrice de LED)
* Ordinateur avec Arduino IDE installé (pour la programmation de l'ESP32)
* Câble micro USB (pour connecter l'ESP32 à l'ordinateur)
* Imprimante 3D pour imprimer le boitier

## Instalation Logiciels

Installer Arduino IDE :
a. Accédez au site officiel d'Arduino à l'adresse https://www.arduino.cc/en/software et téléchargez la dernière version d'Arduino IDE pour votre système d'exploitation (Windows, macOS ou Linux).
b. Installez Arduino IDE en suivant les instructions d'installation pour votre système d'exploitation.

* Ajouter la prise en charge de l'ESP32 :

  a. Ouvrez Arduino IDE.

  b. Allez dans Fichier -> Préférences (ou Arduino -> Préférences sur macOS).

  c. Dans le champ "URL de gestionnaire de cartes supplémentaires", ajoutez cette URL : https://dl.espressif.com/dl/package_esp32_index.json et cliquez sur "OK".

  d. Allez dans Outils -> Type de carte -> Gestionnaire de cartes.

  e. Dans la barre de recherche, tapez "esp32" et installez "esp32" par Espressif Systems.

* Installer les bibliothèques nécessaires :

  a. Allez dans Croquis -> Inclure une bibliothèque -> Gérer les bibliothèques.

  b. Dans la barre de recherche, tapez "Adafruit NeoPixel" et installez la bibliothèque Adafruit NeoPixel.

  c. Dans la barre de recherche, tapez "AsyncTCP" et installez la bibliothèque AsyncTCP par Hristo Gochkov.

  d. Dans la barre de recherche, tapez "ESPAsyncWebServer" et installez la bibliothèque ESPAsyncWebServer par Hristo Gochkov.

* Configurer l'ESP32 :

  a. Connectez votre ESP32 à l'ordinateur à l'aide d'un câble micro USB.

  b. Dans Arduino IDE, allez dans Outils -> Type de carte et sélectionnez le modèle de votre ESP32 (par exemple, "DOIT ESP32 DEVKIT V1").

  c. Allez dans Outils -> Port et sélectionnez le port série correspondant à votre ESP32.

Vous êtes maintenant prêt à charger votre code sur l'ESP32.

## Personalisation Programme ESP

* Ouvrir le fichier du projet dans Arduino IDE :

  a. Téléchargez et décompressez le fichier contenant le code source de votre projet.

  b. Localisez et ouvrez le fichier "ProgrammeESPMatriceLedClasic.ino" dans Arduino IDE.

* Modifier les paramètres Wi-Fi et la broche LED :

  a. Dans le fichier "ProgrammeESPMatriceLedClasic.ino", localisez la ligne 17 et remplacez "SSID de votre wifi" par le SSID de votre réseau Wi-Fi.
  Exemple : const char* ssid = "MonReseauWifi";

  b. Sur la ligne 18, remplacez "Mots de passe de votre wifi" par le mot de passe de votre réseau Wi-Fi.
  Exemple : const char* password = "MotDePasseWifi";

  c. (Optionnel) Si vous souhaitez modifier la broche sur laquelle la broche DATA de la matrice LED est connectée, localisez la ligne 7 et changez la valeur de 
  LED_PIN.
  Exemple : #define LED_PIN 14

* Vérifier et téléverser le code :

  a. Cliquez sur le bouton "Vérifier" (coche) dans l'angle supérieur gauche de Arduino IDE pour vérifier que votre code ne contient pas d'erreurs.

  b. Si la vérification réussit, cliquez sur le bouton "Téléverser" (flèche vers la droite) pour téléverser le code sur votre ESP32.

Une fois le téléversement terminé, votre ESP32 devrait être prêt à fonctionner avec les paramètres que vous avez définis.

## Réalisation du montage entre l'ESP32 et la matrice de LEDs :

* cablage

  a. Éteignez votre ESP32 et assurez-vous qu'il n'est pas alimenté avant de commencer le montage.

  b. Identifiez les broches de la matrice de LEDs : généralement, elles sont marquées VCC (alimentation)rouge, GND (masse)blanc et DIN (entrée de données)vert.

  c. Connectez les broches de la matrice de LEDs à l'ESP32 :

      i.   Reliez la broche VCC de la matrice de LEDs à la broche 5V de l'ESP32 (selon la tension de fonctionnement de votre matrice, consultez la documentation de votre matrice de LEDs pour connaître la tension appropriée).
    
      ii. Connectez la broche GND de la matrice de LEDs à la broche GND de l'ESP32.
    
      iii. Connectez la broche DIN de la matrice de LEDs à la broche GPIO définie dans le code (par défaut GPIO 14, définie à la ligne 7 du fichier 
    "ProgrammeESPMatriceLedClasic.ino").

d. (Atention) Si votre matrice de LEDs nécessite une alimentation externe, assurez-vous de connecter l'alimentation externe noir - et rouge + de votre alimentation

Une fois le montage terminé, alimentez votre matrice LED et vérifiez que votre esp fonctione la LEDs s'allume ,surtout ne brancher plus a partir de maintenan l'esp en usb sans avoir alimenter votre matrice LED cela ferais crammer votre esp car il essayerais d'alimenter la matrice led mais il n'est pas assez puisant donc pour injecter un nouveau code soit connecter d'abord l'laim a votre matrice soit debrancher votre matrice de votre esp (c'est pour cela que je conseille d'utiliser des connecteur a 3pin)

si vous avez bien entré vos info de connection wifi et la pin utiliser pour la matrice led celle ci devrais afficher des annimation!
## Bravo
Vous pouvez maintenant utiliser l'interface web pour contrôler les paramètres de l'animation, tels que le nombre de répétitions, le délai entre les animations, la luminosité et la durée de chaque frame. Pour accéder à l'interface web, connectez votre ordinateur ou votre smartphone au même réseau Wi-Fi que l'ESP32 et entrez l'adresse IP de l'ESP32 (affichée dans le moniteur série) dans un navigateur web.

# Matrice Led Animation (création du boitier)

  ## fabriquer votre boitier pour votre matrice
bientot developer

# Matrice Led Animation (Modifier les annimation)

  ## comment crer ses propre animation
bientot developer
