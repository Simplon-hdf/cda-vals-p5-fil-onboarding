# Benchmark

Ce document présente le processus de sélection de la stack technique pour un bot Discord, ainsi que celle du SGBDR associé à son API.

## Processus

Des critères ont été définis selon les besoins du projet, chacun pondéré en fonction de son importance relative. Chaque solution a ensuite été évaluée selon ces critères.

---

## Contexte technique

- 🎯 Le projet consiste à créer un bot Discord interagissant avec une API existante.
- 🧱 L’API est développée en Node.js (projet [bots-discord-api](https://github.com/Simplon-hdf/bots-discord-api)).
- ⚡ Objectif de performance : traitement réactif des messages et commandes.
- 📦 Le système devra pouvoir évoluer


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
| **Total**   |                 | **60⭐**    | **47⭐**    | **52⭐**            | **47⭐**| **51⭐**   | **50⭐**    |

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
| **Total**|                 | **69.0⭐**  | **53.0⭐** | **43.0⭐** | **47.0⭐** | **43.5⭐** | **53.0⭐** |

---

## Conclusion

- ✅ **Pour le bot Discord**, `discord.js` a était choisit pour sa rapidité, sa maturité, et la grande  communauté.
- ✅ **Pour la base de données**, `PostgreSQL` s’impose par sa stabilité, sa scalabilité et ses performances équilibrées. Il est particulièrement adapté à un projet évolutif avec des exigences solides en intégrité des données et en fiabilité.

---

## Versions et sources

- **discord.js** : v14  
- **PostgreSQL** : v16
