---
date: 2019-10-11
keywords: js, .js, format de fichier js, comment ouvrir des fichiers js, fichiers javascript
auteur:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Format de fichier JS
linktitle: JS
description: "Découvrez le format de fichier JS et les API qui peuvent créer et ouvrir des fichiers JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## Qu'est-ce qu'un fichier JS ? ##

JS (JavaScript) sont des fichiers contenant du code JavaScript à exécuter sur des pages Web. Les fichiers JavaScript sont stockés avec l'extension .js. Dans le document [HTML](/fr/web/html/), vous pouvez soit intégrer le code JavaScript en utilisant le \ <script>\</script> balises ou inclure un fichier JS. Semblables aux fichiers [CSS](/fr/web/css/), les fichiers JS peuvent être inclus dans plusieurs documents HTML pour la réutilisation du code. JavaScript peut être utilisé pour manipuler le DOM HTML.

## Bref historique ##

JavaScript a été livré pour la première fois dans le cadre du navigateur Navigator en septembre 1995 sous le nom de LiveScript par Netscape. Il a été renommé JavaScript trois mois plus tard. En 1996, Microsoft a procédé à la rétro-ingénierie de l'interpréteur de Navigator pour créer JScript. JScript a été publié avec Internet Explorer et était très différent de JavaScript.

Netscape a soumis JavaScript à ECMA International, ce qui a conduit à la publication officielle de la première spécification ECMAScript en 1997. ECMAScript 2 a été publié en 1998, ECMAScript 3 en 1999 et les travaux sur ECMAScript 4 ont commencé en 2000 mais n'ont jamais abouti.

Jesse James Garrett en 2005 a publié un livre blanc où il a inventé le terme * Ajax *. Cela utilisait JavaScript comme colonne vertébrale pour créer des applications Web qui chargeaient des données en arrière-plan et évitaient les rechargements de page complète. Cela a abouti à la création de bibliothèques comme JQuery, Prototype, Dojo, etc.

Google a lancé le navigateur Chrome avec le moteur JavaScript V8 en 2008. Début 2009, un accord a été conclu pour combiner tous les travaux pertinents et faire avancer JavaScript. Cela a abouti à la publication de la norme ECMAScript 5 en décembre 2009.

## Comment utiliser les fichiers JS ##

Pour utiliser un fichier JS, vous l'incluez dans le document HTML. Vous utilisez la balise de lien pour inclure le fichier comme indiqué ci-dessous.

```html
<script src="site.js"></script>
```

L'attribut *src* de la balise *script* contient le chemin d'accès au fichier JS. En faisant cela, la fonctionnalité JS est ajoutée au document HTML.

## Syntaxe JS ##

Les fichiers JavaScript peuvent contenir des variables, des opérateurs, des fonctions, des conditions, des boucles, des tableaux, des objets, etc. Vous trouverez ci-dessous un bref aperçu de la syntaxe de JavaScript.

- Chaque commande se termine par un point-virgule (;).
- Utilisez le mot-clé *var* pour déclarer des variables.
- Prend en charge les opérateurs arithmétiques ( + - * / ) pour calculer les valeurs.
- Les commentaires sur une seule ligne sont ajoutés avec // et les commentaires sur plusieurs lignes sont entourés de /* et */.
- Tous les identifiants sont sensibles à la casse, c'est-à-dire que *modelNo* et *modelno* sont deux variables différentes.
- Les fonctions sont définies à l'aide du mot-clé *function*.
- Les tableaux peuvent être définis à l'aide de crochets [].
- JS prend en charge les opérateurs de comparaison comme ==, != , >=, !==, etc.
- Les classes peuvent être définies à l'aide du mot-clé *class*.

## Exemple d'utilisation JS ##

Ce qui suit montre un exemple de fichier JavaScript d'utilisation simple.

### Document HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Code JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Références ##

- [JS - Wikipédia](https://en.wikipedia.org/wiki/JavaScript)

