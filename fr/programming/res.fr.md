{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - Script de ressources compilé en C++",
  "description":"En savoir plus sur le format de fichier RES avec un exemple RES et des API qui peuvent créer et ouvrir des fichiers RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Qu'est-ce qu'un fichier RES ?
Le fichier avec le suffixe ou l'extension .res peut appartenir à de nombreuses catégories de format de fichier. Ici, nous discutons du format de fichier RES qui est un script de ressources compilé C++ ; un fichier binaire créé par Microsoft Resource Compiler (rc) qui contient des données de ressources ; basé sur le contenu du fichier de définition de ressource ; pertinent pour son projet logiciel parent. Le fichier .res est généralement reformaté en un fichier objet de ressource pour le lier au fichier exécutable d'une application.

## Format de fichier RES
Le format de fichier RES appartient au Microsoft Resource Compiler (rc). Le compilateur de ressources est un outil qui compile les ressources telles que les curseurs, les icônes, les menus et les boîtes de dialogue que votre application utilise. Les fichiers de ressources ont généralement une extension .res ; contient des ressources, telles que des curseurs, des images et des informations de version. Un fichier RES peut être un fichier de ressources 16 ou 32 bits.
## Structure du fichier de ressources
Un fichier de ressources contient une série d'entrées de ressources diverses. Chaque entrée contient un en-tête de ressource et des données pertinentes. Un en-tête de ressource est généralement aligné sur DWORD dans le fichier et contient les éléments suivants :

- Un **DWORD** pour spécifier la taille de l'en-tête de la ressource
- Un **DWORD** pour spécifier la taille des données de ressource
- Le type de ressource
- Le nom de la ressource
- Informations supplémentaires sur les ressources

La structure d'en-tête de ressource définit le format du fichier RES. Les données de la ressource suivent l'en-tête de la ressource. Certaines ressources ajoutent également un modèle d'en-tête de groupe spécifique aux ressources pour fournir des informations sur un groupe de ressources. Voici quelques-uns des types d'entrée de ressource et leur description :

### Ressources de la table des accélérateurs
Une table d'accélérateurs est une entrée de ressource dans un fichier RES sans en-tête de groupe. Le modèle **ACCELTABLEENTRY** définit chaque entrée dans la table des accélérateurs. Un fichier RES peut avoir plusieurs tables d'accélérateurs.

### Ressources de curseur et d'icône
Bien que le système considère chaque icône et curseur comme un seul fichier, ceux-ci sont stockés dans des fichiers RES en tant que groupe de ressources d'icônes ou de ressources de curseur. Les formats de fichier des ressources d'icône et de curseur sont les mêmes. Un en-tête de groupe de ressources suit tous les composants de groupe d'icônes ou de curseurs individuels dans le fichier .res.

### Ressources de la boîte de dialogue
Une boîte de dialogue est également réalisée en tant qu'entrée de ressource dans le fichier RES. Il contient un modèle d'en-tête de boîte de dialogue **DLGTEMPLATE** et un modèle **DLGITEMTEMPLATE** pour chaque contrôle spécifique de la boîte de dialogue. Les modèles **DLGTEMPLATEEX** et **DLGITEMTEMPLATEEX** expliquent le format des ressources de boîte de dialogue étendues.

### Ressources de polices
Une ressource de menu contient un modèle **MENUHEADER** puis un ou plusieurs modèles **NORMALMENUITEM** ou **POPUPMENUITEM**, un pour chaque élément de menu dans le modèle de menu. Les modèles **MENUEX_TEMPLATE_HEADER** et **MENUEX_TEMPLATE_ITEM** expliquent le format des ressources de menu étendu.

### Ressources du tableau des messages
Une table de messages se compose d'un texte formaté à afficher sous forme de message d'erreur ou dans une boîte de message. Le modèle principal dans une ressource de table de messages est la structure **MESSAGE_RESOURCE_DATA**.

### Ressources de version
Le modèle principal dans une ressource de version est **VS_FIXEDFILEINFO**. Les modèles supplémentaires incluent **VarFileInfo** pour stocker les données relatives aux informations de langue et **StringFileInfo** pour les informations de chaîne personnalisées.




## Références

* [Formats de fichiers de ressources](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



