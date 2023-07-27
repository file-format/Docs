{
  "date" : "2021-04-08",
  "keywords" :[ "lz file", "lz file format", "wat is een lz file", "file", "lz example", "lz file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip gecomprimeerd bestandsformaat",
  "description":"Meer informatie over de LZ-bestandsindeling en API's die LZ-bestanden kunnen maken en openen.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Wat is een LZ-bestand?

Een bestand met de extensie .lz is een gecomprimeerd archiefbestand dat is gemaakt met Lzip, een gratis opdrachtregelprogramma voor compressie. Het ondersteunt aaneenschakeling om ondersteuningsbestanden te comprimeren. LZ-bestanden hebben het mediatype application/lzip en ondersteunen hogere compressieverhoudingen dan [BZ2](/nl/compression/bz2/). LZ zijn gebaseerd op het LZMA-algoritme (Lempel-Ziv-Markov chain) en bevatten een 32-bits CRC-controlesom en ident-bytes voor het controleren van de integriteit van het bestand.

## LZMA gecomprimeerd formaat

Het gecomprimeerde LZMA-formaat bestaat uit een gecomprimeerde stroom bits die is gecodeerd met behulp van adaptieve binaire bereikcoder. De stream is verdeeld in pakketten. Elk pakket beschrijft een enkele byte of een LZ77-reeks. De lengte en afstand van elk pakket is impliciet of expliciet gecodeerd.

De zeven soorten pakketten zijn als volgt ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence) |Packet name |Packet description|
---|---|---|
|0 + byteCode| LIT| Een enkele byte gecodeerd met behulp van een adaptieve binaire bereikcoder.|
|1+0 + len + afstand| MATCH| Een typische LZ77-reeks die de lengte en afstand van de reeks beschrijft.|
|1+1+0+0| KORTHERHALEN| Een LZ77-reeks van één byte. Afstand is gelijk aan de laatst gebruikte LZ77 afstand.|
|1+1+0+1 + len| LANGREP[0]| Een LZ77-reeks. Afstand is gelijk aan de laatst gebruikte LZ77 afstand.|
|1+1+1+0 + len| LANGREP[1]| Een LZ77-reeks. De afstand is gelijk aan de op één na laatst gebruikte LZ77-afstand.|
|1+1+1+1+0 + len| LANGREP[2]| Een LZ77-reeks. De afstand is gelijk aan de op twee na laatst gebruikte LZ77-afstand.|
|1+1+1+1+1 + len| LANGREP[3]| Een LZ77-reeks. Afstand is gelijk aan de op drie na laatst gebruikte LZ77-afstand.|


## Referenties

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

