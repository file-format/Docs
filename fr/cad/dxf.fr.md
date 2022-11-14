{
  "date" : "2020-03-16",
  "keywords" :[ "Fichier DXF", "Format de fichier", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DXF et les API qui peuvent créer et ouvrir des fichiers DXF.",
  "title" :"Format de fichier DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DXF ?

DXF, Drawing Interchange Format ou Drawing Exchange Format, est une représentation de données balisées du fichier de dessin AutoCAD. Chaque élément du fichier a un nombre entier de préfixe appelé code de groupe. Ce code de groupe représente en fait l'élément qui suit et indique la signification d'un élément de données pour un type d'objet donné. DXF permet de représenter presque toutes les informations spécifiées par l'utilisateur dans un fichier de dessin.

Le format de fichier DXF a été développé par Autodesk en tant que format de fichier de données CAO pour l'interopérabilité des données entre AutoCAD et d'autres applications. Ainsi, les données peuvent être importées d'autres formats vers DXF vers AutoCAD conformément aux spécifications d'interopérabilité du format de fichier DXF.

## Bref historique ##


L'histoire du format de fichier DXF remonte à 1982 lorsqu'il a été introduit dans le cadre d'AutoCAD 1.0. Les versions initiales d'AutoCAD ne prennent en charge que le format de fichier ASCII de DXF. Avec la version 10 d'AutoCAD (et au-dessus) en 1988, la prise en charge des formats de fichier ASCII et binaire DXF a été introduite dans AutoCAD. Au début, Autodesk ne partageait aucune spécification de format de fichier et, de ce fait, l'importation correcte de fichiers DXF n'était pas facile. Cependant, Autodesk publie désormais les spécifications DXF et les met à la disposition du grand public.

## Spécifications du format de fichier ##

Le format de fichier DXF utilise le code de groupe et les paires de valeurs pour organiser le contenu en sections. Chaque section est composée d'enregistrements où chaque enregistrement se compose d'un code de groupe et d'un élément de données. Chaque code de groupe et chaque valeur sont sur leur propre ligne dans le fichier DXF. Chaque section commence par un code de groupe 0 suivi de la chaîne SECTION. Ceci est suivi d'un code de groupe 2 et d'une chaîne indiquant le nom de la section (par exemple, SECTION1). Chaque section est composée de codes de groupe et de valeurs qui définissent ses éléments. Une section se termine par un 0 suivi de la chaîne ENDSEC.

Le format de fichier DXF considère les objets différents des entités. Les objets n'ont pas de représentation graphique ici mais les entités en ont. Ainsi, les entrées dans DXF sont appelées objets graphiques tandis que les objets objets sont appelés objets non graphiques. Les sections BLOC et ENTITES du fichier DXF contiennent des Entités et l'utilisation des codes de groupe dans ces deux sections est identique. La fin d'une entité est indiquée par le groupe 0 suivant, qui commence l'entité suivante ou indique la fin de la section.

### Structure du fichier ###

Les sections d'un fichier DXF sont organisées dans l'ordre suivant :

|Section|Description de base
---|---|
|En-tête|Cette section contient des informations générales sur le dessin. C'est comme la fonctionnalité Paramètres de votre téléphone, qui contient les différentes variables associées au dessin et ses valeurs associées. Par exemple, la section En-tête définira la version d'AutoCAD utilisée par le fichier DXF (la variable $ACADVER) ou l'unité utilisée pour mesurer les angles dans le fichier (la variable $AUNITS)
|Classes|La section CLASSES contient les informations pour les classes définies par l'application dont les instances apparaissent dans les sections BLOCKS, ENTITIES et OBJECTS de la base de données.
|Tables|Cette section contient des définitions pour plusieurs tables différentes, chacune contenant un certain nombre d'entrées de symboles différentes. Par exemple, le [type de ligne](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) (LTYPE) définit le motif des tirets, des points, du texte et des symboles dans le fichier DXF et leur mise à l'échelle. Voici une liste complète des tables trouvées dans cette section :<ul><li> Tableau des ID d'application (APPID)</li><li> Table d'enregistrements de blocs (BLOCK_RECORD)</li><li> Tableau Style de cote (TYPE DE COTES)</li><li> Tableau des couches (LAYER)</li><li> Tableau Type de ligne (LTYPE)</li><li> Tableau des styles de texte (STYLE)</li><li> Tableau du système de coordonnées utilisateur (SCU)</li><li> Voir (VOIR) le tableau</li><li> Tableau de configuration des fenêtres (VPORT)</li></ul>
|Blocs|Cette section contient les objets graphiques et les entités de dessin qui composent chaque référence de bloc dans le dessin.
|Entités|Cette section contient les données d'objet réelles et les entités graphiques du dessin. Cela peut inclure des données brutes - par exemple, une entité de cercle est définie par son épaisseur, le point central, son rayon et la direction d'extrusion.
|Objets|Ici, vous trouverez les parties non graphiques du dessin. Par exemple, les dictionnaires AutoCAD sont stockés ici.

## Références ##

* [Spécifications des fichiers DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF par Wikipédia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

