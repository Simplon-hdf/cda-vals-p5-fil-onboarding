# 📋 Plan de Test — Bot Discord de Collecte de Ressources

---

## Introduction

Ce plan de test décrit les vérifications à effectuer pour garantir le bon fonctionnement du bot Discord et de son API.  

---

## Périmètre des tests

| Composant                            | Couverture visée |
|-------------------------------------|------------------|
| Fonctions du bot (commandes, logique) | 80%             |
| Calculs / Formules d'expérience     | 100%             |
| Opérations CRUD (ressources, utilisateurs) | 50%        |
| Endpoints API                       | 100%             |

---

## Stratégie de test

### 🔹 Tests Unitaires

**Objectif :** Valider les comportements attendus de chaque fonction isolée.

- Commandes Discord
- Fonctions de calcul (XP, classement)
- Validation des entrées utilisateur

### 🔹 Tests d’intégration

**Objectif :** Vérifier le bon fonctionnement entre les composants.

- Interaction Bot ↔ API
- API ↔ PostgreSQL
- Bot ↔ Discord 

### 🔹 Tests End-to-End (E2E)

**Objectif :** Tester l’ensemble du parcours utilisateur.

- Commande utilisateur Discord → Sauvegarde dans la base
- Recherche de ressource → Résultat affiché dans Discord
- Ajout de tags / votes → BDD mise à jour

---

## Ressources humaines & techniques

- **Équipe de test:**
  - 3 développeurs

- **Outils :**
  - Jest  
  - Docker

---

## Environnement de test

- Node.js
- PostgreSQL 
- Clé API du bot 
- Serveur Discord privé de test

---

## ✅ Critères d’acceptation

| Critère                             | Détail                                                           |
|------------------------------------|-------------------------------------------------------------------|
| Aucune erreur critique non gérée   | Toutes les erreurs critiques prévues doivent être interceptées    |
| Pas de message perdu               | Toutes les interactions utilisateur sont traitées                 |
| Résilience à la latence Discord    | Pas de crash ou timeout en cas de réponse lente                   |
| Persistance des données            | Les ressources et actions sont bien enregistrées en BDD           |


