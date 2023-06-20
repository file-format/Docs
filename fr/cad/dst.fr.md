{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "fichier", "format", "extension", "API", "Jeu de feuilles AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - Fichier de jeu de feuilles AutoCAD",
  "description" :"En savoir plus sur le fichier .dst et les API qui peuvent créer et ouvrir des fichiers DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Qu'est-ce qu'un fichier DST ?

Un fichier DST est un fichier AutoCAD qui contient des associations et des informations permettant de définir des jeux de feuilles. Ceux-ci sont stockés dans le dossier de stockage des jeux de feuilles par défaut, Jeux de feuilles AutoCAD. Les fichiers DST ne contiennent pas les dispositions de dessin réelles, mais font référence à celles-ci à partir des fichiers [DWG](/fr/cad/dwg/) et [DWT](/fr/cad/dwt/) sélectionnés associés à ces jeux de feuilles. Dans un environnement réseau, tous les membres de l'équipe doivent avoir un accès réseau à ces fichiers associés. Les fils DST sont enregistrés sur le disque au format de fichier [XML](/fr/web/xml/).

## Format de fichier DST - Plus d'informations

Les fichiers DST sont créés avec l'outil AutoDesk Sheet Set Manager (SSM). Lorsqu'un membre de l'équipe accède à un fichier, le fichier DST est brièvement ouvert, puis stocké avec les informations mises à jour. L'accès simultané au même fichier DST est géré par l'outil SSM qui affiche une icône de verrouillage lorsque le fichier est en accès.

À tout moment, l'état de la feuille peut être dans l'un des états suivants.

* La feuille est disponible pour l'édition.
* La feuille est verrouillée.
* La feuille est manquante ou trouvée dans un emplacement de dossier inattendu.

## Références

* [À propos de l'utilisation des jeux de feuilles DST](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [En savoir plus sur les jeux de feuilles](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Maîtriser les jeux de feuilles AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

