

# Dictionnaire de données




| Nom de la table         | Nom de la colonne                | Type         | Contraintes              | Exemple                                | Description                                      |
|-------------------------|----------------------------------|--------------|--------------------------|----------------------------------------|--------------------------------------------------|
| UTILISATEUR             | id_utilisateur                   | BIGINT       | PRIMARY KEY              | 1187363829782638592                    | Identifiant unique de l’utilisateur              |
| UTILISATEUR             | nom_utilisateur                  | VARCHAR(100) | NOT NULL                 | Dupont                                 | Nom de famille de l’utilisateur                  |
| UTILISATEUR             | prenom_utilisateur               | VARCHAR(100) | NOT NULL                 | Alice                                  | Prénom de l’utilisateur                          |
| UTILISATEUR             | date_creation_utilisateur        | TIMESTAMPZ   | NOT NULL                 | 2025-07-15 10:30:00                    | Date de création de l’utilisateur                |
| UTILISATEUR             | date_modification_utilisateur    | TIMESTAMPZ   |                          | 2025-07-15 12:00:00                    | Date de modification de l’utilisateur            |
| ROLE                    | id_role                          | SMALLSERIAL  | PRIMARY KEY              | 1                                      | Identifiant unique du rôle                       |
| ROLE                    | nom_role                         | VARCHAR(50)  | NOT NULL                 | Administrateur                         | Nom du rôle                                      |
| ROLE                    | date_creation_role               | TIMESTAMPZ   | NOT NULL                 | 2025-06-10 09:00:00                    | Date de création du rôle                         |
| ROLE                    | date_modification_role           | TIMESTAMPZ   |                          | 2025-06-12 14:45:00                    | Date de modification du rôle                     |
| FORMATION               | id_formation                     | UUID         | PRIMARY KEY              | 550e8400-e29b-41d4-a716-446655440000   | Identifiant unique de la formation               |
| FORMATION               | libelle_formation                | VARCHAR(100) | NOT NULL                 | CDA                                    | Libellé ou nom de la formation                   |
| FORMATION               | date_creation_formation          | TIMESTAMPZ   | NOT NULL                 | 2025-01-01 08:00:00                    | Date de création de la formation                 |
| FORMATION               | date_modification_formation      | TIMESTAMPZ   |                          | 2025-01-15 09:00:00                    | Date de modification de la formation             |
| STATUT_IDENTIFICATION   | id_statut_identification         | SMALLSERIAL  | PRIMARY KEY              | 1                                      | Identifiant du statut d’identification           |
| STATUT_IDENTIFICATION   | libelle_identification           | VARCHAR(50)  | NOT NULL                 | en_attente                             | Statut : en_attente, accepté, refusé             |
| STATUT_IDENTIFICATION   | date_creation_identification     | TIMESTAMPZ   | NOT NULL                 | 2025-01-10 10:00:00                    | Date de création du statut                       |
| STATUT_IDENTIFICATION   | date_modification_identification | TIMESTAMPZ   |                          | 2025-01-12 11:30:00                    | Date de modification du statut                   |
| STATUT_PROMO            | id_statut_promo                  | SMALLSERIAL  | PRIMARY KEY              | 1                                      | Identifiant du statut de promo                   |
| STATUT_PROMO            | libelle_statut_promo             | VARCHAR(50)  | NOT NULL                 | active                                 | Statut : active, archivée                        |
| STATUT_PROMO            | date_creation_statut_promo       | TIMESTAMPZ   | NOT NULL                 | 2025-01-20 13:00:00                    | Date de création du statut                       |
| STATUT_PROMO            | date_modification_statut_promo   | TIMESTAMPZ   |                          | 2025-01-22 13:00:00                    | Date de modification du statut                   |
| CAMPUS                  | id_campus                        | UUID         | PRIMARY KEY              | 550e8400-e29b-41d4-a716-446655440000   | Identifiant du campus                            |
| CAMPUS                  | nom_campus                       | VARCHAR(100) | NOT NULL                 | Lille                                  | Nom du campus                                    |
| CAMPUS                  | date_creation_campus             | TIMESTAMPZ   | NOT NULL                 | 2025-03-01 08:00:00                    | Date de création du campus                       |
| CAMPUS                  | date_modification_campus         | TIMESTAMPZ   |                          | 2025-03-02 08:00:00                    | Date de modification du campus                   |
| PROMO                   | id_promo                         | UUID         | PRIMARY KEY              | 550e8400-e29b-41d4-a716-446655440000   | Identifiant de la promotion                      |
| PROMO                   | nom_promo                        | VARCHAR(100) | NOT NULL                 | Promo Java 2025                        | Nom de la promotion                              |
| PROMO                   | date_debut_promo                 | DATE         | NOT NULL                 | 2025-04-01                             | Date de début de la promotion                    |
| PROMO                   | date_fin_promo                   | DATE         | NOT NULL                 | 2025-12-31                             | Date de fin de la promotion                      |
| PROMO                   | date_creation_promo              | TIMESTAMPZ   | NOT NULL                 | 2025-03-01 10:00:00                    | Date de création de la promotion                 |
| PROMO                   | date_modification_promo          | TIMESTAMPZ   |                          | 2025-03-02 10:00:00                    | Date de modification                             |
| PROMO                   | id_statut_promo                  | SMALLSERIAL  | FK NOT NULL              | 1                                      | Statut (clé étrangère vers STATUT_PROMO)         |
| PROMO                   | id_formation                     | UUID         | FK NOT NULL              | 550e8400-e29b-41d4-a716-446655440000   | Formation associée                               |
| PROMO                   | id_campus                        | UUID         | FK NOT NULL              | 550e8400-e29b-41d4-a716-446655440000   | Campus associé                                   |
| IDENTIFICATION          | id_identification                | UUID         | PRIMARY KEY              | 550e8400-e29b-41d4-a716-446655440000   | Identifiant de l'identification                  |
| IDENTIFICATION          | date_creation_identification     | TIMESTAMPZ   | NOT NULL                 | 2025-05-01 10:00:00                    | Date de création                                 |
| IDENTIFICATION          | date_modification_identification | TIMESTAMPZ   |                          | 2025-05-01 10:30:00                    | Date de modification                             |
| IDENTIFICATION          | id_statut_identification         | SMALLSERIAL  | FK NOT NULL              | 2                                      | Statut de l’identification                       |
| UTILISATEUR_ROLE        | id_utilisateur                   | BIGINT       | PK, FK                   | 1187363829782638592                    | Utilisateur associé                              |
| UTILISATEUR_ROLE        | id_role                          | SMALLSERIAL  | PK, FK                   | 1                                      | Rôle associé                                     |
| FAIRE_DEMANDE           | id_utilisateur                   | BIGINT       | PK, FK                   | 1187363829782638592                    | Utilisateur qui fait la demande                  |
| FAIRE_DEMANDE           | id_identification                | UUID         | PK, FK                   | 550e8400-e29b-41d4-a716-446655440000   | Identification demandée                          |
| APPARTENIR_PROMO        | id_promo                         | UUID         | PK, FK                   | 550e8400-e29b-41d4-a716-446655440000   | Promotion à laquelle appartient                  |
| APPARTENIR_PROMO        | id_identification                | UUID         | PK, FK                   | 550e8400-e29b-41d4-a716-446655440000   | Identification associée                          |

