# RBAC

Ce document décrit le modèle d’autorisations basé sur les rôles (RBAC) utilisé pour contrôler l’accès aux fonctionnalités du système.

---

## Rôles définis

| Rôle        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| **Admin**   | Rôle ayant tous les droits sur le système (création, modification, logs). |
| **CDP**     | Chef de projet responsable de la gestion quotidienne des promos.          |
| **Apprenant** | Utilisateur final, membre d’une promo, accès restreint.                  |

---

##  Accès aux actions par rôle

| Action                                     | Admin | CDP  | Apprenant |
|--------------------------------------------|:-----:|:----:|:---------:|
| Créer une promo                            | ✅    | ✅   | ❌        |
| Modifier une promo                         | ✅    | ✅   | ❌        |
| Supprimer une promo                        | ✅    | ✅   | ❌        |
| Créer des rôles pour une promo             | ✅    | ✅   | ❌        |
| Valider une demande d’identification       | ❌    | ✅   | ❌        |
| Rejoindre une promo                        | ❌    | ❌   | ✅        |
| Consulter les salons de sa promo           | ❌    | ❌   | ✅        |
| Voir les promos disponibles                | ✅    | ✅   | ✅        |
| Masquer ou afficher une promo              | ✅    | ✅   | ❌        |
| Lire les logs                              | ✅    | ❌   | ❌        |
| Créer un post ou forum dans une promo      | ✅    | ✅   | ✅        |

---


