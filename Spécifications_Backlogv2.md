# Backlog Produit HomeSkolar

## Tableau des Développeurs
| **Rôle**     | **Développeurs** |
| ------------ | ---------------- |
| **Backend**  | Dev1, Dev2       |
| **Frontend** | Dev3, Dev4       |

---

## À FAIRE

### Authentification [P0]
- **[US1] En tant qu'utilisateur, je veux pouvoir créer un compte avec mes informations personnelles**
  - **Critères**: Validation email, choix du rôle (élève/tuteur), mot de passe sécurisé
  - **Estimation**: 3 jours
  - **Dépendances**: Aucune
  - **Test**: Vérifier que les emails sont validés, que les mots de passe sont sécurisés, et que le rôle est bien enregistré.

- **[US2] En tant qu'utilisateur, je veux pouvoir me connecter à mon compte**
  - **Critères**: Email/mot de passe valides, gestion des erreurs
  - **Estimation**: 2 jours
  - **Dépendances**: US1
  - **Test**: Vérifier qu’un utilisateur peut se connecter avec des informations valides et qu’un message d’erreur s’affiche sinon.

- **[US3] En tant qu'utilisateur, je veux pouvoir réinitialiser mon mot de passe**
  - **Critères**: Envoi email sécurisé, limitation tentatives
  - **Estimation**: 1 jour
  - **Dépendances**: US1
  - **Test**: Vérifier l’envoi d’email de réinitialisation et la limitation des tentatives par utilisateur.

---

### Communication [P1]
- **[US4] En tant qu'utilisateur, je veux pouvoir envoyer des messages à mon tuteur/élève**
  - **Critères**: Messages instantanés, historique conservé
  - **Estimation**: 4 jours
  - **Dépendances**: US1, US2
  - **Test**: Vérifier que les messages s’affichent instantanément et que l’historique est conservé.

- **[US5] En tant qu'utilisateur, je veux pouvoir épingler des messages importants**
  - **Critères**: Épinglage/désépinglage, section dédiée aux messages épinglés
  - **Estimation**: 2 jours
  - **Dépendances**: US4
  - **Test**: Vérifier que les messages peuvent être épinglés et apparaissent dans une section dédiée.

- **[US6] En tant qu'utilisateur, je veux recevoir des notifications pour les nouveaux messages**
  - **Critères**: Notification en temps réel, compteur messages non lus
  - **Estimation**: 2 jours
  - **Dépendances**: US4
  - **Test**: Vérifier la réception de notifications en temps réel et le compteur des messages non lus.

---

### Planification [P1]
- **[US7] En tant qu'utilisateur, je veux voir un calendrier de mes rendez-vous**
  - **Critères**: Vue mensuelle/hebdomadaire, distinction types événements
  - **Estimation**: 4 jours
  - **Dépendances**: US1, US2
  - **Test**: Vérifier que les événements s’affichent correctement selon la vue choisie et sont catégorisés.

- **[US8] En tant qu'utilisateur, je veux pouvoir planifier des rendez-vous**
  - **Critères**: Choix date/heure, durée, description
  - **Estimation**: 3 jours
  - **Dépendances**: US7
  - **Test**: Vérifier que l’utilisateur peut créer, modifier et supprimer un rendez-vous.

---

### Gestion des tâches [P2]
- **[US9] En tant que tuteur, je veux pouvoir assigner des tâches après une rencontre**
  - **Critères**: Description, date limite, statut
  - **Estimation**: 3 jours
  - **Dépendances**: US8
  - **Test**: Vérifier qu’un tuteur peut assigner une tâche avec les champs requis.

- **[US10] En tant qu'utilisateur, je veux pouvoir créer des tâches personnelles**
  - **Critères**: Tâches privées, rappels personnalisables
  - **Estimation**: 2 jours
  - **Dépendances**: US1
  - **Test**: Vérifier que l’utilisateur peut créer une tâche privée et recevoir des rappels.

---

## Sprints Planifiés

### **Sprint 1** : Authentification
| **US** | **Tâche**                     | **Développeurs** | **Estimation** |
| ------ | ----------------------------- | ---------------- | -------------- |
| US1    | Création de compte            | Dev1, Dev3       | 3 jours        |
| US2    | Connexion                     | Dev1, Dev3       | 2 jours        |
| US3    | Réinitialisation mot de passe | Dev2, Dev3       | 1 jour         |

### **Sprint 2** : Communication
| **US** | **Tâche**             | **Développeurs** | **Estimation** |
| ------ | --------------------- | ---------------- | -------------- |
| US4    | Messagerie            | Dev2, Dev4       | 4 jours        |
| US5    | Épinglage de messages | Dev2, Dev4       | 2 jours        |
| US6    | Notifications         | Dev2, Dev4       | 2 jours        |

### **Sprint 3** : Planification et Gestion des tâches
| **US** | **Tâche**                       | **Développeurs** | **Estimation** |
| ------ | ------------------------------- | ---------------- | -------------- |
| US7    | Calendrier                      | Dev1, Dev4       | 4 jours        |
| US8    | Planification de rendez-vous    | Dev1, Dev4       | 3 jours        |
| US9    | Assignation des tâches          | Dev2, Dev4       | 3 jours        |
| US10   | Création de tâches personnelles | Dev1, Dev4       | 2 jours        |

---

## Tableau récapitulatif

| **US** | **Tâche**                       | **Priorité** | **Dépendances** | **Estimation** |
| ------ | ------------------------------- | ------------ | --------------- | -------------- |
| US1    | Création de compte              | P0           | Aucune          | 3 jours        |
| US2    | Connexion                       | P0           | US1             | 2 jours        |
| US3    | Réinitialisation mot de passe   | P0           | US1             | 1 jour         |
| US4    | Messagerie                      | P1           | US1, US2        | 4 jours        |
| US5    | Épinglage de messages           | P1           | US4             | 2 jours        |
| US6    | Notifications                   | P1           | US4             | 2 jours        |
| US7    | Calendrier                      | P1           | US1, US2        | 4 jours        |
| US8    | Planification de rendez-vous    | P1           | US7             | 3 jours        |
| US9    | Assignation des tâches          | P2           | US8             | 3 jours        |
| US10   | Création de tâches personnelles | P2           | US1             | 2 jours        |

---

## LÉGENDE
- **P0**: Priorité Critique
- **P1**: Priorité Haute
- **P2**: Priorité Moyenne
