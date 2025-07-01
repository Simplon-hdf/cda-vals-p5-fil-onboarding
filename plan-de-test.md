# 📋 Plan de Test — Tableau vierge

## Introduction

Ce plan de test décrit les vérifications à effectuer pour garantir le bon fonctionnement du bot Discord et de son API.

## Périmètre des tests

- Les fonctions du bots : 80%
- Calculs/Formules d'expérience: 100%
- Operation CRUD: 50%
- Les endpoints: 100%   


## Stratégie de test

- Tests Unitaires: Commandes Discord, Fonction métier
- Intégration: Connexion API-BDD PostgreSQL, Interactions avec Discord
- E2E: Entré de la commande à la base de donnée


## Ressources

- Qui: Toute l'équipe (3 personnes)
- Jest pour les tests (NodeJS)
- Serveur Discord pour test


## Environnement de test

- NodeJS
- PostgreSQL (local)
- Docker
- Clé API bot
- Serveur Discord de test


## Critères d'acceptation

- Pas d'erreurs (Requêtes API renvoient les bons code HTTP)
- Exception faite des erreurs prises en charge
- Pas de message perdu
- Persistance des données



