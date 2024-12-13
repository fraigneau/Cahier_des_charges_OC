# Backlog Produit HomeSkolar prout

!!!!!!!!add tableau, add determination de qui fais quelle tache ! Sprint 
!!!!!!!! ajout cat test 

## À FAIRE

### Authentification [P0]
- [US1] En tant qu'utilisateur, je veux pouvoir créer un compte avec mes informations personnelles 
  - Critères: Validation email, choix du rôle (élève/tuteur), mot de passe sécurisé
  - Estimation: 3 jours
  - Dépendances: Aucune

- [US2] En tant qu'utilisateur, je veux pouvoir me connecter à mon compte
  - Critères: Email/mot de passe valides, gestion des erreurs
  - Estimation: 2 jours
  - Dépendances: US1

- [US3] En tant qu'utilisateur, je veux pouvoir réinitialiser mon mot de passe
  - Critères: Envoi email sécurisé, limitation tentatives
  - Estimation: 1 jour
  - Dépendances: US1

### Communication [P1]
- [US4] En tant qu'utilisateur, je veux pouvoir envoyer des messages à mon tuteur/élève
  - Critères: Messages instantanés, historique conservé
  - Estimation: 4 jours
  - Dépendances: US1, US2

- [US5] En tant qu'utilisateur, je veux pouvoir épingler des messages importants
  - Critères: Épinglage/désépinglage, section dédiée aux messages épinglés
  - Estimation: 2 jours
  - Dépendances: US4

- [US6] En tant qu'utilisateur, je veux recevoir des notifications pour les nouveaux messages
  - Critères: Notification en temps réel, compteur messages non lus
  - Estimation: 2 jours
  - Dépendances: US4

### Planification [P1]
- [US7] En tant qu'utilisateur, je veux voir un calendrier de mes rendez-vous
  - Critères: Vue mensuelle/hebdomadaire, distinction types événements
  - Estimation: 4 jours
  - Dépendances: US1, US2

- [US8] En tant qu'utilisateur, je veux pouvoir planifier des rendez-vous
  - Critères: Choix date/heure, durée, description
  - Estimation: 3 jours
  - Dépendances: US7

### Gestion des tâches [P2]
- [US9] En tant que tuteur, je veux pouvoir assigner des tâches après une rencontre
  - Critères: Description, date limite, statut
  - Estimation: 3 jours
  - Dépendances: US8

- [US10] En tant qu'utilisateur, je veux pouvoir créer des tâches personnelles
  - Critères: Tâches privées, rappels personnalisables
  - Estimation: 2 jours
  - Dépendances: US1

## LÉGENDE
- P0: Priorité Critique
- P1: Priorité Haute
- P2: Priorité Moyenne