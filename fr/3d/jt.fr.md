{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "fichier", "extension", "format", "fbx 3D", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier JT et les API qui peuvent créer et ouvrir des fichiers JT.",
  "title" :"JT - Format de fichier de tessellation Jupiter",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier JT ?

**JT** (Jupiter Tessellation) est un format de données 3D normalisé ISO efficace, flexible et axé sur l'industrie, développé par Siemens PLM Software. Les domaines de la CAO mécanique de l'aérospatiale, de l'industrie automobile et de l'équipement lourd utilisent JT comme format de visualisation 3D le plus utilisé.

Le format JT est un graphe de scène qui prend en charge les attributs et les nœuds spécifiques à la CAO. Des techniques de compression sophistiquées sont utilisées pour stocker les données de facettes (triangles). Ce format est structuré pour prendre en charge les attributs visuels, les informations sur les produits et la fabrication (PMI) et les métadonnées. Il existe un bon support pour le streaming asynchrone de contenu. Dans l'industrie mécanique lourde, les professionnels utilisent le fichier JT dans leurs solutions de CAO et leurs logiciels de gestion du cycle de vie des produits (PLM) pour examiner la géométrie de produits complexes.

Comme JT prend en charge presque tous les formats CAO 3D importants, son assemblage peut traiter une variété de combinaisons appelées "multi-CAO". Cet assemblage multi-CAO est toujours bien géré et à jour car la synchronisation entre les fichiers natifs de description des produits CAO avec leurs fichiers JT associés s'effectue automatiquement. Les fichiers JT sont à l'origine légers, donc considérés comme adaptés aux collaborations sur Internet. Les entreprises collaborent en envoyant des visualisations 3D sur le support beaucoup plus facilement par rapport aux fichiers CAO originaux "lourds". De plus, les fichiers JT garantissent de nombreuses fonctionnalités de sécurité qui rendent le partage de la propriété intellectuelle plus sécurisé.

## Bref historique du format de fichier JT

Engineering Animation, Inc. et Hewlett Packard étaient les concepteurs originaux de JT, qui ont développé ce format en tant que boîte à outils Direct Model. Après l'acquisition d'EAI par UGS Corp. JT est devenu une partie de la suite d'UGS. Au début de 2007, UGS a annoncé JT comme son format 3D principal. La même année, Siemens AG a acheté UGS et s'est avéré être Siemens PLM Software. Siemens utilise JT comme format d'interopérabilité commun et format d'archivage des données. En 2009, l'ISO a accepté la spécification JT pour publication en tant que spécification ISO publiquement disponible (PAS). Au milieu de 2010, ProSTEP iViP a annoncé qu'au niveau industriel, JT et STEP AP 242 XML peuvent être utilisés ensemble pour obtenir le maximum d'avantages dans les données. scénarios d'échange. En 2012, JT a été officiellement déclaré format de visualisation 3D normalisé ISO (ISO 14306:2012 (ISO JT V1)).

## Format de fichier JT ##

Tous les objets au format JT sont représentés par un identifiant d'objet et les références entre les objets sont gérées par l'identifiant de l'objet référencé. L'intégrité de ces références d'objet peut être maintenue par des pointeurs unswizzling/swizzling.

Un fichier JT est organisé en une série de blocs et le bloc d'en-tête est toujours le premier bloc de données du fichier. Une série de segments de données et un segment TOC suivent immédiatement le bloc d'en-tête. Le seul segment de données (segment 6 LSG) possède un fichier JT conforme à la référence existe toujours. Le segment TOC contient les informations d'emplacement de tous les autres segments de données de ce fichier.

{{< figure src="../JT-1.png" alt="Format de fichier JT" >}}

### En-tête de fichier ###

L'en-tête de fichier est le premier bloc de la hiérarchie des données du fichier JT. Les informations de version et les informations d'emplacement de la table des matières sont incluses dans l'en-tête, ce qui facilite la lecture des fichiers par les chargeurs. Le contenu de l'en-tête de fichier est organisé comme suit.

### Segment de table des matières ###

Le segment TOC doit exister dans un fichier et contient des informations d'identification et d'emplacement de tous les autres segments de données. L'emplacement réel du segment TOC est spécifié par le champ TOC Offset de l'en-tête du fichier. Chaque segment de données adressable individuellement est représenté par une entrée TOC dans un segment TOC.

### Segment de données ###

Le fichier JT définit toutes les données stockées dans un segment de données. Certains segments de données peuvent compresser tous les octets de données d'informations restés dans le segment. Les segments de données ont la structure suivante :

![alt text](../JT-2.png "JT Data Segment")

Le tableau suivant décrit différents types de segments de données :

|Nom|Description
---|---|
|Segment LSG|Comprend une collection d'objets liés par des références dirigées pour former LSG (structure de graphe acyclique dirigée)
|Shape LOD segment|contient les données de définition des formes géométriques (par exemple, sommets, normales, polygones, etc.)
|Segment JT B-Rep|Avec un élément pour que les données représentent la limite géométrique précise d'une portion individuelle au format JT B-Rep.
|Segment XT B-Rep|Avoir un élément pour que les données représentent la limite géométrique précise d'une portion individuelle au format de représentation des limites
|Segment filaire|Les données représentent une image filaire 3D précise pour une portion particulière définie par un élément contenu dans ce segment.
|Segment de métadonnées|Permet de stocker les métadonnées dans des segments adressables distincts.
|Segment JT ULP|Comportant un élément pour que les données représentent la limite géométrique semi-précise d'une portion individuelle au format JT ULP.
|Segment JT LWPA|Contient un élément définissant les données analytiques d'une pièce particulière. LWPA inclut la collection de surfaces analytiques dans la définition b-rep de la pièce.

## Compression ##

Les exigences de transmission et de stockage des modèles 3D sont plus exigeantes, de sorte que les fichiers JT peuvent bénéficier de la compression. Un modèle de données JT peut être composé de différents fichiers utilisant différentes techniques de compression, mais le processus de compression est transparent pour l'utilisateur des données JT.

Jusqu'à présent, JT Open Toolkit (en standard) et la compression avancée sont deux techniques de compression utilisées par les fichiers JT. JT Open Toolkit utilise un algorithme de compression simple et sans perte, tandis que la compression avancée utilise une technique de compression plus raffinée et spécifique au domaine qui conduit à une compression géométrique avec perte. Les applications clientes préfèrent la compression avancée plutôt que l'utilisation de la compression standard, car la compression avancée donne des taux de compression assez élevés. La rétrocompatibilité avec les applications de visualisation de fichiers JT ordinaires est maintenue grâce à la fourniture d'une compression standard. Le formulaire de compression doit être compatible avec la version du format de fichier JT qui peut être vue lorsqu'un fichier JT s'ouvre à l'aide de l'éditeur de texte et inclus dans les informations d'en-tête ASCII.

## Références ##

* [Référence du format de fichier JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (format de visualisation)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)

