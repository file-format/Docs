{
"date": "08/06/2023",
  "keywords": [
"fichier hpp",
"qu'est-ce qu'un fichier hpp",
"que contient le fichier hpp",
"exemple de fichier hpp",
"quel est le format du fichier hpp",
"déposer",
"extension de fichier hpp",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier HPP - Fichier d'en-tête C++",
  "description":"Découvrez le format HPP et les API permettant de créer et d'ouvrir des fichiers HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent" : "programming"
}
},
"lastmod": "2023-06-08"
}

## Qu'est-ce qu'un fichier HPP ?

Le format de fichier « .hpp » est couramment utilisé pour les fichiers d'en-tête dans le langage de programmation C++. Les fichiers d'en-tête contiennent généralement des déclarations et des définitions de fonctions, classes, variables et constantes utilisées par d'autres fichiers de code source dans le projet C++.

Le but de l'utilisation des fichiers d'en-tête est de fournir un moyen de partager du code commun sur plusieurs fichiers de code source sans dupliquer le code lui-même. Lorsque le fichier source C++ doit accéder aux déclarations ou aux définitions du fichier d'en-tête, il inclut le fichier d'en-tête à l'aide de la directive du préprocesseur `#include`.

L'extension de fichier « .hpp » est souvent utilisée pour indiquer qu'un fichier est un fichier d'en-tête C++. Il n'est pas obligatoire d'utiliser cette extension spécifique pour les fichiers d'en-tête, et vous pouvez également rencontrer des fichiers d'en-tête avec « .h » ou d'autres extensions. Le choix de l’extension est en grande partie une question de convention et de préférence personnelle.

Lorsqu'un fichier source C++ inclut un fichier d'en-tête à l'aide de `#include`, le compilateur combine efficacement le contenu du fichier d'en-tête avec le fichier source avant de le compiler en tant qu'unité. Cela permet au fichier source d'accéder aux déclarations et aux définitions dans le fichier d'en-tête, fournissant ainsi les informations nécessaires au compilateur pour effectuer la vérification de type et la génération de code.

## Que contient le fichier HPP ?

Voici quelques contenus courants que vous pouvez trouver dans le fichier « .hpp » :

- **Déclarations de fonctions :** Les fichiers d'en-tête incluent souvent des déclarations de fonctions sans leurs implémentations réelles. Ces déclarations fournissent des informations sur le nom de la fonction, le type de retour et les paramètres, permettant à d'autres fichiers de code source d'utiliser la fonction sans avoir besoin de connaître les détails d'implémentation.
- **Déclarations de classe :** Les fichiers d'en-tête peuvent contenir des déclarations de classe, notamment le nom de la classe, les variables membres, les fonctions membres et les spécificateurs d'accès. En incluant la déclaration de classe dans le fichier d'en-tête, d'autres fichiers de code source peuvent créer des objets de cette classe et accéder à ses membres.
- **Déclarations de constantes :** Les fichiers d'en-tête peuvent définir des constantes, telles que des variables globales ou des valeurs d'énumération destinées à être partagées entre plusieurs fichiers de code source. Ces constantes sont accessibles en incluant le fichier d'en-tête dans d'autres fichiers source, leur permettant d'utiliser les constantes définies.
- **Définitions de types :** Les fichiers d'en-tête peuvent contenir des définitions de types utilisant le mot-clé "typedef" ou des alias de type utilisant le mot-clé "using". Ces définitions créent de nouveaux noms pour les types existants, rendant le code plus lisible et plus maintenable.
- **Définitions de fonctions en ligne :** Dans certains cas, les fichiers d'en-tête peuvent contenir des définitions de fonctions en ligne. Les fonctions en ligne sont de petites fonctions qui sont développées sur le site d'appel plutôt que d'être appelées en tant que fonction distincte. L’inclusion d’une définition de fonction en ligne dans le fichier d’en-tête permet au compilateur de remplacer directement l’appel de fonction par le corps de la fonction, améliorant potentiellement les performances.

## Exemple de fichier HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Quel est le format du fichier HPP ?

HPP est un fichier texte brut mais suit les règles générales et la syntaxe du langage de programmation C++. Voici une description du format général et de la structure du fichier « .hpp » :

- **Protections d'en-tête :** En règle générale, un fichier ".hpp" commence par des protections d'en-tête pour empêcher plusieurs inclusions du même fichier. Ceci est réalisé à l'aide de directives de préprocesseur telles que `#ifndef`, `#define` et `#endif`. La protection d'en-tête garantit que le contenu du fichier n'est inclus qu'une seule fois pendant le processus de compilation.
- **Instructions d'inclusion :** Après les protections d'en-tête, vous pouvez inclure d'autres fichiers d'en-tête nécessaires à l'aide de la directive `#include`. Ceux-ci peuvent inclure des en-têtes de bibliothèque standard ou d'autres en-têtes personnalisés requis par votre code.
- **Déclarations et définitions :** Le contenu principal du fichier ".hpp" est constitué des déclarations et, dans certains cas, des définitions de classes, fonctions, constantes, alias de type et autres éléments. Par exemple, vous pouvez déclarer des classes à l'aide du mot-clé `class`, des fonctions à l'aide de leur type de retour, de leur nom et de leur liste de paramètres, et des constantes à l'aide du mot-clé `const` suivi de leur type et de leur nom.
- **Définitions de fonctions en ligne :** Dans certains cas, vous pouvez inclure des définitions de fonctions en ligne directement dans le fichier ".hpp". Les fonctions en ligne sont généralement définies dans le corps de la classe, ce qui signifie que la définition de la fonction est incluse à côté de sa déclaration. Cela peut être fait en préfixant la définition de fonction avec le mot-clé `inline`.
- **Déclarations d'espaces de noms :** Si vous utilisez des espaces de noms dans votre code, vous pouvez les déclarer dans le fichier ".hpp". Cela se fait en utilisant le mot-clé `namespace` suivi du nom de l'espace de noms et en enfermant le code pertinent dans le bloc d'espace de noms.

## Les références
* [Fichiers d'en-tête (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

