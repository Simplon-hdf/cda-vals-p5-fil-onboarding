# 📚 Dictionnaire de Données

---

## **Message**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_message`           | UUID       | Identifiant unique du message                       | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `titre`                | varchar    | Titre du message                                    | `GitHub action explanation video`             |                        |
| `description`          | text       | Description du message                              | `Voici une vidéo explicative de GitHub Actions pour débutants` | NOT NULL               |
| `date_publication`     | timestamp  | Date de publication du message                      | `2002-10-20`                                  | NOT NULL               |
| `date_modification`    | date       | Date de modification du message                     | `2002-10-20`                                  |                        |
| `snowflake_message`    | varchar    | ID du message sur Discord                           | `1387453638036946985`                         | UNIQUE, NOT NULL       |

---

## **Solution**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_solution`          | UUID       | Identifiant unique de la solution                   | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |

---

## **Question**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_question`          | UUID       | Identifiant unique de la question                   | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |

---

## **Ressource**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_ressource`         | UUID       | Identifiant unique de la ressource                  | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `lien`                 | varchar    | Lien de la ressource                                | `www.google.com`                              |                        |

---

## **Étiquette**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_etiquette`         | UUID       | Identifiant unique de l’étiquette                   | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `nom_etiquette`        | varchar    | Nom de l’étiquette                                  | `git`                                        | UNIQUE, NOT NULL       |

---

## **Forum**

| **Attribut**           | **Type**       | **Description**                        | **Exemple**              | **Contrainte**    |
|------------------------|----------------|----------------------------------------|--------------------------|-------------------|
| `id_forum`             | UUID           | Identifiant unique du forum            | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f` | Primary key        |
| `nom_forum`            | varchar(100)   | Nom du forum                           | `conception`             | NOT NULL          |

---

## **Membre**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_membre`            | UUID       | Identifiant unique du membre                        | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `snowflake_user`       | varchar    | ID Discord de l’utilisateur                         | `1387453638036946985`                         | UNIQUE, NOT NULL       |

---

## **Votes**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_vote_message`      | UUID       | Identifiant unique du vote sur un message          | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `vote_type`            | boolean    | Vote positif (1) ou négatif (0)                     | `1`                                           | NOT NULL               |

---

## **XP**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_xp`                | UUID       | Identifiant unique de l’expérience (XP)             | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |

---

## **XP Type**

| **Attribut**           | **Type**   | **Description**                                     | **Exemple**                                  | **Contrainte**         |
|------------------------|------------|-----------------------------------------------------|----------------------------------------------|------------------------|
| `id_xp_type`           | UUID       | Identifiant unique du type d’expérience             | `4f9a2b18-7c7b-4c8a-bc90-9e0b1e2d4a5f`         | Primary key            |
| `libelle_type_xp`      | varchar    | Nom du type d’expérience                            | `Ressource`                                   | UNIQUE, NOT NULL       |
| `valeur_type_xp`       | int        | Valeur du type d’expérience                         | `10`                                          | NOT NULL               |
