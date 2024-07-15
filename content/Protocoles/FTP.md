### Protocole FTP (File Transfer Protocol)

## Introduction au FTP
Le File Transfer Protocol (FTP) est un protocole de communication standard utilisé pour transférer des fichiers d'un ordinateur à un autre sur un réseau TCP/IP, comme Internet. FTP est un protocole de la couche application dans le modèle OSI.

## Fonctionnement de FTP
FTP fonctionne selon un modèle client-serveur. Le client FTP initie une connexion avec un serveur FTP pour télécharger (download) ou téléverser (upload) des fichiers. Il utilise deux connexions distinctes :
1. **Connexion de contrôle** : Utilisée pour envoyer des commandes et recevoir des réponses.
2. **Connexion de données** : Utilisée pour le transfert réel des fichiers.

## Ports Utilisés par FTP
- **Port 21** : Utilisé pour la connexion de contrôle.
- **Port 20** : Utilisé pour la connexion de données en mode actif.

## Modes de Connexion FTP
1. **Mode Actif** :
   - Le client initie la connexion de contrôle sur le port 21 du serveur.
   - Pour la connexion de données, le serveur initie la connexion depuis son port 20 vers un port dynamique choisi par le client.
   
   ![Mode Actif FTP](https://cloudzy.com/wp-content/uploads/active-ftp.jpg *(Suggestion d'image pour illustrer le mode actif)

2. **Mode Passif** :
   - Le client initie la connexion de contrôle sur le port 21 du serveur.
   - Le client initie également la connexion de données vers un port dynamique spécifié par le serveur.
   
   ![Mode Passif FTP](https://cloudzy.com/wp-content/uploads/passive-ftp.jpg) 
## Commandes FTP Communes
- **USER** : Authentifie l'utilisateur.
- **PASS** : Fournit le mot de passe de l'utilisateur.
- **LIST** : Liste les fichiers du répertoire courant.
- **RETR** : Télécharge un fichier du serveur.
- **STOR** : Télécharge un fichier vers le serveur.

## Sécurité de FTP
FTP transmet les données, y compris les informations de connexion (nom d'utilisateur et mot de passe), en texte clair, ce qui le rend vulnérable aux interceptions. Pour sécuriser les transferts de fichiers, il est recommandé d'utiliser des variantes sécurisées comme FTPS (FTP Secure) ou SFTP (SSH File Transfer Protocol).

- **FTPS** : Ajoute une couche de sécurité SSL/TLS à FTP.
- **SFTP** : Utilise le protocole SSH pour le transfert sécurisé de fichiers.

## Configuration Basique de FTP sur un Routeur Cisco
```shell
Router(config)# ip ftp username <username>
Router(config)# ip ftp password <password>
Router(config)# ip ftp source-interface <interface>
```

## Exercice Pratique
1. **Installer un serveur FTP** : Utiliser un logiciel comme FileZilla Server.
2. **Configurer le serveur FTP** : Définir les utilisateurs et permissions.
3. **Tester la connexion FTP** : Utiliser un client FTP comme FileZilla Client pour se connecter au serveur et transférer des fichiers.

## Conclusion
FTP est un protocole essentiel pour le transfert de fichiers sur les réseaux TCP/IP. Bien que simple à utiliser, il présente des faiblesses en termes de sécurité, ce qui nécessite l'utilisation de versions sécurisées comme FTPS et SFTP. Maîtriser FTP est crucial pour l'administration réseau, et une compréhension approfondie de ses modes de fonctionnement et de ses commandes vous aidera à réussir votre certification CCNA.

## Ressources Supplémentaires

- [Les protocoles FTP, FTPS et SFTP pour les débutants](https://www.it-connect.fr/les-protocoles-ftp-ftps-et-sftp-pour-les-debutants/)

