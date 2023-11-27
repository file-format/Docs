{
"date": "2023-05-16",
  "keywords": [
"fichier sami",
"qu'est-ce qu'un fichier sami",
"exemple de fichier sami",
"déposer",
"extension de fichier sami",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier SAMI - Fichier d'échange de sous-titres et de métadonnées",
  "description":"Découvrez le format SAMI et les API permettant de créer et d'ouvrir des fichiers SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent" : "video"
}
},
"derniermod": "2023-05-16"
}

## Qu'est-ce qu'un fichier SAMI ?

Un fichier avec l'extension « .sami » fait généralement référence à un fichier d'échange de sous-titres et de métadonnées (SAMI). SAMI est un format de sous-titrage utilisé pour afficher des sous-titres ou des sous-titres codés dans les vidéos. Il a été initialement développé par Microsoft pour son Windows Media Player.

Les fichiers SAMI contiennent des informations de synchronisation et du contenu textuel pour les sous-titres ou les sous-titres codés, leur permettant d'être synchronisés avec une lecture vidéo. Le format prend en charge les options de formatage de base telles que le style de police, la couleur et le positionnement des sous-titres à l'écran.

Les fichiers SAMI sont généralement des fichiers texte brut et peuvent être ouverts et modifiés à l'aide d'un éditeur de texte. Le contenu d'un fichier SAMI comprend généralement une section d'en-tête qui fournit des informations sur le fichier, suivie d'entrées de sous-titres individuelles avec leur timing et leur texte respectifs.

Voici un exemple de ce à quoi pourrait ressembler un fichier SAMI :

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Les fichiers SAMI sont couramment utilisés avec des lecteurs vidéo ou des lecteurs multimédias prenant en charge l'affichage des sous-titres, tels que Windows Media Player ou VLC Media Player. Le lecteur lit le fichier SAMI et synchronise les sous-titres avec le contenu vidéo, permettant aux téléspectateurs de lire les sous-titres tout en regardant la vidéo.

## Balises HTML prises en charge

Les fichiers SAMI (Subtitles And Metadata Interchange) prennent en charge un ensemble limité de balises de type HTML pour le formatage et le style des sous-titres. Voici quelques-unes des balises couramment utilisées prises en charge par SAMI :

- ``<SAMI> :`` L'élément racine qui encapsule l'intégralité du fichier SAMI.
- ``<HEAD> :`` Contient les informations d'en-tête du fichier SAMI.
<html>- ``<TITLE> :`` Spécifie le titre du fichier SAMI. </html>
- ``<BODY> :`` Enferme les entrées de sous-titres et leurs informations de synchronisation.
- ``<SYNC> :`` Représente un point de synchronisation pour une entrée de sous-titre. Il précise le moment auquel le sous-titre doit être affiché.
- ``<P> :`` Entoure le contenu textuel réel d'un sous-titre. Il est généralement utilisé dans un<SYNC> bloc.
<html>- `` <FONT>:`` Définit les propriétés de police pour le texte inclus. Des attributs tels que Couleur, Visage, Taille et Style peuvent être utilisés pour modifier l'apparence de la police.</font>
- ``<BR> :`` Insère un saut de ligne dans un sous-titre.
<html>- ``<B> :`` Rend le texte ci-joint en gras.</b>
<html>- ``<I> :`` Rend le texte inclus en italique.</i>
<html>- ``<U> :`` Rend le texte ci-joint souligné.</u>
- ``<C> :`` Spécifie la position ou l'alignement du texte des sous-titres à l'écran. Il prend en charge des attributs tels que Centre, Milieu, Gauche, Droite, Haut, Bas et leurs combinaisons.
- ``<LANG> :`` Spécifie le code de langue pour le texte des sous-titres. Cela aide à identifier la langue des sous-titres.

Voici quelques-unes des balises de base prises en charge par les fichiers SAMI. Il est important de noter que SAMI ne prend pas en charge toute la gamme des balises et attributs HTML. Les balises prises en charge sont principalement axées sur le style et le positionnement des sous-titres plutôt que sur une structuration ou une interactivité étendue des documents.

## Les références
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

