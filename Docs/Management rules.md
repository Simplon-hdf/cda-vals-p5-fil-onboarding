# Règles de gestion

## Gestion des promotions

**RG01 :** Une promotion est définie par : un nom unique, une formation, un campus, une date de début, une date de fin.

**RG02 :** Une promotion a un chargé de projet.

**RG03 :** Une promotion peut avoir un ou plusieurs formateurs.

**RG04 :** Deux promotions ne peuvent pas avoir le même nom.

**RG05 :** Une promotion est active entre sa date de début et son archivage.

**RG06 :** Une promotion est archivée automatiquement 30 jours après sa date de fin.

**RG07 :** La création d'une promo crée un rôle unique associé à la promo.

**RG08 :** Une promotion a des rôles automatiquement associés aux participants en fonction de la formation et du campus.

**RG09 :** Une section pour la promotion est créée automatiquement à la date de début.

**RG10 :** Une promotion archivée voit sa section supprimée de Discord.

**RG11 :** Lors de l'archivage, seulement les noms, dates, apprenants, formateur(s) et CDP sont conservés dans la BDD.

## Campus

**RG12 :** Un campus est défini par : un nom unique, une date de création.

## Formation

**RG13 :** Un formation est défini par : un nom unique, une date de création.

## Template

**RG14 :** Un template définit une catégorie Discord avec des salons, forums, et salons vocaux.

**RG15 :** Lors de la création d'une promotion, la promotion sera basée sur le template.

**RG16 :** Les forums d'un template contiennent une liste de posts.

**RG17 :** Un template contient les permissions associées aux différents salons.

## Utilisateur

**RG18 :** Un utilisateur a des rôles.

**RG19 :** Un utilisateur est défini par un compte Discord, un nom et un prénom.

**RG20 :** Un utilisateur peut être un nouvel arrivant, apprenant, un CDP ou un formateur.

**RG21 :** Un utilisateur peut être un admin.

## Nouvel arrivant

**RG22 :** Un nouvel arrivant peut demander de rejoindre une promotion en tant qu'apprenant ou formateur.

**RG23 :** Un nouvel arrivant doit renseigner son nom et son prénom en demandant de rejoindre une promotion.

**RG24 :** Un nouvel arrivant doit lire une explication du système d'onboarding.

## Apprenant

**RG25 :** Un apprenant peut demander de rejoindre une promotion.

**RG26 :** Un apprenant peut faire partie d'une seule promotion à la fois.

**RG27 :** Un apprenant est défini par le rôle apprenant.

## Chef de projet

**RG28 :** Un CDP peut créer une promo.

**RG29 :** Un CDP peut modifier une promo.

**RG30 :** Un CDP peut supprimer une promo.

**RG31 :** Un CDP est en charge d'une ou plusieurs promo(s).

**RG32 :** Un CDP doit accepter les demandes des personnes souhaitant rejoindre une promo dont il est en charge.

## Formateur

**RG33 :** Un formateur peut faire partie d'une ou plusieurs promotions.

## Administrateur

**RG34 :** Un administrateur peut créer une promo.

**RG35 :** Un administrateur peut modifier une promo.

**RG36 :** Un administrateur peut supprimer une promo.

**RG37 :** Un administrateur peut créer un campus.

**RG38 :** Un administrateur peut modifier un campus.

**RG39 :** Un administrateur peut supprimer un campus.

**RG40 :** Un administrateur peut créer une formation.

**RG41 :** Un administrateur peut modifier une formation.

**RG42 :** Un administrateur peut supprimer une formation.


## Rôles et accès

**RG43 :** Le rôle "nouvel arrivant" est attribué lorsqu'on rejoint le serveur.

**RG44 :** Un administrateur est défini par le rôle Administrator.

**RG45 :** Un formateur est défini par le rôle formateur.

**RG46 :** Un CDP est défini par le rôle CDP.

**RG47 :** Les rôles sont générés automatiquement à la création d'une promotion.

**RG48 :** Rejoindre une formation donne aux participants le rôle unique, le rôle du type de formation, le rôle apprenant ou formateur et le rôle du campus de la formation.

**RG49 :** Rejoindre une formation retire le rôle nouvel arrivant.

**RG50 :** Le rôle apprenant est automatiquement rajouté aux participants au début de la formation.

**RG51 :** Le rôle alumni est automatiquement rajouté aux participants à la fin de la formation.

**RG52 :** Le rôle unique de la promotion est supprimé de Discord à la fin de la promotion.
