# Etude de la faille Evil Twin

## Introduction

La faille Evil Twin est une technique de piratage de réseau sans fil qui consiste à créer une réplique d'un point d'accès WiFi légitime pour tromper les utilisateurs et les inciter à se connecter à un réseau malveillant.  
Lorsque les utilisateurs se connectent à cette réplique, les pirates peuvent voler des informations sensibles, comme des mots de passe ou des données de carte de crédit, ou encore rediriger les utilisateurs vers des sites web malveillants.  

![Schema](https://www.okta.com/sites/default/files/media/image/2022-08/EVILTWINATTACK_GRAPHIC_1.png)

## 1. Partie de cours

Afin de mieux appréhender cette faille, un cours est disponible dans au fichier `docs/cours.pdf`. Nous vous recommandons de le lire avant de continuer.

## 2. TP

### 2.1. Installation de la faille

Le point d'accès malveillant est mis en place sur une carte ESP8266 qui est fournie.  
Il est donc nécessaire pour l'étudiant d'avoir préalablement téléchargé l'IDE Arduino sur l'ordinateur utilisé pour ce TP.  

Le code utilisé est une adaptation du code trouvable au lien lien suivant : https://github.com/M1z23R/ESP8266-EvilTwin.  
Le code Arduino utilisé dans ce projet est utilisé pour configurer et contrôler le module ESP8266. Il utilise des bibliothèques telles que ESP8266WiFi et ESP8266WebServer pour gérer les connexions Wi-Fi et les requêtes HTTP. Le code définit également des variables pour stocker les informations de connexion du point d'accès, comme le nom du réseau et le mot de passe. Il y a une fonction setup() qui configure le module ESP8266 en tant que point d'accès et définit les paramètres de sécurité pour le point d'accès. Il y a également une fonction loop() qui gère les requêtes HTTP entrantes et dirige les utilisateurs vers la page web appropriée en fonction de leur demande.

Une fois ces librairies téléchargées vous pouvez maintenant exécuter le code contenu dans `setup/setup.ino`. Il est bien sur nécessaire de le téléverser vers le port menant vers la carte ESp8266.  

Une fois le module ESP8266 configuré, le code permet de créer un point d'accès Wi-Fi qui ressemble à un point d'accès légitime en utilisant les informations de connexion stockées dans les variables. Les utilisateurs qui se connectent à ce point d'accès seront redirigés vers une page web qui affiche une publicité ou qui demande des informations de connexion. Le code enregistre également les informations de connexion capturées dans une variable pour une utilisation ultérieure.   
Une démonstration de son utilisation est accessbile via `setup/demo.mp4`.

### 2.2. Résolution de la faille

Il existe plusieurs programmes qui peuvent aider à contrer les attaques Evil Twin. Ces programmes incluent :  
* Logiciels de sécurité pour la connexion Wi-Fi : Ces logiciels peuvent détecter les points d'accès suspects et vous alerter si vous vous connectez à un Evil Twin.
* VPN (Réseau privé virtuel) : Les VPN cryptent vos données et vous protègent contre les attaques Evil Twin en vous connectant à un réseau sécurisé.
* Logiciels de gestion de réseau : Ces logiciels peuvent vous aider à identifier les points d'accès sur votre réseau et à vérifier la validité de la connexion.
* Logiciels de détection d'intrusion : Ces logiciels peuvent vous aider à détecter les tentatives d'intrusion sur votre réseau et à alerter les administrateurs en cas de menace.
* Logiciels de sécurité pour les réseaux Wi-Fi : Ces logiciels peuvent vous aider à protéger vos réseaux Wi-Fi contre les attaques Evil Twin en utilisant des protoc
de sécurité tels que WPA2 et en configurant des paramètres de sécurité appropriés.
* Systèmes de prévention contre les intrusions Wi-Fi (WIPS) : Ces systèmes peuvent surveiller en temps réel les activités sur votre réseau Wi-Fi et détecter les tentatives d'intrusion, y compris les attaques Evil Twin.
* Utiliser des firewalls : Les firewalls peuvent bloquer les connexions non autorisées et aider à protéger contre les attaques Evil Twin.  

Il est important de noter que la sécurité d'un réseau dépend de la combinaison de plusieurs mesures de sécurité. Il est donc important de combiner différentes solutions pour protéger efficacement contre les attaques Evil Twin. Il est également important de maintenir ces programmes à jour et de les configurer correctement pour maximiser leur efficacité.

## 3. Test de connaissances

Afin de tester vos connaissances, un qcm est disponible via `docs/qcm.pdf`.


