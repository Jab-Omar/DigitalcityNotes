# Le Protocole POP3

## Introduction

Le protocole POP3 (Post Office Protocol version 3) est utilisé pour récupérer des emails depuis un serveur de messagerie vers un client de messagerie. POP3 permet aux utilisateurs de télécharger leurs emails pour les lire hors ligne, facilitant ainsi la gestion des messages sur des clients de messagerie locaux. Comprendre POP3 est essentiel pour toute certification réseau, y compris le CCNA.

## 1. Fonctionnement de POP3

POP3 est un protocole de la couche application (layer 7) du modèle OSI et fonctionne principalement sur le port 110. POP3 suit un modèle de requête/réponse où le client envoie des commandes au serveur et le serveur répond avec les messages demandés.

### Modèle OSI et POP3
![Modèle OSI](https://www.a10networks.com/wp-content/uploads/osi-network-model-protocol-and-services-1-1024x866.png)

- **Couche Application (POP3)**
- **Couche Transport (TCP)**
- **Couche Réseau (IP)**
- **Couche Liaison de données et Physique (Ethernet, Wi-Fi)**

## 2. Commandes POP3

POP3 utilise plusieurs commandes pour gérer la récupération des emails :

- **USER** : Identifie le nom d'utilisateur du compte de messagerie.
- **PASS** : Authentifie l'utilisateur avec un mot de passe.
- **STAT** : Demande le statut de la boîte aux lettres (nombre de messages et taille totale).
- **LIST** : Liste les messages et leurs tailles.
- **RETR** : Récupère un message spécifique.
- **DELE** : Supprime un message spécifique.
- **QUIT** : Termine la session POP3.

## 3. Structure d'une Session POP3

Une session POP3 typique comprend les éléments suivants :

```plaintext
+OK POP3 server ready
USER utilisateur@example.com
+OK
PASS motdepasse
+OK
STAT
+OK 2 320
LIST
+OK
1 200
2 120
RETR 1
+OK 200 octets
<contenu du message>
DELE 1
+OK
QUIT
+OK POP3 server signing off
```

- **USER** : Le client s'identifie avec son nom d'utilisateur.
- **PASS** : Authentifie l'utilisateur avec un mot de passe.
- **STAT** : Demande le statut de la boîte aux lettres.
- **LIST** : Liste les messages disponibles.
- **RETR** : Récupère un message spécifique.
- **DELE** : Supprime un message spécifique.
- **QUIT** : Termine la session.

## 4. Codes de Réponse POP3

Les serveurs POP3 répondent avec des codes de statut pour indiquer le résultat de chaque commande :

- **+OK** : Indique que la commande a été acceptée et exécutée avec succès.
- **-ERR** : Indique que la commande a échoué.

## 5. Sécurisation avec POP3S

POP3S (POP3 Secure) est la version sécurisée de POP3, utilisant SSL/TLS pour chiffrer les données entre le client et le serveur. POP3S fonctionne principalement sur le port 995.

## Ressources Supplémentaires

- [RFC 1939 - Post Office Protocol - Version 3](https://tools.ietf.org/html/rfc1939)
- [MDN Web Docs - POP3](https://developer.mozilla.org/en-US/docs/Glossary/POP3)
- [Découverte des protocoles SMTP, POP, IMAP et MAPI](https://www.it-connect.fr/messagerie-decouverte-des-protocoles-smtp-pop-imap-et-mapi//)

---