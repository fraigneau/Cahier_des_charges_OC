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



### RÉCAPITULATIF PAR DÉVELOPPEUR

| Tâche                        | Développeur |
| ---------------------------- | ----------- |
| [US1] Création de compte     | Dev1        |
| [US2] Connexion              | Dev2        |
| [US3] Réinitialisation MDP   | Dev3        |
| [US4] Messagerie instantanée | Dev1        |
| [US5] Épinglage de messages  | Dev4        |
| [US6] Notifications          | Dev2        |
| [US7] Calendrier             | Dev3        |
| [US8] Planification          | Dev4        |
| [US9] Assignation de tâches  | Dev1        |
| [US10] Tâches personnelles   | Dev3        |

---

## SPRINT 1 (2 Semaines)

### Objectifs du Sprint:
1. Implémentation de la fonctionnalité d'authentification (US1, US2, US3).
2. Mise en place de la messagerie de base (US4).

### Détails:
- **Semaine 1**:
  - Dev1: US1 (Backend + Frontend)
  - Dev2: US2 (Backend + Frontend)
  - Dev3: US3 (Backend + Frontend)
- **Semaine 2**:
  - Dev1: US4 (Backend + Frontend)
  - Dev2: Tests de validation pour US1, US2, US3
  - Dev3: Intégration et validation de la messagerie (US4)

## SPRINT 2 (2 Semaines)

### Objectifs du Sprint:
1. Amélioration des fonctionnalités de messagerie (US5, US6).
2. Mise en place du calendrier et de la planification (US7, US8).

### Détails:
- **Semaine 1**:
  - Dev4: US5 (Frontend uniquement)
  - Dev2: US6 (Backend + Frontend)
  - Dev3: US7 (Backend + Frontend)
- **Semaine 2**:
  - Dev1: US8 (Backend + Frontend)
  - Dev3: Tests et validation complète des événements (US7, US8)

---

## LÉGENDE
- **P0**: Priorité Critique - Indispensable pour assurer un fonctionnement de base du produit. Sans ces tâches, l'application ne peut pas être utilisée.
- **P1**: Priorité Haute - Fonctionnalités clés qui enrichissent significativement l'expérience utilisateur et sont essentielles à moyen terme.
- **P2**: Priorité Moyenne - Améliorations ou fonctionnalités secondaires qui peuvent être différées si nécessaire.
- **Frontend**: Tâches liées à l’interface utilisateur, comprenant la présentation et les interactions visuelles.
- **Backend**: Tâches liées à la logique serveur ou à la gestion des données, telles que les bases de données et les API.

