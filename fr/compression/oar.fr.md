{
  "date" : "2021-04-08",
  "keywords" :[ "fichier oar", "format de fichier oar", "qu'est-ce qu'un fichier oar", "fichier", "exemple oar", "extension de fichier oar","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Format de fichier d'archive OpenSimulator",
  "description":"En savoir plus sur le format de fichier OAR et les API qui peuvent créer et ouvrir des fichiers OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Qu'est-ce qu'un fichier OAR ?

Un fichier avec l'extension .oar est un fichier d'archive utilisé par l'application OpenSimulator qui est un serveur d'application 3D open-source pour créer un environnement virtuel accessible à plusieurs utilisateurs sur le réseau. Le format de fichier OAR fournit les données d'actifs nécessaires pour charger entièrement le terrain, les textures d'objets et les inventaires sur un système différent. OpenSimulator dispose également d'une hypergrille facultative qui permet aux utilisateurs de visiter d'autres installations OpenSimulator sur le Web. Les fichiers OAR ont une application/oar de type Internet MIME et contiennent un ou plusieurs fichiers archivés.


## Format de fichier OAR

OAR sont des fichiers binaires stockés dans un format de fichier d'archive compressé. La dernière version du format de fichier OAR est [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) qui a des changements majeurs par rapport à sa précédente [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). La dernière version prend en charge le stockage de plusieurs régions dans un seul OAR et n'est pas rétrocompatible avec les versions d'OpenSimulator antérieures à 0.7.5. Un fichier OAR est un fichier tar gzippé (tar.gz) au format tar unix d'origine (pas USTAR).

## Exemple de régions OAR
Les fichiers AOR peuvent contenir plusieurs régions. La structure de l'archive est la suivante (cet exemple contient 4 régions) :

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Le fichier de contrôle d'archive contient un numéro de version majeur pour définir la compatibilité avec les futurs changements de format. La présence d'actifs au format OAR est indiquée par l'élément booléen<assets_included> . Les informations sur les régions incluses sont contenues dans un manifeste présent dans le fichier de contrôle. Un exemple de Archive.xml est le suivant.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Références

* [Format OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

