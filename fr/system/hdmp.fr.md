{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier HDMP - Format de fichier de vidage de tas Windows",
  "description":"En savoir plus sur le format de fichier HDMP et les API qui peuvent créer et ouvrir des fichiers HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Qu'est-ce qu'un fichier HDMP ?

Le fichier HDMP est un vidage de mémoire non compressé lorsqu'une application ou un programme se bloque en raison d'une erreur. Il n'est créé que par Windows XP/Vista et contient un vidage de l'état de l'application lorsqu'elle a planté. Étant non compressés, les fichiers HDMP occupent plus d'espace sur le disque que les fichiers Minidump [MDMP](/fr/system/mdmp/) qui sont compressés à des fins de création de rapports.

Les applications pouvant être utilisées pour **ouvrir** ou analyser des fichiers HDMP incluent Microsoft Visual Studio avec des outils de débogage pour Windows.

## Format de fichier HDMP

Les fichiers HDMP sont stockés sur disque en tant que fichiers binaires et n'offrent aucun avantage s'ils sont ouverts sans les applications appropriées. Ceux-ci contiennent des données système pertinentes enregistrées lorsque l'erreur s'est produite.

### Différence entre les formats de fichiers HDMP et MDMP

HDMP sont des fichiers de vidage de mémoire non compressés. En revanche, MDMP sont des mini fichiers de vidage qui sont compressés pour réduire la taille du fichier et envoyés à Microsoft pour signaler le problème.

## Référence ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

