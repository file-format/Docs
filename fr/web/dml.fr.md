{
  "date" : "2021-05-25",
  "keywords" :[ "DML","fichier DML", "format de fichier DML", "type de fichier DML", "fichier", "type", "qu'est-ce qu'un fichier DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - Fichier HTML DynaScript",
  "description":"En savoir plus sur le format de fichier DML et les API qui peuvent créer et ouvrir des fichiers DML.",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## Qu'est-ce qu'un fichier DML ?

Un fichier avec l'extension .dml est un fichier de code de page de script Web créé avec DyanScript. DynaScript est un langage de script dynamique [HTML](/fr/web/html/) qui est compatible avec ECMAScript et fournit la plupart des mêmes fonctionnalités que les autres langages de script. Il est similaire au code ColdFusion et au code Microsoft Active Server Pages (ASP). Les fichiers DML peuvent être ouverts et affichés dans des navigateurs Web standard similaires à d'autres pages HTML.

## Format de fichier DML

Les fichiers DML sont créés au format de fichier texte brut et peuvent être ouverts avec un éditeur de texte pour afficher le code. L'écriture de code à l'aide du langage de script DML peut être utilisée pour générer dynamiquement du code HTML sur des pages DML hébergées côté serveur. Les DynaScripts sont construits à partir des éléments de langage suivants :


* Balise SCRIPT - Celles-ci sont intégrées dans les documents sous forme de commentaires HTML. Un commentaire HTML est marqué par un \ <!-- tag.
* Littéraux - Ce sont des valeurs fixes dans les fichiers DynaScript. Des exemples de ceux-ci incluent des entiers tels que 123 , 0x3F , 0123, des nombres à virgule flottante tels que 456.789 , 3.2e-8, des booléens tels que vrai ou faux et des chaînes telles que "La pluie en Espagne"
* Variables - Les variables DynaScript n'ont pas besoin d'être définies ou de les affecter à un type de données fixe. Une variable doit avoir une valeur avant que vous ne l'utilisiez dans une expression ; sinon, un avertissement d'exécution est généré.
* Expressions - Il s'agit de combinaisons de variables, de valeurs littérales, d'opérateurs et d'autres expressions. Le côté droit d'une instruction d'affectation est une expression.
* Opérateurs - Ceux-ci opèrent sur une ou plusieurs expressions appelées opérandes. Ceux-ci peuvent être ternaires, binaires ou unaires : les opérateurs ternaires agissent sur trois expressions, les opérateurs binaires agissent sur deux expressions et les opérateurs unaires agissent sur une.
* Déclarations - Elles contrôlent le déroulement des scripts, manipulent les objets et la programmation générale. En général, ces instructions suivent la syntaxe C et Java standard. Les exemples sont les boucles if-else, do-while, switch, break, continue, etc. comme tout autre langage de script.
* Fonctions - Les fonctions, comme tout autre langage de script, vous permettent d'encapsuler un ensemble d'instructions une fois dans un document en tant que fonction, puis de l'utiliser plusieurs fois dans tout le document (en appelant la fonction). DynaScript prend également en charge les fonctions.
* Objets - DynaScript est orienté objet et prend en charge les "objets" et les concepts fondamentaux orientés objet d'encapsulation, de polymorphisme et d'héritage.

