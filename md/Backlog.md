# Backlog Produit HomeSkolar

## À FAIRE

### Authentification [P0]
- **[US1]** En tant qu'utilisateur, je veux pouvoir créer un compte avec mes informations personnelles
  - **Critères**: Validation email, choix du rôle (élève/tuteur), mot de passe sécurisé
  - **Estimation**: 3 jours
  - **Dépendances**: Aucune
  - **Tests**: Validation des champs, test de régression sur le formulaire, scénarios de test automatisés sur la création de compte

- **[US2]** En tant qu'utilisateur, je veux pouvoir me connecter à mon compte
  - **Critères**: Email/mot de passe valides, gestion des erreurs
  - **Estimation**: 2 jours
  - **Dépendances**: US1
  - **Tests**: Tests unitaires pour validation des crédentials, tests manuels pour la gestion des erreurs

- **[US3]** En tant qu'utilisateur, je veux pouvoir réinitialiser mon mot de passe
  - **Critères**: Envoi email sécurisé, limitation tentatives
  - **Estimation**: 1 jour
  - **Dépendances**: US1
  - **Tests**: Tests d’intégration pour l’envoi de mails, tests de sécurité sur la limitation de tentatives

### Communication [P1]
- **[US4]** En tant qu'utilisateur, je veux pouvoir envoyer des messages à mon tuteur/élève
  - **Critères**: Messages instantanés, historique conservé
  - **Estimation**: 4 jours
  - **Dépendances**: US1, US2
  - **Tests**: Tests de performance pour l’instantanéité, tests de persistance sur l’historique

- **[US5]** En tant qu'utilisateur, je veux pouvoir épingler des messages importants
  - **Critères**: Épinglage/désépinglage, section dédiée aux messages épinglés
  - **Estimation**: 2 jours
  - **Dépendances**: US4
  - **Tests**: Tests fonctionnels sur l’épinglage/désépinglage, validation UX sur la section dédiée

- **[US6]** En tant qu'utilisateur, je veux recevoir des notifications pour les nouveaux messages
  - **Critères**: Notification en temps réel, compteur messages non lus
  - **Estimation**: 2 jours
  - **Dépendances**: US4
  - **Tests**: Tests de notification push, tests fonctionnels sur le compteur de messages non lus

### Planification [P1]
- **[US7]** En tant qu'utilisateur, je veux voir un calendrier de mes rendez-vous
  - **Critères**: Vue mensuelle/hebdomadaire, distinction types événements
  - **Estimation**: 4 jours
  - **Dépendances**: US1, US2
  - **Tests**: Tests d’interface sur les vues, validation des événements multiples

- **[US8]** En tant qu'utilisateur, je veux pouvoir planifier des rendez-vous
  - **Critères**: Choix date/heure, durée, description
  - **Estimation**: 3 jours
  - **Dépendances**: US7
  - **Tests**: Tests unitaires sur les validations de date/heure, tests de régression sur la fonctionnalité de planification

### Gestion des tâches [P2]
- **[US9]** En tant que tuteur, je veux pouvoir assigner des tâches après une rencontre
  - **Critères**: Description, date limite, statut
  - **Estimation**: 3 jours
  - **Dépendances**: US8
  - **Tests**: Tests fonctionnels sur l’assignation, validation des rappels pour les tâches

- **[US10]** En tant qu'utilisateur, je veux pouvoir créer des tâches personnelles
  - **Critères**: Tâches privées, rappels personnalisables
  - **Estimation**: 2 jours
  - **Dépendances**: US1
  - **Tests**: Tests unitaires pour les rappels, tests UX pour les tâches privées

---

## Tableau des Développeurs
| **Rôle**     | **Développeurs** |
| ------------ | ---------------- |
| **Backend**  | Dev1, Dev2       |
| **Frontend** | Dev3, Dev4       |

---

## **Sprint 1** (15 jours)  
| **Semaine**   | **Tâches**                                          | **Dev**    | **Durée (jours)** |
| ------------- | --------------------------------------------------- | ---------- | ----------------- |
| **Semaine 1** | **Objectif**: Mise en place de l'authentification   |            |                   |
|               | Implémentation de **US1** (Backend + Frontend)      | Dev1, Dev3 | 3 jours           |
|               | Implémentation de **US2** (Backend + Frontend)      | Dev2, Dev4 | 2 jours           |
|               | Début de **US3** (Backend uniquement)               | Dev1       | 1 jour            |
| **Semaine 2** | **Objectif**: Intégration de la messagerie          |            |                   |
|               | Finalisation de **US3** (Frontend uniquement)       | Dev3       | 1 jour            |
|               | Implémentation de **US4** (Backend + Frontend)      | Dev1, Dev3 | 4 jours           |
|               | Validation des tests pour **US1**, **US2**, **US3** | Dev2, Dev4 | 2 jours           |

---

## **Sprint 2** (15 jours)  
| **Semaine**   | **Tâches**                                                     | **Dev**    | **Durée (jours)** |
| ------------- | -------------------------------------------------------------- | ---------- | ----------------- |
| **Semaine 1** | **Objectif**: Amélioration de la messagerie                    |            |                   |
|               | Implémentation de **US5** (Frontend uniquement)                | Dev3       | 2 jours           |
|               | Implémentation de **US6** (Backend + Frontend)                 | Dev2, Dev4 | 2 jours           |
|               | Début de **US7** (Backend + Frontend)                          | Dev1, Dev4 | 2 jours           |
| **Semaine 2** | **Objectif**: Mise en place du calendrier et validation        |            |                   |
|               | Finalisation de **US7** (Backend + Frontend)                   | Dev1, Dev4 | 2 jours           |
|               | Implémentation de **US8** (Backend + Frontend)                 | Dev1, Dev3 | 3 jours           |
|               | Tests et validation complète des événements (**US7**, **US8**) | Dev2, Dev4 | 2 jours           |

---

## LÉGENDE
- **P0**: Priorité Critique - Indispensable pour assurer un fonctionnement de base du produit. Sans ces tâches, l'application ne peut pas être utilisée.
- **P1**: Priorité Haute - Fonctionnalités clés qui enrichissent significativement l'expérience utilisateur et sont essentielles à moyen terme.
- **P2**: Priorité Moyenne - Améliorations ou fonctionnalités secondaires qui peuvent être différées si nécessaire.
- **Frontend**: Tâches liées à l’interface utilisateur, comprenant la présentation et les interactions visuelles.
- **Backend**: Tâches liées à la logique serveur ou à la gestion des données, telles que les bases de données et les API.

