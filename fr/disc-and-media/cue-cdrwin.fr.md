{
"date": "2023-10-18",
   "keywords":[
"signal",
"fichier de repère",
"fichier de feuille de repère cue cdrwin",
"comment ouvrir un fichier cue",
"déposer",
"extension de fichier de repère",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier CUE - Feuille de repères CDRWIN",
   "description":"Découvrez le format de fichier CUE CDRWIN Cue Sheet et les API permettant de créer et d'ouvrir des fichiers CUE.",
"linktitle": "CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
"parent" : "disc-and-media"
}
},
"lastmod": "2023-10-18"
}

## Qu'est-ce qu'un fichier CUE ?

Un fichier **.CUE**, également connu sous le nom de **CDRWIN Cue Sheet**, est un fichier texte brut qui contient des informations sur les pistes et la disposition d'un CD audio ou d'une image disque, généralement au format BIN ou ISO. Ces fichiers sont souvent utilisés pour décrire la structure et le contenu du disque, permettant ainsi aux logiciels de gravure de CD ou aux logiciels de lecteur virtuel de reproduire avec précision le disque original.

## Exemple de fichier CUE

Voici un exemple de ce à quoi pourrait ressembler le fichier « .cue » :

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## Feuille de repères CDRWIN

CDRWIN Cue Sheet est une variante spécifique du format de fichier « .cue » utilisé par le logiciel CDRWIN. CDRWIN est un logiciel de gravure et de création de CD/DVD et ses feuilles « .cue » sont conçues pour être utilisées avec ce logiciel. Ces feuilles ".cue" contiennent les informations nécessaires à CDRWIN pour créer ou graver avec précision un CD ou un DVD.

Voici quelques détails clés spécifiques aux feuilles de repères CDRWIN :

1. **Unique à CDRWIN** : les feuilles « .cue » de CDRWIN sont un format propriétaire spécifique au logiciel CDRWIN. Bien qu'ils partagent des similitudes avec les fichiers « .cue » standard, ils sont conçus pour fonctionner avec les fonctionnalités et les paramètres de CDRWIN.
    






2. **Interface conviviale** : CDRWIN fournit une interface facile à utiliser pour créer et éditer ses feuilles ".cue". Les utilisateurs peuvent ajouter ou modifier des informations sur les pistes, les index, les espaces et d'autres paramètres de manière conviviale.
    






3. **Types de disques compatibles** : Les feuilles de repère CDRWIN sont principalement utilisées pour créer divers types de CD et DVD, notamment des disques de données, des CD audio, des disques en mode mixte et bien plus encore. Le format permet aux utilisateurs de spécifier le type et le contenu du disque qu'ils souhaitent créer.
    






4. **Contrôle de la disposition du disque** : Les feuilles de repère CDRWIN offrent un contrôle détaillé sur la disposition et la structure du disque, y compris l'ordre des pistes, les paramètres de pause/espace et toute autre préférence spécifique que l'utilisateur peut avoir.
    






5. **Prise en charge ISO et BIN** : CDRWIN peut fonctionner avec les formats d'image disque ISO et BIN. La feuille ".cue" spécifie quel fichier image est utilisé pour le disque, garantissant ainsi une bonne synchronisation entre les repères et l'image.
    






6. **Gravure et extraction** : Ces feuilles ".cue" sont cruciales lors de la gravure de disques ou de l'extraction de pistes de disques à l'aide de CDRWIN. Ils permettent de garantir que le produit final correspond à la mise en page et au contenu prévus.
    






7. **Sauvegarde et restauration** : les utilisateurs de CDRWIN créent souvent des feuilles ".cue" lorsqu'ils effectuent des sauvegardes de leurs CD ou DVD. Ces feuilles peuvent ensuite être utilisées pour restaurer le contenu du disque, y compris la disposition des pistes et le timing.

## Comment ouvrir le fichier CUE?

Les feuilles de repère CDRWIN sont spécialement conçues pour le logiciel CDRWIN, elles sont donc généralement destinées à être ouvertes et utilisées dans CDRWIN.

Programmes qui ouvrent ou référencent des fichiers CUE

-CDRWIN
- Projets intelligents IsoBuster
- Systèmes EZB UltraISO

## Autres fichiers CUE

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.cue**.

**Disque et média**
- [CUE - Fichier de feuille de repère](/fr/disc-and-media/cue/)
- [CUE - Feuille de repères CDRWIN](/fr/disc-and-media/cue-cdrwin/)

## Les références
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

