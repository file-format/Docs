{
  "date" : "2023-01-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier ODTTF - Format de fichier de police OpenType obfusqué",
  "description":"En savoir plus sur le format de fichier ODTTF et les API qui peuvent créer et ouvrir des fichiers ODTTF.",
  "linktitle" : "ODTTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-13"
}

## Qu'est-ce qu'un fichier ODTTF ?

Un fichier ODTTF est un format de fichier de police utilisé par les formats de fichier [.XPS](/fr/page-description-language/xps/) et Microsoft Office 2007. Il contient une police OpenType obfusquée qui a été modifiée afin de rendre difficile l'extraction des informations de conception de la police ou la rétro-ingénierie du code source de la police. ODTTF est basé sur les polices utilisées dans les documents originaux mais n'est pas au format brut et peut ne pas être lu par un logiciel tiers pour extraire les données de police.

Vous pouvez ouvrir les fichiers ODTTF à l'aide de Pagemark XpsViewer, Apple Safari avec Pagemark XpsPlugin, Mozilla Firefox avec Pagemark XpsPlugin,
Affichage NiXPS et édition NiXPS.

## Format de fichier ODTTF

La structure de format de fichier interne du format de fichier ODTTF n'est pas connue car ceux-ci sont stockés au format obscurci intégré. Ceux-ci peuvent être intégrés dans des documents numériques tels que .PDF ou .DOCX.

## Références
* [Spécifications des polices OpenType par Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [Aperçu de TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

