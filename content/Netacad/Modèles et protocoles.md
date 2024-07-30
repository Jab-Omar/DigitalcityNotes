# Modèles et protocoles

[[Configuration de base IOS]]⬅️ - [[|Résumé]]⬇️ - [[]]➡️ - [Flashcard Anki]()🃏

---

## Concepts Fondamentaux de la Communication

### Éléments de la Communication

- **Source du message (émetteur)** : Personnes ou dispositifs électroniques envoyant un message.
- **Destination du message (récepteur)** : Personnes ou dispositifs recevant et interprétant le message.
- **Canal** : Média permettant au message de voyager de la source à la destination.

### Protocoles de Communication

Les protocoles sont des règles gouvernant la communication. Ils assurent la bonne transmission et compréhension des messages.

#### Exigences des Protocoles Réseau

1. **Encodage du message** : Conversion des informations pour la transmission.
2. **Formatage et encapsulation du message** : Structuration et emballage des messages pour la transmission.
3. **Taille du message** : Division des messages en morceaux gérables.
4. **Timing du message** :
   - **Contrôle de flux** : Gestion de la vitesse de transmission des données.
   - **Délai de réponse** : Temps d'attente avant de considérer une réponse comme absente.
   - **Méthode d'accès** : Détermination du moment opportun pour envoyer un message.
5. **Options de livraison du message** :
   - **Unicast (Monocast)** : Un destinataire unique.
   - **Multicast (Multidiffusion)** : Un groupe spécifique de destinataires.
   - **Broadcast (Diffusion)** : Tous les dispositifs sur le réseau.

### Schémas Mermaid pour Visualiser les Concepts

#### Schéma de Communication de Base

```mermaid
graph TD;
    A[Source du Message] -->|Encodage| B[Signal];
    B -->|Transmission| C[Canal];
    C -->|Décodage| D[Destination du Message];
```

#### Schéma de l'Encapsulation des Messages

```mermaid
graph TD;
    A[Message Original] --> B[Encapsulation];
    B -->|Enveloppe| C[Message Encapsulé];
    C -->|Transmission| D[Canal];
    D -->|Désencapsulation| E[Message Original];
```

### Explications Additionnelles

- **Encodage** : Transformation d'informations en un format transmissible.
- **Décodage** : Retour du format transmis à l'information originale.
- **Formatage** : Structure spécifique d'un message selon le canal utilisé.
- **Encapsulation** : Enveloppement d'un message dans un autre format (ex : lettre dans une enveloppe).
- **Désencapsulation** : Retrait du message de son enveloppe formatée.

### Points Clés à Retenir

- Les réseaux nécessitent plus qu'une simple connexion physique pour communiquer ; des protocoles sont nécessaires.
- La communication efficace repose sur l'encodage, le formatage, la gestion du timing et le contrôle de flux.
- Les messages peuvent être envoyés à un seul destinataire, à un groupe, ou diffusés à tous les dispositifs sur le réseau.

---
## Vue d'Ensemble des Protocoles Réseau

Les protocoles réseau définissent un format commun et des règles pour l'échange de messages entre dispositifs. Ils sont mis en œuvre par les dispositifs finaux et intermédiaires en logiciel, matériel, ou les deux. Chaque protocole réseau a sa propre fonction, format et règles de communication.

| Type de Protocole | Description |
| --- | --- |
| **Protocoles de Communication Réseau** | Permettent à deux ou plusieurs dispositifs de communiquer sur un ou plusieurs réseaux. Exemples : IP, TCP, HTTP. |
| **Protocoles de Sécurité Réseau** | Sécurisent les données pour fournir authentification, intégrité et chiffrement des données. Exemples : SSH, SSL, TLS. |
| **Protocoles de Routage** | Permettent aux routeurs d'échanger des informations de route, de comparer des chemins et de sélectionner le meilleur chemin vers le réseau de destination. Exemples : OSPF, BGP. |
| **Protocoles de Découverte de Services** | Utilisés pour la détection automatique des dispositifs ou services. Exemples : DHCP, DNS. |

### Fonctions des Protocoles Réseau

Les protocoles de communication réseau remplissent diverses fonctions nécessaires pour les communications entre dispositifs finaux.

