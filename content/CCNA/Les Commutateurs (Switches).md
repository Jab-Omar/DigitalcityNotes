## Introduction

Les commutateurs (ou switches) sont des dispositifs essentiels dans les réseaux informatiques modernes. Leur rôle principal est de connecter et de gérer efficacement le trafic réseau au sein d'un réseau local (LAN). Comprendre leurs fonctionnalités, leur configuration et leur utilisation est crucial pour réussir l'examen CCNA.

## Fonctionnalités Principales

### Commutation de Cadres (Frame Switching)

Les commutateurs opèrent au niveau de la couche 2 du modèle OSI. Ils utilisent des adresses MAC (Media Access Control) pour transférer les paquets de données entre les périphériques connectés au réseau local.

### Table de Commutation (Switching Table)

Chaque commutateur maintient une table de commutation qui associe les adresses MAC des périphériques connectés aux ports physiques du commutateur. Cela permet de diriger efficacement les paquets vers leur destination sans saturer le réseau.

### VLAN (Virtual LAN)

Les commutateurs supportent la création de VLAN, qui segmentent logiquement un réseau en plusieurs sous-réseaux virtuels. Cela améliore la sécurité, la gestion et l'efficacité du réseau en isolant le trafic au sein de groupes spécifiques.

## Composants Clés

### Ports Ethernet

Les commutateurs possèdent plusieurs ports Ethernet (par exemple, 10/100/1000 Mbps) pour connecter des périphériques tels que des ordinateurs, des imprimantes et d'autres commutateurs.

### Table de MAC

Chaque commutateur maintient une table de correspondance des adresses MAC, indiquant quel périphérique est connecté à quel port. Cette table est mise à jour dynamiquement à mesure que les périphériques se connectent ou se déconnectent.

## Configuration et Gestion

### Configuration de Base

La configuration d'un commutateur peut se faire via une interface de ligne de commande (CLI) ou une interface graphique. Les administrateurs réseau définissent les paramètres de VLAN, les adresses IP de gestion et les sécurités de port.

### Sécurité des Ports

Les commutateurs utilisent des fonctionnalités comme les VLAN natifs et les listes de contrôle d'accès (ACL) pour sécuriser les ports et limiter l'accès au réseau.

## Protocoles de Gestion

### SNMP (Simple Network Management Protocol)

Pour surveiller et gérer les commutateurs à distance, SNMP est souvent utilisé. Cela permet de collecter des informations sur les performances, de diagnostiquer les problèmes et de configurer les paramètres à distance.
