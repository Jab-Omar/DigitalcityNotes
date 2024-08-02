# Le Protocole SMTP

## Introduction

Le protocole SMTP (Simple Mail Transfer Protocol) est utilisé pour la transmission des emails sur Internet. SMTP permet d'envoyer des messages depuis un client de messagerie vers un serveur de messagerie, ainsi que de transférer des emails entre serveurs. Comprendre SMTP est essentiel pour toute certification réseau, y compris le CCNA.

## 1. Fonctionnement de SMTP

SMTP est un protocole de la couche application (layer 7) du modèle OSI et fonctionne principalement sur le port 25. Comme HTTP, SMTP est basé sur un modèle de requête/réponse, mais il se concentre spécifiquement sur l'envoi de mails.

#### Modèle OSI et SMTP
![Modèle OSI](https://www.a10networks.com/wp-content/uploads/osi-network-model-protocol-and-services-1-1024x866.png)

- **Couche Application (SMTP)**
- **Couche Transport (TCP)**
- **Couche Réseau (IP)**
- **Couche Liaison de données et Physique (Ethernet, Wi-Fi)**

## 2. Commandes SMTP

SMTP utilise plusieurs commandes pour gérer l'envoi des emails :

- **HELO** : Identifie le client au serveur.
- **MAIL FROM** : Indique l'adresse de l'expéditeur.
- **RCPT TO** : Indique l'adresse du destinataire.
- **DATA** : Indique que les lignes suivantes contiennent les données du message.
- **QUIT** : Termine la session SMTP.

## 3. Structure d'une Session SMTP

Une session SMTP typique comprend les éléments suivants :

```plaintext
HELO client.example.com
250 Hello client.example.com
MAIL FROM:<expediteur@example.com>
250 OK
RCPT TO:<destinataire@example.com>
250 OK
DATA
354 Start mail input; end with <CRLF>.<CRLF>
Subject: Test Email

Ceci est un test de message.
.
250 OK: Message accepted for delivery
QUIT
221 Bye
```

- **HELO** : Le client s'identifie au serveur.
- **MAIL FROM** : Spécifie l'adresse de l'expéditeur.
- **RCPT TO** : Spécifie l'adresse du destinataire.
- **DATA** : Commence la transmission des données du message.
- **QUIT** : Termine la session.

## 4. Codes de Réponse SMTP

Les serveurs SMTP répondent avec des codes numériques pour indiquer le statut de chaque commande :

- **2xx** : Succès (par exemple, 250 OK)
- **3xx** : Commande intermédiaire (par exemple, 354 Start mail input)
- **4xx** : Erreur temporaire (par exemple, 450 Requested mail action not taken)
- **5xx** : Erreur permanente (par exemple, 550 Requested action not taken: mailbox unavailable)

## 5. Sécurisation avec SMTPS

SMTPS (SMTP Secure) est la version sécurisée de SMTP, utilisant SSL/TLS pour chiffrer les données entre le client et le serveur. SMTPS fonctionne principalement sur le port 465 ou utilise STARTTLS sur le port 587 pour mettre à niveau une connexion non sécurisée.

## Ressources Supplémentaires

- [RFC 5321 - Simple Mail Transfer Protocol](https://tools.ietf.org/html/rfc5321)
- [MDN Web Docs - SMTP](https://developer.mozilla.org/en-US/docs/Glossary/SMTP)
- [Découverte des protocoles SMTP, POP, IMAP et MAPI](https://www.it-connect.fr/messagerie-decouverte-des-protocoles-smtp-pop-imap-et-mapi//)
- [Wireshark/SMTP](https://en.wikiversity.org/wiki/Wireshark/SMTP)

---