| Fonction | Description |
| --- | --- |
| **Adressage** | Identifie l'émetteur et le récepteur du message en utilisant un schéma d'adressage défini. Exemples : Ethernet, IPv4, IPv6. |
| **Fiabilité** | Assure la livraison garantie des messages même en cas de perte ou de corruption. Exemple : TCP. |
| **Contrôle de Flux** | Assure que les données circulent à un rythme efficace entre les dispositifs communicants. Exemple : TCP. |
| **Séquençage** | Attribue des étiquettes uniques à chaque segment de données transmis pour une réassemblage correct. Exemple : TCP. |
| **Détection d'Erreurs** | Détermine si les données sont corrompues pendant la transmission. Exemples : Ethernet, IPv4, IPv6, TCP. |
| **Interface Applicative** | Contient des informations pour la communication entre processus réseau. Exemple : HTTP pour accéder à une page web. |

### Interaction des Protocoles

Un message envoyé sur un réseau informatique nécessite généralement l'utilisation de plusieurs protocoles, chacun ayant ses propres fonctions et format.

#### Exemple : Demande de Page Web

1. **HTTP** : Gouverne l'interaction entre un serveur web et un client web.
2. **TCP** : Gère les conversations individuelles et garantit la livraison fiable de l'information.
3. **IP** : Responsable de la livraison des messages de l'expéditeur au destinataire.
4. **Ethernet** : Assure la livraison des messages d'une carte réseau (NIC) à une autre sur le même réseau local (LAN) Ethernet.

```mermaid
graph TD;
    A[Client Web] -->|HTTP| B[Serveur Web];
    B -->|TCP| C[Serveur Web];
    C -->|IP| D[Serveur Web];
    D -->|Ethernet| E[Serveur Web];
```

### Concepts Clés

- Les dispositifs doivent suivre les mêmes règles ou protocoles pour communiquer.
- Chaque protocole réseau a une fonction spécifique, qu'il soit pour la communication générale, la sécurité, le routage, ou la découverte de services.
- Les fonctions des protocoles incluent l'adressage, la fiabilité, le contrôle de flux, le séquençage, la détection d'erreurs et l'interface applicative.
- Plusieurs protocoles peuvent être utilisés simultanément pour accomplir une tâche de communication réseau.

---
## Suites de Protocoles

### Suites de Protocoles Réseau

Les protocoles réseau doivent souvent fonctionner ensemble pour offrir une expérience en ligne fluide. Les suites de protocoles sont conçues pour fonctionner en harmonie.

Une suite de protocoles est un groupe de protocoles interconnectés nécessaires pour effectuer une fonction de communication. 

Pour visualiser comment les protocoles d'une suite interagissent, imagine-les comme une pile. Chaque couche de la pile fournit des services à la couche supérieure et dépend des services de la couche inférieure.


### Évolution des Suites de Protocoles

Depuis les années 1970, plusieurs suites de protocoles ont été développées par des organisations de normalisation ou des vendeurs. Voici un aperçu de quelques suites de protocoles importantes :

| Couche TCP/IP | TCP/IP | ISO | AppleTalk | Novell NetWare |
| --- | --- | --- | --- | --- |
| **Application** | HTTP, DNS, DHCP, FTP | ACSE, ROSE, TRSE, SESE | AFP | NDS |
| **Transport** | TCP, UDP | TP0-TP4 | ATP, AEP, NBP, RTMP | SPX |
| **Internet** | IPv4, IPv6, ICMPv4, ICMPv6 | CONP/CMNS, CLNP/CLNS | AARP | IPX |
| **Accès Réseau** | Ethernet, ARP, WLAN | Ethernet, ARP, WLAN | Ethernet, ARP, WLAN | Ethernet, ARP, WLAN |

- **Internet Protocol Suite (TCP/IP)** : La suite de protocoles la plus couramment utilisée aujourd'hui. Maintenue par l'Internet Engineering Task Force (IETF).
- **Open Systems Interconnection (OSI)** : Développée en 1977, cette suite est principalement connue pour son modèle de référence en sept couches.
- **AppleTalk** : Une suite propriétaire lancée par Apple en 1985 et remplacée par TCP/IP en 1995.
- **Novell NetWare** : Une suite propriétaire et un système d'exploitation réseau lancé en 1983 et remplacé par TCP/IP en 1995.

