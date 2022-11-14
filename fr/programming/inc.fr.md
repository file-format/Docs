{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extension de fichier INC - Qu'est-ce qu'un fichier INC ?",
  "description":"En savoir plus sur le format de fichier INC Include et les API qui peuvent créer et ouvrir des fichiers INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Qu'est-ce qu'un fichier INC ?

Un fichier INC est un fichier inclus utilisé par le code source du logiciel pour référencer les informations d'en-tête. Il est similaire au [format de fichier .h](/fr/programming/h/) et contient des déclarations, des fonctions, des en-têtes ou des macros qui peuvent être réutilisés par des fichiers de code source tels que C++. Les fichiers INC sont utilisés par une variété de langages de programmation tels que C, [C++](/fr/programming/cpp/), Pascal, [PHP](/fr/programming/php/) et [Java](/fr/programming/java/). Les éditeurs de texte tels que Microsoft Notepad, Notepad ++ et TextEdit peuvent être utilisés pour ouvrir les fichiers INC.

## Format de fichier INC - Plus d'informations

Un fichier INC est enregistré en tant que fichier texte brut avec toutes les déclarations incluses selon la syntaxe de déclaration. Un fichier INC peut également référencer d'autres fichiers INC. Une fois créé, le fichier INC fait partie du projet et peut être référencé à partir de fichiers source tels que C++. Il peut être référencé par plusieurs fichiers source pour éviter toute duplication.

## Contenu du fichier INC

Les fichiers INC peuvent inclure les informations suivantes.

**`Variables`** - Dans le cas de la programmation orientée objet (POO), un fichier d'en-tête de classe contient les définitions de toutes les variables de niveau de classe accessibles dans les fichiers de code source d'implémentation

**`Déclaration de méthodes`** - Toutes les déclarations de méthodes sont incluses dans les fichiers d'en-tête .h pour être accessibles dans plusieurs fichiers d'implémentation.

**`Définitions de fonctions non en ligne`** - Les fichiers d'en-tête peuvent également contenir des définitions de méthodes non en ligne.

## Inconvénient d'utiliser le fichier INC en PHP

PHP sont des scripts côté serveur qui s'exécutent sur le serveur et renvoient les résultats aux pages Web appelantes. Si un fichier PHP fait référence à un fichier INC et que le serveur n'est pas configuré pour analyser les fichiers .inc (ce qui est très courant), un utilisateur peut afficher le code source php dans le fichier .inc en visitant le répertoire URL. Il faut donc être prudent lors de l'utilisation de fichiers INC comme fichiers d'inclusion dans PHP.

## Références

* [Utiliser INC en PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

