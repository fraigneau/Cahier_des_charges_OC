# Spécifications Techniques - CodeIguanas

## 1. Architecture du projet

### 1.1. Type d'application
- **Type** : Application Web.
- **Architecture** : Client-serveur.
- **Frontend** : Application web accessible via un navigateur.
- **Backend** : API REST pour la gestion des données et des fonctionnalités.

### 1.2. Technologies recommandées
- **Frontend** :
  - Framework : React.js ou Vue.js.
  - Langages : HTML, CSS, JavaScript (TypeScript recommandé).
  - Bibliothèque UI : Material-UI ou Tailwind CSS.
- **Backend** :
  - Langage : Node.js (avec Express.js) ou Java (Spring Boot).
  - Base de données : PostgreSQL pour les données relationnelles.
  - Authentification : JSON Web Tokens (JWT).
- **Infrastructure** :
  - Serveur : Hébergement sur un service cloud (AWS, Azure, ou Heroku).
  - CI/CD : GitHub Actions ou GitLab CI pour l'intégration continue.
  - Sécurité : HTTPS obligatoire, données sensibles chiffrées.

---

## 2. Gestion des utilisateurs

### 2.1. Authentification
- **Mécanisme** : Authentification basée sur JWT.
- **Flux** :
  - Lors de la connexion, le serveur génère un token JWT.
  - Le token est envoyé au client et utilisé pour chaque requête nécessitant une authentification.
- **Sécurité** :
  - Mot de passe haché avec bcrypt (minimum 10 rounds).
  - Limitation des tentatives de connexion pour éviter les attaques par force brute.

### 2.2. Gestion des rôles
- **Rôles utilisateurs** : 
  - Élève : Accès limité à son propre contenu.
  - Tuteur : Gestion des tâches et interactions avec les élèves assignés.
  - Administrateur : Gestion des utilisateurs et des relations E-B.
- **Contrôle d’accès** : Middleware pour vérifier les droits d'accès à chaque endpoint.

---

## 3. Communication élève-tuteur

### 3.1. Messagerie
- **Backend** :
  - Stockage des messages dans une table relationnelle (exemple : `messages`).
  - Champs principaux : ID message, ID expéditeur, ID destinataire, contenu, date, état (lu/non lu).
  - API REST :
    - `POST /messages` : Envoi de message.
    - `GET /messages` : Récupération des messages entre deux utilisateurs.
    - `PATCH /messages/:id` : Marquer un message comme lu.
- **Frontend** :
  - Affichage des messages dans un format "discussion".
  - Option pour épingler un message, enregistré côté serveur.
- **Notifications** :
  - WebSockets ou service de notification push pour avertir l’utilisateur en temps réel.

---

## 4. Planification des rencontres

### 4.1. Calendrier
- **Backend** :
  - Stockage des événements dans une table `events`.
  - Champs principaux : ID événement, titre, description, date, heure, durée, ID utilisateur.
  - API REST :
    - `POST /events` : Création d’un événement.
    - `GET /events` : Récupération des événements par utilisateur.
    - `PATCH /events/:id` : Modification d’un événement.
    - `DELETE /events/:id` : Suppression d’un événement.
- **Frontend** :
  - Intégration d’une bibliothèque de calendrier (exemple : FullCalendar.js).
  - Vue hebdomadaire/mensuelle.
  - Notifications de rappel via des alertes ou un email.

---

## 5. Gestion des tâches

### 5.1. Tâches liées aux rencontres
- **Backend** :
  - Table `tasks` avec les champs :
    - ID tâche, ID créateur (élève ou tuteur), ID élève concerné, description, date d’échéance, statut (en cours, terminé).
  - API REST :
    - `POST /tasks` : Création d’une tâche.
    - `GET /tasks` : Récupération des tâches liées à un utilisateur.
    - `PATCH /tasks/:id` : Mise à jour du statut ou des détails d’une tâche.
    - `DELETE /tasks/:id` : Suppression d’une tâche.
- **Frontend** :
  - Liste des tâches par statut.
  - Option pour ajouter une tâche personnelle ou liée à une rencontre.
  - Notifications pour les échéances imminentes.

---

## 6. Performance et sécurité

### 6.1. Optimisation des performances
- Mise en cache des requêtes fréquentes avec Redis.
- Pagination pour les requêtes longues (messages, tâches).
- Compression des réponses HTTP avec gzip.

### 6.2. Sécurité
- **Backend** :
  - Validation des entrées pour prévenir les injections SQL.
  - Protection contre les attaques XSS et CSRF.
  - Chiffrement SSL/TLS pour toutes les communications.
- **Frontend** :
  - Validation côté client pour les formulaires.
  - Protection des données sensibles en localStorage avec expiration du token.

---

## 7. Documentation et tests

### 7.1. Documentation
- Documentation des API avec Swagger ou Postman.
- Manuel utilisateur pour l’application.

### 7.2. Tests
- Tests unitaires pour les fonctions critiques (Jest pour Node.js ou JUnit pour Java).
- Tests d’intégration pour vérifier les interactions entre les modules.
- Tests d’interface utilisateur avec Cypress ou Selenium.

---

## 8. Récapitulatif technique

| **Module**               | **Technologie utilisée**                                    |
|---------------------------|------------------------------------------------------------|
| **Frontend**              | React.js, Material-UI, Axios                               |
| **Backend**               | Node.js (Express), PostgreSQL, JWT                        |
| **Base de données**       | PostgreSQL                                                 |
| **Calendrier**            | FullCalendar.js                                           |
| **Messagerie**            | WebSocket, REST API                                       |
| **Notifications**         | WebSockets ou Push API                                    |
| **CI/CD**                 | GitHub Actions, Docker                                    |

---

Cette spécification technique servira de guide pour les développeurs durant la mise en œuvre du projet **CodeIguanas**.