### Suite de Protocoles TCP/IP

Aujourd'hui, la suite de protocoles TCP/IP inclut de nombreux protocoles et continue d'évoluer pour supporter de nouveaux services. Voici une vue d'ensemble :

| Couche | Protocoles |
| --- | --- |
| **Application** | DNS, DHCPv4, DHCPv6, SLAAC, SMTP, POP3, IMAP, FTP, SFTP, TFTP, HTTP, HTTPS, REST |
| **Transport** | TCP, UDP |
| **Internet** | IPv4, IPv6, NAT, ICMPv4, ICMPv6, ICMPv6 ND, OSPF, EIGRP, BGP |
| **Accès Réseau** | ARP, Ethernet, WLAN |

#### Aspects importants de TCP/IP

- **Protocole ouvert** : Disponible gratuitement et utilisable par tout fournisseur.
- **Protocole basé sur des normes** : Approuvé par l'industrie du réseau, assurant l'interopérabilité des produits de différents fabricants.

### Processus de Communication TCP/IP

Le processus de communication TCP/IP illustre comment les données sont transmises d'un serveur web à un client en utilisant les différentes couches de la suite de protocoles TCP/IP.

#### Étapes du Processus de Communication :

1. **Couche Application (HTTP)** : Le serveur web prépare la page HTML à envoyer et utilise HTTP pour formater les données. L'en-tête HTTP contient des informations sur la requête et la réponse.
2. **Couche Transport (TCP)** : TCP segmente les données en morceaux gérables et ajoute un en-tête pour assurer que les segments arrivent correctement et dans le bon ordre.
3. **Couche Internet (IP)** : Les segments TCP sont encapsulés dans des paquets IP. L'en-tête IP ajoute les adresses IP source et destination.
4. **Couche Accès Réseau (Ethernet)** : Les paquets IP sont encapsulés dans des trames Ethernet. Les trames sont converties en bits et transmises physiquement sur le réseau.

```mermaid
sequenceDiagram
    participant WebServer
    participant WebClient
    WebServer->>WebClient: HTTP (Application Layer)
    WebServer->>WebClient: TCP (Transport Layer)
    WebServer->>WebClient: IP (Internet Layer)
    WebServer->>WebClient: Ethernet (Network Access Layer)
```

Chaque flèche représente l'ajout d'un en-tête par la couche correspondante, encapsulant les données pour la transmission vers le client.

---

## Organisations de Normalisation

Les normes ouvertes encouragent l'interopérabilité, la concurrence et l'innovation. Elles garantissent également qu'aucun produit d'une seule entreprise ne peut monopoliser le marché ou avoir un avantage injuste sur ses concurrents.

Dans le domaine des réseaux, les normes sont développées par des organisations internationales de normalisation. Ces organisations sont généralement neutres, à but non lucratif, et établies pour développer et promouvoir le concept de normes ouvertes. Elles jouent un rôle crucial dans le maintien d'un internet ouvert avec des spécifications et des protocoles librement accessibles, pouvant être mis en œuvre par tout fournisseur.

### Les Principales Organisations de Normalisation

Les organisations de normalisation se répartissent en plusieurs catégories, chacune ayant des responsabilités spécifiques pour promouvoir et créer des normes dans différents domaines :

#### Normes Internet
- **Internet Society (ISOC)** : Promeut le développement ouvert et l'évolution de l'utilisation d'internet dans le monde entier.
- **Internet Architecture Board (IAB)** : Responsable de la gestion globale et du développement des normes internet.
- **Internet Engineering Task Force (IETF)** : Développe, met à jour et maintient les technologies internet et TCP/IP.
- **Internet Research Task Force (IRTF)** : Axée sur la recherche à long terme liée aux protocoles internet et TCP/IP.

```mermaid
graph TD;
    ISOC[Internet Society - ISOC] --> IAB[Internet Architecture Board - IAB];
    IAB --> IETF[Internet Engineering Task Force - IETF];
    IAB --> IRTF[Internet Research Task Force - IRTF];
    IETF --> IESG[Internet Engineering Steering Group - IESG];
    IRTF --> IRSG[Internet Research Steering Group - IRSG];
```

