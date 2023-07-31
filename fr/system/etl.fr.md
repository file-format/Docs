{
  "date" : "2022-02-22",
  "keywords" :[ "ETL", "extension", "fichier", "format", "système", "Pilote", "Pilote de périphérique Windows", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichiers ETL - Fichier journal de suivi des événements Microsoft",
  "description":"En savoir plus sur le format de fichier ETL et les API qui peuvent créer et ouvrir des fichiers ETL.",
  "linktitle" : "ETL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-02-22"
}

## Qu'est-ce qu'un fichier ETL ?

Les fichiers ETL sont des fichiers journaux contenant des journaux d'événements générés par le noyau du système d'exploitation Microsoft. Ces fichiers journaux incluent les erreurs, les avertissements et d'autres événements au niveau de l'application et du système. Les fichiers ETL sont utiles pour analyser et résoudre les problèmes au niveau du système. Les problèmes courants enregistrés dans les fichiers ETL incluent ceux générés par les accès au disque et les défauts de page. Microsoft fournit deux applications, Tracerpt et Event Viewer pour lire et afficher le contenu des fichiers ETL. Les fichiers ETL peuvent être convertis en d'autres formats de fichiers tels que [TXT](/fr/word-processing/txt/) et [CSV](/fr/spreadsheet/csv/) à l'aide de Tracerpt.

## Format de fichier ETL

Les fichiers ETL sont enregistrés sur le disque au format binaire compressé pour réduire l'espace disque.

## Ouvrir les fichiers ETL à l'aide de Windows Performance Analyzer

Les données des fichiers ETL peuvent être lues et visualisées sous forme de tableaux et de graphiques à l'aide de l'application Microsoft Windows Performance Analyzer (WPA). Le guide [Ouverture et analyse des fichiers ETL](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/opening-and-analyzing-etl-files-in-wpa) fournit des informations sur le fonctionnement avec les fichiers ETL.

## Références

* [Analyseur de performances Windows](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/getting-started--windows-performance-analyzer--wpa-)
* [Guide de démarrage rapide WPA](https://learn.microsoft.com/en-us/windows-hardware/test/wpt/wpa-quick-start-guide)

