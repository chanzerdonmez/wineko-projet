# WINEKO

**WINEKO** est une plateforme e-commerce spécialisée dans le déstockage de produits non alimentaires. Ce projet inclut une application front-end développée avec Angular et une API back-end sécurisée avec Spring Boot.

## Table des Matières
1. [Prérequis](#prérequis)
2. [Installation](#installation)
3. [Configuration](#configuration)
4. [Utilisation](#utilisation)
5. [API Documentation](#api-documentation)
6. [Technologies](#technologies)
7. [Contribuer](#contribuer)
8. [Licence](#licence)

## Prérequis

Avant de commencer, assurez-vous d’avoir les éléments suivants installés sur votre machine :

- [Node.js](https://nodejs.org/en/) (version 14 ou supérieure)
- [Angular CLI](https://angular.io/cli)
- [Java 11+](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)
- [MySQL](https://www.mysql.com/)

## Installation

### 1. Clonez le dépôt

```bash
git clone https://github.com/chanzerdonmez/wineko-projet.git
cd WINEKO

2. Installation du Front-end

cd frontend
npm install
ng serve
Le front-end sera accessible sur http://localhost:4200.

3. Installation du Back-end

cd backend
mvn install
java -jar target/api-0.0.1-SNAPSHOT.jar
Le back-end sera accessible sur http://localhost:8080.

Configuration

Configuration de la base de données
Créez un fichier .env dans le répertoire backend pour configurer la connexion à la base de données MySQL et d'autres variables sensibles.

Exemple de configuration .env :

env
Copier le code
SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3307/winekovf
SPRING_DATASOURCE_USERNAME=root
SPRING_DATASOURCE_PASSWORD=

RECAPTCHA_SITE_KEY=your-recaptcha-site-key
RECAPTCHA_SECRET_KEY=your-recaptcha-secret-key
Assurez-vous d'avoir créé une base de données MySQL nommée wineko_db.

Utilisation

Lancer le projet localement
Lancer le back-end : Depuis le répertoire backend, exécutez :

java -jar target/api-0.0.1-SNAPSHOT.jar
Lancer le front-end : Depuis le répertoire frontend, exécutez :

ng serve
Accédez à l'application via http://localhost:4200.

Lancer les tests
Tests unitaires Front-end :

cd frontend
ng test
Tests Back-end :

cd backend
mvn test
API Documentation

L'API REST de WINEKO expose plusieurs endpoints pour gérer les utilisateurs, produits, et commandes. Voici un aperçu des principales routes :

Authentification
POST /api/open/login: Authentifie un utilisateur.
POST /api/open/register: Inscrit un nouvel utilisateur.
GET /api/open/confirm: Confirme un compte utilisateur via un token.


Produits
GET /api/products: Récupère la liste des produits.
GET /api/products/{id}: Récupère les détails d’un produit.


Panier
POST /api/carts/{userId}/items: Ajoute un article au panier de l'utilisateur.
GET /api/carts/{userId}: Récupère les détails du panier de l'utilisateur.


Sécurité des API
L'authentification des routes protégées est gérée via des JWT (JSON Web Tokens). Assurez-vous de bien configurer les tokens dans les requêtes pour accéder aux routes sécurisées.

Technologies

Le projet WINEKO utilise les technologies suivantes :

Front-end : Angular (TypeScript, HTML, SCSS)
Back-end : Spring Boot (Java)
Base de données : MySQL
Authentification : JSON Web Tokens (JWT)
Sécurité : Spring Security, SSL/TLS pour HTTPS, BCrypt pour le hachage des mots de passe
Déploiement : Docker, Nginx, Certbot pour SSL


Contribuer

Les contributions sont les bienvenues ! Pour contribuer :

Forkez ce dépôt.
Créez une branche pour votre fonctionnalité (git checkout -b feature/nouvelle-fonctionnalité).
Commitez vos modifications (git commit -m 'Ajout d'une nouvelle fonctionnalité').
Poussez sur la branche (git push origin feature/nouvelle-fonctionnalité).
Soumettez une Pull Request.
