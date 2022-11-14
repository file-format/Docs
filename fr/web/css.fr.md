---
date: 2019-10-11
keywords: css, .css, format de fichier css, comment ouvrir des fichiers css, feuilles de style en cascade
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier CSS
linktitle: CSS
description: "Découvrez le format de fichier CSS et les API qui peuvent créer et ouvrir des fichiers CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Qu'est-ce qu'un fichier CSS ? ##

CSS (Cascading Style Sheets) sont des fichiers qui décrivent comment les éléments HTML sont affichés à l'écran, sur papier, etc. Avec HTML, vous pouvez avoir des styles intégrés ou des styles peuvent être définis dans une feuille de style externe. Pour intégrer les styles, le \ <style>\</style> les balises sont utilisées. Les feuilles de style externes sont stockées dans des fichiers avec l'extension .css. Avec le CSS externe, vous pouvez l'inclure sur plusieurs pages HTML pour mettre à jour le style de ces pages. Même un seul fichier CSS peut être utilisé pour styliser un site Web complet.

## Bref historique ##

CSS1 est sorti en 1996 avec Bert Bos comme co-auteur. Le groupe de travail CSS a commencé à travailler sur les problèmes qui n'étaient pas abordés dans CSS1. Cela a abouti à la création de CSS2 en novembre 1997 qui a été publiée en tant que recommandation du W3C le 12 mai 1998. Cette version a ajouté la prise en charge des périphériques spécifiques aux médias tels que les imprimantes, les polices téléchargeables, les tableaux et le positionnement des éléments. En juin 1999, CSS3 est devenu la recommandation du W3C. Cela a divisé la documentation en modules où chaque module avait des fonctionnalités d'extension définies dans CSS2.

## Comment utiliser les fichiers CSS ##

Pour utiliser un fichier CSS, vous l'incluez dans la section d'en-tête du document HTML. Vous utilisez la balise de lien pour inclure le fichier comme indiqué ci-dessous.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

l'attribut *href* de la balise de lien contient le chemin vers le fichier CSS. Ce faisant, les styles applicables contenus dans le fichier CSS inclus sont appliqués au document HTML.

## Syntaxe CSS ##

Une règle CSS comprend deux composants, un sélecteur et une déclaration. Un sélecteur pointe vers un élément du document HTML. Il peut s'agir d'une balise d'élément, d'un nom de classe, d'un nom d'identifiant, de plusieurs balises affichant la hiérarchie, etc. Une déclaration contient la définition de style comprenant la propriété et la valeur. La propriété identifie la propriété de l'élément que vous souhaitez modifier et la valeur définit sa nouvelle valeur. Chaque règle CSS peut avoir plusieurs déclarations. Voici un exemple de règle CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Dans l'exemple ci-dessus, nous avons le **h1** comme sélecteur qui sélectionne toutes les balises h1 dans le document HTML. La règle a deux déclarations, une pour font-weight et l'autre pour color. *font-weight* et *color* sont des propriétés et *700* et *forestgreen* sont leurs valeurs respectivement.

## Exemple d'utilisation CSS ##

Ce qui suit montre l'exemple de document HTML et la feuille de style utilisée pour le styliser. L'image de comparaison est également ajoutée pour comparer les documents HTML stylés et simples

### Document HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Feuille de style CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Comparaison de sortie ###

Le côté gauche de l'image affiche le document HTML sans les styles appliqués et le côté droit affiche le document HTML avec les styles appliqués.

{{< figure src="../CssExample.jpg" alt="Exemple d'image" >}}

## Références ##

- [CSS - Wikipédia](https://en.wikipedia.org/wiki/CSS)

