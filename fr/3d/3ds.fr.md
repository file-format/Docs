{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","fichier", "format", "type de fichier", "extension","qu'est-ce qu'un fichier 3DS ?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier 3DS et les API qui peuvent ouvrir et créer des fichiers 3DS.",
  "title" :"Format de fichier 3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier 3DS ?

Un fichier avec l'extension .3ds représente le format de fichier de maillage 3D Sudio (DOS) utilisé par Autodesk 3D Studio. Autodesk 3D Studio est présent sur le marché des formats de fichiers 3D depuis les années 1990 et a maintenant évolué vers 3D Studio MAX pour travailler avec la modélisation, l'animation et le rendu 3D. Un fichier 3DS contient des données pour la représentation 3D de scènes et d'images et est l'un des formats de fichiers populaires pour l'importation et l'exportation de données 3D. Il prend en compte des informations telles que les emplacements des caméras, les données de maillage, les informations d'éclairage, les configurations de fenêtres, les données de groupe de lissage, les références bitmap et les attributs pour créer des sommets et des polygones pour le rendu d'une scène.

## Format de fichier 3DS - Plus d'informations
À sa base, 3DS est un format de fichier binaire et suit une structure prédéfinie pour stocker et récupérer des données. Le format de fichier binaire permet au format de fichier 3DS d'être plus rapide et plus petit par rapport aux formats de fichier texte. Les données à l'intérieur d'un fichier 3DS sont stockées sous la forme de morceaux.

### Bloc 3DS

Chaque morceau dans un fichier 3DS est un bloc de données qui contient un ID, la longueur du bloc pour l'emplacement du bloc suivant et les données elles-mêmes. L'ID de bloc permet aux lecteurs de format de fichier 3DS d'ignorer les blocs qu'ils ne reconnaissent pas. Cela aide également à l'extensibilité du format. Chaque bloc stocke des informations relatives aux formes, à l'éclairage et aux informations de visualisation qui, ensemble, rendent la scène. Les morceaux sont disposés dans une structure hiérarchique dans un fichier 3DS et ressemblent à une arborescence d'objets de document XML dans la représentation.

**Identifiant de bloc :** Les deux premiers octets d'un bloc représentent un identifiant de bloc qui permet au lecteur de fichier de décider de le prendre en compte lors de la lecture ou de l'ignorer.

**Longueur du bloc :** L'identifiant du bloc est suivi d'un entier de 4 octets (en petit-boutiste) qui représente la longueur du bloc. Cette longueur comprend également la longueur des données, la longueur de ses sous-blocs et l'en-tête de 6 octets.

**Charge utile :** La longueur du bloc est suivie des octets réels de données pour le bloc, suivis de ses sous-blocs dans la même structure hiérarchique qui peut être étendue à plusieurs niveaux de profondeur.

### Structure d'un bloc

La structure hiérarchique d'un morceau simple est comme indiqué ci-dessous :

**Un morceau**

|début|fin|taille|nom
--- | --- | --- | ---
|0|1|2|ID de bloc
|2|5|4|Bloc suivant

Les blocs ont une hiérarchie qui leur est imposée et qui est identifiée par son ID. Un fichier 3ds a l'ID de bloc principal 4D4Dh. Il s'agit toujours du premier morceau du fichier. Avec dans le morceau principal se trouvent les morceaux principaux.

** Principaux morceaux **

|id|Description
--- | ---
|3D3D|Début des données de maillage d'objet.
|B000|Début des données keyframer.

Le pointeur Next Chunk après le bloc ID pointe vers le morceau Main suivant.
Directement après un morceau principal se trouve un autre morceau. Il peut s'agir de tout autre type de bloc autorisé dans sa portée principale.
Pour la description du maillage (3D3D), il peut s'agir de n'importe quel multiple de.

**Sous-blocs de 3D3D - Mesh Block**


|id|Description
--- | ---
|1100|inconnu
|1200|Couleur de fond.
|1201|inconnu
|1300|inconnu
|1400|inconnu
|1420|inconnu
|1450|inconnu
|1500|inconnu
|2100|Bloc de couleur ambiante
|2200|brouillard ?
|2201|brouillard ?
|2210|brouillard ?
|2300|inconnu
|3000|inconnu
|4000|Bloc objet
|7001|inconnu
|AFFF|inconnu

**Sous-blocs de 4000 - Bloc de description d'objet**
Le premier élément de Subchunk 4000 est une chaîne ASCIIZ du nom des objets.
N'oubliez pas qu'un objet peut être un maillage, une lumière ou une caméra.

|id|Description
--- | ---
|4010|inconnu
|4012|ombre ?
|4100|Objet polygone triangulaire
|4600|Lumière
|4700|Caméra

## Références

* [Formats de fichier de géométrie - Autodesk] (https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - Par Wikipédia](https://en.wikipedia.org/wiki/.3ds)
