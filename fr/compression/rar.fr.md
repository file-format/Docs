{
  "date" : "2019-10-11",
  "keywords" :[ "fichier rar", "format de fichier rar", "qu'est-ce qu'un fichier rar", "fichier", "exemple rar", "extension de fichier rar","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RAR",
  "description":"Qu'est-ce qu'une extension de fichier RAR et les API qui peuvent créer et ouvrir des fichiers RAR.",
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier RAR ?

Les fichiers avec l'extension .rar sont des fichiers d'archive créés pour stocker des informations sous forme compressée ou normale. RAR, qui signifie Roshal ARchive file format, est un format de fichier propriétaire créé par Eugene Roshal en 1995, qui était un ingénieur logiciel russe. Le format est utilisé pour archiver des fichiers avec différentes méthodes, y compris diverses techniques de compression. Il existe plusieurs logiciels d'application disponibles pour Windows, Linux et MacOS pour l'extraction de fichiers RAR. Le logiciel WinRAR, par RARLab, est l'utilitaire d'archivage de fichiers shareware (gratuit pendant 40 jours) pour la plate-forme Microsoft Windows ; le logiciel a été porté sur Linux (uniquement en tant qu'extracteur) par le même auteur, Eugene Roshal.

## Historique des versions du format de fichier RAR

* v1.3 (original, n'a pas de signature "Rar!")
* v1.5
* v2.0 - publié avec WinRAR 2.0 et Rar pour MS-DOS 2.0
* v2.9 - publié dans WinRAR version 3.00
* v5.0 - pris en charge par WinRAR 5.0 et versions ultérieures

## Principales caractéristiques du format RAR

RAR est dans le domaine depuis assez longtemps et est l'un des formats de fichiers d'archivage préférés. Les principales caractéristiques du format RAR sont :

**`Taux de compression élevé :`** Supérieur à [ZIP](/fr/compression/zip/), comparable aux formats 7z et zipx.

**`Cryptage de fichier fort par conception :`** Les archives RAR4 cryptées reposent sur un cryptage basé sur AES-128 tandis que les archives RAR5 cryptées reposent sur un cryptage AES-256 avec une planification de clé améliorée

**`Capacités avancées de correction d'erreurs et de récupération de données :`** enregistrements de récupération facultatifs lors de la création de l'archive

**`Taille du fichier :`** Minimum 20 octets et maximum 2^63 octets (8 exaoctets de taille totale de l'archive)

**`Archives RAR multi-volumes :`** Possibilité de diviser des archives volumineuses en plusieurs fichiers plus petits pour faciliter le transfert sur le réseau. Dans ce cas, les extensions de fichier sont incrémentées de 1 pour représenter les volumes divisés

## Format de fichier RAR

Les spécifications complètes du format RAR ne sont pas disponibles publiquement et c'est pourquoi les détails sur le format ne peuvent pas être formulés de manière concise.

### Disposition générale des archives

La disposition générale d'un format de fichier RAR introduit dans la version 5.0 est la suivante :

|Format de fichier
---|
|Module auto-extractible (en option)
|Signature RAR 5.0
|En-tête de chiffrement d'archive (facultatif)
|En-tête de l'archive principale
|En-tête du service de commentaire d'archive (facultatif)
En-tête de fichier 1
|En-têtes de service (NTFS ACL, flux, etc.) pour le fichier précédent (facultatif)
|...
|En-tête de fichier N
|En-têtes de service (NTFS ACL, flux, etc.) pour le fichier précédent (facultatif)
|Enregistrement de récupération (facultatif)
|Fin de l'entête de l'archive

Des informations sur chaque section du fichier RAR mentionnée ci-dessus peuvent être trouvées dans le document [Spécifications du format de fichier RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### Archives RAR auto-extractibles

Si le fichier RAR lui-même est auto-extractible, les informations auto-extractibles sont contenues au début du fichier précédant la signature de l'archive. Sa taille et son contenu ne sont pas définis.

#### Signature RAR 5.0

La signature RAR est un en-tête de 8 octets composé du nombre magique suivant :

0x 52 61 72 21 1A 07 00

où

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## Références

* [Format d'archive RAR 5.0] (https://www.rarlab.com/technote.htm)
* [RAR - Par Wikipédia](https://en.wikipedia.org/wiki/RAR_(file_format))

