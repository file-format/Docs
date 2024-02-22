{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier EAZ - Qu'est-ce qu'un fichier EAZ et comment l'ouvrir ?",
  "description":"Découvrez le format de fichier EAZ et les API permettant de créer et d'ouvrir des fichiers EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-frz"
}
},
  "lastmod" : "2023-12-23"
}

## Qu'est-ce qu'un fichier EAZ ?

Le fichier EAZ est un fichier complémentaire utilisé par ArcGIS Explorer, une application gratuite développée par ESRI pour l'exploration, la visualisation et le partage de cartes. Il contient une archive de fichiers compressés qui comprend un [XML file](/web/xml/), du code compilé et les fichiers de prise en charge nécessaires au complément. Ces fichiers sont utilisés pour étendre les fonctionnalités de base du logiciel en incorporant de nouveaux boutons, des fenêtres ancrables et d'autres extensions.

## Format de fichier EAZ - Plus d'informations

Les fichiers EAZ sont créés grâce à l'utilisation du SDK ArcGIS Explorer, un kit de développement conçu pour créer des fonctionnalités personnalisées dans ArcGIS Explorer. Ces fichiers utilisent la compression [ZIP](/compression/zip/) pour empaqueter efficacement leur contenu. Au cœur de l'archive, le fichier **Addins.xml** réside dans le répertoire racine, servant de composant essentiel qui décrit et détaille les différentes personnalisations intégrées dans le fichier EAZ.

Le fichier Addins.xml agit essentiellement comme une feuille de route, offrant un aperçu des améliorations, modifications et extensions spécifiques que le fichier EAZ introduit dans ArcGIS Explorer. Grâce à cette structure complète, les développeurs peuvent encapsuler et intégrer de manière transparente de nouvelles fonctionnalités, boutons et fenêtres ancrables, améliorant ainsi la fonctionnalité globale et l'expérience utilisateur de l'application ArcGIS Explorer.

## Les références

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
