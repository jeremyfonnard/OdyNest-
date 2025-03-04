# OdyNest-

## Présentation
Aujourd’hui, de plus en plus de personnes cherchent des expériences uniques et des voyages clés en main sans se soucier de l’organisation. Notre plateforme répond à ce besoin en proposant une interface intuitive où les utilisateurs peuvent réserver des séjours de différentes durées ou des expériences immersives en quelques clics. Que ce soit un week-end romantique, une aventure sportive ou une expérience culinaire, nous offrons une large gamme de choix adaptée à tous les goûts et budgets.

Notre application se divise en 4 espaces :
- une interface visiteur où ceux-ci pourront uniquement rechercher les expériences,
- une interface utilisateur où les clients peuvent rechercher, réserver, annuler leurs expériences et donner leurs avis (uniquement pendant ou après l'expérience),
- une interface prestataire où ceux-ci pourront créer, modifier et supprimer des événements, et voir qui participe à leurs événements,
- une interface administrateur permettant de gérer les offres (valider en amont les propositions des prestataires), les réservations et le suivi des utilisateurs.
L'objectif est de proposer une expérience fluide et agréable, que ce soit pour les voyageurs ou les prestataires de services.

## Parcours visiteur/utilisateur
Accueil : Le visiteur arrive sur la plateforme et découvre les expériences et séjours disponibles.

Recherche et filtre : Il peut rechercher une expérience en fonction de la destination, du type d’activité, de la durée et du prix.

Consultation des offres : En cliquant sur une offre, il accède aux détails (description, photos, avis, prix, disponibilité).

Réservation : Une fois l’expérience choisie, il devra créer un compte ou se connecter pour réserver en ligne et payer via une plateforme sécurisée (Stripe)

Confirmation et suivi : L’utilisateur reçoit un email de confirmation et peut retrouver sa réservation dans son espace personnel.

Expérience et avis : Après avoir vécu son expérience, il peut laisser un avis pour aider les futurs voyageurs
Email envoyé à l'utilisateur : Un email de rappel est envoyé après la fin de l'expérience pour encourager l'utilisateur à laisser un avis.

## Concrètement et techniquement
### 1. Base de données

Utilisateurs : Nom, prénom, email, mot de passe hashé, historique des réservations

Prestataire : Nom, prénom/entreprise, email, mots de passe hashé, Id expérience / évenements

Expériences/Voyages/Événement : Nom, description, prix, lieu, durée, photos, avis, disponibilités, ID prestataire

Réservations : ID utilisateur, ID expérience, date de réservation, statut (confirmé, en attente, annulé)

Avis : ID utilisateur, ID expérience, note, commentaire

### 2. Front

Voici les principaux composants de l’application : 

- Page d’accueil : Présentation des offres phares, suggestions personnalisées et moteur de recherche.

- Moteur de recherche avec filtres : Recherche d’expériences par destination(lieu), type d’activité, durée et prix. 

- Page détaillée d’une expérience : Description complète, photos, avis, disponibilité et bouton de réservation (qui ramène à Stripe). +Encart qui affiche les autres événements proposés par le prestataire. 

- Système de réservation : Interface intuitive permettant aux utilisateurs de sélectionner une date et réserver leur expérience selon les disponibilités.

- Espace utilisateur : Tableau de bord affichant l’historique des réservations, détails des voyages et options de gestion (modifier/supprimer son compte).

- Espace prestataire : Tableau de bord avec création/modification/suppression d'événements. +Détails des voyageurs inscrits

- Interface administrateur : Outils de gestion des offres, réservations et utilisateurs pour les administrateurs et prestataires. 

L’accent sera mis sur l’ergonomie et l’expérience utilisateur pour garantir une navigation intuitive et efficace. 🚀✨

### 3. Back-end

Le back-end sera développé en Rails et Stimulus avec une base de données SQLite. Les principales API que nous allons implémenter :

- API de gestion des mails 

- API de paiement via Stripe

Compétences actuelles : Maîtrise de HTML, CSS, Bootstrap, Rails, SQLite, intégration de Stripe

## Versions à rendre
### Version basique
  Une version basique de la plateforme permettant aux utilisateurs de :

  ✅ S’inscrire et se connecter (utilisateur, prestataire, administrateur)

  ✅ Consulter une liste d’expériences et de voyages (affichage basique des offres avec titre, lieu, description, prix, durée).

  ✅ Accéder à la page détaillée d’une expérience (avec photos et description complète).

  ✅ Réserver une expérience (ajout d’un formulaire de réservation sans paiement intégré).

  ✅ Interface prestataire minimaliste (pour ajouter et gérer les expériences, valider les réservations, voir les voyageurs inscrits et en attente)

  ✅ Interface administrateur minimaliste. Le MVP se concentre sur un système simple de réservation, sans paiement en ligne ni gestion avancée des 
utilisateurs. L’objectif est de tester l’intérêt des utilisateurs et de poser les bases du projet. 🚀✈️

### Version finale
Pour la version finale, nous prévoyons d'ajouter les fonctionnalités suivantes :

  ✅ Intégration Stripe : Mise en place d'un système de paiements sécurisés pour faciliter les transactions.

  ✅ Système d’avis et de notation : Permettre aux utilisateurs de noter et donner leur avis sur les services, renforçant la confiance et la qualité.

  ✅ Dashboard utilisateur : Un tableau de bord personnel affichant l'historique complet des réservations, les paiements et les préférences. 

  ✅ Interface prestataire : Un tableau de bord affichant les événements créés et en attente, les voyageurs inscrits et en attente, et les paiements reçus. Possibilité de modifier les événements, et possibilité de les supprimer si personne n'est encore inscrit.

  ✅ Interface administrateur : Un panneau complet permettant aux administrateurs de gérer les offres, les utilisateurs, et de suivre les statistiques.

  ✅ Version mobile optimisée : Une version responsive et fluide pour les smartphones, garantissant une expérience de navigation agréable.

### À terme ++

✅ Intégration d'une map pour localiser les événements proposés

✅ Recommandations intelligentes : Un algorithme de recommandations personnalisées basé sur l’historique et les préférences des utilisateurs, pour offrir des suggestions pertinentes.

