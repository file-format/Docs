{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Format de définition de canal",
  "description" :"Découvrez ce qu'est un fichier CDF et les API qui peuvent créer et ouvrir des fichiers CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Qu'est-ce qu'un fichier CDF ?

Un fichier avec l'extension .cdf est un format de fichier de distribution d'informations basé sur XLM qui a été utilisé pour publier des mises à jour fréquentes en tant que "canaux". Les informations sont publiées à partir de n'importe quel serveur Web et sont automatiquement transmises aux ordinateurs dotés de programmes de réception compatibles tels que les navigateurs Web. Les utilisateurs s'abonnent aux canaux actifs et reçoivent des mises à jour programmées sur leur bureau.
Les fichiers CDF étaient auparavant utilisés conjointement avec les technologies Active Channel, Active Desktop et Smart Offline Favorites de Microsoft.

## Format de fichier CDF

Les fichiers CDF sont enregistrés sous forme de fichiers XML qui est un format de fichier Web générique pour l'échange d'informations. Le format de fichier CDF est un ancien format maintenant et n'a jamais été largement adopté. En comparaison, le RSS de Netscape était plus connu et largement utilisé.

### Exemple de format de fichier CDF

Voici un exemple générique du format de fichier CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domaine/dossier/"
LASTMOD="1998-11-05T22:12"
PRECACHE="OUI"
NIVEAU="0">
<TITLE>Titre de la chaîne</TITLE>
<ABSTRACT>Synopsis du contenu de la chaîne.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="OUI"
NIVEAU="1">
<TITLE>Titre de la page deux</TITLE>
<ABSTRACT>Synopsis du contenu de la page deux.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Références

* [Format de définition de canal - Par Wikipedia](https://en.wikipedia.org/wiki/Channel_Definition_Format)

