{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier WHL - Fichier de package Python Wheel",
  "description":"En savoir plus sur le format de fichier WHL et les API qui peuvent créer et ouvrir des fichiers WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Qu'est-ce qu'un fichier WHL ?

Un fichier WHL (Wheel) est un fichier de package de distribution enregistré au format de roue de Python. Il s'agit d'une installation au format standard des distributions Python et contient tous les fichiers et métadonnées nécessaires à l'installation. Le fichier WHL contient également des informations sur les versions et plates-formes Python prises en charge par ce fichier wheel. Semblable à un fichier d'installation [MSI](/fr/executable/msi/), le format de fichier WHL est un format prêt à installer qui permet d'exécuter le package d'installation sans créer la distribution source.

## Format de fichier WHL

Le format de fichier WHL est une archive [ZIP](/fr/compression/zip/) (.zip) qui contient tous les fichiers d'installation et les métadonnées requises par les installateurs pour l'installation d'un package. Ces fichiers WHL peuvent être extraits à l'aide de l'option de décompression ou d'applications logicielles de décompression standard telles que WinZIP et WinRAR.

### Convention de nom de fichier WHL

Un fichier WHL est nommé selon la convention suivante.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Un exemple de nom de fichier WHL est le suivant.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptography` est le nom du paquet.
* `2.9.2` est la version du package de cryptographie. Une version est une chaîne conforme à la PEP 440 telle que 2.9.2, 3.4 ou 3.9.0.a3.
* `cp35` est la balise Python et indique l'implémentation et la version Python requises par la roue.
* `abi3` est la balise ABI. ABI signifie interface binaire d'application.
* `macosx_10_9_x86_64` est la balise de plate-forme, qui se trouve être assez longue.

## Références

* [Qu'est-ce que Python Wheels et pourquoi devriez-vous vous en soucier ?](https://realpython.com/python-wheels/)
* [Roue Python](https://pypi.org/project/wheel/)

