{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "fichier wpl", "extension", "format", "qu'est-ce qu'un fichier wpl", "musique", "format de fichier wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier WPL et les API qui peuvent créer, convertir et ouvrir des fichiers WPL.",
  "title" :"WPL - Fichier de liste de lecture du lecteur Windows Media",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Qu'est-ce qu'un fichier WPL ?

Un fichier avec l'extension .wpl contient la liste de lecture des chansons à exécuter sur Microsoft Windows Media Player. Ces fichiers sont généralement créés par les utilisateurs pour leurs collections vidéo et audio. Le contenu écrit dans un fichier WPL n'est que des chemins de répertoire ou des emplacements pour les fichiers multimédia sélectionnés par le créateur du fichier .wpl, de sorte que l'application de lecteur multimédia peut rapidement trouver et lire le contenu multimédia à partir de leurs emplacements de répertoire.

## Format de fichier WPL

WPL (Windows Media Player Playlist) est un format de fichier propriétaire utilisé dans les versions 9 ou supérieures de Microsoft Windows Media Player. Il s'agit d'un format de fichier informatique qui stocke des listes de lecture multimédia. Par défaut, la liste de lecture est enregistrée avec une extension .wpl (Windows Media Player Playlist). Vous pouvez utiliser l'extension [.m3u](/fr/audio/m3u) à la place, si vous souhaitez lire vos disques de données sur un appareil qui ne prend pas en charge cette extension. Les éléments d'un fichier WPL sont représentés au format XML.

L'élément de niveau supérieur "smil" spécifie que les éléments du fichier suivent la structure SMIL (Synchronized Multimedia Integration Language). Le fichier est créé et enregistré avec l'extension .wpl et son type MIME est application/vnd.ms-wpl.

### Exemple WPL

Voici un exemple de fichier wpl :
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Références ##

* [MPEG-1 Audio Layer II - Par Wikipédia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

