{
  "date" : "2020-08-20",
  "keywords" :[ "fichier fnt", "format de fichier fnt", "qu'est-ce qu'un fichier fnt", "fichier", "exemple fnt", "extension de fichier fnt","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Fichier de police Windows",
  "description":"En savoir plus sur le format de fichier FNT et les API qui peuvent créer et ouvrir des fichiers FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Qu'est-ce qu'un fichier FNT ?

Un fichier avec l'extension .fnt est un fichier de police qui stocke des informations de police génériques sur les systèmes d'exploitation Windows. Les fichiers FNT ont été principalement remplacés par les formats de fichier TrueType (.TTF) et OpenType (.OTF). Il s'agit d'un format de fichier de police obsolète à ce jour. Ces fichiers peuvent stocker un seul évaluateur ou une police vectorielle. Tous les pilotes de périphérique prennent en charge les polices Windows 2.x. Cependant, tous les pilotes de périphérique
prend en charge la version Windows 3.0.

## Format de fichier FNT

Les fichiers FNT sont capables de stocker une seule police raster ou vectorielle. Les formats vectoriels sont plus fréquemment utilisés par GDI par rapport au raster où le glyphe de chaque charte est défini à l'aide d'un petit bitmap. La raison évidente du remplacement de .fnt par .ttf et .otf est son format raster.

### En-tête du fichier de police
Le début des fichiers de police raster et vectoriel est commun, suivi de différentes informations pour chaque type de fichier. L'en-tête du fichier de police inclut pour Windows 3.0 comprend six nouveaux champs comme suit qui sont mis à zéro pour assurer la compatibilité avec les futures versions de Windows.

* dDrapeaux
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfRéservé1

Pour des informations détaillées sur les en-têtes pour Windows 3.0 et 2.0, visitez le [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Références
* [Format de fichier de police] (https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Comment installer ou supprimer une police dans Windows] (https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

