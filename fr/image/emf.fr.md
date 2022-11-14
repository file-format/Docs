{
  "date" : "2019-10-11",
  "keywords" :[ "fichier emf", "format de fichier emf", "qu'est-ce qu'un fichier emf", "fichier", "exemple emf", "extension de fichier emf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Format de métafichier amélioré",
  "description":"En savoir plus sur le format de fichier EMF et les API qui peuvent créer et ouvrir des fichiers EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier EMF ?

Le **format de métafichier amélioré (EMF)** stocke les images graphiques indépendamment de l'appareil. Les métafichiers d'EMF comprennent des enregistrements de longueur variable dans l'ordre chronologique qui peuvent restituer l'image stockée après analyse sur n'importe quel périphérique de sortie. Ces enregistrements de longueur variable peuvent être des définitions d'objets fermés, des commandes de dessin et des propriétés graphiques essentielles pour restituer l'image avec précision. Lorsqu'un appareil ouvre un métafichier EMF à l'aide de son propre environnement graphique, les proportions, dimensions, couleurs et autres propriétés graphiques de l'image d'origine restent les mêmes quelle que soit la plate-forme de l'appareil d'ouverture.

## Bref historique ##

En 1990, Microsoft a conçu un format de fichier image Windows Metafile ([WMF](/fr/image/wmf/)) pour Microsoft Windows. Les métafichiers Windows sont au format 16 bits pouvant contenir certains composants bitmap. WMF peut être constitué de graphiques vectoriels et est destiné à rester portable entre différentes applications. En 1993, Win32/GDI a annoncé le métafichier amélioré (EMF), une version plus récente avec une flexibilité et une évolutivité améliorées. EMF est également utilisé comme commandes de langage graphique pour exécuter les pilotes d'imprimante. Microsoft recommande désormais le format de métafichier amélioré (EMF) plutôt que le format Windows (WMF). Lorsque Windows XP a été introduit, la version Enhanced Metafile Format Plus (EMF+) a été publiée. Cette version plus récente trouve son chemin en sérialisant les appels d'API GDI +, de même que les appels d'enregistrements WMF/EMF vers GDI. Il existe une version compressée gzip d'EMF appelée EMZ.

## Format de métafichier EMF ##

Voici les éléments essentiels du format de métafichier amélioré :

* Un EMR_HEADER (version, taille, la résolution de l'image à la création)
* Une table pour les objets GDI
* Une palette réservée (facultatif)
* Enregistrements de métafichiers organisés en structure de tableau (paramètres de propriété, objets définis, commandes de dessin)
* Enregistrement EMR_EOF (dernier enregistrement dans le métafichier EMF)

## Versions EMF ##
* ** Original ** : la version originale spécifie l'enregistrement nécessaire pour conserver l'image d'origine et la conserver indépendamment de l'appareil. De plus prend en charge l'enregistrement contenant des objets graphiques et des commandes pour le dessin.
* **Version 1** : la deuxième version d'EMF a amélioré la flexibilité et l'indépendance de l'appareil en ajoutant l'enregistrement pour le format de pixel et la possibilité d'utiliser la commande OpenGL.
* **Version 2** : la troisième version a amélioré la précision en ajoutant le système métrique pour mesurer les distances de surface de l'appareil, laissant l'enregistrement plus évolutif.

## Enregistrements de métafichiers améliorés ##

Les enregistrements de métafichier sont organisés sous forme de tableau. Ces enregistrements ont une structure ENHMETARECORD et une longueur variable. ENHMETARECORD spécifie les données qui définissent les fonctions GDI pour créer une image à l'aide du format de métafichier amélioré. La structure **ENHMETAHEADER** est toujours le premier enregistrement dans ce format. Cet en-tête EMF contient les informations suivantes.

Chaque enregistrement de métafichier amélioré a deux membres d'EMR (fournit la structure de base) au début. Le premier membre reconnaît la fonction GDI (les paramètres sont utilisés dans l'enregistrement) qui détermine le type d'enregistrement et est connu sous le nom d'iType. L'autre membre nSize définit la taille de chaque enregistrement. Paramètres restants (le cas échéant) et données supplémentaires disposées immédiatement sous nSize. Immédiatement après l'en-tête, une description textuelle facultative peut être présente. Le nom de l'image et de l'auteur est enregistré dans cette description textuelle. La palette dont la présence est une option spécifie les couleurs utilisées dans la création de métafichier amélioré. Les autres enregistrements servent à spécifier la fonction GDI qui est essentielle dans la création d'image.

Au moins un enregistrement EMF doit être présent dans chaque métafichier. Les informations de passage d'un enregistrement à l'autre dépendent des enregistrements EMF, de sorte que ces enregistrements doivent être disposés de manière adjacente. À n'importe quel enregistrement donné dans le métafichier sauf EOF_record, la longueur de cet enregistrement particulier est définie pour passer à l'enregistrement suivant.

## Création de métafichier améliorée ##

La fonction **CreateEnhMetaFile** est utilisée pour créer un métafichier amélioré. Les arguments de cette fonction sont utilisés pour les dimensions et le stockage de l'image sur disque/mémoire. De plus, cette fonction nécessite la dimension de l'appareil dans lequel l'image est apparue en premier (appareil référencé) et le contexte de l'appareil de référence (DC). Ainsi, les arguments pour gérer ce contrôleur de domaine doivent être fournis lors de l'appel de la fonction **CreateEnhMetaFile**. La syntaxe de fonction est la suivante :
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC :** poignée vers un appareil de référence.

**lptoFilename :** Un pointeur vers le nom du fichier.

**lprc:** Le pointeur vers la structure ovale spécifie les dimensions de l'image en mm.

**lpDesc :** un pointeur vers une chaîne pour le titre de l'image et le nom de l'application qui a créé l'image.

## Opérations améliorées sur les métafichiers ##

Voici les tâches qui peuvent être accomplies à l'aide du handle d'un métafichier amélioré.

* Afficher et modifier l'image stockée.
* Produire des copies de métafichiers améliorées.
* Récupérer la copie d'un en-tête EMF, la description facultative et la version binaire d'un métafichier amélioré
* Récapitulez les couleurs dans la palette.

## Objets graphiques ##

Dans les opérations de dessin et de peinture, les objets graphiques peuvent être créés par des enregistrements de création d'objet et peuvent être enregistrés pour une utilisation ultérieure. Un enregistrement `EMR_SELECTOBJECT` peut récupérer ces objets graphiques à l'aide du contexte de périphérique de lecture. Les stylos, les palettes, les pinceaux, les espaces colorimétriques, les polices et les objets de stock sont des types d'objets réutilisables.

## Ordre des octets ##

Le format Little-endian est utilisé pour stocker des données dans des enregistrements de métafichier.

## Versionnage ##

Le format de fichier EMF a été révisé deux fois. Les versions modifiées sont l'original, l'extension 1 et l'extension 2. Les versions étendues ont une disposition pour les enregistrements OpenGL et un descripteur facultatif pour le format de pixel interne. Une installation de mesure en millilitres est ajoutée pour les dimensions affichées.

## Références ##

* [Métafichiers au format amélioré | Microsoft Docs] (https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Format et spécification de métafichier améliorés](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

