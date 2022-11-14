{
  "date" : "2021-07-29",
  "keywords" :[ "fichier pes", "format de fichier pes", "qu'est-ce qu'un fichier pes", "fichier", "exemple pes", "extension de fichier pes","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PES - Format de broderie Brother PE",
  "description":"En savoir plus sur le format de fichier PES et les API qui peuvent créer et ouvrir des fichiers PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Qu'est-ce qu'un fichier de broderie PES ?

Le fichier de broderie PES est un fichier de conception qui contient des instructions pour les machines à broder/coudre. Il a été développé par Brother Industries pour leurs machines à broder, mais a ensuite été formalisé en tant que format de fichier général. Les fichiers PES sont utilisés par les machines à coudre pour lire les instructions de couture d'un motif sur du tissu. Ces fichiers ont deux objectifs ; fournissant d'abord des informations de conception pour l'application PE-Design développée par Brother Industries et deuxièmement, fournissant le nom du motif, les couleurs et les codes de la machine à broder tels que "stop", "jump" et "trim".

## Format de fichier PES - Plus d'informations

Un fichier PES est enregistré sur le disque au format de fichier binaire. Il contient plusieurs sections contenant des informations de couture stockées à l'aide d'une méthode prédéfinie. Le format de fichier PES est le suivant.

* Données de version - Donne des informations sur la version et peut être n'importe quelle valeur `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC Seek Value - Un entier little-endian de 4 octets suivant immédiatement les données de version et représentant la valeur de recherche pour la section PEC qui contient les détails de conception
* Section PSE - Contient des informations de conception pertinentes pour le Brother PE-Design et peut être d'autres applications de couture
* Section PCE - Peut être n'importe où dans le fichier PSE mais référencé par la valeur de recherche PEC.

## Type de machines à coudre utilisant le fichier PES

Les fichiers PES sont principalement créés par le logiciel PE-Design utilisé avec les machines à coudre Brother. Parmi les autres machines pouvant prendre en charge les fichiers PES, citons les machines à broder domestiques Babylock et Bernina.

## Comment convertir des fichiers PSE ?

L'application logicielle PE-Design peut [convertir le fichier PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+fichier) vers d'autres formats tels que .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd ou .xxx. Cela peut être fait à l'aide de l'application PE-Design en ouvrant le fichier et en sélectionnant le format de conversion.

## Références

* [PE Design - Manuel d'instructions](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

