{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier GDOC - Raccourci Google Docs",
  "description":"Découvrez ce qu'est un fichier GDOC et les API qui peuvent créer et ouvrir des fichiers GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Qu'est-ce qu'un fichier GDOC ?

Un fichier GDOC est un fichier de raccourci qui pointe vers un fichier situé sur Google Drive, un service de stockage de documents basé sur le cloud. Lorsque le client Google Drive est installé sur un ordinateur et qu'un document y est créé, le lecteur crée un document dans le stockage cloud en ligne et écrit l'[URL](/fr/web/url/) de ce document dans le fichier GDOC de Google local Dossier Drive. Lorsque ce fichier de raccourci est double-cliqué, le navigateur Web par défaut ouvre le document à partir de l'emplacement [URL](/fr/web/url/). Si ce fichier de raccourci est déplacé hors de ce dossier, le lien vers le document en ligne est rompu.

## Format de fichier GDOC - Plus d'informations

Le fichier GDOC contient un raccourci vers le document en ligne écrit au format de fichier [JSON](/fr/web/json/). Le navigateur ouvrant les fichiers GDOC lit les informations d'URL et ouvre le document lié pour l'affichage à condition que l'utilisateur soit connecté à ce compte Google où le document est stocké. Les fichiers GDOC ne contiennent pas le contenu du document.

### Exemple de fichier GDOC

Le fichier GDOC peut être ouvert dans un éditeur de texte et son contenu ressemble à ce qui suit.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Comme on peut le voir, le contenu est formaté en JSON avec l'URL d'un document et l'ID de document associé.

## Références

* [Google Docs n'ouvre ni les fichiers gdoc ni docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

