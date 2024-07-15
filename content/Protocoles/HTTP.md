## Note Pédagogique : Le Protocole HTTP

#### Introduction
Le protocole HTTP (HyperText Transfer Protocol) est l'un des protocoles les plus utilisés sur Internet. Il permet la communication entre les clients (navigateurs web) et les serveurs web, facilitant ainsi la récupération et l'affichage de pages web. Comprendre HTTP est crucial pour toute certification réseau, y compris le CCNA.

#### 1. Fonctionnement de HTTP

HTTP est un protocole de la couche application (layer 7) du modèle OSI (Open Systems Interconnection) et fonctionne principalement sur le port 80. Il est basé sur un modèle de requête/réponse où le client envoie une requête au serveur, et le serveur répond avec les données demandées.

##### Modèle OSI et HTTP
![Modèle OSI](https://www.a10networks.com/wp-content/uploads/osi-network-model-protocol-and-services-1-1024x866.png|)

- **Couche Application (HTTP)**
- **Couche Transport (TCP)**
- **Couche Réseau (IP)**
- **Couche Liaison de données et Physique (Ethernet, Wi-Fi)**

#### 2. Méthodes HTTP

HTTP utilise différentes méthodes pour indiquer l'action désirée par le client sur le serveur :

- **GET** : Récupérer des données du serveur.
- **POST** : Envoyer des données au serveur pour traitement.
- **PUT** : Mettre à jour une ressource existante ou en créer une nouvelle.
- **DELETE** : Supprimer une ressource spécifique.
- **HEAD** : Identique à GET, mais sans le corps de la réponse.
- **OPTIONS** : Décrire les options de communication disponibles pour la ressource cible.

#### 3. Structure d'une Requête HTTP

Une requête HTTP typique comprend les éléments suivants :

```plaintext
GET /index.html HTTP/1.1
Host: www.example.com
User-Agent: Mozilla/5.0
Accept: text/html
```

- **Ligne de requête** : Indique la méthode (GET), le chemin (/index.html) et la version du protocole (HTTP/1.1).
- **En-têtes de requête** : Fournissent des informations supplémentaires comme l'hôte (Host), l'agent utilisateur (User-Agent) et le type de contenu accepté (Accept).

#### 4. Structure d'une Réponse HTTP

Une réponse HTTP typique comprend les éléments suivants :

```plaintext
HTTP/1.1 200 OK
Content-Type: text/html
Content-Length: 137
```

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>
<h1>This is a Heading</h1>
<p>This is a paragraph.</p>
</body>
</html>
```

- **Ligne d'état** : Indique la version du protocole (HTTP/1.1), le code d'état (200) et le message (OK).
- **En-têtes de réponse** : Fournissent des informations sur le type de contenu (Content-Type) et la longueur du contenu (Content-Length).
- **Corps de la réponse** : Contient les données réelles, comme le HTML de la page web.

#### 5. Codes de Statut HTTP

Les codes de statut HTTP indiquent le résultat de la requête du client. Voici quelques codes communs :

- **1xx** : Informations (par exemple, 100 Continue)
- **2xx** : Succès (par exemple, 200 OK, 201 Created)
- **3xx** : Redirection (par exemple, 301 Moved Permanently, 302 Found)
- **4xx** : Erreur du client (par exemple, 404 Not Found, 401 Unauthorized)
- **5xx** : Erreur du serveur (par exemple, 500 Internal Server Error, 503 Service Unavailable)

![HTTP Status Codes](https://static.semrush.com/blog/uploads/media/3a/79/3a7950050980a0e2de37bc1a632cc321/wmkPPztB7KlAC7fPzO0-85NG8t0B9IEh4JEbt_ELP1pvJMhof9vt2pDSwrBZeXodoqaoV_Es1Rur-AWoeoOdV-RIde2vjqyMQuxrqch62uXZ1bsI0yaaMWx-f4cg4BlmOQrI2kFJ6CPXECCd69KeopE.png)

#### 6. HTTPS : HTTP Sécurisé

HTTPS (HTTP Secure) est la version sécurisée de HTTP, utilisant SSL/TLS pour chiffrer les données entre le client et le serveur. HTTPS fonctionne principalement sur le port 443.

#### 7. Labo Pratiques

##### Exercice 1 : Analyse d'une Requête HTTP

Utilisez un outil comme Wireshark pour capturer et analyser une requête HTTP lorsque vous visitez un site web.

##### Exercice 2 : Création d'une Page Web Simple

Créez une page HTML simple et hébergez-la sur un serveur web local (comme Apache ou Nginx). Utilisez votre navigateur pour envoyer des requêtes HTTP et observez les réponses.

#### Ressources Supplémentaires

- [RFC 2616 - Hypertext Transfer Protocol -- HTTP/1.1](https://www.ietf.org/rfc/rfc2616.txt)
- [MDN Web Docs - HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP)
- [Le protocole HTTP pour les débutants](https://www.it-connect.fr/le-protocole-http-pour-les-debutants/)
- [Wireshark/HTTP](https://en.wikiversity.org/wiki/Wireshark/HTTP)


