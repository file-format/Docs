{
  "date" : "2019-10-11",
  "keywords" :[ "fichier png", "format de fichier png", "qu'est-ce qu'un fichier png", "fichier", "exemple png", "extension de fichier png","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PNG - Fichier d'image raster",
  "description":"En savoir plus sur le format de fichier PNG et les API qui peuvent créer et ouvrir des fichiers PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier PNG ?

Un fichier **PNG** (Portable Network Graphics) est un format de fichier image raster qui utilise une compression sans perte. Ce format de fichier a été créé en remplacement du Graphics Interchange Format ([GIF](/fr/image/gif/)) et n'a aucune limitation de copyright. Cependant, le format de fichier PNG ne prend pas en charge les animations. Le format de fichier PNG prend en charge la compression d'image sans perte, ce qui le rend populaire parmi ses utilisateurs. Au fil du temps, PNG est devenu l'un des formats de fichiers image les plus utilisés.

## Bref historique du format de fichier PNG

La principale raison derrière la création du format de fichier PNG était l'algorithme de compression breveté, Lempel-Ziv-Welch, utilisé dans le format de fichier GIF. Ceci, ainsi que d'autres limitations GIF, a créé un besoin de remplacement du format de fichier [**GIF**](/fr/image/gif/). La première proposition et le premier nom pour le format de fichier PNG sont arrivés en janvier 1995. Les événements clés concernant les formats de fichier PNG sont répertoriés ci-dessous :

* Octobre 1996 : la version 1.0 des spécifications PNG a été publiée et est apparue plus tard sous la référence [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. La même chose est devenue une recommandation du W3C en octobre 1996.
* Décembre 1998 : La version 1.1, avec quelques petits changements et l'ajout de trois nouveaux morceaux, est sortie.
* Août 1999 : La version 1.2, ajoutant un morceau supplémentaire, est sortie.
* Novembre 2003 : PNG devient une norme internationale (ISO/IEC 15948:2003). Cette version de PNG ne diffère que légèrement de la version 1.2 et n'ajoute aucun nouveau morceau.
* Mars 2004 : ISO/CEI 15948:2004

## Comparaison fonctionnelle de GIF et PNG

Le format de fichier PNG a été conçu pour être simple et portable, juridiquement libre, interchangeable, flexible et robuste. Le tableau suivant répertorie les fonctionnalités GIF héritées par le format de fichier PNG en plus des nouvelles fonctionnalités.

|Caractéristique|GIF|PNG|
---|---|---|
|Images en couleurs d'index jusqu'à 256 couleurs|Oui|Oui|
|Prise en charge du streaming|Oui|Oui|
|Transparence|Oui|Oui|
|Informations complémentaires|Oui|Oui|
|Indépendance matérielle et plate-forme|Oui|Oui|
|En vigueur|Oui|Oui|
|Images Truecolor jusqu'à 48 bits par pixel|Non|Oui|
|Images en niveaux de gris jusqu'à 16 bits par pixel|Non|Oui|
|Canal alpha complet (masques de transparence généraux)|Non|Oui|
|Informations sur le gamma de l'image|Non|Oui|
|Fiabilité|Non|Oui|
|Présentation initiale plus rapide|Non|Oui|

## Structure des fichiers PNG

Presque tous les systèmes d'exploitation prennent en charge l'ouverture des fichiers PNG. Par exemple, la visionneuse Microsoft Windows a la capacité d'ouvrir les fichiers PNG car le système d'exploitation dispose par défaut de la prise en charge disponible dans le cadre de l'installation. Un fichier PNG se compose d'une "signature" PNG suivie d'une série de //morceaux//.

### En-tête de fichier PNG

Les huit premiers octets d'un fichier PNG contiennent toujours les valeurs (décimales) suivantes :

{{{137 80 78 71 13 10 26 10 }}}

Cette signature indique que le reste du fichier contient une seule image PNG, constituée d'une série de blocs commençant par un bloc IHDR et se terminant par un bloc IEND.

### Morceaux ###

Chaque bloc est composé de quatre parties :

**Longueur :** Un entier non signé de 4 octets indiquant le nombre d'octets dans le champ de données du segment. La longueur ne compte que le champ de données, pas lui-même, le code de type de bloc ou le CRC. Zéro est une longueur valide. Bien que les encodeurs et les décodeurs doivent traiter la longueur comme non signée, sa valeur ne doit pas dépasser 231 octets.

**Type de bloc :** Un code de type de bloc de 4 octets. Pour faciliter la description et l'examen des fichiers PNG, les codes de type sont limités aux lettres ASCII majuscules et minuscules (AZ et az, ou décimal 65-90 et 97-122). Cependant, les encodeurs et les décodeurs doivent traiter les codes comme des valeurs binaires fixes, et non comme des chaînes de caractères. Par exemple, il ne serait pas correct de représenter le code de type IDAT par les équivalents EBCDIC de ces lettres. Des conventions de nommage supplémentaires pour les types de blocs sont abordées dans la section suivante.

**Données de bloc :** Les octets de données appropriés au type de bloc, le cas échéant. Ce champ peut être de longueur nulle.

**CRC :** Un CRC (Cyclic Redundancy Check) de 4 octets calculé sur les octets précédents dans le bloc, y compris les champs de code de type de bloc et de données de bloc, mais sans le champ de longueur. Le CRC est toujours présent, même pour les blocs ne contenant aucune donnée.

La longueur des données de bloc peut être n'importe quel nombre d'octets jusqu'au maximum ; par conséquent, les implémenteurs ne peuvent pas supposer que les blocs sont alignés sur des limites supérieures à octets.

Les blocs peuvent apparaître dans n'importe quel ordre, sous réserve des restrictions imposées à chaque type de bloc. (Une restriction notable est que IHDR doit apparaître en premier et IEND doit apparaître en dernier ; ainsi le bloc IEND sert de marqueur de fin de fichier.) Plusieurs blocs du même type peuvent apparaître, mais uniquement si cela est spécifiquement autorisé pour ce type.

#### Types de blocs

Les types de blocs sont classés en blocs **critiques** et **auxiliaires** en fonction de la valeur ASCII sensible à la casse de 4 octets attribuée au type de bloc. Toutes les implémentations doivent comprendre et restituer avec succès les blocs critiques standard. Une image PNG valide doit contenir un bloc IHDR, un ou plusieurs blocs IDAT et un bloc IEND.

### Compression

La méthode de compression PNG 0 (la seule méthode de compression actuellement définie pour PNG) spécifie la compression deflate/inflate avec une fenêtre glissante d'au plus 32768 octets. La compression Deflate est un dérivé de LZ77 utilisé dans les programmes zip, gzip, pkzip et associés. Des recherches approfondies ont été effectuées à l'appui de son statut sans brevet. Les données compressées dans le flux de données zlib sont stockées sous la forme d'une série de blocs, chacun pouvant représenter des données brutes (non compressées), des données compressées LZ77 codées avec des codes Huffman fixes ou des données compressées LZ77 codées avec des codes Huffman personnalisés. Un bit marqueur dans le bloc final l'identifie comme le dernier bloc, permettant au décodeur de reconnaître la fin du flux de données compressé.

#### Filtrage de pré-compression

Des filtres de pré-compression sont appliqués pour préparer les données d'image pour une compression optimale. La méthode de filtre PNG définit cinq types de filtres de base comme suit :

|Type de filtre|Nom|Valeur prévue|
---|---|---|
|0|Aucun|La ligne de balayage est transmise sans modification|
|1|Sub|Transmet la différence entre chaque octet et la valeur de l'octet correspondant du pixel précédent.|
|2|Up|Le filtre Up() est comme le filtre Sub() sauf que le pixel immédiatement au-dessus du pixel actuel, plutôt que juste à sa gauche, est utilisé comme prédicteur.|
|3|Moyenne|Le filtre Moyenne() utilise la moyenne des deux pixels voisins (gauche et supérieur) pour prédire la valeur d'un pixel.|
|4|Paeth|Le filtre Paeth() calcule une simple fonction linéaire des trois pixels voisins (gauche, haut, haut gauche), puis choisit comme prédicteur le pixel voisin le plus proche de la valeur calculée.|

Les algorithmes de filtrage sont appliqués aux "octets", et non aux pixels, quelle que soit la profondeur de bits ou le type de couleur de l'image. Les algorithmes de filtrage fonctionnent sur la séquence d'octets formée par une ligne de balayage. Si l'image comprend un canal alpha, les données alpha sont filtrées de la même manière que les données d'image.

Lorsque l'image est entrelacée, chaque passage du motif entrelacé est traité comme une image indépendante à des fins de filtrage. Les filtres travaillent sur les séquences d'octets formées par les pixels réellement transmis lors d'un passage, et la "ligne de balayage précédente" est celle transmise précédemment dans le même passage, et non celle adjacente dans l'image complète. Notez que la sous-image transmise en une seule passe est toujours rectangulaire, mais a une largeur et/ou une hauteur plus petite que l'image complète. Le filtrage n'est pas appliqué lorsque cette sous-image est vide.

## Références ##

* [PNG - Page d'accueil](http://www.libpng.org/pub/png/)

