
## Introduction à l'IDS

Un **Intrusion Detection System (IDS)** est une solution de sécurité réseau conçue pour détecter les activités malveillantes ou non autorisées sur un réseau ou un système informatique. Contrairement à un **Intrusion Prevention System (IPS)**, l'IDS se contente de détecter et d'alerter sur les potentielles intrusions sans prendre d'actions correctives automatiques.

## Fonctionnement de l'IDS

L'IDS fonctionne en surveillant le trafic réseau ou les journaux de système pour identifier des signes d'activités suspectes ou malveillantes. Il utilise des méthodes telles que la correspondance de signatures (détection basée sur des signatures de menaces connues) et l'analyse heuristique (détection basée sur le comportement) pour identifier les menaces potentielles.



## Types d'IDS

1. **Network-based IDS (NIDS) :**
   - **Description :** Déployé à des points stratégiques du réseau pour surveiller le trafic global.
   - **Avantages :** Large couverture, capable de surveiller l'ensemble du réseau.
   - **Inconvénients :** Peut être submergé par un volume élevé de trafic.

2. **Host-based IDS (HIDS) :**
   - **Description :** Installé sur des dispositifs individuels pour surveiller les activités locales.
   - **Avantages :** Granularité élevée, surveillance spécifique à chaque hôte.
   - **Inconvénients :** Consomme des ressources locales, nécessite une gestion sur chaque hôte.

3. **Hybrid IDS :**
   - **Description :** Combine les fonctionnalités de NIDS et HIDS pour une couverture complète.
   - **Avantages :** Offre une protection à la fois globale et granulaire.
   - **Inconvénients :** Peut être complexe à configurer et à gérer.



## Rôles et Avantages de l'IDS

1. **Détection des Intrusions :**
   - Identifie les tentatives d'accès non autorisé et les activités malveillantes.

2. **Enregistrement et Analyse :**
   - Garde des journaux détaillés des événements de sécurité pour une analyse post-incident.

3. **Alerte en Temps Réel :**
   - Envoie des alertes immédiates aux administrateurs réseau lorsqu'une menace est détectée.

4. **Complémentarité avec d'autres Solutions de Sécurité :**
   - Travaille de concert avec les firewalls, les IPS et d'autres outils de sécurité pour une protection globale.



## Configuration de Base d'un IDS Snort (Exemple)

Voici un exemple de configuration de base d'un IDS utilisant Snort, un IDS open-source populaire :

```shell
# Installer Snort
sudo apt-get install snort

# Configurer l'interface réseau
sudo nano /etc/snort/snort.conf

# Ajouter la configuration de base
var HOME_NET 192.168.1.0/24
var EXTERNAL_NET any
var RULE_PATH /etc/snort/rules

# Définir des règles de détection simples
include $RULE_PATH/local.rules

# Créer un fichier de règles locales
sudo nano /etc/snort/rules/local.rules

# Exemple de règle simple pour détecter les tentatives de ping
alert icmp any any -> $HOME_NET any (msg:"ICMP Echo Request Detected"; sid:1000001; rev:1;)

# Démarrer Snort
sudo snort -A console -i eth0 -c /etc/snort/snort.conf
```


#### Conclusion

Les IDS sont des outils essentiels pour la sécurité réseau, offrant une détection proactive des menaces. Comprendre leur fonctionnement, leurs types et leur configuration est indispensable pour tout professionnel en administration réseau visant une certification CCNA.
