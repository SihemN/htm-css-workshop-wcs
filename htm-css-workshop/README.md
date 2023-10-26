# HTML/CSS Basics workshop 

Règles de cet atelier : construire et concevoir une page web uniquement avec une structure HTML sémantique (pas de classe, pas d'identifiant en CSS).

## Initialisation

Créez un fichier *index.html*.
- Ouvrez le fichier avec votre IDE préféré et ajoutez les balises de base HTML5 (DOCTYPE, html, head, body).
- Créez un fichier *style.css*.
- Dans le `<head>`, ajoutez d'abord quelques balises obligatoires comme `<meta>` ou `<title>` :
  ```html
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML|CSS Workshop</title>
  </head>
  ```
- Ajoutez ensuite une balise `<link>` avec le lien vers *style.css*.
- Dans *index.html*, dans le `<body>`, ajoutez une balise `<h1>` avec le texte `Hello world !!!`.
- Dans *style.css*, ajoutez le code :
  ```css
  h1 {
    color: #a306b6; 
  }
  ```
- Ouvrez *index.html* dans votre navigateur, et vérifiez que vous pouvez lire le message : 'Hello world !!!' en violet WCS.

Bon travail !

## Mise en page de votre site Web

Vous devrez créer une page d'accueil de base en suivant la mise en page ci-dessous (**n'essayez pas** d'être parfait au pixel près, cette image n'est qu'un guide, la couleur rose est désormais remplacée par du violet).

<a href="./desktop_layout.png" target="_blank">Ouvrir dans un nouvel onglet <i class="bi bi-box-arrow-up-right"></i></a> 
![Mise en page à reproduire](desktop_layout.png)

Les navigateurs ont une taille par défaut pour chaque élément HTML (marge, taille de police, etc.). C'est utile mais parfois vous préférerez réinitialiser certains comportements par défaut. Dans cet atelier, il pourrait être intéressant de supprimer la marge sur `<body>`. De plus, utiliser `box-sizing: border-box` sur chaque élément vous aidera à gérer le dimensionnement des éléments (plus d'informations sur [box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)).

```css
* {
  box-sizing: border-box;
}
body {
  margin:0;
}
```

### Navbar

- Essayez de reproduire la barre de navigation. Commencez à créer une balise `<nav>` et ajoutez la couleur d'arrière-plan `#a306b6`.
- Ensuite, analysez la structure de la barre de navigation. Vous avez un logo « Workshop » en haut à gauche et un groupe d'éléments de menu en dessous.
- Utiliser une liste non ordonnée peut être une bonne idée pour le groupe de menus, mais n'oubliez pas de l'afficher horizontalement et sans les puces.

### Header

- Enveloppez votre `<h1>` dans une balise `<header>` et ajoutez une hauteur minimale de 250 px.
- Ajoutez une image d'arrière-plan (par exemple une image ramdon sur [Loremflicker](https://loremflickr.com/1920/600) ou [Picsum](https://picsum.photos/1920/600)).
- Centrez votre titre principal et modifiez la taille/couleur de la police si nécessaire.

> Astuce : [Gérer la taille de l'arrière-plan](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size)

### Section À propos de nous 

- Une bonne pratique consiste à envelopper les sections dans une balise `<main>`.
- Ajoutez un premier `<section>` et un `<h2>` selon le modèle.
- Ajoutez du faux texte dans un paragraphe. Modifiez `line-height` (1.5) et `font-family` (Verdana) pour améliorer la lisibilité. Cela peut être fait dans les propriétés « body ».
- Limitez la « largeur maximale » à 65 canaux. Cela garantira que vous disposerez d’une largeur de texte ne dépassant pas 85 caractères, ce qui rendra la lecture plus confortable.
>Une petite explication : en css, l'unité `ch` est une unité relative à la largeur du caractère 0 (le caractère le plus large dans la plupart des polices). Spécifier 65ch permet d'assurer une largeur de colonne comprise entre 65 et environ 85 caractères tous signes confondus, une largeur de bloc de texte fortement recommandée par de nombreuses études sur l'accessibilité numérique et nos comportements de lecture. Plus d'explications sur [cet article](https://medium.com/@matuzo/writing-css-with-accessibility-in-mind-8514a0007939) ou [celui-ci](https://www.smashingmagazine.com/2014/09/balancing-line-length-font-size-responsive-web-design/#line-length-measure-and-reading) si le sujet vous intéresse.


- Enfin, vous pouvez utiliser la propriété `margin` pour centrer le bloc horizontalement.

[Centrer en CSS : un guide complet](https://css-tricks.com/centering-css-complete-guide/)

### Section Articles en vedette

- Ajouter une nouvelle `<section>`.
- Donnez-lui un `<h2>` avec le contenu texte approprié.
- Ajoutez 4 enfants `<article>` ci-dessous.
- Chaque article peut avoir `<h1>` contenant son nom.
- Ajustez la mise en page pour obtenir 2 éléments par ligne avec les propriétés `display` et `width`.
Des effets d'arrondi et d'ombre portée peuvent être obtenus avec `border-radius` et `box-shadow`.

### Footer

Parce que vous avez un `<header>`, vous avez besoin d'un `<footer>`. Cela ne devrait pas poser de problème pour vous 😉.
