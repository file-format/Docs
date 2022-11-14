{
  "date" : "2019-10-11",
  "keywords" :[ "fichier u3d", "format de fichier u3d", "qu'est-ce qu'un fichier u3d", "fichier", "exemple u3d", "extension de fichier u3d","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Format de fichier 3D universel",
  "description":"En savoir plus sur le format de fichier U3D et les API qui peuvent ouvrir et créer des fichiers U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier U3D ?

**U3D** (Universal 3D) est un format de fichier compressé et une structure de données pour l'infographie 3D. Il contient des informations sur le modèle 3D telles que les maillages triangulaires, l'éclairage, l'ombrage, les données de mouvement, les lignes et les points avec couleur et structure. Le format a été accepté comme norme [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm) en août 2005. Les documents 3D [PDF](/fr/pdf/) prennent en charge U3D objets incorporés et peuvent être visualisés dans Adobe Reader (version 7 et ultérieure).

Le format U3D a été développé dans le but d'établir une norme universelle pour le stockage et l'échange de données tridimensionnelles. Cependant, le format trouve sa principale utilisation dans l'encodage pour PDF 3D plutôt que d'être utilisé comme format d'échange. Acrobat 3D convertit un type de fichier 3D pris en charge en U3D ou PRC lors de la conversion au format PDF.

## Format de fichier U3D

Les fichiers U3D sont au format de fichier binaire qui a subi quatre éditions comme décrit par le document de référence [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm), entraînant une mise à jour des spécifications à chaque édition. La norme de fichier PDF ISO-32000 accepte U3D comme type d'annotation et multimédia autorisé.

La première édition d'U3D était axée sur les représentations clés des propriétés graphiques 3D telles que la géométrie, la couleur, les textures, l'éclairage, les os et l'animation basée sur la transformation. Les deuxième et troisième éditions ont corrigé certains errata dans la première édition, la troisième version étant le type le plus couramment utilisé dans les logiciels de l'industrie. La quatrième édition fournit des définitions pour les primitives d'ordre supérieur (surfaces courbes). [Les spécifications U3D] (http://www.ecma-international.org/publications/standards/Ecma-363.htm) sont disponibles en ligne pour référence sur le site Web de l'ECMA.

### Types de données dans les fichiers U3D

Le fichier binaire contiendra les types suivants : U8, U16, U32, U64, I16, I32, F32, F64 et String.

* U8 : Un entier non signé de 8 bits
* U16 : Un entier non signé de 16 bits
* U32 : Un entier 32 bits non signé
* U64 : Un entier 64 bits non signé
* I16 : Un entier 16 bits signé
* F32 : un flotteur simple précision IEEE.
* F64 : Un flotteur double précision IEEE.
* Chaîne : les chaînes d'un fichier U3D commencent par un entier 16 bits non signé qui définit la longueur totale des caractères de la chaîne. Les chaînes sont toujours traitées en respectant la casse.

## Structure des fichiers U3D

Un fichier U3D contient une séquence de blocs. Il existe 3 types différents de bloc dans chaque fichier U3D.

* Bloc d'en-tête de fichier
* Bloc de déclaration
* Bloc Suite

Le chargeur détermine la fin d'un bloc si les données de ce bloc ne sont pas requises ou si un décodeur pour ce type de bloc n'est pas disponible.

{{< figure src="../u3d.png" alt="Format de fichier U3D" >}}

### Bloc d'en-tête de fichier
Un bloc d'en-tête de fichier contient des informations de fichier qui sont utilisées par le chargé pour déterminer comment lire le fichier.

### Bloc de déclaration

Les blocs de déclaration contiennent des informations sur les objets du fichier. Les objets d'un bloc de déclaration doivent être définis.

### Bloc Suite

Des informations supplémentaires pour les objets déclarés dans un bloc de déclaration sont fournies dans le bloc de continuation. Chaque bloc de continuation doit être associé à un bloc de déclaration.


## Références ##

* [Format de fichier U3D - Wikipédia](https://en.wikipedia.org/wiki/Universal_3D)
* [Spécifications du format de fichier ECMA U3D] (https://www.ecma-international.org/publications/standards/Ecma-363.htm)