#### Normes TCP/IP
- **Internet Corporation for Assigned Names and Numbers (ICANN)** : Coordonne l'allocation des adresses IP, la gestion des noms de domaine et l'attribution d'autres informations utilisées dans les protocoles TCP/IP.
- **Internet Assigned Numbers Authority (IANA)** : Supervise et gère l'allocation des adresses IP, la gestion des noms de domaine et les identifiants de protocoles pour le compte de l'ICANN.

```mermaid
graph TD;
    ICANN[Internet Corporation for Assigned Names and Numbers - ICANN] --> IANA[Internet Assigned Numbers Authority - IANA];
    IANA --> IP_Addresses[IP Addresses];
    IANA --> Domain_Names[Domain Names];
    IANA --> TCP_UDP_Ports[TCP/UDP Port Numbers];
```

#### Normes Électroniques et de Communication
- **Institute of Electrical and Electronics Engineers (IEEE)** : Organisation dédiée à l'innovation technologique et à la création de normes dans divers domaines, y compris les télécommunications et les réseaux.
- **Electronic Industries Alliance (EIA)** : Connue pour ses normes relatives au câblage électrique, aux connecteurs et aux racks de 19 pouces utilisés pour monter les équipements de réseau.
- **Telecommunications Industry Association (TIA)** : Développe des normes de communication dans divers domaines, y compris les équipements radio, les tours cellulaires et les dispositifs VoIP.
- **International Telecommunications Union-Telecommunication Standardization Sector (ITU-T)** : Une des plus grandes et plus anciennes organisations de normalisation des communications, définissant des normes pour la compression vidéo, IPTV, et les communications à large bande.

```mermaid
graph TD;
    IEEE[Institute of Electrical and Electronics Engineers - IEEE];
    EIA[Electronic Industries Alliance - EIA];
    TIA[Telecommunications Industry Association - TIA];
    ITU_T[International Telecommunications Union-Telecommunication Standardization Sector - ITU-T];
    
    IEEE --> EIA;
    IEEE --> TIA;
    TIA --> ITU_T;
```

### Importance des Normes Ouvertes

Les normes ouvertes permettent l'interopérabilité entre les produits de différents fabricants. Par exemple, lorsque vous achetez un routeur sans fil pour votre maison, vous avez le choix entre de nombreux vendeurs, chacun incorporant des protocoles standard comme IPv4, IPv6, DHCP, SLAAC, Ethernet et 802.11 WLAN. Ces normes permettent également à un client utilisant le système d'exploitation Apple OS X de télécharger une page web depuis un serveur web fonctionnant sous le système d'exploitation Linux, car les deux systèmes mettent en œuvre les protocoles standards ouverts, tels que ceux de la suite de protocoles TCP/IP.

---
## Modèles de Référence

### Les Avantages d’un Modèle en Couches

Lorsque vous étudiez les réseaux, il peut être difficile de visualiser comment les paquets circulent réellement à travers le réseau, un peu comme il est difficile de voir comment les composants d'une voiture sont assemblés sur une chaîne de montage. Les modèles en couches sont utiles pour imaginer et comprendre ce qui se passe dans un réseau.

Les concepts complexes comme le fonctionnement d’un réseau peuvent être difficiles à expliquer et à comprendre. Pour cette raison, un modèle en couches est utilisé pour modulariser les opérations d'un réseau en couches gérables.

Les avantages d'utiliser un modèle en couches pour décrire les protocoles et les opérations du réseau incluent :

- Aide à la conception des protocoles, car les protocoles qui fonctionnent à une couche spécifique ont des informations définies sur lesquelles ils agissent et une interface définie avec les couches supérieures et inférieures.
- Favorise la concurrence car les produits de différents fabricants peuvent fonctionner ensemble.
- Empêche les changements technologiques ou de capacité dans une couche d'affecter les autres couches supérieures et inférieures.
- Fournit un langage commun pour décrire les fonctions et capacités du réseau.

Il existe deux modèles en couches utilisés pour décrire les opérations du réseau :

