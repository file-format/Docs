{
  "date" : "2021-01-21",
  "keywords" :[ "fichier otp", "format de fichier otp", "qu'est-ce qu'un fichier otp", "fichier", "exemple otp", "extension de fichier otp","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - Modèle de présentation OpenDocument",
  "description":"En savoir plus sur le format de fichier OTP et les API qui peuvent créer et ouvrir des fichiers OTP.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Qu'est-ce qu'un fichier OTP ?

Les fichiers avec l'extension .otp représentent des fichiers de modèle de présentation créés par des applications au format standard OASIS OpenDocument. Le contenu d'un tel fichier comprend des informations de présentation sous forme de diapositives avec du texte, des images, des formes, du contenu multimédia, des effets de transition et d'autres éléments de diapositive. Ces fichiers de modèle sont utilisés pour créer rapidement de nouvelles présentations en fonction des informations de style stockées dans le modèle lui-même. Les fichiers OTP peuvent être créés et enregistrés avec plusieurs applications différentes telles que Impress fourni avec la suite OpenOffice et Microsoft PowerPoint. Le format de fichier OTP est similaire aux fichiers de modèle Microsoft PowerPoint [.pot](/fr/presentation/pot/) et [.potx](/fr/presentation/potx/).

## Format de fichier OTP

Le format de fichier OTP est basé sur la norme OpenDocument qui prend en charge la représentation du document sous la forme d'un document XML unique ainsi que la collecte de plusieurs sous-documents dans un seul package compressé au format [ZIP](/fr/compression/zip/). Le contenu du fichier est distribué dans plusieurs fichiers xml regroupés. Ces multiples fichiers [XML](/fr/web/xml/) contiennent des informations sur le style, le contenu, les méta-informations et les paramètres du document, comme indiqué ci-dessous.

* `content.xml` - Contenu du document et styles automatiques utilisés dans le contenu.
* `styles.xml` - Styles utilisés dans le contenu du document et styles automatiques utilisés dans les styles eux-mêmes.
* `meta.xml` - Documentez les méta-informations, telles que l'auteur ou l'heure de la dernière action d'enregistrement.
* `settings.xml` - Paramètres spécifiques à l'application, tels que la taille de la fenêtre ou les informations sur l'imprimante.

## Références

* [OpenDocument - Par Wikipédia](https://en.wikipedia.org/wiki/OpenDocument)

