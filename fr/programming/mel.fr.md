{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Langage Maya Embedded","fichier", "extension", "format de fichier", "Maya 3D", "Guide de programmation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Format de fichier de langage intégré Maya",
  "description":"En savoir plus sur le format de fichier MEL et les API qui peuvent créer et ouvrir des fichiers MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Qu'est-ce qu'un fichier MEL ?

Un fichier avec l'extension .mel (Maya Embedded Language) est un langage de script utilisé par Autodesk Maya pour créer des interfaces graphiques. Il vous permet d'automatiser la création d'éléments graphiques à l'aide de scripts exécutables en plus de l'interface graphique de Maya. MEL vous permet de créer des interfaces graphiques sans apprendre à programmer. Ceci est réalisé en créant des macros et des actions personnalisées qui accélèrent les tâches répétitives. Ces procédures et scripts vous permettent de créer des modélisations, des animations, des dynamiques et des rendus de tâches personnalisés. Autodesk Maya 2020 peut être utilisé pour ouvrir et afficher le contenu d'un fichier EML.

## Format de fichier MEL - Plus d'informations

Un [manuel de référence] du programmeur (https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) est disponible pour les développeurs dans la section de documentation de Maya. MEL est basé sur des commandes de script shell, similaires à UINX, pour réaliser des choses. Les commandes basées sur les scripts le rendent non pertinent pour la programmation conventionnelle et orientée objet (OOP), ce qui entraîne aucune utilisation de structures de données, d'appels de fonctions ou d'utilisation de la POO comme dans d'autres langages.

Voici quelques points clés à propos de MEL.

`Comments` - Chaque instruction dans MEL doit se terminer par un point-virgule (;), même à la fin d'un bloc.

`Returning Values` - Indiquer une expression qui renvoie une valeur n'imprime pas automatiquement la valeur dans MEL. Au lieu de cela, cela provoque une erreur.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Commandes pour créer, modifier et supprimer` - La même commande est utilisée pour créer des choses, modifier des choses ou demander des informations sur des choses existantes. Cependant, un indicateur contrôle ce que fait la commande (création, modification ou requête).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - La syntaxe de la fonction renvoie automatiquement une valeur. Pour obtenir une valeur de retour à l'aide de la syntaxe de commande, vous devez placer la commande entre guillemets.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Références

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