- Modèle de Référence OSI (Open System Interconnection)
- Modèle de Référence TCP/IP
### Le Modèle de Référence OSI

Le modèle de référence OSI fournit une liste complète de fonctions et de services pouvant se produire à chaque couche. Ce modèle assure la cohérence des protocoles et services réseau en décrivant ce qui doit être fait à une couche particulière, sans prescrire comment cela doit être accompli.

Il décrit également l'interaction de chaque couche avec les couches directement supérieures et inférieures. Les protocoles TCP/IP discutés dans ce cours sont structurés autour des modèles OSI et TCP/IP.

| Couche OSI          | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| 7 - Application     | Contient les protocoles utilisés pour les communications de processus à processus.              |
| 6 - Présentation    | Assure la représentation commune des données transférées entre les services de la couche application. |
| 5 - Session         | Offre des services à la couche présentation pour organiser son dialogue et gérer l'échange de données. |
| 4 - Transport       | Définit les services pour segmenter, transférer et réassembler les données pour des communications individuelles entre les dispositifs finaux. |
| 3 - Réseau          | Offre des services pour échanger les morceaux individuels de données sur le réseau entre les dispositifs finaux identifiés. |
| 2 - Liaison de données | Décrit les méthodes pour échanger des trames de données entre les dispositifs sur un média commun. |
| 1 - Physique        | Décrit les moyens mécaniques, électriques, fonctionnels et procéduraux pour activer, maintenir et désactiver les connexions physiques pour une transmission de bits vers et depuis un dispositif réseau. |

### Le Modèle de Protocole TCP/IP

Le modèle de protocole TCP/IP pour les communications interréseaux a été créé au début des années 1970 et est parfois appelé le modèle internet. Ce modèle correspond étroitement à la structure d'une suite de protocoles spécifique. Le modèle TCP/IP est un modèle de protocole car il décrit les fonctions qui se produisent à chaque couche des protocoles dans la suite TCP/IP.

| Couche TCP/IP       | Description                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| 4 - Application     | Représente les données à l'utilisateur, plus l'encodage et le contrôle de dialogue.              |
| 3 - Transport       | Prend en charge la communication entre divers dispositifs sur des réseaux divers.                |
| 2 - Internet        | Détermine le meilleur chemin à travers le réseau.                                                |
| 1 - Accès Réseau    | Contrôle les dispositifs matériels et les médias qui composent le réseau.                        |

Les définitions des protocoles standards et des protocoles TCP/IP sont discutées dans un forum public et définies dans un ensemble de RFC (Request for Comments) disponibles publiquement. Un RFC est rédigé par des ingénieurs réseau et envoyé à d'autres membres de l'IETF pour commentaires.

### Comparaison des Modèles OSI et TCP/IP

Les protocoles qui composent la suite de protocoles TCP/IP peuvent également être décrits en termes de modèle de référence OSI. Dans le modèle OSI, la couche d'accès au réseau et la couche application du modèle TCP/IP sont divisées davantage pour décrire les fonctions discrètes qui doivent se produire à ces couches.

Au niveau de la couche d'accès réseau, la suite de protocoles TCP/IP ne spécifie pas quels protocoles utiliser lors de la transmission sur un support physique ; elle décrit seulement le transfert de la couche internet vers les protocoles réseau physiques. Les couches 1 et 2 du modèle OSI discutent des procédures nécessaires pour accéder aux médias et des moyens physiques pour envoyer des données sur un réseau.

```mermaid
graph LR;
    subgraph OSI_Model [Modèle OSI]
        direction TB;
        App_OSI[Application] 
        Pres_OSI[Présentation] 
        Sess_OSI[Session] 
        Trans_OSI[Transport] 
        Net_OSI[Réseau] 
        Data_OSI[Liaison de données] 
        Phy_OSI[Physique] 
    end;

    subgraph TCPIP_Model [Modèle TCP/IP]
        direction TB;
        App_TCP[Application] 
        Trans_TCP[Transport] 
        Inter_TCP[Internet] 
        NetAcc_TCP[Accès Réseau] 
    end;

    App_TCP --- App_OSI;
    App_TCP --- Pres_OSI;
    App_TCP --- Sess_OSI;
    Trans_TCP --- Trans_OSI;
    Inter_TCP --- Net_OSI;
    NetAcc_TCP --- Data_OSI;
    NetAcc_TCP --- Phy_OSI;

```

