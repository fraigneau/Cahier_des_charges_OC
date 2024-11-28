# Spécifications Fonctionnelles - CodeIguanas

---

## 1. Authentification des utilisateurs

### Description :
Permettre aux élèves (**E**) et aux bénévoles (**B**) de s’inscrire, se connecter et gérer leurs informations personnelles.

### Fonctionnalités :
- **Inscription** :
  - Les utilisateurs remplissent un formulaire contenant :
    - Nom, prénom, adresse email, mot de passe.
    - Rôle à choisir entre élève ou bénévole.
  - Enregistrement sécurisé des données dans la base de données.
  - Vérification de l’unicité de l’adresse email.
- **Connexion** :
  - Saisie de l'email et du mot de passe pour accéder au compte.
  - Gestion des erreurs (mauvais mot de passe ou email inconnu).
- **Mot de passe oublié** :
  - Système de récupération via email.
- **Gestion des données personnelles** :
  - Possibilité de consulter et modifier les informations (nom, email, mot de passe).

### Critères de validation :
- Un utilisateur inscrit peut se connecter avec les identifiants fournis.
- Le système de récupération de mot de passe fonctionne et garantit une sécurité adéquate.

---

## 2. Communication élève-tuteur

### Description :
Mettre en place une messagerie simple pour permettre la communication entre élèves et tuteurs.

### Fonctionnalités :
- **Échanges de messages** :
  - Les élèves peuvent envoyer des messages à leur tuteur assigné.
  - Les tuteurs peuvent répondre aux messages des élèves.
- **Épinglage des messages** :
  - Chaque utilisateur peut épingler certains messages pour les retrouver rapidement.
- **Notifications** :
  - Notification en temps réel pour tout message non lu.

### Critères de validation :
- Les messages sont visibles uniquement entre l’élève et son tuteur.
- Les utilisateurs reçoivent des notifications pour les nouveaux messages.
- Les messages épinglés apparaissent dans une section dédiée.

---

## 3. Planification des rencontres

### Description :
Créer un calendrier interactif pour planifier les rendez-vous entre élèves et tuteurs.

### Fonctionnalités :
- **Page calendrier** :
  - Vue hebdomadaire et mensuelle des événements.
  - Possibilité d’ajouter un événement avec :
    - Date, heure, durée.
    - Description optionnelle (ex. : type de rencontre, lieu).
  - Affichage des événements planifiés entre l’élève et son tuteur.
- **Gestion des événements** :
  - Modification ou suppression des rendez-vous.
  - Notifications avant les événements (rappel).

### Critères de validation :
- Les événements apparaissent correctement dans le calendrier.
- Les rappels sont envoyés à l’élève et au tuteur avant chaque rencontre.

---

## 4. Gestion des tâches

### Description :
Permettre la création et le suivi des tâches assignées après chaque rencontre ou par les utilisateurs eux-mêmes.

### Fonctionnalités :
- **Tâches liées à une rencontre** :
  - Créées par le tuteur à la fin d'une rencontre.
  - Notifications pour informer l'élève des tâches à réaliser.
  - Suivi de l’état des tâches (en cours, terminé).
- **Tâches personnelles** :
  - Créées par l’élève ou le tuteur indépendamment des rencontres.
  - Possibilité de définir une échéance ou des rappels.
- **Modification et suppression** :
  - Modification possible des tâches (titre, description, date d’échéance).
  - Suppression possible des tâches obsolètes.

### Critères de validation :
- Les tâches créées sont visibles dans l’agenda de l’utilisateur.
- Les utilisateurs peuvent cocher une tâche comme "terminée".
- Les rappels et notifications fonctionnent correctement.

---

## Récapitulatif des exigences fonctionnelles

| **Module**                | **Fonctionnalité principale**                                                                 |
|---------------------------|-----------------------------------------------------------------------------------------------|
| **Authentification**      | Inscription, connexion, récupération de mot de passe.                                         |
| **Communication**         | Messagerie entre élèves et tuteurs avec épinglage des messages et notifications.              |
| **Planification**         | Calendrier interactif pour la gestion des rendez-vous.                                        |
| **Gestion des tâches**    | Création, modification, et suivi des tâches (liées à une rencontre ou personnelles).          |
