
## Introduction
Les points d'accès (Access Points ou AP) sont des dispositifs essentiels dans les réseaux sans fil (Wi-Fi). Ils permettent aux appareils sans fil de se connecter à un réseau câblé, facilitant ainsi la communication et l'accès aux ressources réseau.

## Définition et Fonctionnement
Un point d'accès (AP) est un appareil réseau qui permet aux dispositifs sans fil, comme les ordinateurs portables, les smartphones et les tablettes, de se connecter à un réseau local (LAN) en utilisant le Wi-Fi. Contrairement à un routeur, un AP ne gère pas le routage des paquets entre différents réseaux, mais il joue un rôle crucial dans la distribution du signal sans fil et dans la gestion des connexions des clients.

### Fonctionnalités de Base
1. **Connectivité Wi-Fi** : Les AP émettent et reçoivent des signaux radio pour permettre aux appareils sans fil de se connecter au réseau.
2. **Pont entre Réseau Câblé et Sans Fil** : Ils sont souvent connectés à un réseau câblé via un port Ethernet, créant ainsi un pont entre les segments filaires et sans fil du réseau.
3. **Gestion des Connexions** : Les AP gèrent les connexions des clients sans fil, assurant la répartition efficace de la bande passante et la gestion des canaux pour minimiser les interférences.

### Types de Points d'Accès
1. **Autonomes (Standalone APs)** : Ces APs fonctionnent de manière indépendante et sont configurés et gérés individuellement.
2. **Centralisés (Controller-Based APs)** : Ces APs sont gérés par un contrôleur centralisé, facilitant la gestion et la configuration d'un grand nombre de points d'accès.
3. **Basés sur le Cloud** : Les APs basés sur le cloud sont gérés via des plateformes de gestion en ligne, offrant une flexibilité et une scalabilité accrues.

## Protocoles et Standards
Les points d'accès utilisent différents standards Wi-Fi définis par l'IEEE (Institute of Electrical and Electronics Engineers). Les principaux standards sont :
- **802.11a** : Offre des débits jusqu'à 54 Mbps dans la bande 5 GHz.
- **802.11b** : Offre des débits jusqu'à 11 Mbps dans la bande 2.4 GHz.
- **802.11g** : Offre des débits jusqu'à 54 Mbps dans la bande 2.4 GHz.
- **802.11n** : Offre des débits jusqu'à 600 Mbps en utilisant les bandes 2.4 GHz et 5 GHz.
- **802.11ac** : Offre des débits jusqu'à 1 Gbps dans la bande 5 GHz.
- **802.11ax (Wi-Fi 6)** : Offre des débits jusqu'à 10 Gbps en utilisant les bandes 2.4 GHz et 5 GHz avec une meilleure efficacité et capacité.

## Configuration et Sécurité
### Configuration
1. **Paramètres de Base** : SSID (Service Set Identifier), mode de fonctionnement (AP, répétiteur, pont), canal, bande de fréquence.
2. **Sécurité** : Configuration de la sécurité sans fil (WPA2, WPA3), filtrage MAC, et autres mesures de sécurité.

### Sécurité
Les points d'accès doivent être sécurisés pour protéger le réseau contre les accès non autorisés. Les principales mesures de sécurité incluent :
- **WPA2/WPA3** : Protocoles de sécurité pour le chiffrement des données.
- **Filtrage d'adresse MAC** : Restriction des appareils pouvant se connecter à l'AP en fonction de leur adresse MAC.
- **Segmentation de Réseau (VLANs)** : Utilisation de VLANs pour séparer le trafic et renforcer la sécurité.

## Exemples Pratiques
1. **Configuration de Base d’un AP Cisco** :
   ```shell
   interface dot11radio 0
   ssid MonReseau
   authentication open
   authentication key-management wpa
   wpa-psk ascii "motdepasse"
   ```

2. **Création d’un VLAN et Association à un SSID** :
   ```shell
   vlan 10
   name VLAN_WiFi
   interface dot11radio 0
   ssid MonReseau
   vlan 10
   ```

## Schéma Illustratif

```plaintext
                +-----------+
                |           |
                |   Routeur |
                |           |
                +-----+-----+
                      |
              +-------+-------+
              |               |
              |   Switch      |
              |               |
              +-------+-------+
                      |
              +-------+-------+
              |               |
              |   Access Point|
              |               |
              +-------+-------+
                      |
          -----------------------
          |       |       |     |
         AP1     AP2     AP3   AP4
```

## Conclusion
Les points d'accès sont des éléments clés pour déployer des réseaux sans fil robustes et performants. Leur configuration correcte et leur gestion sécurisée sont essentielles pour garantir la fiabilité et la sécurité du réseau.
