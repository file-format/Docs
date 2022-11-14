{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Format de fichier", "CAO", "Ouvrir", "Créer" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DWG et les API permettant de créer et d'ouvrir des fichiers DWG.",
  "title" :"Format de fichier DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DWG ?

Les fichiers avec l'extension DWG représentent des fichiers binaires propriétaires utilisés pour contenir des données de conception 2D et 3D. Comme DXF, qui sont des fichiers ASCII, DWG représente le format de fichier binaire pour les dessins CAO (conception assistée par ordinateur). Il contient des images vectorielles et des métadonnées pour la représentation du contenu des fichiers CAO. Des visualiseurs gratuits sont disponibles pour visualiser les fichiers DWG sur le système d'exploitation Windows, tels que le DWG TrueView gratuit d'Autodesk. Il existe également d'autres applications tierces qui prennent en charge l'accès aux fichiers DWG. Les fichiers DWG contiennent des informations créées par l'utilisateur et incluent :

* Dessins
* Données géométriques
* Cartes et photos

Ce format est largement utilisé par les architectes, les ingénieurs et les concepteurs à diverses fins de conception.

## Bref historique ##

Le format de fichier DWG a évolué avec le temps depuis son introduction officielle en 1982. Un bref aperçu des événements passés du point de vue de l'histoire est le suivant.

**1982 :** Autodesk a autorisé le format de fichier DWG , qui a été développé par Mike Riddle en 1970, comme base d'AutoCAD.

**1998 :** Avec la sortie d'AutoCAD R14.01, Autodesk a ajouté la vérification des fichiers via une fonction appelée DWGCHECK qui intégrait une somme de contrôle chiffrée et un code produit, appelé WaterMark par Autodesk, dans les fichiers DWG créés par le programme.

**2006 :** Autodesk a modifié AutoCAD 2007 pour inclure la "technologie TrustedDWG" afin d'intégrer la chaîne de texte "Autodesk DWG. Ce fichier est un fichier DWG de confiance enregistré en dernier par une application Autodesk ou une application sous licence Autodesk" dans les fichiers DWG. Le but était d'aider les utilisateurs de logiciels Autodesk à s'assurer que ces fichiers ont été créés par une application Autodesk ou RealDWG, ce qui devrait certainement aider à réduire le risque d'incompatibilités.

## Structure du fichier ##

DWG a été l'un des formats de fichiers les plus utilisés par une gamme d'applications et possède une structure de fichier robuste. Étant donné que DWG est un format de fichier binaire, il n'est pas lisible par l'homme comme le format de fichier ASCII [DXF](/fr/cad/dxf/). Les fichiers DWG incluent généralement des informations sur les coordonnées de l'image et toutes les métadonnées qui y sont associées. Les [spécifications] complètes (https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) du format de fichier DWG sont disponibles au téléchargement par OpenDesign. La structure de fichier du format de fichier DWG est résumée comme suit.

**En-tête** : l'en-tête du fichier se compose de variables d'en-tête DWG et d'informations sur le contrôle de redondance cyclique (CRC) qui est utilisé pour la détection des erreurs. Chaque sous-section est un vecteur spécialisé dans lequel différentes longueurs de bits sont utilisées pour représenter différentes étiquettes. Par exemple, les 6 premiers bits de la variable d'en-tête DWG représentent la chaîne de version.

**Définitions de classes :** Un fichier DWG peut contenir de nombreuses classes en fonction de l'objectif spécifique du fichier .dwg. Des informations telles que la taille des métadonnées de classe de la zone de données de classe, le numéro de classe et la somme de contrôle en plus d'autres.

**Modèle** : Ceci est facultatif et pour les versions R15 et R15, cette section se trouve sous la section Espace libre d'objet.

**Remplissage** : les métadonnées sont suffixées et postfixées avec un nombre spécifique d'octets, ce qui rend les anciennes versions du logiciel AutoCAD compatibles avec le nouveau format de fichier DWG.

**Données d'image** : les métadonnées de cette section dépendent du type .dwg spécifique. Pour les utilisateurs R14 et R15, cette section est facultative.

**Données d'objet** : les données d'objet consistent en une liste complète d'entités de table, d'entrées de dictionnaire, etc. correspondant à la liste d'objets existante.

**Object Map** : l'emplacement de chaque objet dans le fichier est spécifié dans cette section du fichier. La plupart des métadonnées de cette section sont des descripteurs de fichiers qui jouent un rôle dans l'identification et le re-rendu de l'objet.

**Espace libre d'objets** : cette section est facultative pour tous les utilisateurs

**Deuxième en-tête** : un doublon de la section d'en-tête de fichier vers la fin du fichier DWG

## Références ##

* [Spécifications du format de fichier DWG] (https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [La spécification du fichier DWG](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - Par Wikipédia](https://en.wikipedia.org/wiki/.dwg)