Les principales similitudes se situent dans les couches de transport et de réseau ; cependant, les deux modèles diffèrent dans la manière dont ils se rapportent aux couches supérieures et inférieures :

- La couche 3 du modèle OSI, la couche réseau, correspond directement à la couche internet du modèle TCP/IP. Cette couche est utilisée pour décrire les protocoles qui adressent et acheminent les messages à travers un internetwork.
- La couche 4 du modèle OSI, la couche transport, correspond directement à la couche transport du modèle TCP/IP. Cette couche décrit les services et les fonctions générales qui assurent la livraison ordonnée et fiable des données entre les hôtes source et destination.
- La couche application du modèle TCP/IP inclut plusieurs protocoles qui fournissent des fonctionnalités spécifiques à une variété d'applications utilisateur final. Les couches 5, 6 et 7 du modèle OSI sont utilisées comme références pour les développeurs de logiciels d'application et les fournisseurs pour produire des applications qui fonctionnent sur les réseaux.

---
## Encapsulation des Données

**Segmentation des Messages**

Comprendre le modèle OSI et le modèle TCP/IP est crucial pour saisir comment les données sont encapsulées dans un réseau. Au lieu d'envoyer un grand flux de données, il est préférable de le diviser en segments plus petits, un processus appelé segmentation. 

**Avantages** :
- **Accélération du transfert** : Les données segmentées permettent une meilleure utilisation de la bande passante, facilitant l'envoi simultané de plusieurs communications (multiplexage).
- **Efficacité** : Si un segment échoue, seule cette partie doit être retransmise, évitant de renvoyer l'intégralité du flux.

**Séquençage**

Chaque segment doit être identifié par un numéro de séquence pour garantir un réassemblage correct à la destination. Le protocole TCP s'occupe de cette tâche.

**Unités de Données de Protocole (Protocol Data Units - PDU)**

Lorsqu'une donnée traverse les différentes couches du modèle, chaque couche ajoute des en-têtes, processus connu sous le nom d'encapsulation. La forme que prend une donnée à chaque couche est appelée Unité de Données de Protocole (UDP).

**Terminologie des PDUs** :
- **Données (Data)** : Terme général au niveau de l'application.
- **Segment (Segment)** : PDU de la couche transport (TCP).
- **Paquet (Packet)** : PDU de la couche réseau (IP).
- **Trame (Frame)** : PDU de la couche de liaison de données.
- **Bits (Bits)** : PDU de la couche physique.

### Schémas

#### Processus d'Encapsulation

```mermaid
flowchart TD
    A[Données HTTP] -->|Encapsulation| B[Segment TCP]
    B -->|Encapsulation| C[Paquet IP]
    C -->|Encapsulation| D[Trame Ethernet]
    D -->|Transmission| E[Bits]
```

### Exemples

**Exemple d'Encapsulation**

Lorsqu'une page web est envoyée d'un serveur à un client, le processus d'encapsulation se déroule comme suit :

1. **Couche Application** : Le serveur prépare les données HTML et ajoute un en-tête HTTP.
2. **Couche Transport** : Les données HTTP sont livrées à TCP, où un en-tête TCP est ajouté.
3. **Couche Réseau** : Le segment TCP est encapsulé avec un en-tête IP, formant un paquet.
4. **Couche de Liaison de Données** : Le paquet IP est encapsulé avec des informations Ethernet, créant une trame.
5. **Couche Physique** : La trame est convertie en bits pour la transmission.

**Exemple de Dé-Encapsulation**

Au niveau du destinataire, le processus inverse (dé-encapsulation) se produit, consistant à retirer les en-têtes de protocole à mesure que les données montent dans la pile jusqu'à l'application finale.

---
## Adressage Réseau

### Importance de l'Adressage

L'adressage dans un réseau est crucial pour assurer la communication entre les dispositifs. Pour que les messages segmentés circulent correctement, ils doivent être correctement adressés. Les couches réseau (Layer 3) et liaison de données (Layer 2) jouent un rôle essentiel dans la livraison des données.

