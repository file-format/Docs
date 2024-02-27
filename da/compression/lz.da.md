{
  "date": "2021-04-08",
  "keywords": [
"lz fil",
"lz filformat",
"hvad er en lz fil",
"fil",
"lz eksempel",
"lz filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ - Lzip komprimeret filformat",
  "description": "Lær om LZ filformat og API'er, der kan oprette og åbne LZ filer.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-daz"
}
},
  "lastmod": "2021-04-19"
}

## Hvad er en LZ fil?

En fil med filtypenavnet .lz er en komprimeret arkivfil oprettet med Lzip, som er et gratis kommandolinjeværktøj til komprimering. Det understøtter sammenkædning for at komprimere støttefiler. LZ-filer har medietype application/lzip og understøtter højere komprimeringsforhold end [BZ2](/compression/bz2/). LZ er baseret på LZMA (Lempel-Ziv-Markov chain) algoritmen og inkluderer en 32-bit CRC checksum og ident bytes til kontrol af filens integritet.

## LZMA komprimeret format

Det komprimerede LZMA-format består af en komprimeret strøm af bit, der er kodet ved hjælp af adaptiv binær områdekoder. Strømmen er opdelt i pakker. Hver pakke beskriver enten en enkelt byte eller en LZ77-sekvens. Længden og afstanden af hver pakke er implicit eller eksplicit kodet.

De syv typer pakker er som følger ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + bytekode| LIT| En enkelt byte kodet ved hjælp af en adaptiv binær områdekoder.|
|1+0 + len + dist| MATCH| En typisk LZ77-sekvens, der beskriver sekvenslængde og -afstand.|
|1+1+0+0| KORTTREP| En en-byte LZ77-sekvens. Afstand er lig med den sidst anvendte LZ77-afstand.|
|1+1+0+1 + len| LONGREP[0]| En LZ77-sekvens. Afstand er lig med den sidst anvendte LZ77-afstand.|
|1+1+1+0 + len| LANGREP[1]| En LZ77-sekvens. Afstand er lig med den næstsidst brugte LZ77-afstand.|
|1+1+1+1+0 + len| LONGREP[2]| En LZ77-sekvens. Afstand er lig med den tredje sidst brugte LZ77 distance.|
|1+1+1+1+1 + len| LONGREP[3]| En LZ77-sekvens. Afstand er lig med den fjerde sidst brugte LZ77 distance.|


## Referencer

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)

* [Lzip](https://en.wikipedia.org/wiki/Lzip)


