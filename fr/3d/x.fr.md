{
  "date" : "2020-01-11",
  "keywords" :[ "fichier x", "format de fichier x", "qu'est-ce qu'un fichier x", "fichier", "exemple x", "extension de fichier x","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Format de fichier DirectX 2.0",
  "description":"En savoir plus sur le format de fichier DirectX X et les API qui peuvent ouvrir et créer des fichiers DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Qu'est-ce qu'un fichier X ?

Un fichier avec l'extension .x fait référence au format de fichier hérité [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics introduit avec Microsoft DirectX 2.0. Il a été utilisé pour le rendu graphique 3D dans les jeux et spécifie les structures des maillages, des textures, des animations et des objets définis par l'utilisateur. Il est obsolète depuis 2014 car le format de fichier Autodesk FBX sert mieux comme format plus moderne. X est basé sur des modèles et est libre de toute connaissance d'utilisation.

Vous pouvez ouvrir des fichiers DirectX X à l'aide de Microsoft DirectX et des éditeurs de texte courants.

## Format de fichier X

La [référence du fichier X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) contient des informations de référence pour les éléments d'API utilisés pour travailler avec les fichiers DirectX .x. Le format fournit des primitives de données de bas niveau qui sont utilisées par d'autres applications pour définir des primitives de niveau supérieur via des modèles de données. DirectX 6.0 a introduit des interfaces et des méthodes qui permettent de lire et d'écrire dans des fichiers .x. DirectX 3.0 a introduit une version binaire de ce format de fichier.

La [référence du format de fichier X](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) définie par DirectX 9 contient des informations de référence pour .x fichiers en binaire ainsi que des encodages de texte.

### Encodage binaire

Le [format binaire](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) définit le format DirectX X comme une représentation symbolique du format texte. Ces jetons peuvent être autonomes pour donner une structure grammaticale ou peuvent être des jetons porteurs d'enregistrement fournissant les données nécessaires.

#### Entête

L'en-tête binaire peut être lu et écrit en utilisant les définitions suivantes.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Encodage de texte

Les fichiers DirectX .x ne dépendent pas de la façon dont le fichier est utilisé et ne sont spécifiques à aucune application. Cette approche basée sur des modèles permet au format de fichier .x d'être utilisé par n'importe quelle application cliente.


#### Entête

L'en-tête de longueur variable est obligatoire et doit se trouver au début du flux de données. L'en-tête contient les données suivantes.

|Type |Sous-type |Taille |Contenu |Signification du contenu|
---|---|---|---|---|
|Numéro magique (obligatoire)| | 4 octets |xof |
|Numéro de version (obligatoire) |Numéro majeur |2 octets |03 |Version majeure 3|
| |Numéro mineur |2 octets |02 |Version mineure 2|
|Type de format (obligatoire)| |4 octets |"txt " |Fichier Texte|
| | | |"bac "| Fichier binaire|
| | | |"tzip"| Fichier texte compressé MSZip |
| | | |"zip"| Fichier binaire compressé MSZip|
|Taille flottante (obligatoire)| |4 octets| 0064| Flottants 64 bits |
| | | |0032 |Flottants 32 bits|


## Références

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Référence du format de fichier DirectX 9](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

