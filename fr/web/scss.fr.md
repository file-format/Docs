---
date: 2019-10-11
keywords: scss, .scss, format de fichier scss, comment ouvrir des fichiers scss, feuille de style syntaxiquement géniale, préprocesseur css, toupet
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier SCSS - Feuille de style en cascade Sass
linktitle: SCSS
description: "Découvrez le format de fichier SCSS et les API qui peuvent créer et ouvrir des fichiers SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Qu'est-ce qu'un fichier SCSS ? ##

SCSS est la deuxième syntaxe de Sass (Syntactically Awesome Stylesheet) qui utilise des crochets au lieu d'indentations. SCSS a été conçu de manière à ce qu'un fichier CSS3 valide soit également un fichier SCSS valide. Les fichiers SCSS sont stockés avec l'extension .scss.

## Pourquoi utiliser SCSS ##

Comme la conception des sites Web devient complexe, il en résulte des fichiers [CSS](/fr/web/css/) volumineux. De tels fichiers sont plus difficiles à maintenir. C'est là qu'intervient SCSS. SCSS introduit les variables, l'imbrication, les mixins, les importations et l'héritage des sélecteurs dans le développement CSS. Ces ajouts rendent le travail avec le design beaucoup plus amusant.

## Comment utiliser les fichiers SCSS ##

Les fichiers SCSS ne sont pas inclus directement dans le document [HTML](/fr/web/html/) comme CSS. Au lieu de cela, les fichiers SCSS sont convertis en fichiers CSS qui sont inclus dans les fichiers HTML. Pour installer SCSS sur votre système, suivez les instructions données sur le [Site officiel de Sass](https://sass-lang.com/install).
Pour convertir SCSS en CSS, vous pouvez soit convertir un fichier SCSS déjà enregistré, soit surveiller les modifications et convertir au fur et à mesure que le fichier est enregistré. Les commandes pour les deux sont données ci-dessous.

### Convertir une fois ###

Le premier paramètre est le fichier SCSS source et le second paramètre est le fichier CSS de sortie.

```cmd
sass main.scss main.css
```

### Surveillez les changements ###

La commande a un indicateur *watch** supplémentaire qui maintient la commande en cours d'exécution et dès que le fichier SCSS est enregistré, la sortie CSS est générée.

```cmd
sass --watch main.scss main.css
```

## Syntaxe SCSS ##

SCSS prend en charge les variables, l'imbrication, les mixins, les importations, l'héritage de sélecteur, etc. Vous trouverez ci-dessous des exemples de ces fonctionnalités.

### Variables ###

En utilisant des variables, vous pouvez définir des informations réutilisables telles que la couleur primaire ou la couleur d'arrière-plan du bouton d'enregistrement. Ceci est utile si vous avez besoin de modifier ces informations, vous les modifiez simplement à un endroit et elles sont mises à jour partout où elles sont utilisées.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Vous pouvez imbriquer les sélecteurs CSS de la même manière que la hiérarchie HTML. Dans l'exemple ci-dessous, la plage est imbriquée dans le bloc h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Les mixins peuvent être utilisés pour regrouper des propriétés similaires qui sont utilisées ensemble à plusieurs endroits. Vous pouvez également passer des paramètres aux mixins.

**SCSS**

**Déclarer un mixin**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Avec un mixin**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

L'extension/l'héritage est utile dans les cas où les propriétés d'un sélecteur doivent être partagées avec un autre sélecteur. Dans l'exemple ci-dessous, le sélecteur *.error-notice* prend toutes les propriétés du sélecteur *.error-text* et ajoute les propriétés de bordure et de remplissage.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

L'importation peut être utile dans la séparation des préoccupations. Vous pouvez diviser les styles de manière à ce que les styles d'en-tête soient dans un fichier séparé, les styles de pied de page soient dans un fichier séparé, toutes les variables de couleur utilisées dans les styles puissent être dans un fichier séparé, etc. En utilisant cette technique, le les styles restent organisés. Vous importez simplement les fichiers dans votre fichier SCSS principal, comme indiqué dans l'exemple ci-dessous. Vous n'avez pas besoin de spécifier l'extension de fichier dans l'instruction d'importation. Sass compile directement tous les fichiers SCSS. Pour éviter que les fichiers d'importation soient compilés directement, vous pouvez les rendre partiels en ajoutant un trait de soulignement (_) avant leur nom. Vous pouvez importer des partiels similaires aux fichiers SCSS normaux sans le trait de soulignement.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

Le CSS de sortie aura les styles de tous les fichiers importés.

## Références ##

- [SCSS - Wikipédia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

