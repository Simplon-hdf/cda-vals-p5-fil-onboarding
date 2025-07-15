# RBAC

Ce document décrit le modèle d’autorisations basé sur les rôles (RBAC) utilisé pour contrôler l’accès aux fonctionnalités du système.

---

## Rôles définis

| Rôle        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| **Admin**   | Rôle ayant tous les droits sur le système (création, modification, logs).   |
| **CDP**     | Chef de projet responsable de la gestion quotidienne des promos.            |
| **Apprenant** | Utilisateur final, membre d’une promo, accès restreint.                   |
| **Formateur** | En charge d'une ou plusieur promo, accès restreint                        |
| **Staff Simplon**| Membre de Simplon, peut gérer des demandes                                 |


---

##  Accès aux actions par rôle

| Action                                     | Admin | CDP  | Apprenant | Formateur | Staff Simplon |
|--------------------------------------------|:-----:|:----:|:---------:|:---------:|:-------------:|
| Créer une promo                            | ✅    | ✅   | ❌        |❌         |❌             |
| Modifier une promo                         | ✅    | ✅   | ❌        |❌         |❌             |
| Supprimer une promo                        | ✅    | ✅   | ❌        |❌         |❌             |
| Valider une demande d’identification       | ❌    | ✅   | ❌        |❌         |✅             |
| Faire une demande pour rejoindre une promo | ❌    | ❌   | ✅        |✅         |✅             |
| Consulter les salons de sa promo           | ❌    | ❌   | ✅        |✅         |✅             |
| Voir les promos disponibles                | ✅    | ✅   | ✅        |✅         |✅             |
| Lire les logs                              | ✅    | ❌   | ❌        |❌         |❌             |
| Créer un post ou forum dans une promo      | ✅    | ✅   | ✅        |✅         |✅             |

---


