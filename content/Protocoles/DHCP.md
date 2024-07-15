
## Introduction

Le Dynamic Host Configuration Protocol (DHCP) est un protocole réseau utilisé pour attribuer dynamiquement des adresses IP et d'autres configurations réseau à des appareils sur un réseau. Il permet aux administrateurs de centraliser et d'automatiser la gestion des adresses IP, ce qui simplifie grandement la configuration et la maintenance des réseaux.

## Fonctionnement de base du DHCP

### Étapes du processus DHCP

1. **Découverte DHCP (DHCP Discover)**: Le client envoie un message de découverte DHCP (DHCPDISCOVER) pour trouver les serveurs DHCP disponibles.
   

2. **Offre DHCP (DHCP Offer)**: Les serveurs DHCP répondent au message de découverte en envoyant une offre DHCP (DHCPOFFER) qui contient une adresse IP et d'autres informations de configuration.


3. **Demande DHCP (DHCP Request)**: Le client choisit une offre et répond avec un message de demande DHCP (DHCPREQUEST), indiquant qu'il accepte l'offre de ce serveur spécifique.

4.  **Accusé de réception DHCP (DHCP Acknowledge)**: Le serveur DHCP confirme l'allocation de l'adresse IP avec un message de reconnaissance DHCP (DHCPACK), finalisant le processus de configuration.

![Image du  processus DHCP](https://crnetpackets.com/wp-content/uploads/2017/04/dhcp-basics-initial2.png)
#### Allocation d'adresses IP

Le DHCP peut allouer des adresses IP de trois manières :
- **Allocation dynamique**: Les adresses IP sont attribuées à partir d'un pool pour une durée déterminée.
- **Allocation automatique**: Les adresses IP sont attribuées de façon permanente à un client dès la première connexion.
- **Allocation manuelle**: Les adresses IP sont réservées et attribuées manuellement par un administrateur réseau.

### Composants du DHCP

- **Client DHCP**: Appareil demandant une configuration réseau (ordinateur, smartphone, etc.).
- **Serveur DHCP**: Serveur qui gère et attribue les configurations réseau aux clients.
- **Agent de relais DHCP**: Dispositif qui transfère les messages DHCP entre les clients et les serveurs lorsque ceux-ci ne sont pas sur le même sous-réseau.

### Configuration d'un serveur DHCP Cisco

#### Exemple de configuration de base

```plaintext
Router(config)# ip dhcp pool VLAN10
Router(dhcp-config)# network 192.168.10.0 255.255.255.0
Router(dhcp-config)# default-router 192.168.10.1
Router(dhcp-config)# dns-server 8.8.8.8 8.8.4.4
Router(dhcp-config)# lease 7
```

### Meilleures pratiques pour le DHCP

1. **Réservation d'adresses IP**: Réserver des adresses IP pour des dispositifs critiques (serveurs, imprimantes).

2. **Sécurisation du DHCP**: Utiliser des fonctionnalités comme DHCP Snooping pour empêcher les attaques de type rogue DHCP.
   
3. **Surveillance et gestion**: Utiliser des outils de surveillance pour vérifier l'utilisation des adresses IP et les conflits d'adresses IP.

### Concepts avancés

#### DHCP Relay

Lorsque les clients DHCP et les serveurs DHCP sont sur des sous-réseaux différents, un agent de relais DHCP est utilisé pour transférer les messages DHCP entre eux.

**Exemple de configuration d'un relais DHCP sur un routeur Cisco**:

```plaintext
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# ip helper-address 192.168.2.1
```

![Relai DHCP](data:image/png;base64,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)
### Conclusion

Le DHCP est un protocole essentiel pour la gestion des adresses IP dans les réseaux modernes. Il simplifie la configuration réseau, réduit les erreurs humaines et permet une gestion centralisée efficace.


