{
  "date" : "2020-03-02",
  "keywords" :["SVG", "fichier", "format de fichier", "Langage de description de page", "Scalaire"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier SVG et les API qui peuvent créer et ouvrir des fichiers SVG.",
  "title" :"Qu'est-ce qu'un fichier SVG ?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Qu'est-ce qu'un fichier SVG ? ##

Un fichier SVG est un fichier Scalar Vector Graphics qui utilise un format de texte basé sur XML pour décrire l'apparence d'une image. Le mot Scalable fait référence au fait que le SVG peut être mis à l'échelle à différentes tailles sans perte de qualité. La description textuelle de ces fichiers les rend indépendants de la résolution. C'est l'un des formats les plus utilisés pour créer un site Web et imprimer des graphiques afin d'atteindre l'évolutivité. Le format ne peut cependant être utilisé que pour les graphiques en deux dimensions. Les fichiers SVG peuvent être visualisés/ouverts dans presque tous les navigateurs modernes, y compris Chrome, Internet Explorer, Firefox et Safari.

## Bref historique ##

Les spécifications SVG sont disponibles en tant que norme ouverte par le World Wide Web Consortium (W3C) depuis 1999. Avant cela, des spécifications de format de fichier similaires dans six formats différents ont été soumises au W3C jusqu'en 1998. Une mise à jour a été appliquée aux spécifications en 2011 et la version 1.1 . En 2016, SVG 2 a été publié en tant que version plus récente comprenant des fonctionnalités en plus de celles de SVG 1.1.

## Spécifications du format de fichier ##

Le modèle d'objet de document SVG (DOM) jette les bases de toutes les spécifications et interfaces qui correspondent aux sections particulières des spécifications. Les visualiseurs SVG doivent implémenter les interfaces SVG DOM telles que définies dans les spécifications W3C. Son DOM expose plusieurs interfaces pour différents types de données et éléments.

### Formes SVG ###

SVG a des éléments de forme prédéfinis qui peuvent être utilisés par les développeurs :

* Rectangle<rect>
* Cercle<circle>
* Ellipse<ellipse>
* Ligne<line>
* Polyligne<polyline>
* Polygone<polygon>
* Chemin<path>

Sur la base de ces formes et spécifications, les domaines fonctionnels de SVG sont les suivants.

**Chemins** - Les chemins sont utilisés pour représenter des contours de formes simples et composées. Les codages sont utilisés pour définir la nature de l'opération. Par exemple, M est utilisé pour Déplacer vers, L est utilisé pour Ligne vers, Z est utilisé pour fermer un chemin, etc.

**Formes de base** - Des chemins en ligne droite et des chemins constitués d'une série de segments de ligne droite connectés (polylignes), ainsi que des polygones fermés, des cercles et des ellipses peuvent être dessinés. Les rectangles et les rectangles aux coins arrondis sont également des éléments standard.

**Texte** - La représentation textuelle est exprimée sous forme de données de caractères XML où de nombreux effets visuels peuvent être appliqués au texte. Les spécifications permettent de gérer du texte bidirectionnel, du texte vertical et des caractères le long d'un chemin courbe.

**Peinture** - Les formes peuvent être remplies et/ou délimitées avec une couleur, un dégradé ou un motif, ce qui permet de les rendre opaques ou d'avoir n'importe quel degré de transparence. Les entités de fin de ligne telles que les pointes de flèches ou les symboles apparaissant aux sommets d'un polygone sont représentées par des marqueurs.

**Couleur** - Les spécifications SVG permettent d'appliquer des couleurs à tous les éléments SVG visibles, soit directement, soit via le remplissage, le contour et d'autres propriétés. Différents codes de couleur peuvent être utilisés pour spécifier comme le noir ou le bleu, la représentation hexadécimale, décimale ou en pourcentage de la forme RVB.

**Dégradés et motifs** - Les formes d'un fichier SVG peuvent être remplies ou délimitées par des couleurs unies, des dégradés ou des motifs répétitifs.

**Effets de filtre** - Il s'agit en fait d'une série d'opérations graphiques qui sont appliquées à un graphique vectoriel source donné pour produire un résultat modifié.

**Interactivité** - Les utilisateurs peuvent interagir avec les fichiers SVG en modifiant le focus, les clics de souris, le défilement ou le zoom de l'image. L'interactivité permet aux images SVG d'interagir avec les utilisateurs de différentes manières, comme mentionné ci-dessus.

**Lien** - Il est possible que les images SVG aient des hyperliens vers d'autres documents. Ceci est réalisé via le XML Linking Language ou XLink. Cela permet de créer des états de vue spécifiques qui sont utilisés pour effectuer un zoom avant/arrière sur une zone spécifique ou pour limiter la vue à un élément spécifique.

**Scripting** - Semblable au HTML, tous les aspects d'un document SVG sont accessibles pour être manipulés à l'aide de scripts. Les objets SVG DOM fournissent des conseils pour y parvenir en utilisant l'élément et l'attribut SVG. Les scripts sont inclus dans des éléments de balise `script` et peuvent s'exécuter en réponse à des événements de pointeur, de clavier ou de document, selon les besoins.

**Animation** - Les éléments DOM<animate> ,<animateMotion> et<animateColor> vous permet d'inclure une animation pour le contenu SVG. Bien sûr, cela n'est pas réalisable sans utiliser de scripts et de minuteries intégrées. Ces animations peuvent être continues et peuvent être mises en boucle ainsi que répétées tout en répondant aux événements de l'utilisateur.

**Polices** - Le texte en SVG peut faire référence à des fichiers de polices externes tels que les polices système. En l'absence de telles polices, le texte en SVG ne sera pas rendu à la sortie. Cela peut être surmonté en incorporant les glyphes requis dans un tel fichier en tant que police qui est ensuite rendue à l'aide de la<text> élément.

## Exemples ##
Les lignes suivantes montrent comment un cercle est représenté à l'aide du script SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Les lignes de code suivantes montrent comment utiliser le<text> bloc pour le rendu du texte en SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Références ##

* [Spécifications SVG du W3C](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipédia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

