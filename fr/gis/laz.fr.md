{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Fichier d'échange de données LIDAR compressé",
  "description":"Découvrez le format de fichier LAZ et les API permettant de créer et d'ouvrir des fichiers LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Qu'est-ce qu'un fichier LAZ ?

Le format de fichier LAZ est une version compressée du format de fichier LAS (Lidar LASer), spécialement conçu pour stocker les données de nuages de points lidar. Les fichiers LAZ conservent les mêmes données et la même structure que les fichiers LAS, mais utilisent des techniques de compression sans perte pour réduire la taille du fichier tout en préservant la fidélité des données d'origine.

## Format de fichier LAZ – Bref historique

Le format de fichier LAZ a été développé pour répondre à la demande croissante de stockage et de transmission efficaces de grands ensembles de données lidar. En compressant les fichiers LAS, les fichiers LAZ réduisent considérablement leur taille, ce qui les rend plus faciles à gérer et à transférer. La compression est obtenue en utilisant une combinaison de différents algorithmes, tels que le codage entropique et le codage à longueur variable, pour représenter les attributs des points lidar sous une forme plus compacte.

## Format de fichier LAZ

Malgré la compression, les fichiers LAZ conservent la capacité de restaurer entièrement les données LAS d'origine sans aucune perte d'informations. Cela signifie qu'une fois qu'un fichier LAZ est décompressé, il peut être traité et analysé de la même manière qu'un fichier LAS non compressé. Le processus de compression et de décompression est généralement effectué à l'aide de logiciels spécialisés ou de bibliothèques prenant en charge le format LAZ.

Le format de fichier LAZ maintient la compatibilité avec les fichiers LAS, garantissant l'interopérabilité entre les logiciels lidar et les outils de traitement. Cela signifie que les applications capables de lire et de traiter les fichiers LAS peuvent généralement gérer les fichiers LAZ sans aucune modification. De plus, les fichiers LAZ incluent toujours l'en-tête du fichier, les enregistrements de longueur variable (VLR) et les enregistrements de données ponctuelles, préservant la même structure que les fichiers LAS.

## Avantages du format de fichier LAZ

**Taille de fichier réduite :** La compression LAZ réduit considérablement la taille des fichiers des ensembles de données lidar, les rendant plus faciles à gérer et à stocker et à transférer.

**Intégrité des données :** La compression LAZ est sans perte, ce qui signifie que les données décompressées sont une réplique exacte des données LAS d'origine, garantissant ainsi l'absence de perte d'informations ou de précision.

**Interopérabilité :** les fichiers LAZ sont compatibles avec les fichiers LAS, permettant une intégration transparente avec les logiciels et flux de travail lidar existants.

**Traitement efficace :** En raison de leur taille réduite, les fichiers LAZ peuvent être chargés et traités plus rapidement, améliorant ainsi les temps globaux de traitement et d'analyse.

Le format de fichier LAZ est devenu largement adopté par la communauté lidar comme norme pour le stockage et l'échange de données lidar compressées. Il offre un équilibre entre une compression efficace des données et leur intégrité, permettant une gestion plus facile de grands ensembles de données lidar tout en conservant la précision et la qualité des données d'origine.

## Les références

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
