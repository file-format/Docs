{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier TPSR - Fichier de rapport de session pilote TeamViewer",
  "description":"En savoir plus sur le format de fichier TPSR et les API qui peuvent créer et ouvrir des fichiers TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Qu'est-ce qu'un fichier TPSR ?

Un TPSR est un fichier de protocole de connexion utilisé par TeamViewer Assist AR (anciennement connu sous le nom de TeamViewer Pilot). Les informations stockées dans un fichier TPSR sont stockées au format de fichier compressé [ZIP](/fr/compression/zip/). TPSR contient un historique détaillé de la connexion TeamViewer entre un expert et un technicien pour résoudre le problème et à des fins d'examen. Les informations contenues dans un fichier TPSR incluent le type d'appareil, le nom, l'ID d'assistance AR, l'ID d'expert, la date et l'heure et la durée de la connexion. Ces données sont stockées dans un fichier [JSON](/fr/web/json/) à l'intérieur de l'archive TPSR compressée.

## Format de fichier TPSR

Un fichier TPSR est stocké sur un disque au format de fichier d'archive ZIP où le contenu est stocké dans un fichier JSON. Il est généré automatiquement une fois la connexion Assist AR terminée, à condition que l'option de rapport de connexion soit activée dans TeamViewer.

TeamViewer Assist AR permet aux experts de se connecter aux techniciens pour obtenir le flux EN DIRECT de l'extrémité distante via la caméra mobile. Ils peuvent aider les techniciens à résoudre le problème par téléphone.

## Ouvrir les fichiers TPSR

Vous pouvez ouvrir les fichiers TPSR à l'aide de la version de bureau du logiciel TeamViewer. S'il est installé sur votre ordinateur, double-cliquez sur le fichier TPSR pour l'ouvrir dans le logiciel TeamViewer. Les fichiers TPSR peuvent également être exportés vers des fichiers [PDF](/fr/pdf/) ou peuvent être imprimés pour avoir une copie imprimée du fichier de protocole.

## Références ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

