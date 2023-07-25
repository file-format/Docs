{
  "date" : "2019-10-11",
  "keywords" :[ "fichier shp", "format de fichier shp", "qu'est-ce qu'un fichier shp", "fichier", "exemple shp", "extension de fichier shp","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - Fichier de formes ESRI",
  "description":"En savoir plus sur le format de fichier SHP et les API qui peuvent créer et ouvrir des fichiers SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier SHP ?

SHP est l'extension de fichier pour l'un des principaux types de fichiers utilisés pour la représentation de ESRI Shapefile. Il représente les informations géospatiales sous la forme de données vectorielles à utiliser par les applications des systèmes d'information géographique (SIG). Le format a été développé en tant que spécifications ouvertes afin de faciliter l'interopérabilité entre ESRI et d'autres produits logiciels.

## Représentation des données

Comme mentionné, un format de fichier de formes décrit les informations géospatiales d'un ensemble de données sous forme d'entités vectorielles. Ces caractéristiques vectorielles incluent :

* points
* lignes
* polygones

Ces caractéristiques combinées peuvent représenter presque tous les types de formes comme les puits d'eau, les frontières des pays, les points spatiaux, le débit des rivières, les lacs, etc. Chaque entité vectorielle peut avoir des attributs qui définissent réellement le but de cette entité. Par exemple, un fichier de formes contenant des villes de Los Angeles peut avoir le nom de la ville et la température comme attributs, ce qui donne une représentation significative aux données spatiales.

## Fichiers associés

Un fichier shp autonome ne peut pas être utilisé par des applications logicielles pour donner un sens aux données qu'il contient. Afin de donner un sens aux informations contenues dans un tel fichier, un fichier de formes utilise les fichiers obligatoires supplémentaires suivants.

* fichier shx - fichier d'index
* fichier dbf - un fichier dBASE qui stocke tous les attributs des formes dans le fichier principal
* fichier prj - stocke les informations de projet du fichier

Il peut également y avoir d'autres fichiers facultatifs qui partagent le même nom que le fichier principal.

## Spécifications du format de fichier SHP

Les spécifications ouvertes du fichier de formes sont disponibles en ligne auprès d'ESRI sous la forme de [Description technique](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) et élaborent en détail la structure globale du fichier. Les informations contenues dans le fichier .shp principal se composent d'en-têtes et d'enregistrements. L'en-tête de fichier de longueur fixe est suivi d'enregistrements de longueur variable où chaque enregistrement est constitué d'un en-tête d'enregistrement de longueur fixe suivi d'un contenu d'enregistrement de longueur variable.

### En-tête du fichier SHP principal

L'en-tête de fichier principal commence au début du fichier et a une longueur de 100 octets. L'organisation de cet en-tête de fichier principal avec la position des octets, la valeur, le type et l'ordre des octets est indiquée dans le tableau suivant.


|Octets|Champ|Valeur|Type|Ordre des octets
---|---|---|---|---|
|0-3|Code de fichier|9994|Entier|Big Endian
|4-23|Inutilisé|0|Entier|Big Endian
|24-27|Longueur du fichier|Longueur du fichier|Entier|Big Endian
|28-31|Version|1000|Entier|Little Endian
|32-35|Type de forme|Type de forme|Entier|Little Endian
|36-67|Rectangle de délimitation minimal|Xmin, Ymin, Xmax et Ymax|double|Little Endian
|68-83|Boîte englobante|Zmin, Zmax|double|Little Endian
|84-99|Boîte englobante|Mmin, Mmax|double|

Il est à noter que la valeur de la longueur du fichier est la longueur totale du fichier en mots de 16 bits qui comprend également les cinquante mots de 16 bits constituant l'en-tête.

#### Types de forme

Les valeurs du champ des types de formes dans le tableau ci-dessus sont les suivantes :


|Valeur|Type de forme
---|---|
|0|Forme nulle
|1|Point
|3|Polyligne
|5|Polygone
|8|Multipoint
|11|PointZ
|13|PolyLigneZ
|15|PolygoneZ
|18|MultiPointZ
|21|PointM
|23|PolyLigneM
|25|PolygoneM
|28|MultiPointM
|31|Multipatch

### Enregistrements de données ###

L'en-tête du fichier principal est suivi d'enregistrements de longueur variable où chaque enregistrement consiste en un en-tête d'enregistrement de longueur fixe suivi d'un contenu d'enregistrement de longueur variable.

#### En-tête d'enregistrement ####

L'en-tête d'enregistrement contient des informations sur le numéro d'enregistrement et la longueur du contenu de l'enregistrement dans une longueur fixe de 8 octets. L'organisation de l'en-tête d'enregistrement est la suivante :


|Octets|Champ|Valeur|Type|Ordre des octets
---|---|---|---|---|
|0-3|Numéro d'enregistrement|Numéro d'enregistrement|Entier|Grand
|4-7|Longueur de l'enregistrement|Longueur de l'enregistrement|Entier|Grand

#### Contenu de l'enregistrement ####

Le contenu d'un enregistrement de fichier de formes consiste en un type de forme suivi des données géométriques de cette forme. Un type de forme de 0 représente une forme nulle qui n'a pas de données géométriques pour la forme. La longueur du contenu de l'enregistrement reflète les parties et les sommets de la forme. Prenons un exemple de type de forme de point pour expliquer comment un enregistrement contient des informations sur un tel type de forme.

Un point représente un certain emplacement géographique dans l'ordre X,Y où chaque coordonnée est représentée par une valeur à double précision. Le tableau suivant montre la disposition d'un type de forme Point.


|Octets|Type de forme|Valeur|Type|Nombre|Ordre des octets
---|---|---|---|---|---|
|0-3|Type de forme|1|Entier|1|Petit
|4-11|X|X|double|1|Petit
|12-19|Y|Y|double|1|Petit

Des exemples d'autres types de formes peuvent être trouvés dans le document de description technique ESRI.

## Références ##

* [Description technique du fichier de forme ESRI](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) par ESRI

