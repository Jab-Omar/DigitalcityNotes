
## Introduction
Dans les réseaux sans fil modernes, la gestion centralisée des points d'accès et des infrastructures réseau est cruciale pour garantir la performance, la sécurité et la facilité de maintenance. Cisco propose deux solutions majeures pour la gestion centralisée : Cisco DNA Center et les Contrôleurs LAN Sans Fil (WLC).

## Cisco DNA Center
Cisco Digital Network Architecture (DNA) Center est une solution de gestion réseau basée sur l'intention qui offre une automatisation, une assurance et une gestion centralisée des réseaux filaires et sans fil. 

### Fonctionnalités Principales
1. **Automatisation** : Simplifie et accélère le déploiement des réseaux avec des modèles et des politiques prédéfinis.
2. **Assurance** : Fournit une visibilité approfondie sur le réseau et les utilisateurs avec des capacités de surveillance et d'analyse en temps réel.
3. **Sécurité** : Intègre des fonctionnalités de sécurité avancées pour détecter et atténuer les menaces.
4. **Analyse et Intelligence Artificielle** : Utilise des algorithmes de machine learning pour optimiser la performance du réseau.

### Architecture et Composants
1. **Interface Utilisateur (Dashboard)** : Fournit une vue unifiée de l'ensemble du réseau avec des tableaux de bord personnalisables.
2. **Automatisation des Politiques** : Permet de définir et de déployer des politiques de sécurité et de QoS (Quality of Service).
3. **Outils d'Assurance** : Analyse la performance du réseau et identifie les problèmes potentiels.
4. **API** : Offre des interfaces programmatiques pour intégrer et automatiser des opérations réseau.

## Contrôleurs LAN Sans Fil (WLC)
Les contrôleurs LAN sans fil (Wireless LAN Controllers) de Cisco centralisent la gestion des points d'accès sans fil pour améliorer l'évolutivité, la sécurité et la facilité de gestion du réseau sans fil.

### Fonctionnalités Principales
1. **Gestion Centralisée des AP** : Permet la configuration et la gestion de plusieurs points d'accès depuis un seul endroit.
2. **Sécurité Améliorée** : Offre des fonctionnalités de sécurité robustes comme l'authentification 802.1X et le chiffrement WPA3.
3. **Roaming Optimisé** : Facilite le roaming des clients entre différents AP sans perte de connexion.
4. **Surveillance et Dépannage** : Fournit des outils pour surveiller la santé du réseau sans fil et diagnostiquer les problèmes.

### Types de WLC
1. **WLC Physiques** : Matériel dédié pour la gestion des AP, comme le Cisco 5508 Wireless Controller.
2. **WLC Virtuels** : Solutions logicielles déployées sur des machines virtuelles, comme le Cisco vWLC.

### Configuration de Base
1. **Connexion et Accès** : Accéder au contrôleur via une interface web ou une console CLI.
2. **Ajout d’AP** : Enregistrer et configurer les points d'accès pour qu'ils soient gérés par le WLC.
3. **Configuration des SSID** : Définir et configurer les réseaux sans fil (SSID) pour les clients.
4. **Sécurité** : Configurer les politiques de sécurité, y compris les types d'authentification et de chiffrement.

#### Schéma Illustratif

```plaintext
      +-----------------+              +-------------------+
      |                 |              |                   |
      | Cisco DNA Center|              |   WLC Controller  |
      |                 |              |                   |
      +--------+--------+              +--------+----------+
               |                               |
               |                               |
      +--------+--------+                      |
      |                 |                      |
      |     Switch      |----------------------+
      |                 |
      +--------+--------+
               |
               |
      +--------+--------+
      |                 |
      |  Access Points  |
      |                 |
      +--------+--------+
               |
               |
          -------------

```

## Exemples Pratiques
##### Configuration d'un SSID sur un WLC via CLI
```shell
config wlan create 1 MonReseau MonReseau
config wlan security wpa akm psk set-key ascii 1 MonMotDePasse
config wlan enable 1
```

### Configuration d'un AP sur Cisco DNA Center
1. **Ajouter un Dispositif** : Naviguer vers le tableau de bord, sélectionner "Dispositifs" et ajouter un nouveau point d'accès.
2. **Définir une Politique** : Créer et appliquer une politique pour le point d'accès nouvellement ajouté.
3. **Déploiement** : Déployer les configurations et vérifier le bon fonctionnement via l'outil d'assurance.

## Conclusion
Cisco DNA Center et les contrôleurs LAN sans fil (WLC) sont des solutions puissantes pour la gestion centralisée des réseaux sans fil. Leur utilisation permet de simplifier la gestion, d'améliorer la sécurité et d'optimiser la performance du réseau. Une compréhension approfondie de ces outils est essentielle pour tout administrateur réseau cherchant à obtenir des certifications CCNA et ITILv4.
