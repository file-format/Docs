---
date: 2019-10-11
keywords: culot, .sass, format de fichier sass, comment ouvrir les fichiers sass, feuille de style syntaxiquement géniale, préprocesseur css, culot
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier Sass
linktitle: Sass
description: "Découvrez le format de fichier Sass et les API qui peuvent créer et ouvrir des fichiers Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## Qu'est-ce qu'un fichier SASS ? ##

Sass (feuilles de style syntaxiquement impressionnantes) est un langage de script de préprocesseur. Il est compilé dans [CSS](/fr/web/css/) et est stocké avec l'extension .sass. Sass se compose de deux syntaxes, l'original basé sur des indentations qui utilise l'extension .sass et le plus récent SCSS avec un formatage de bloc comme CSS qui utilise l'extension .scss.

## Pourquoi utiliser Sass ##

Sass est vraiment utile pour maintenir les styles car il fournit de nombreuses fonctionnalités telles que l'introduction de variables, l'imbrication, les mixins, les importations et l'héritage de sélecteur qui rendent le travail avec les styles amusant.

## Comment utiliser les fichiers SASS ##

Les fichiers SASS ne sont pas inclus directement dans le document [HTML](/fr/web/html/) mais sont plutôt convertis en fichiers CSS qui sont inclus dans les fichiers HTML. Vous pouvez installer Sass sur votre système en suivant les instructions données sur le [Site officiel de Sass](https://sass-lang.com/install).

Sass peut être converti en CSS en convertissant un fichier SASS déjà enregistré ou en surveillant les modifications et en convertissant au fur et à mesure que le fichier est enregistré. Les commandes pour les deux sont données ci-dessous.

### Convertir une fois ###

Le premier paramètre de la commande est le fichier SASS source et le second paramètre est le fichier CSS de sortie.

```cmd
sass main.sass main.css
```

### Surveillez les changements ###

La commande ci-dessus peut être exécutée avec un indicateur *watch* supplémentaire qui maintient la commande en cours d'exécution et dès que le fichier Sass est enregistré, la sortie CSS est générée.

```cmd
sass --watch main.sass main.css
```

## Syntaxe Sass ##

Sass prend en charge les variables, l'imbrication, les mixins, les importations, l'héritage de sélecteur, etc. Vous trouverez ci-dessous des exemples de ces fonctionnalités.

### Variables ###

Les variables peuvent être utilisées pour définir des informations réutilisables telles que la couleur primaire ou le remplissage d'un bouton. Cela peut s'avérer utile si, à l'avenir, vous deviez modifier ces informations, vous les modifiez simplement à un endroit et elles sont mises à jour partout.

**Toupet**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS généré**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Imbrication ###

Les sélecteurs CSS peuvent être imbriqués de la même manière que la hiérarchie HTML. Dans l'exemple suivant, la plage est imbriquée dans le bloc h1.

**Toupet**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS généré**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Mixins ###

Les mixins sont utilisés pour regrouper des propriétés similaires qui sont utilisées à plusieurs endroits. Les mixins prennent également en charge les paramètres.

**Toupet**

**Déclarer un mixin**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Avec un mixin**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**CSS généré**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Se déployer ###

L'extension/l'héritage peut s'avérer utile dans les cas où les propriétés d'un sélecteur doivent être partagées avec un autre sélecteur. Dans l'exemple ci-dessous, le sélecteur *.error-notice* prend toutes les propriétés du sélecteur *.error-text* et ajoute les propriétés border et padding.

**Toupet**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**CSS généré**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Importer ###

L'importation peut être utile si vous structurez vos styles dans différents fichiers en fonction de la fonctionnalité ou de toute autre structure que vous suivez. Vous pouvez importer tous ces fichiers dans un fichier SASS principal qui sera ensuite converti en CSS. Lors de l'importation, vous n'avez pas besoin de spécifier l'extension de fichier dans l'instruction d'importation. Sass compile directement tous les fichiers SASS. Pour éviter que les fichiers d'importation ne soient compilés directement, vous pouvez les rendre partiels en ajoutant un trait de soulignement (_) au début de leur nom. Les partiels sont importés de la même manière que les fichiers Sass normaux.

**Toupet**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

Le CSS de sortie aura les styles de tous les fichiers importés.

## Références ##

- [Sass - Wikipédia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

