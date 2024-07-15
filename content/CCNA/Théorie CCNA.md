# Théorie pour l'Examen CCNA v1.1 (200-301)



## 1.0 Fondamentaux du réseau (Network Fundamentals)
### 1.1 Expliquer le rôle et la fonction des composants réseau (network components)

> [!note] [[Le rôle et la fonction des composants réseau]]
>- [[1.1.a Routers (routeurs)]]
>- [[1.1.b Switches de couche 2 et couche 3 (Layer 2 and Layer 3 switches)]]
>- [[1.1.c Next-generation firewalls (pare-feux de nouvelle génération) et IPS]]
>- [[1.1.d Access points (points d'accès)]]
>- [[1.1.e Controllers (contrôleurs)]]
>- [[1.1.f Endpoints (points de terminaison)]]
>- [[1.1.g Servers (serveurs)]]
>- [[1.1.h PoE (alimentation par Ethernet)]]

### 1.2 Décrire les caractéristiques des architectures de topologie réseau (network topology architectures)

>[!summary] [[Les caractéristiques des architectures de topologie réseau (network topology architectures)]]
>- [[1.2.a Two-tier (deux niveaux)]]
>- [[1.2.b Three-tier (trois niveaux)]]
>- [[1.2.c Spine-leaf]]
>- [[1.2.d WAN (réseau étendu)]]
>- [[1.2.e Small office/home office (SOHO) (petit bureau/bureau à domicile)]]
>- [[1.2.f On-premises (sur site) et cloud]]

### 1.3 Comparer les types d'interfaces physiques et de câblage

>[!info] [[Les types d'interfaces physiques et de câblage]]
>- [[1.3.a Single-mode fiber (fibre monomode), multimode fiber (fibre multimode), copper (cuivre)]]
>- [[1.3.b Connections (connexions) (Ethernet shared media et point-to-point)]]

### 1.4 Identifier les problèmes d'interface et de câblage (collisions, erreurs, mismatch duplex (duplex dépareillé) et/ou vitesse)

>[!tip] [[Identifier les problèmes d'interface et de câblage (collisions, erreurs, mismatch duplex (duplex dépareillé) et/ou vitesse)]]

### [[1.5 Comparer TCP à UDP]]

### [[1.6 Configurer et vérifier l'adressage IPv4 et le subnetting (sous-réseau)]]

### [[1.7 Décrire l'adressage privé IPv4]]

### [[1.8 Configurer et vérifier l'adressage IPv6 et le prefix (préfixe)]]

### [[1.9 Décrire les types d'adresses IPv6]]
- [[1.9.a Unicast (global, unique local (local unique), et link local (lien local))]]
- [[1.9.b Anycast]]
- [[1.9.c Multicast]]
- [[1.9.d Modified EUI 64 (EUI 64 modifié)]]

### [[1.10 Vérifier les paramètres IP pour les systèmes d'exploitation client (Windows, Mac OS, Linux)]]

### [[1.11 Décrire les principes du sans fil (wireless)]]
- [[1.11.a Nonoverlapping Wi-Fi channels (canaux Wi-Fi non chevauchants)]]
- [[1.11.b SSID]]
- [[1.11.c RF (radiofréquence)]]
- [[1.11.d Encryption (chiffrement)]]

### [[1.12 Expliquer les fondamentaux de la virtualisation (virtualization) (virtualisation de serveur, conteneurs, et VRFs)]]

### [[1.13 Décrire les concepts de commutation (switching)]]
- [[1.13.a MAC learning (apprentissage) et aging (vieillissement)]]
- [[1.13.b Frame switching (commutation de trames)]]
- [[1.13.c Frame flooding (inondation de trames)]]
- [[1.13.d MAC address table (table d'adresses MAC)]]

## 2.0 Accès au réseau (Network Access)
### [[2.1 Configurer et vérifier les VLANs (normal range) (plage normale) sur plusieurs switches]]
- [[2.1.a Access ports (ports d'accès) (données et voix)]]
- [[2.1.b Default VLAN (VLAN par défaut)]]
- [[2.1.c InterVLAN connectivity (connectivité InterVLAN)]]

### [[2.2 Configurer et vérifier la connectivité entre switches]]
- [[2.2.a Trunk ports (ports de trunk)]]
- [[2.2.b 802.1Q]]
- [[2.2.c Native VLAN (VLAN natif)]]

### [[2.3 Configurer et vérifier les protocoles de découverte de couche 2 (Layer 2 discovery protocols) (Cisco Discovery Protocol et LLDP)]]

### [[2.4 Configurer et vérifier (Layer 2/Layer 3) EtherChannel (LACP)]]

### [[2.5 Interpréter les opérations de base du Rapid PVST+ Spanning Tree Protocol]]
- [[2.5.a Root port (port racine), root bridge (pont racine) (primaire/secondaire), et autres noms de port]]
- [[2.5.b Port states and roles (états et rôles des ports)]]
- [[2.5.c PortFast]]
- [[2.5.d Root guard (protection de la racine), loop guard (protection contre les boucles), BPDU filter (filtrage BPDU), et BPDU guard (protection BPDU)]]

### [[2.6 Décrire les architectures sans fil (Cisco Wireless Architectures) et les modes AP (points d'accès)]]

### [[2.7 Décrire les connexions de l'infrastructure physique des composants WLAN (AP, WLC, ports d'accès/trunk, et LAG)]]

### [[2.8 Décrire l'accès à la gestion des dispositifs réseau (network device management) (Telnet, SSH, HTTP, HTTPS, console, TACACS+/RADIUS, et gestion cloud)]]

### [[2.9 Interpréter la configuration GUI du LAN sans fil pour la connectivité des clients, telle que la création de WLAN, les paramètres de sécurité, les profils QoS, et les paramètres avancés]]

## 3.0 Connectivité IP (IP Connectivity)
### [[3.1 Interpréter les composants de la table de routage (routing table)]]
- [[3.1.a Routing protocol code (code du protocole de routage)]]
- [[3.1.b Prefix (préfixe)]]
- [[3.1.c Network mask (masque de réseau)]]
- [[3.1.d Next hop (prochain saut)]]
- [[3.1.e Administrative distance (distance administrative)]]
- [[3.1.f Metric (métrique)]]
- [[3.1.g Gateway of last resort (passerelle de dernier recours)]]

### [[3.2 Déterminer comment un routeur prend une décision de transfert par défaut]]
- [[3.2.a Longest prefix match (correspondance de préfixe la plus longue)]]
- [[3.2.b Administrative distance (distance administrative)]]
- [[3.2.c Routing protocol metric (métrique du protocole de routage)]]

### [[3.3 Configurer et vérifier le routage statique IPv4 et IPv6]]
- [[3.3.a Default route (route par défaut)]]
- [[3.3.b Network route (route de réseau)]]
- [[3.3.c Host route (route d'hôte)]]
- [[3.3.d Floating static (statique flottante)]]

### [[3.4 Configurer et vérifier OSPFv2 en zone unique (single area)]]
- [[3.4.a Neighbor adjacencies (adjacences de voisinage)]]
- [[3.4.b Point-to-point]]
- [[3.4.c Broadcast (sélection DR/BDR)]]
- [[3.4.d Router ID (ID du routeur)]]

### [[3.5 Décrire l'objectif, les fonctions et les concepts des protocoles de redondance de premier saut (first hop redundancy protocols)]]

## 4.0 Services IP (IP Services)
### [[4.1 Configurer et vérifier la NAT de source interne (inside source NAT) en utilisant des pools et des statiques]]

### [[4.2 Configurer et vérifier le NTP en mode client et serveur]]

### [[4.3 Expliquer le rôle du DHCP et DNS au sein du réseau]]

### [[4.4 Expliquer la fonction du SNMP dans les opérations réseau (network operations)]]

### [[4.5 Décrire l'utilisation des fonctionnalités syslog, y compris les facilities (installations) et les niveaux de sévérité]]

### [[4.6 Configurer et vérifier le client et relais DHCP]]

### [[4.7 Expliquer le comportement de transfert par saut (forwarding per-hop behavior) pour la QoS tel que la classification, le marquage, la mise en file d'attente, la congestion, la régulation et la mise en forme]]

### [[4.8 Configurer les dispositifs réseau pour l'accès à distance en utilisant SSH]]

### [[4.9 Décrire les capacités et les fonctions de TFTP/FTP dans le réseau]]

## 5.0 Fondamentaux de la sécurité (Security Fundamentals)
### [[5.1 Définir les concepts clés de la sécurité (menaces, vulnérabilités, exploits et techniques de mitigation)]]

### [[5.2 Décrire les éléments du programme de sécurité (sensibilisation des utilisateurs, formation et contrôle d'accès physique)]]

### [[5.3 Configurer et vérifier le contrôle d'accès aux dispositifs en utilisant des mots de passe locaux]]

### [[5.4 Décrire les éléments de la politique de mot de passe de sécurité, tels que la gestion, la complexité et les alternatives de mot de passe (authentification multifactorielle, certificats et biométrie)]]

### [[5.5 Décrire les VPNs d'accès à distance et site à site IPsec]]

### [[5.6 Configurer et vérifier les listes de contrôle d'accès (ACLs)]]

### [[5.7 Configurer et vérifier les fonctionnalités de sécurité de couche 2 (DHCP snooping, dynamic ARP inspection et port security)]]

### [[5.8 Comparer les concepts d'authentification, d'autorisation et de comptabilité]]

### [[5.9 Décrire les protocoles de sécurité sans fil (WPA, WPA2 et WPA3)]]

### [[5.10 Configurer et vérifier le WLAN dans le GUI en utilisant WPA2 PSK]]

## 6.0 Automatisation et programmabilité (Automation and Programmability)
### [[6.1 Expliquer comment l'automatisation impacte la gestion du réseau (network management)]]

### [[6.2 Comparer les réseaux traditionnels avec la mise en réseau basée sur le contrôleur (controller-based networking)]]

### [[6.3 Décrire l'architecture basée sur le contrôleur et définie par logiciel (software defined architecture) (overlay, underlay, et fabric)]]
- [[6.3.a Séparation du plan de contrôle et du plan de données (Separation of control plane and data plane)]]
- [[6.3.b APIs Northbound et Southbound]]

### [[6.4 Expliquer l'IA (intelligence artificielle) (générative et prédictive) et l'apprentissage automatique (machine learning) dans les opérations réseau (network operations)]]

### [[6.5 Décrire les caractéristiques des APIs basées sur REST (authentication types (types d'authentification), CRUD, HTTP verbs (verbes HTTP) et data encoding (encodage des données))]]

### [[6.6 Reconnaître les capacités des mécanismes de gestion de configuration (configuration management) tels que Ansible et Terraform]]

### [[6.7 Reconnaître les composants des données encodées en JSON (JSON-encoded data)]]
