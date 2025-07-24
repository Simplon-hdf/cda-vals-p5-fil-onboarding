# 📋 Plan de Test — Bot Discord de Collecte de Ressources

---

## Introduction

Ce plan de test décrit les vérifications à effectuer pour garantir le bon fonctionnement du bot Discord et de son API.

---

## Périmètre des tests

| Composant                           | Couverture visée |
|-------------------------------------|------------------|
| Commandes et évènements Discord     | 80%              |
| Gestion des rôles                   | 100%             |
| Intégration Bot/API                 | 50%              |
| Endpoints API                       | 100%             |

---

## Stratégie de test

### 🔹 Tests Unitaires

**Objectif :** Valider les comportements attendus de chaque fonction isolée.

- Commandes Discord
- Rôles et permissions correctement attribués (avec mock)
- Fonctions utilitaires
- Archivage

### 🔹 Tests d’intégration

**Objectif :** Vérifier le bon fonctionnement entre les modules.

- Interaction Bot <-> API
- API <-> PostgreSQL
- Bot <-> Discord

### 🔹 Tests End-to-End (E2E)

**Objectif :** Tester l’ensemble du parcours utilisateur.

- Commande utilisateur Discord -> Sauvegarde dans la base de données
- Création/Archivage d'une promotion -> Rôles correctement attribués, salons créés/supprimés
- Demande de rejoindre une promotion -> Accepter/Refuser
---

## Ressources humaines & techniques

- **Équipe de test:**
  - 3 développeurs

- **Outils :**
  - Jest
  - Supertest
  - Docker
  - Serveur Discord privé

  ---

## Environnement de test

- Node.js (Bot, API)
- NestJS (API)
- PostgreSQL
- Docker Compose
- Variables d'environnement (.env.test)
- Clé API du bot
- Serveur Discord privé de test

---

## Critères d’acceptation

| Critère                             | Détail                                                           |
|------------------------------------|-------------------------------------------------------------------|
| Aucune erreur critique non gérée   | Toutes les erreurs critiques prévues doivent être interceptées    |
| Pas de message perdu               | Toutes les interactions utilisateur sont traitées                 |
| Résilience à la latence Discord    | Pas de crash ou timeout en cas de réponse lente                   |
| Persistance des données            | Les ressources et actions sont bien enregistrées en BDD           |