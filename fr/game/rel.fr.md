{
  "date" : "2021-09-08",
  "keywords" :[ "fichier rel", "format de fichier rel", "qu'est-ce qu'un fichier rel", "fichier", "exemple rel", "extension de fichier rel","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier REL et les API qui peuvent créer et ouvrir des fichiers REL.",
  "title" :"REL - Fichier de module déplaçable",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Qu'est-ce qu'un fichier REL ?
Un fichier avec l'extension .rel peut être utilisé à plusieurs fins. Par conséquent, en termes de classification de jeu, il est connu comme un fichier de module déplaçable utilisé par certains jeux Nintendo Wii, tels que Brawl, Super Smash Bros et Mario Kart Wii. Il comprend les données de jeu, y compris les modèles de personnages et les étapes. Les fichiers REL fonctionnent de la même manière que les fichiers .DLL utilisés par Microsoft Windows.

## Format de fichier REL
Dans un format de fichier REL, le fichier est divisé en plusieurs sections, regroupées par accès similaire, par exemple, les données en lecture seule dans une section, tout le code exécutable est placé dans une autre, etc. Le fichier commence par une section d'en-tête, suivie de :
- Tableau contenant des informations sur la section.
- Les données de section.
- Informations de déménagement.

### En-tête de fichier
Le fichier commence par un en-tête de jusqu'à 0x4C octets :
| Décalage | Taille | Nom du champ | Descriptif |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | identifiant | Numéro d'identification arbitraire. Doit être unique parmi tous les REL utilisés par un jeu. Ne doit pas être 0. |
| 0x04 | 4 | suivant | Pointeur vers le module suivant, rempli au moment de l'exécution. |
| 0x08 | 4 | préc | Pointeur vers le module précédent, rempli à l'exécution. |
| 0x0c | 4 | nombreSections | Nombre de sections dans le fichier. |
| 0x10 | 4 | sectionInfoOffset | Décalage au début de la table de section. |
| 0x14 | 4 | nameOffset | Décalage vers la chaîne ASCII contenant le nom du module. Peut être NULL. Relatif au début du fichier REL. |
| 0x18 | 4 | nomTaille | Taille du nom du module en octets. |
| 0x1c | 4 | version | Numéro de version du format de fichier REL. |
| 0x20 | 4 | bssTaille | Taille de la section '.bss'. |
| 0x24 | 4 | Décalagerel | Décalage à la table de relocalisation. |
| 0x28 | 4 | impOffset | Décalage vers la table imp. |
| 0x2c | 4 | impSize | Taille de la table imp en octets. |
| 0x30 | 1 | prologSection | Index dans la table de section à laquelle le prologue est relatif. Ignorer si ce champ vaut 0. |
| 0x31 | 1 | épilogueSection | Index dans la table de section à laquelle l'épilogue est relatif. Ignorer si ce champ vaut 0. |
| 0x32 | 1 | non résoluSection | Index dans la table de section à laquelle non résolu est relatif. Ignorer si ce champ vaut 0. |
| 0x33 | 1 | bssSection | Index dans la table de section à laquelle bss est relatif. Rempli à l'exécution ! |
| 0x34 | 4 | prologue | Décalage dans la section spécifiée de la fonction _prolog. |
| 0x38 | 4 | épilogue | Décalage dans la section spécifiée de la fonction _epilog. |
| 0x3c | 4 | non résolu | Décalage dans la section spécifiée de la fonction _unresolved. |
| 0x40 | 4 | aligner | Version ≥ 2 uniquement. Contrainte d'alignement sur toutes les sections, exprimée en puissance de 2. |
| 0x44 | 4 | bssAligner | Version ≥ 2 uniquement. Contrainte d'alignement sur toutes les sections '.bss', exprimée en puissance de 2. |
| 0x48 | 4 | taillefixe | Version ≥ 3 uniquement. Si REL est lié avec OSLinkFixed (au lieu de OSLink), l'espace après cette adresse peut être utilisé à d'autres fins (comme BSS). |

### Tableau d'informations sur les sections
La table d'informations de section contient des entrées **numSections** de 0x8 octets chacune :
| Décalage | Taille | Descriptif |
-------|------------|-------------|
| 0x0 | 30 bits | Décalage du début du REL à la section. Si c'est zéro, la section est une section non initialisée (c'est-à-dire .bss). |
| 0x3.6 | 1 bit | Inconnue. |
| 0x3.7 | 1 bit | Drapeau exécutable ; si c'est 1 la section est exécutable. |
| 0x4 | 4 | Longueur en octets de la section. S'il s'agit de zéro, cette entrée est ignorée. |
| 0x8 | Entrée suivante | Entrée suivante |

### Données de relocalisation
Les données de relocalisation sont une ou plusieurs listes de structures de 0x8 octets. La fin de chaque liste est marquée par le code de type spécial 203 :
| Décalage | Nom | Taille | Descriptif |
-------|------------|------------|-----|
| 0x0 | décalage | 2 | Décalage en octets du déplacement précédent vers celui-ci. S'il s'agit du premier déplacement dans la section, il est relatif au début de la section. |
| 0x2 | taper | 1 | Le type de déménagement. Décrit ci-dessous. |
| 0x3 | rubrique | 1 | La section du symbole par rapport à laquelle se déplacer. Pour le type de relocalisation spécial 202, il s'agit plutôt du numéro de la section de ce fichier à laquelle s'appliquent les entrées de relocalisation suivantes. |
| 0x4 | ajouter | 4 | Décalage en octets du symbole par rapport auquel se déplacer, par rapport au début de sa section. Il s'agit plutôt d'une adresse absolue pour les relocalisations vers main.dol. |
| 0x8 | Entrée suivante | Entrée suivante | Entrée suivante |


 




## Références


* [Format de module d'objet relocalisable](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


