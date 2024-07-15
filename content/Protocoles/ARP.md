
# Address Resolution Protocol (ARP)

## Introduction
Address Resolution Protocol (ARP) est un protocole essentiel dans les réseaux informatiques. Son rôle principal est de faire le lien entre une adresse IP et une adresse MAC (Media Access Control) au sein d'un réseau local.

## Fonctionnement de l'ARP
Lorsqu'un périphérique souhaite communiquer avec un autre périphérique sur le même réseau local, il a besoin de l'adresse MAC de ce périphérique pour établir la communication. Voici comment ARP facilite cette tâche :

1. **Requête ARP** :
    
    - Un périphérique A souhaite connaître l'adresse MAC d'un périphérique B pour lui envoyer des données.
    - Périphérique A envoie une requête ARP de type "ARP Request" contenant l'adresse IP de B.
    - Cette requête est une diffusion (broadcast) sur le réseau local, demandant à tous les périphériques de répondre s'ils connaissent l'adresse IP demandée.

1. **Réponse ARP** :
    
    - Périphérique B, reconnaissant son adresse IP dans la requête ARP, répond avec un "ARP Reply".
    - Ce reply contient l'adresse MAC de B.
    - Périphérique A reçoit cette réponse et peut maintenant établir une connexion directe avec B en utilisant son adresse MAC.

## Exemple pratique

Imaginons un réseau où un ordinateur A (IP: 192.168.1.2) veut communiquer avec un serveur B (IP: 192.168.1.1). Voici ce qui se passe :

- A envoie une requête ARP demandant "Qui a l'adresse 192.168.1.1 ?"
- Le serveur B, reconnaissant son adresse IP, répond avec son adresse MAC.
- A reçoit la réponse et peut maintenant envoyer des données directement à B en utilisant l'adresse MAC de B.

## Schéma explicatif

![Schéma ARP](https://d33wubrfki0l68.cloudfront.net/0b32c7f56c154842ed3cbb2da278047f7cf3085e/14bac/assets/images/ccna/lucidchart/39d27763-5350-4d31-970e-bb52862bde1f.png)
## Conclusion
ARP joue un rôle crucial dans la communication au niveau local en permettant la résolution des adresses IP en adresses MAC, facilitant ainsi l'échange de données dans un réseau. Comprendre son fonctionnement est essentiel pour tout administrateur réseau.