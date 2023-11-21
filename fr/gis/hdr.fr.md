{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier HDR - Format de fichier d'en-tête ESRI BIL",
  "description":"Qu'est-ce qu'un fichier HDR ?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Qu'est-ce qu'un fichier HDR ?

Un fichier HDR est un fichier d'en-tête SIG qui contient des informations d'en-tête pour un fichier Bande entrelacée par ligne (.BIL). Il décrit les données de l'image et porte le même nom que celui du fichier image. Un fichier HDR comprend un ensemble d'entrées, chacune décrivant un attribut particulier de l'image. Le fichier HDR décrit la présentation et le formatage du fichier BIL pour la traduction en coordonnées du monde réel en combinaison avec un fichier de géoréférencement distinct.

## Format de fichier HDR

Les fichiers HDR sont enregistrés au format de fichier texte ASCII. Il contient un ensemble d'entrées où chaque entrée décrit un attribut particulier de l'image. Chaque fichier HDR a le format suivant :

```
<keyword> <value>
```

`<keyword> ` - Il indique l'attribut particulier qui est en cours de définition
`<value> ` - C'est la valeur à laquelle l'attribut est défini

Il n'y a aucune limitation quant à l'ordre des entrées dans l'en-tête. Cependant, chaque entrée doit se trouver sur une ligne distincte de la ligne pour respecter la méthode d'analyse utilisée par les lecteurs HDR.

## Résumé des mots-clés utilisés dans le fichier HDR

|Mot clé |Valeur acceptable |Par défaut|
---|---|---|
|nrows |tout entier > 0| aucun
|ncols |tout entier > 0| aucun
|nbandes |tout entier > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|ordre des octets| I = Intel;M = Motorola |identique à la machine hôte|
|mise en page| bil, bip, bsq| billet|
|skipbytes| tout entier ≥ 0| 0
|ulxmap |n'importe quel nombre réel| 0|
|ulymap |n'importe quel nombre réel |nrows - 1|
|xdim |n'importe quel nombre réel| 1
|ydim |n'importe quel nombre réel| 1
|bandrowbytes |tout entier > 0| plus petit entier ≥ (ncols x nbits) / 8|
|totalrowbytes |tout entier > 0| pour bil : nbands x bandrowbytes ; pour bip : plus petit entier ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |tout entier ≥ 0| 0|

## Les références

* [Format de fichier HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

