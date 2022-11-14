{
  "date" : "2020-08-20",
  "keywords" :[ "fichier fon", "format de fichier fon", "qu'est-ce qu'un fichier fon", "fichier", "exemple fon", "extension de fichier fon","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Fichier de bibliothèque de polices",
  "description":"En savoir plus sur le format de fichier FON et les API qui peuvent créer et ouvrir des fichiers FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Qu'est-ce qu'un fichier FON ?

Un fichier avec l'extension .fon est une bibliothèque de polices Microsoft Windows 3.x qui est en fait un fichier exécutable mais renommé en .fon. Il s'agit d'une collection de fichiers [.fnt](/fr/font/fnt/) en soi et les applications y font référence lors de l'accès à la police système. C'est pourquoi il agit comme un fichier de ressources. Il peut être ouvert sur le système d'exploitation Windows à l'aide de l'application Microsoft Windows Font View.

## Format de fichier FON

Un fichier FON contient des ressources de police et a le format de fichier Resource (.res). Le format de fichier .res spécifie l'en-tête du fichier ainsi que les spécifications de la section de données. Un .fnt est également un fichier de données de ressources qui est inclus avec un fichier de ressources. Les fichiers FON ont un format de fichier binaire et ont un type MIME application/octet-stream.

Les ressources de police, contrairement à d'autres types de ressources, ne sont pas ajoutées aux ressources d'une application. Au lieu de cela, ils sont ajoutés aux fichiers EXE et renommés en fichiers .fon, ce qui donne des fichiers de bibliothèque au lieu d'applications. Plusieurs polices individuelles constituent des composants d'un groupe de polices où chaque groupe suit une structure de groupe de ressources. Les ressources de police utilisent ces structures de groupe de ressources. L'en-tête de groupe contient toutes les informations nécessaires pour accéder à une police spécifique du groupe. Une ressource de composant de police a le format suivant.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/fr/font/fnt/) file)
```
Un seul fichier de ressources .rc peut avoir des déclarations de ressources mixtes. Les groupes de polices peuvent se trouver n'importe où dans le fichier de ressources et n'ont pas besoin d'être contigus. Il est indispensable que les programmes créant des fichiers .RES ajoutent la saisie manuelle de FONTDIR. Voici la structure de l'en-tête de groupe.

```
[En-tête de ressource normal (type = 7)]

WORD NombreDePolices ; // Nombre total dans le fichier .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal ;
struct FontDirEntry {
WORD dfVersion ;
DWORD dfSize;
char dfCopyright[60] ;
WORD dfType ;
MOT dfPoints ;
WORD dfVertRes ;
MOT dfHorizRes ;
MOT dfAscent ;
WORD dfInternalLeading ;
WORD dfExternalLeading ;
BYTE dfItalique ;
BYTE dfUnderline ;
BYTE dfStrikeOut ;
WORD dfWeight ;
BYTE dfCharSet ;
WORD dfPixWidth ;
WORD dfPixHeight ;
BYTE dfPitchAndFamily ;
WORD dfAvgWidth ;
WORD dfMaxWidth ;
BYTE dfPremierChar ;
BYTE dfLastChar ;
BYTE dfDefaultChar ;
BYTE dfBreakChar ;
WORD dfWidthBytes ;
DWORD dfDevice ;
DWORD dfFace;
DWORD dfRéservé ;
char szDeviceName[] ;
char szFaceName[] ;
} ;
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

