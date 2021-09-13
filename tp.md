# Cours git

## Introduction

La pratique se fait en binôme, avec 2 ordinateurs par binôme (1 ordinateur par personne).

L'objectif est de montrer comment git permet de travailler collaborativement, et comment gérer les conflits lors de l'intégration des changements distants.

Dans ce TP nous abordons les notions suivantes:

- les commits
- le remote et ses interactions
- les branches (locales, remote)
- le merge

## Collaborer avec git

### Avant de commencer

Commencez par configurer git sur vos ordinateurs [1 et 2]

```
git config --global user.name "Prénom Nom"
git config --global user.email prenom.nom@example.com
```

Créez un compte GitHub: https://github.com/ et retenez le "handle" (votre pseudo).

### Mise en place

#### Mettre en place le projet avec GitHub

Une seule des deux personnes doit effectuer ces étapes.

1. Créez le repository
   - en haut à droite, cliquez sur "+"
   - cliquez sur "New repository"
   - mettez le nom que vous voulez, la description que vous voulez
   - sélectionnez "Private"
   - validez et créez le repository
2. Autorisez votre binôme à y accéder
   - allez dans l'onglet "Settings"
   - dans la page "Manage access"
   - cliquez sur le bouton "Invite a collaborator"
   - entrez son "handle", cliquez dessus, puis "Add XXX to this repository"

#### Téléchargez le projet sur vos ordinateurs

Dans l'onglet "Code", cliquez sur le bouton "HTTPS" et copiez le lien (par exemple `https://github.com/GuillaumeDesforges/cours-git-2021.git`)

Clonez le projet sur vos ordinateurs (sur les deux ordinateurs)

```
git clone <url>
```

Un dossier a été créé qui correspond au nom du repository sur GitHub, déplacez-vous-y:

```
cd <nom du dossier>
```

#### Collaborer sans conflit

Assignez vous chacun la mention "ordinateur 1" et "ordinateur 2" pour la suite du TP.

Nous allons d'abord aborder le workflow le plus simple.

- Sur l'ordinateur 1
  - Créez le fichier avec le contenu suivant: https://github.com/GuillaumeDesforges/cours-git-2021-demo/blob/fa6fb7b244d0fab8ea55d7cd1e85101495e4ea8e/script.py
  - Créez un commit
  - Envoyez ce commit sur le repository

Vous pouvez vérifier que le contenu est à jour en rafraîchissant la page web GitHub de votre repository.

- Sur l'ordinateur 2
  - Récupérez ces changements et intégrez-les
  - Editez le fichier, par exemple en enlevant la ligne 8 ("Hello world")
  - Créez un commit
  - Envoyez ce commit sur le repository
- Sur l'ordinateur 1
  - Récupérez ces changements et intégrez-les

#### Collaborer avec conflit

- Sur l'ordinateur 1
  - Editez le fichier, par exemple en changeant le nom de la fonction `main`
  - Créez un commit
  - Envoyez ce commit sur le repository
- Sur l'ordinateur 2
  - Editez le fichier, par exemple en changeant le nom de la fonction `main` (avec un autre nom que celui choisi par votre binôme)
  - Créez un commit
  - Essayez d'envoyez ce commit sur le repository
  - Récupérez ces changements et intégrez-les
  - Envoyez vos changements sur le repository
- Sur l'ordinateur 1
  - Récupérez ces changements et intégrez-les

#### Collaborer avec les Pull Requests

- Sur l'ordinateur 1
  - Créez une nouvelle branche
  - Editez le fichier
  - Créez un commit sur cette nouvelle branche
  - Envoyez cette nouvelle branche sur le repository
  - Dans GitHub, créez une "Pull Request" et assignez votre binôme en "reviewer"
- Sur l'ordinateur 2
  - Recevez la notification, allez sur la Pull Request
  - Réalisez une revue de la branche (insérez au moins 1 commentaire demandant un changement)
- Sur l'ordinateur 1
  - Recevez la notification, allez sur la Pull Request
  - Relisez la revue, répondez aux commentaires ou effectuez les changements demandés
- Vous pouvez répéter ce processus plusieurs fois
- Une fois le résultat satisfaisant, c'est l'ordinateur 1 qui doit "merge"
  - Cliquez sur le bouton "Merge Pull Request"
  - Vous pouvez généralement supprimer la branche en cliquant sur "Delete branch"