#### Rôles des Couches Réseau et Liaison de Données

- **Couche Réseau (Network Layer)** : Utilise des adresses logiques (adresses IP) pour acheminer des paquets IP d'un dispositif source à une destination, potentiellement sur des réseaux différents.
- **Couche Liaison de Données (Data Link Layer)** : Utilise des adresses physiques (adresses MAC) pour transmettre des trames entre dispositifs sur le même réseau local.

#### Diagramme de l'Adressage

```mermaid
graph TD;
    A[Couche Physique] -->|Bits de synchronisation| B[Couche Liaison de Données];
    B -->|Adresses physiques MAC| C[Couche Réseau];
    C -->|Adresses logiques IP| D[Couche Transport];
    D -->|Numéros de port| E[Couche Application];
```
### Adresse Logique de Couche 3

Une **adresse IP** est utilisée pour identifier de manière unique un dispositif sur un réseau. Elle est essentielle pour acheminer les paquets IP.

#### Structure de l'Adresse IP

Une adresse IP se divise en deux parties :

1. **Partie Réseau (Network Portion)** : Indique le réseau auquel appartient l'adresse.
2. **Partie Hôte (Host Portion)** : Identifie un appareil spécifique sur le réseau.

#### Exemple d'Adresse IP

Imaginons une situation où :
- **Source IP** : 192.168.1.110 (PC1)
- **Destination IP** : 172.16.1.99 (Serveur Web)

Le paquet IP part de PC1, traverse des routeurs, et atteint le serveur Web.


### Communication sur le Même Réseau

#### Adresses IPv4

Supposons que PC1 souhaite communiquer avec un serveur FTP sur le même réseau :

- **Adresse IP Source** : 192.168.1.110 (PC1)
- **Adresse IP Destination** : 192.168.1.9 (Serveur FTP)

#### Diagramme de Communication Locale

```mermaid
flowchart LR
    A[PC1] --> B[Serveur FTP]
    A -- MAC: AA-AA-AA-AA-AA-AA --> B
    A -- IP: 192.168.1.110 --> B
    B -- IP: 192.168.1.9 --> B

```

#### Rôle des Adresses de Liaison de Données

- **Source MAC** : Adresse MAC de PC1 (AA-AA-AA-AA-AA-AA).
- **Destination MAC** : Adresse MAC du serveur FTP (CC-CC-CC-CC-CC-CC).

Les trames contenant le paquet IP peuvent être directement transmises entre les dispositifs.

### Communication entre Réseaux Distants

#### Exemple de Communication à Travers des Réseaux

Lorsqu'un paquet est envoyé à un serveur sur un réseau différent, les adresses IP sont également différentes.

- **Adresse IP Source** : 192.168.1.110 (PC1)
- **Adresse IP Destination** : 172.16.1.99 (Serveur Web)

#### Diagramme de Communication entre Réseaux

```mermaid
flowchart TD
    A[PC1] -->|MAC: AA-AA-AA-AA-AA-AA| B[R1]
    B -->|MAC: 11-11-11-11-11-11| C[R2]
    C -->|MAC: 22-22-22-22-22-22| D[Serveur Web]
    A -->|IP: 192.168.1.110| B -->|IP: 172.16.1.99| D
```

#### Rôle des Adresses de Couche Réseau

Lorsque le paquet IP doit être envoyé à un réseau distant, il doit d'abord être envoyé à la **passerelle par défaut** (router).

- **Source MAC** : Adresse MAC de PC1 (AA-AA-AA-AA-AA-AA).
- **Destination MAC** : Adresse MAC de R1 (11-11-11-11-11-11).

Le paquet est ensuite transmis par R1 à R2, puis au serveur Web.

#### Remarque

Il est impératif de configurer l'adresse IP de la passerelle par défaut sur chaque hôte du réseau local. Tous les paquets destinés à des réseaux distants doivent être envoyés à cette passerelle.

---
## Ce Que J'ai Appris Dans Ce Module

Ce module m’a permis de comprendre les concepts fondamentaux des protocoles de communication dans les réseaux informatiques. Voici les points clés :
### Les Règles de Communication
1. **Éléments de la Communication** :
   - **Expéditeur** (Source du Message)
   - **Destinataire** (Destination du Message)
   - **Canal** (Moyen de Communication)

