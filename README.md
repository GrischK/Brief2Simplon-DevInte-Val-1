# # Brief 2 : Formulaire de contact

L'objectif de ce brief est de créer un formulaire en **HTML5** correspondant aux consignes.

## Contexte

Je postule dans une agence web qui est spécialisée dans la création de site web dans la région des Hauts-De-France.
Je suis invité à présenter un formulaire d’inscription complet **fait uniquement avec HTML**. La sélection du candidat se fera sur le respect des bonnes pratiques de développement et de l’expérience utilisateur.

## Consignes

1.  Forker ce dépôt, puis cloner le fork sur l'ordinateur. Ce dépôt sera mon dépôt git à utiliser tout le long de ce brief.

2.  Tous les champs suivants doivent être présents dans votre formulaire :
- Prénom
- Nom
- Age
- Sexe
- Adresse Mail
- Adresse postale
- Code postal
- Ville
- Métier exercé
- Nationalité
- Date de naissance
- Pays de naissance
- Numéro de sécurité social
- Numéro du passeport
- Date de délivrance du passeport
- Date de validité du passeport

## Modalités pédagogiques

-   **Deadline** : Dimanche 2 Janvier à 23h59
- -**Travail individuel**
-   **Rendus par mail à** : [ameresse@simplon.co](mailto:ameresse@simplon.co) avec comme objet : Brief2 Prénom Nom.

## Critères de performance

- HTML5 seulement : PAS DE CSS
- Passage au validateur [ W3C Validator ](https://validator.w3.org/) sans erreurs.
- Validation du formulaire (Ce qui permet à l'utilisateur de ne pas entrer de mauvaises valeurs par erreur):
    - Chaque champ doit respecter le bon type d’informations, par exemple le code postal le champ ne devrait pouvoir recevoir que 5 chiffres et rien d’autre, l’adresse mail n’accepter que des adresses email valides, etc…
    - Pour le champ "métier exercé", proposer plusieurs type de professions avec choix unique. Pour le champ "Nationalité", proposer évidemment plusieurs propositions avec choix unique et choix par défaut.
- Un fichier README.md à la racine de votre dépôt afin de présenter votre projet. (Écrit en markdown)

# # La réalisation 

## Création du formulaire
Pour la création du formulaire je me suis aidé des cours en ligne sur la plateforme **Openclassrooms** en utilisant plus précisément ce [cours](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1607171-creez-des-formulaires).

## Les attributs et champs utilisés

Voici la liste des attributs utilisés dans le formulaire :
1. Champs :
- **"number"** : un contrôle qui permet de saisir un nombre.
- **"date"** : un contrôle qui permet de saisir une date (composé d'un jour, d'un mois et d'une année).
- **"email"** : un champ qui permet de saisir une adresse éléctronique.
- **"radio"** : un bouton radio qui permet de sélectionner une seule valeur parmi un groupe de différentes valeurs.
- **"submit"** : un bouton qui envoie le formulaire.
- **"text"** : un champ texte sur une seule ligne. Les sauts de ligne sont automatiquement retirés.

2. Attributs
- **form** : L'identifiant du formulaire.
- **name** : Le nom du champ qui sera rattaché à la donnée envoyée via le formulaire.
- **type** : Une chaîne de caractère qui indique l[e type de champ représenté par l'élément `<input>`.
- **"placeholder"** : Indique une expression rationnelle que doit respecter la valeur du contrôle du formulaire.
- **"required"** : Un attribut booléen qui indique que le champ doit être renseigné avant de pouvoir envoyer le formulaire.
- **"value"** : La valeur du champ.
- **"minlenght"** et **"maxlenght"** : Attribut qui contraint à la saisie d'une valeur minimale et maximale.


## Difficultés rencontrées 
La principale difficulté rencontrée a été au niveau de la du **"numéro de sécurité sociale"** et du **"numéro de passeport"**.
En effet pour respecter les contraintes liées à la casse (13 chiffres + clé à 2 chiffres pour le numéro de sécurité sociale et 2 chiffres, 2 lettres, 5 chiffres pour le passeport), je n'ai pas trouvé de solution au niveau de l'attribut patter afin de faire respecter cette casse. 
J'ai donc décidé de créer des champs différents en précisant à l'utilisateur la manière de rentrer les données :
- 2 champs pour le numéro de sécurité sociale :
	- 1 champ de 13 chiffres
	- 1 champ de 2 chiffres pour la clé
- 3 champs pour le numéro de passeport :
	- 1 champ de 2 chiffres
	- 1 champ de 2 lettres
	- 1 champ de 5 lettres	

La seconde difficulté auquelle j'ai dû faire face est celle de rendre obligatoire la saisie d'une des cases du champ **sexe**. 
D'après mes recherches, aucune technique en **HTML** ne permet d'utiliser l'attribut "required" sur un `<input>` de type `<radio>`.

## Ressources utilisées :
Voici une liste non exhaustive des ressources qui m'ont aidé :
- Cours sur les formulaire [Openclassrooms](https://openclassrooms.com/fr/courses/1603881-apprenez-a-creer-votre-site-web-avec-html5-et-css3/1607171-creez-des-formulaires)
- Liste des principales familles de métiers (http://christian.crouzet.pagesperso-orange.fr/smpmp/images-SMT/PCS_2003-A4_2av.pdf)
- Modzilla Developer Network pour les champs et attributs du formulaire notamment en ce qui concerne les pattern (https://developer.mozilla.org/fr/docs/Web/HTML/Element/Input)
- Lien utile qui m'a aidé pour rendre obligatoires la saisie des différents champs (https://www.alsacreations.com/tuto/lire/1391-formulaire-html5-placeholder-required-pattern.html)


