{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Format de fichier Lidar LASer",
  "description":"Découvrez le format de fichier LAS et les API permettant de créer et d'ouvrir des fichiers LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Qu'est-ce qu'un fichier LAS ?

Le format de fichier LAS (Lidar LASer) est un format de fichier binaire spécialement conçu pour stocker les données de nuages de points lidar. Il a été développé et est maintenu par l'American Society for Photogrammetry and Remote Sensing (ASPRS) en tant que format standardisé pour l'échange et l'interopérabilité des données lidar.

Les fichiers LAS stockent des informations détaillées sur les points lidar individuels, y compris leurs coordonnées 3D (x, y et z), les valeurs d'intensité, les codes de classification et des attributs supplémentaires. Le format prend en charge à la fois les données lidar à retour discret et à forme d'onde complète, permettant le stockage de plusieurs retours par impulsion laser.

## Format de fichier LAS

La structure d'un fichier LAS se compose de trois sections principales : l'en-tête du fichier, les enregistrements de longueur variable (VLR) et les enregistrements de données ponctuelles.

1. En-tête de fichier : l'en-tête de fichier contient des informations essentielles sur le fichier LAS, telles que la version du format de données, le format de données de point, le nombre de points, les coordonnées du cadre de délimitation, le système de référence de coordonnées (CRS) et d'autres métadonnées. Il fournit un résumé des données lidar contenues dans le fichier.

2. Enregistrements de longueur variable (VLR) : les VLR sont facultatifs et peuvent stocker des métadonnées supplémentaires et des informations personnalisées sur les données lidar. Les VLR permettent une certaine flexibilité dans l'extension du format pour répondre aux besoins spécifiques des utilisateurs. Des exemples de VLR incluent des informations sur le système de capteurs, les paramètres de traitement des données ou les schémas de classification.

3. Enregistrements de données ponctuelles : les enregistrements de données ponctuelles stockent les mesures lidar réelles. Chaque enregistrement de données de point représente un seul point lidar et contient des attributs tels que les coordonnées x, y et z, les valeurs d'intensité, les codes de classification (par exemple, sol, végétation, bâtiments) et d'autres attributs définis par l'utilisateur. Les enregistrements de points peuvent également stocker des horodatages, des décomptes de retours et des angles de balayage.

Les fichiers LAS prennent en charge différents formats de données (0 à 10) pour s'adapter à différents types de données lidar et au niveau d'informations requis. Par exemple, le format 0 représente un format de point simple avec des informations de base, tandis que les formats 1 à 3 fournissent des données plus complètes, notamment des informations sur la forme d'onde pour chaque retour.

Les fichiers LAS sont largement pris en charge par les logiciels et les outils de traitement lidar, ce qui en fait un format standard pour l'échange et l'analyse de données lidar. De plus, les fichiers LAS peuvent être compressés à l'aide de techniques de compression sans perte pour réduire la taille du fichier tout en préservant la fidélité des données d'origine. La version compressée des fichiers LAS est souvent appelée LAZ, qui offre des capacités efficaces de stockage et de transfert de données.

## Les références

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
