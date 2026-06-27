# Horloge Néon

Ce projet est une horloge numérique au style "néon" réalisée en HTML, CSS et JavaScript.

## Structure du projet

- `index.html` : point d'entrée de la page.
- `style.css` : styles visuels et animations.
- `script.js` : génération de l'affichage horaire et mise à jour en temps réel.

## Comment le projet a été réalisé

### 1. Base HTML

Le fichier `index.html` contient une structure très légère :
- une balise `<main>` qui servira de conteneur pour l'horloge.
- inclusion de `style.css` pour le design.
- inclusion de `script.js` pour l'affichage dynamique.

### 2. Génération des chiffres avec JavaScript

Le fichier `script.js` construit l'horloge dynamiquement :
- il définit un modèle de segments (`bars`) pour chaque chiffre, similaire à un affichage 7-segments.
- chaque chiffre est composé de 7 éléments `<span>` avec des classes de position (`top`, `bottom`, `left`, `right`, `middle`).
- la fonction `addDigits` crée un groupe de chiffres pour les heures, les minutes et les secondes.
- la fonction `addColon` ajoute les deux points séparateurs.
- la fonction `init` récupère l'heure actuelle avec `new Date()` et initialise l'affichage.
- `requestAnimationFrame` est utilisé pour mettre à jour l'heure chaque seconde sans surcharger le navigateur.

### 3. Style et effet néon

Le fichier `style.css` met en place l'apparence néon :
- arrière-plan sombre dégradé pour mettre en valeur les chiffres lumineux.
- chaque segment de chiffre utilise un `clip-path` pour dessiner les formes de segments.
- les chiffres et les séparateurs sont stylisés avec des ombres portées (`drop-shadow`) pour renforcer l'effet lumineux.
- des groupes de `shadow` sont ajoutés derrière les chiffres pour simuler des reflets et une profondeur 3D.
- des animations CSS font tourner légèrement la caméra et déplacer le rendu pour donner du mouvement.

### 4. Compatibilité navigateur

Un contrôle utilisateur détecte Safari avec l'agent utilisateur et applique une classe spécifique pour désactiver certaines transitions, afin d'améliorer la compatibilité sur iOS/macOS.

## Fonctionnalités principales

- affichage des heures, minutes et secondes en temps réel
- design néon et animations 3D
- horloge entièrement construite en JavaScript sans bibliothèque externe
- mise à jour continue via `requestAnimationFrame`

## Comment utiliser

1. Ouvrir `index.html` dans un navigateur.
2. Le script génère automatiquement l'horloge.
3. Aucun serveur ou configuration particulière n'est nécessaire.

## Notes

- Le projet est conçu comme une démonstration visuelle et légère.
- Il est possible d'ajouter facilement des thèmes de couleur ou des effets supplémentaires en modifiant `style.css`.
