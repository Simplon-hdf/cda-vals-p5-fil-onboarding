# Benchmark

Ce document présente le processus de sélection de la stack technique pour un bot Discord, ainsi que celle du SGBDR associé à son API.

## Processus

Des critères ont été définis selon les besoins du projet, chacun pondéré en fonction de son importance relative. Chaque solution a ensuite été évaluée selon ces critères.

---

## Contexte technique

- 🎯 Le projet consiste à créer un bot Discord interagissant avec une API à créer aussi.
- ⚡ Objectif de performance : Traitement réactif des messages et commandes.
- 📦 Le système devra pouvoir évoluer.


---


## Choix de la bibliothèque pour le bot Discord

| Critère                        | Poids | discord.js | discord.py | discord.py rewrite | Eris   | Discord4J | DSharpPlus |
|-------------------------------|:-----:|:----------:|:----------:|:------------------:|:------:|:---------:|:----------:|
| Rapidité                      | 1     | ★★★★       | ★★★        | ★★★                | ★★★★   | ★★★★      | ★★★★       |
| Sécurité                      | 1.5   | ★★★★       | ★★★★       | ★★★★               | ★★★★   | ★★★★      | ★★★★       |
| Efficience (mémoire/matériel)| 2     | ★★★★       | ★★★        | ★★★                | ★★★★   | ★★★★      | ★★★★       |
| Complexité d’utilisation      | 1     | ★★★        | ★★★★       | ★★★★               | ★★★    | ★★★       | ★★★        |
| Communauté & Support          | 1.5   | ★★★★★      | ★★★★       | ★★★★               | ★★★    | ★★★       | ★★★        |
| Ancienneté / Maturité         | 1     | ★★★★★      | ★★★★       | ★★★                | ★★★    | ★★★★      | ★★★        |
| Stabilité                     | 1.5   | ★★★★       | ★★★        | ★★★★               | ★★★    | ★★★★      | ★★★★       |
| Intégration API Discord       | 2     | ★★★★★      | ★★★        | ★★★★               | ★★★    | ★★★★      | ★★★★       |
| Documentation                 | 1.5   | ★★★★       | ★★★        | ★★★★               | ★★★    | ★★★       | ★★★        |
| Mises à jour & Évolutivité    | 1     | ★★★★       | ★★★        | ★★★★               | ★★★    | ★★★       | ★★★        |
| **Total (pondéré)**           |       | **60⭐**   | **47⭐**   | **52⭐**           | **47⭐**| **51⭐** | **50⭐**  |

---

## Choix du SGBDR

| Critère                     | Poids | PostgreSQL | MySQL  | MongoDB | SQLite | Redis  | MariaDB |
|----------------------------|:-----:|:----------:|:------:|:-------:|:------:|:------:|:-------:|
| Rapidité                   | 1.5   | ★★★★       | ★★★★   | ★★★     | ★★★★   | ★★★★★ | ★★★★    |
| Sécurité                   | 2     | ★★★★★      | ★★★★   | ★★      | ★★★    | ★★     | ★★★★    |
| Efficience (mémoire)       | 2     | ★★★★       | ★★★★   | ★★★     | ★★★★   | ★★★★   | ★★★★    |
| Complexité                 | 1     | ★★★        | ★★★    | ★★★★    | ★★★★   | ★★★    | ★★★     |
| Communauté & Support       | 1     | ★★★★★      | ★★★★   | ★★★★    | ★★★    | ★★★    | ★★★★    |
| Ancienneté / Maturité      | 1.5   | ★★★★★      | ★★★★   | ★★★     | ★★★★   | ★★★    | ★★★★    |
| Stabilité                  | 2     | ★★★★★      | ★★★★   | ★★★     | ★★★★   | ★★★    | ★★★★    |
| Scalabilité                | 1.5   | ★★★★       | ★★★★   | ★★★★    | ★★     | ★★★    | ★★★★    |
| Sauvegarde / Restauration  | 1     | ★★★★       | ★★★★   | ★★★★    | ★★★    | ★★★    | ★★★★    |
| **Total (pondéré)**        |       | **69⭐**   |**53⭐**| **43⭐**|**47⭐**|**44⭐**|**53⭐**|

---

## Choix pour l'API

| Critère                    | Poids | Express.js | Fastify  | NestJS (Express) | NestJS (Fastify) | Spring Boot |
|---------------------------|:-----:|:----------:|:--------:|:----------------:|:----------------:|:-----------:|
| Rapidité                  | 1     | ★★★        | ★★★★★   | ★★★              | ★★★★            | ★★★★        |
| Sécurité                  | 1.5   | ★★★        | ★★★★     | ★★★★★            | ★★★★★           | ★★★★★       |
| Efficience (ressources)   | 2     | ★★★        | ★★★★★   | ★★★              | ★★★★            | ★★★         |
| Complexité d’utilisation  | 1     | ★★★★★      | ★★★★     | ★★★              | ★★★★            | ★★          |
| Communauté & Support      | 1.5   | ★★★★★      | ★★★★     | ★★★★             | ★★★★★           | ★★★★        |
| Maturité / Ancienneté     | 1     | ★★★★★      | ★★★      | ★★★              | ★★★             | ★★★★★       |
| Stabilité                 | 1.5   | ★★★★★      | ★★★★★   | ★★★★             | ★★★★            | ★★★★★       |
| Documentation             | 2     | ★★★★       | ★★★★     | ★★★★★            | ★★★★★           | ★★★★        |
| Évolutivité / MàJ         | 1     | ★★★★       | ★★★★★   | ★★★★★            | ★★★★★           | ★★★★        |
| **Total (pondéré)**       |       | **50.5⭐**  | **54.5⭐**| **49.5⭐**         | **55⭐**          | **50⭐**      |


---

## Conclusion

- ✅ **Pour le bot Discord**, `discord.js` a été choisi pour sa rapidité, sa maturité, et la grande communauté.
- ✅ **Pour la base de données**, `PostgreSQL` s’impose par sa stabilité, sa scalabilité et ses performances équilibrées. Il est particulièrement adapté à un projet évolutif avec des exigences solides en intégrité des données et en fiabilité.
- ✅ **Pour l'API**, une combinaison de `NestJS` avec `Fastify` semble la meilleure option pour sa rapidité, sa sécurité, et sa documentation complète. Cette stack permet de bénéficier des avantages de NestJS tout en optimisant les performances grâce à Fastify.

---

## Versions et sources

- **discord.js** : v14  
- **PostgreSQL** : v16
- **NestJS** : v11
- **Fastify** : v5.4
