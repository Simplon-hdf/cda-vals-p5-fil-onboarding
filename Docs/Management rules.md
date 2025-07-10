# Règles de gestion


## Gestion des promotions

**RG01:** Une promotion est définie par : un nom unique, une formation, un campus, une date de début, une date de fin.
**RG02:** Une promotion a un chargé de projet.
**RG03:** Une promotion peut avoir un ou plusieurs formateurs.
**RG04:** Deux promotions ne peuvent pas avoir le méme nom.
**RG05:** Une promotion est active entre sa date de début et son archivage.
**RG06:** Une promotion est archivée automatiquement 30 jours après sa date de fin.
**RG07:** La création d'une promo crée un rôle unique associé à la promo.
**RG08:** Une promotion a des rôles automatiquement associés aux participants en fonction de la formation et campus.
**RG09:** Une section pour la promotion est créer automatiquement à la date de début.
**RG10:** Une promotion archivée voit sa section supprimer de Discord
**RG11:** Lors de l'achivage seulement les noms, dates, apprenants, formateur(s) et CDP sont conserver dans la BDD.


## Campus

**RG12:** Un campus est défini par : un nom unique, une date de création.


## Template

**RG13:** Un template définit une catégorie Discord avec des salons, forums, et salons vocaux.
**RG14:** Lors de la création d'un promotion, la promotion sera basée sur le template.
**RG15:** Les forums d'un template contiennent une liste de posts.
**RG16:** Un template contient les permissions associées aux différents salons.


## Utilisateur

**RG17:** Un utilisateur a des rôles.
**RG18:** Un utilisateur est défini par un compte discord, un nom et un prénom.
**RG19:** Un utilisateur peut être un apprenant, un CDP ou un formateur.
**RG20:** Un utilisateur peut être un Admin.


## Nouvel Arrivant

**RG21:** Un nouvel arrivant peut demander de rejoindre une promotion en tant qu'apprenant ou formateur.
**RG22:** Un nouvel arrivant doit renseigner son nom et son prénom en demandant de rejoindre une promotion.
**RG23:** Un nouvel arrivant doit lire une explication du système d'onboarding.


## Apprenant

**RG24:** Un apprenant peut demander de rejoindre une promotion.
**RG25:** Un apprenant peut faire partie d'une seule promotion à la fois.
**RG26:** Un apprenant est définit par le rôle apprenant.


## Chef De Projet

**RG27:** Un CDP peut créer une promo.
**RG28:** Un CDP peut modifier une promo.
**RG29:** Un CDP peut supprimer une promo.
**RG30:** Un CDP est en charge d'une ou plusieurs promo(s).
**RG31:** Un CDP doit accepter les demandes des persones souhaitant rejoindre une promo dont il est en charge.


## Formateur

**RG32:** Un formateur peut faire partie d'une ou plusieurs promotions.


## Administrateur

**RG33:** Un Administrateur peut créer une promo.
**RG34:** Un Administrateur peut modifier une promo.
**RG35:** Un Administrateur peut supprimer une promo.
**RG36:** Un Administrateur peut créer un nouveau campus.


## Rôles et accès

**RG37:** Le role Nouvelle Arrivant est donnée en rejoignant le serveur.
**RG38:** Un Administrateur est définit par le rôle Administrator.
**RG39:** Un formateur est défini par le rôle formateur.
**RG40:** Un CDP est défini par le rôle CDP.
**RG41:** Les rôles sont généres automatiquement à la création d'une promotion.
**RG42:** Rejoindre une formation donne aux participants le rôle unique, le rôle du type de formation, le rôle apprenant ou formateur et le rôle du campus de la formation.
**RG43:** Rejoindre une formation retire le rôle Nouvel Arrivant.
**RG44:** Le rôle Apprenant est automatiquement rajouté aux participanets au début de la formation.
**RG45:** Le rôle Alumni est automatiquement rajouté aux participants à la fin de la formation.
**RG46:** Le rôle unique de la promotion est supprimé de Discord à la fin de la promotion

