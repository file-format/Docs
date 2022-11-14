{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "partiel", "extension", "fichier", "format", "web", "téléchargé" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Fichier partiellement téléchargé",
  "description":"En savoir plus sur le format de fichier PART et les API qui peuvent créer et ouvrir des fichiers PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Qu'est-ce qu'un fichier PART ? ##

Un fichier pièce ou une extension .part est un fichier partiellement téléchargé. Il est utilisé lorsque les téléchargements sont en cours ou ont été interrompus en raison d'un problème, donnant au gestionnaire de téléchargement la possibilité de reprendre le téléchargement chaque fois que possible.
Cela signifie que le navigateur, tel que Firefox ou les programmes de transfert de fichiers comme eMule, eMule plus, FlashGet, etc. stocke une partie du fichier, appelée fichier Part, pendant le téléchargement sur votre appareil. Ce fichier de pièce vous indiquera si le téléchargement est en cours ou a été interrompu avant la fin. Non seulement cela, mais le fichier PART stocke toutes les données jusqu'à ce que le téléchargement soit terminé, c'est pourquoi certaines d'entre elles peuvent être reprises ultérieurement si vous souhaitez recommencer le téléchargement.

## Format de fichier PART ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
