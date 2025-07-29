# Architecture Logicielle du Système

## 1. Architecture Choisie : Architecture Multicouche (N-tier)

Ce système est conçu selon une architecture logicielle multicouche pour garantir une séparation claire des responsabilités, faciliter la maintenance, l'évolutivité et les tests.

### Couches principales :

- **Présentation :**
  - Client principal : Bot Discord (implémenté avec `Discord.js v14+`)
  - Rôle : Interface utilisateur pour interaction directe

- **Contrôleur / API :**
  - Technologie : `NestJS`
  - Rôle : Gère les requêtes REST API, fait le lien entre le bot et la logique métier

- **Service Métier (Business Logic) :**
  - Modules gérant les rôles, promotions (PROMO), utilisateurs, formation, etc.
  - Implémentation : Services NestJS modulaires

- **Accès aux Données :**
  - ORM : `TypeORM`
  - Base de données : `PostgreSQL`
  - Rôle : Accès, lecture et écriture sécurisée des données

- **Infrastructure :**
  - Conteneurisation : `Docker`
  - Intégration et déploiement continu (CI/CD) : prévu via pipeline GitHub Actions

## 2. Technologies Retenues

| Composant         | Technologie      | Raison de Choix |
|-------------------|------------------|------------------|
| Langage principal | TypeScript       | Fort typage, support par NestJS et Discord.js |
| Back-end Framework| NestJS           | Structure modulaire, support TypeScript natif |
| ORM               | TypeORM          | Intégration facile avec NestJS, support PostgreSQL |
| Base de données   | PostgreSQL       | Robuste, open-source, typage fort |
| Bot Discord       | Discord.js (v14+) | Large communauté, documentation complète |
| Conteneurisation  | Docker           | Isolation d’environnement, portabilité |
| CI/CD             | GitHub Actions (prévu) | Automatisation du déploiement, tests |

## 3. Structure du Dossier `src/`

```bash
src/
├── main.ts               
├── app.module.ts          
├── config/               
├── modules/
│   ├── user/
│   │   ├── user.controller.ts # Endpoint
│   │   ├── user.DTOs.ts
│   │   ├── user.service.ts
│   │   ├── user.mapper.ts
│   │   ├── user.repository.ts
│   │   ├── user.interfaceService.ts
│   │   ├── user.module.ts
│   │   └── entities/user.entity.ts
│   ├── promo/
│   ├── role/
│   └── formation/
├── database/
│   ├── typeorm.config.ts

```