2. **Protocoles** :
   - Régissent l'envoi des messages et comprennent :
     - Identification de l'expéditeur et du destinataire
     - Langue et grammaire communes
     - Vitesse et timing de la livraison
     - Exigences de confirmation ou d'accusé de réception

3. **Composantes Clés des Protocoles** :
   - **Encodage du Message** : Processus de conversion de l'information dans un format adapté pour la transmission.
   - **Décodage du Message** : Inversion de l'encodage pour interpréter l'information.
   - **Format du Message** : Déterminé par le type de message et le canal de livraison.
   - **Timing du Message** : Comprend le contrôle de flux, le délai de réponse et les méthodes d'accès.
   - **Options de Livraison du Message** : Unicast, multicast et broadcast.

### Protocoles
- Les protocoles sont mis en œuvre dans le matériel et le logiciel des dispositifs finaux et des dispositifs intermédiaires.
- Un message utilise généralement plusieurs protocoles, chacun ayant des fonctions et des formats distincts.
- Protocoles Courants :
  - **Famille Ethernet** : Comprend IP, TCP, HTTP, etc.
  - **Protocoles de Sécurité** : SSH, SSL, TLS pour l’authentification, l’intégrité et le chiffrement des données.
  - **Protocoles de Routage** : OSPF et BGP pour l'échange d'informations de routage.
  - **Protocoles de Détection** : DHCP et DNS pour la détection automatique des dispositifs/services.
- Fonctions Clés des Protocoles : adressage, fiabilité, contrôle de flux, séquençage, détection d'erreurs et interface applicative.

### Suites de Protocoles
- Une **suite de protocoles** est un groupe de protocoles interconnectés nécessaires à une fonction de communication.
- Une **pile de protocoles** illustre l'implémentation de ces protocoles.
- La suite de protocoles la plus utilisée aujourd'hui est **TCP/IP**, qui couvre les couches application, transport et internet.

### Organisations de Normalisation
- **Normes Ouvertes** : Favorisent l'interopérabilité, la concurrence et l'innovation.
- Les organisations de normalisation promeuvent et créent des normes pour Internet, comme l'ISOC, l'IAB, l'IETF et l'IRTF.
- Les organisations soutenant TCP/IP incluent ICANN et IANA, tandis que l'IEEE, l'EIA, la TIA et l'ITU-T se concentrent sur les normes électroniques et de communication.

### Modèles de Référence
- **Modèle OSI** : 7 Couches
  - 7 - Application
  - 6 - Présentation
  - 5 - Session
  - 4 - Transport
  - 3 - Réseau
  - 2 - Liaison de Données
  - 1 - Physique

- **Modèle TCP/IP** : 4 Couches
  - 4 - Application
  - 3 - Transport
  - 2 - Internet
  - 1 - Accès Réseau

### Encapsulation des Données
- **Segmentation des Messages** : 
  - Permet d'intercaler plusieurs conversations sur le réseau (multiplexage).
  - Augmente l’efficacité en ne retransmettant que les segments manquants.
- **TCP** : Gère le séquençage des segments.
- **Unité de Données de Protocole (UDP)** : La forme que prend une donnée à chaque couche.
- **Encapsulation** : Les données de la couche supérieure sont encapsulées en descendant vers la couche inférieure, ce processus étant inversé lors de la dé-encapsulation.

### Accès aux Données
- **Couche Réseau** : 
  - Responsable de la livraison des paquets IP de la source à la destination.
- **Couche Liaison de Données** : 
  - Gère la livraison des trames entre les cartes réseau (NIC) sur le même réseau.
- **Adresses IP** : Contiennent des parties réseau et hôte pour IPv4, ainsi que préfixe et ID d’interface pour IPv6.
- **Adresses MAC** : Utilisées sur les réseaux Ethernet pour la livraison locale.
- **Routage** : Si les dispositifs sont sur des réseaux différents, les paquets sont envoyés à un routeur ou à une passerelle par défaut.

---
[[Configuration de base IOS]]⬅️ - [[#Modèles et protocoles|Retour]]⬆️ - [[]]➡️