{
  "date" : "2019-10-11",
  "keywords" :[ "fichier tiff", "format de fichier tiff", "qu'est-ce qu'un fichier tiff", "fichier", "exemple tiff", "extension de fichier tiff","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Format de fichier image",
  "description":"En savoir plus sur le format de fichier TIFF et les API qui peuvent créer et ouvrir des fichiers TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier TIFF ?

TIFF ou TIF, Tagged Image File Format, représente des images raster destinées à être utilisées sur une variété d'appareils conformes à cette norme de format de fichier. Il est capable de décrire des données d'image à deux niveaux, en niveaux de gris, en palette de couleurs et en couleurs dans plusieurs espaces colorimétriques. Il prend en charge les schémas de compression avec perte et sans perte pour choisir entre l'espace et le temps pour les applications utilisant le format. Le format ne dépend pas de la machine et est exempt de limites telles que le processeur, le système d'exploitation ou les systèmes de fichiers.

## Bref historique du format de fichier TIFF

Le format de fichier TIFF a été initialement créé par Aldus Corporation à l'automne 1986, après une série de réunions avec divers fabricants de scanners et développeurs de logiciels. L'objectif principal du format de fichier TIFF était de fournir un format de fichier d'image numérisée commun pour tous les fournisseurs de scanners de bureau. En commençant par la prise en charge du format d'image binaire uniquement, le format a évolué vers la prise en charge des images en niveaux de gris et en couleur au fil du temps. La version initiale des spécifications du format de fichier TIFF peut être étiquetée comme Reivision 3.0 car il y avait deux versions préliminaires antérieures. Une révision majeure 5.0 a été publiée en 1988 qui a ajouté la prise en charge des images de couleur de palette et de la compression LZW. La révision 6.0 des formats de fichiers TIFF a été publiée en 1992 par la suite. En 1994, Adobe Systems a acquis Aldus et les spécifications sont maintenant disponibles et maintenues par Adobe Systems.

## Spécifications du format de fichier TIFF

Le format de fichier TIFF est extensible et a subi plusieurs révisions qui permettent l'inclusion d'une quantité illimitée d'informations privées ou à usage spécial. Un fichier TIFF commence par un en-tête de 8 octets où les octets sont numérotés de 0 à N. Le plus grand fichier TIFF possible a une longueur de 2**32 octets. Le fichier commence par un en-tête de fichier image de 8 octets qui pointe directement vers un fichier image (IFD). Un IFD contient des informations sur l'image ainsi que des pointeurs vers les données d'image réelles.

### En-tête de fichier TIFF

L'en-tête du fichier TIFF de 8 octets contient les informations suivantes :

**Octets 0-1 :** L'ordre des octets utilisé dans le fichier. Les valeurs légales sont : « II » (4949.H) « MM » (4D4D.H).

Dans le format « II », l'ordre des octets va toujours de l'octet le moins significatif à l'octet le plus significatif, pour les entiers 16 bits et 32 bits. C'est ce qu'on appelle l'ordre des octets little-endian. Dans le format « MM », l'ordre des octets est toujours du plus significatif au moins significatif, pour les entiers 16 bits et 32 bits. C'est ce qu'on appelle l'ordre des octets gros-boutien.

**Octets 2-3 :** Un nombre arbitraire mais soigneusement choisi (42) qui identifie davantage le fichier en tant que fichier TIFF. L'ordre des octets dépend de la valeur des octets 0-1.

**Octets 4-7 :** Le décalage (en octets) du premier IFD. Le répertoire peut se trouver à n'importe quel endroit du fichier après l'en-tête, mais doit commencer sur une limite de mot. En particulier, un répertoire de fichiers d'images peut suivre les données d'image qu'il décrit. Les lecteurs doivent suivre les pointeurs partout où ils peuvent mener. Le terme décalage d'octet est toujours utilisé dans ce document pour désigner un emplacement par rapport au début du fichier TIFF. Le premier octet du fichier a un décalage de 0.

### Répertoire des fichiers d'images

Un IFD contient des informations sur l'image ainsi que des pointeurs vers les données d'image réelles. , suivi d'un décalage de 4 octets du prochain IFD (ou 0 s'il n'y en a pas). Il doit y avoir au moins 1 IFD dans un fichier TIFF et chaque IFD doit avoir au moins une entrée.

#### Entrée IFD

Chaque entrée IFD de 12 octets est au format suivant.


|Octets|Description
---|---|
|0-1|Le Tag qui identifie le champ
|2-3|Le type de champ
|4-7|Compte du type indiqué
|8-11|Le décalage de valeur, le décalage de fichier (en octets) de la valeur pour le champ. La valeur doit commencer sur une limite de mot ; le décalage de valeur correspondant sera donc un nombre pair. Ce décalage de fichier peut pointer n'importe où dans le fichier, même après que les données d'image

Un champ TIFF est une entité logique composée d'une balise TIFF et de sa valeur. Ce concept logique est implémenté comme une entrée IFD, plus la valeur réelle si elle ne rentre pas dans la partie valeur/décalage, les 4 derniers octets de l'entrée IFD. Les termes champ TIFF et entrée IFD sont interchangeables dans la plupart des contextes.

### TIFF de base ###

Le TIFF de base est le cœur du TIFF, les éléments essentiels que tous les développeurs TIFF traditionnels devraient prendre en charge dans leurs produits. La conformité au format TIFF est soumise au respect des exigences TIFF de base. Ces exigences sont bien documentées dans le document de spécifications 6.0.

#### Plusieurs images par fichier ####

Il peut y avoir plus d'un IFD dans un fichier TIFF. Chaque IFD définit un sous-fichier. Une utilisation potentielle des sous-fichiers est de décrire des images liées, telles que les pages d'une transmission par télécopie. Un lecteur TIFF de base n'est pas nécessaire pour lire les IFD au-delà du premier.

#### Types d'images ####

L'image TIFF de base a les types suivants :

**Biniveau :** Une image à deux niveaux contient deux couleurs, le noir et le blanc. TIFF permet à une application d'écrire des données à deux niveaux dans un format blanc est zéro ou noir est zéro. Le champ qui enregistre ces informations s'appelle **PhotometricInterpretation**.

* RVB polychrome

Les informations d'interprétation photométrique pour les images Bilevel sont les suivantes :

Balise = 262 (106.H)
Tapez = COURT
**Valeurs**

|Valeur|Description|
---|---|
|0|Pour les images à deux niveaux et niveaux de gris : 0 est représenté en blanc. La valeur maximale est représentée en noir. C'est la valeur normale pour Compression#2|
|1|NoirEstZéro. Pour les images à deux niveaux et niveaux de gris : 0 correspond à une image noire. La valeur maximale est représentée en blanc. Si cette valeur est spécifiée pour Compression#2, l'image doit s'afficher et s'imprimer à l'envers.|

**Niveaux de gris :** Les images en niveaux de gris sont une généralisation des images à deux niveaux. Les images à deux niveaux ne peuvent stocker que des données d'image en noir et blanc, mais les images en niveaux de gris peuvent également stocker des nuances de gris. Pour décrire de telles images, vous devez ajouter ou modifier les champs suivants. Les autres champs obligatoires sont les mêmes que ceux requis pour les images à deux niveaux. Pour les images en niveaux de gris, Compression # 1 ou 32773 (PackBits). Dans Baseline TIFF, les images en niveaux de gris peuvent être stockées sous forme de données non compressées ou compressées avec l'algorithme PackBits.

Les informations **BitsPerSample** pour les images en niveaux de gris sont les suivantes :

Balise = 258 (102.H)
Tapez = COURT

Le nombre de bits par composant. Les valeurs autorisées pour les images en niveaux de gris TIFF de base sont 4 et 8, autorisant 16 ou 256 nuances de gris distinctes.

**Palette-Color :** Les images en palette de couleurs sont similaires aux images en niveaux de gris. Ils ont toujours un composant par pixel, mais la valeur du composant est utilisée comme index dans une table de recherche RVB complète. Pour décrire de telles images, vous devez ajouter ou modifier les champs suivants. Les autres champs obligatoires sont les mêmes que ceux des images en niveaux de gris.
Les informations d'interprétation photométrique pour l'image Palette-Color sont les suivantes :

Interprétation photométrique = 3 (palette de couleurs).
ColorMapTag = 320 (140.H)
Tapez = COURT
N = 3 * (2 bits par échantillon)

Ce champ définit une palette de couleurs Rouge-Vert-Bleu (souvent appelée table de correspondance) pour les images en couleurs de la palette. Dans une image de palette de couleurs, une valeur de pixel est utilisée pour indexer dans une table de recherche RVB. Par exemple, un pixel de couleur de palette ayant une valeur de 0 serait affiché selon le 0ème triplet Rouge, Vert, Bleu. Dans une ColorMap TIFF, toutes les valeurs de Rouge viennent en premier, suivies des valeurs de Vert, puis des valeurs de Bleu. Dans la ColorMap, le noir est représenté par 0,0,0 et le blanc est représenté par 65535, 65535, 65535.

**Couleurs RVB :** Dans une image RVB, chaque pixel est composé de trois composants : rouge, vert et bleu. Il n'y a pas de ColorMap. Pour décrire une image RVB, vous devez ajouter ou modifier les champs et valeurs suivants. Les autres champs obligatoires sont les mêmes que ceux requis pour les images en palette de couleurs.

Bits par échantillon = 8,8,8. Chaque composant a une profondeur de 8 bits dans une image RVB TIFF de base.

Interprétation photométrique = 2 (RVB) et il n'y a pas de ColorMap.

Balise = 277 (115.H)
Tapez = COURT
Le nombre de composants par pixel. Ce nombre est 3 pour les images RVB, sauf si des échantillons supplémentaires sont présents.

## Références ##

* [Format de fichier TIFF - Wikipédia](https://en.wikipedia.org/wiki/TIFF)

