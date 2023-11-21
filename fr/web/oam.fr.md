{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier OAM - Format de fichier du widget Adobe Edge Animate",
  "description" :"Découvrez ce qu'est un fichier OAM et les API qui peuvent créer et ouvrir un fichier OAM.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Qu'est-ce qu'un fichier OAM ?

Un fichier .oam et un fichier de widget animé exporté depuis Adobe Edge Animate Widget. Les animations exportées au format de fichier de widget OAM peuvent être insérées dans d'autres applications Adobe telles que InDesign Documents ([fichier INDD](/fr/page-description-langue/indd/), Dreamweaver et Muse. Les fichiers OAM sont comme des packages de déploiement qui peuvent être facilement inséré dans d'autres projets Adobe pour les utiliser. Les fichiers OAM contiennent des informations sur les ressources, les comportements et le code ActionScript de l'animation. Vous pouvez créer un fichier OAM en publiant un projet Adobe Animate [fichier .AN] (/fr/web/an/) .
Les utilisateurs peuvent créer des fichiers OAM en publiant à partir d'un projet Edge Animate (fichier .AN).

## Format de fichier OAM

Un fichier OAM est enregistré sur le disque sous forme d'archive compressée [ZIP](/fr/compression/zip/). Cela implique que vous pouvez renommer l'extension du fichier en .zip et l'extraire avec n'importe quel utilitaire de compression tel que WinZIP ou WinRAR. La taille réduite du fichier facilite le transfert et le partage de l'animation avec d'autres utilisateurs sur Internet.

### Structure du fichier OAM

La structure de fichier interne d'un fichier .oam est propriétaire et n'est pas documentée publiquement par Adobe. Cependant, il est connu que les fichiers .oam contiennent un ensemble de fichiers et de ressources (tels que des graphiques, de l'audio et du code ActionScript) regroupés dans un seul fichier. Le contenu d'un fichier .oam peut inclure des fichiers [XML](/fr/web/xml/), des fichiers SWF et d'autres fichiers de ressources. La structure exacte du fichier .oam dépend de la version spécifique d'Adobe Animate utilisée pour le créer, ainsi que du type d'animation et des ressources incluses dans le fichier.

Un fichier OAM contient les informations suivantes.

« Actifs : informations sur les ressources graphiques, audio et vidéo utilisées dans l'animation.

« Comportements : Descriptions des actions et des interactions qui se produisent dans l'animation.

`Code ActionScript :` Le code utilisé pour contrôler le comportement et l'interactivité de l'animation.

« Paramètres de publication : informations sur la plate-forme et le format dans lequel l'animation sera publiée, comme HTML5 ou AIR.

`Métadonnées :` Informations supplémentaires telles que l'auteur de l'animation, la date de création et le numéro de version.

## Comment ouvrir le fichier OAM ?

Vous pouvez utiliser les applications suivantes pour ouvrir les fichiers OAM.

* Adobe Edge Animate CC (arrêté)
* Adobe Animer 2023
*Adobe InDesign 2023
*Adobe Dreamweaver 2021

## Les références

* [Publication OAM](https://helpx.adobe.com/animate/using/OAM-publishing.html)

