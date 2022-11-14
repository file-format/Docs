{
  "date" : "2021-04-08",
  "keywords" :[ "fichier lz", "format de fichier lz", "qu'est-ce qu'un fichier lz", "fichier", "exemple lz", "extension de fichier lz","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Format de fichier compressé Lzip",
  "description":"En savoir plus sur le format de fichier LZ et les API qui peuvent créer et ouvrir des fichiers LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Qu'est-ce qu'un fichier LZ ?

Un fichier avec l'extension .lz est un fichier d'archive compressé créé avec Lzip, qui est un outil de ligne de commande gratuit pour la compression. Il prend en charge la concaténation pour compresser les fichiers de support. Les fichiers LZ ont un type de média application/lzip et prennent en charge des taux de compression plus élevés que [BZ2](/fr/compression/bz2). LZ sont basés sur l'algorithme LZMA (chaîne Lempel-Ziv-Markov) et incluent une somme de contrôle CRC 32 bits et des octets d'identification pour vérifier l'intégrité du fichier.

## Format compressé LZMA

Le format compressé LZMA consiste en un flux compressé de bits qui est codé à l'aide d'un codeur de plage binaire adaptatif. Le flux est divisé en paquets. Chaque paquet décrit soit un seul octet, soit une séquence LZ77. La longueur et la distance de chaque paquet sont implicitement ou explicitement codées.

Les sept types de paquets sont les suivants ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Code compacté (séquence de bits) |Nom du paquet |Description du paquet|
---|---|---|
|0 + byteCode| LIT| Un seul octet codé à l'aide d'un codeur de plage binaire adaptatif.|
|1+0 + longueur + dist| MATCH| Une séquence LZ77 typique décrivant la longueur et la distance de la séquence.|
|1+1+0+0| RÉP.RAPPROCHE| Une séquence LZ77 d'un octet. La distance est égale à la dernière distance LZ77 utilisée.|
|1+1+0+1 + longueur| LONGREP[0]| Une séquence LZ77. La distance est égale à la dernière distance LZ77 utilisée.|
|1+1+1+0 + longueur| LONGREP[1]| Une séquence LZ77. La distance est égale à l'avant-dernière distance LZ77 utilisée.|
|1+1+1+1+0 + longueur| LONGREP[2]| Une séquence LZ77. La distance est égale à l'avant-dernière distance LZ77 utilisée.|
|1+1+1+1+1 + longueur| LONGREP[3]| Une séquence LZ77. La distance est égale à la quatrième dernière distance LZ77 utilisée.|


## Références

* [LZMA - Wikipédia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

