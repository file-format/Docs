{
  "date" : "2021-04-08",
  "keywords" :[ "fișier lz", "format fișier lz", "ce este un fișier lz", "fișier", "exemplu lz", "extensie fișier lz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Format de fișier comprimat Lzip",
  "description":"Aflați despre formatul de fișier LZ și despre API-urile care pot crea și deschide fișiere LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Ce este un fișier LZ?

Un fișier cu extensia .lz este un fișier de arhivă comprimat creat cu Lzip, care este un instrument gratuit de linie de comandă pentru compresie. Acceptă concatenarea pentru a comprima fișierele de suport. Fișierele LZ au tip media application/lzip și acceptă rații de compresie mai mari decât [BZ2](/ro/compression/bz2). LZ se bazează pe algoritmul LZMA (lanț Lempel-Ziv-Markov) și includ o sumă de control CRC de 32 de biți și octeți de identificare pentru verificarea integrității fișierului.

## Format comprimat LZMA

Formatul comprimat LZMA constă dintr-un flux comprimat de biți care este codificat folosind un codificator de interval binar adaptiv. Fluxul este împărțit în pachete. Fiecare pachet descrie fie un singur octet, fie o secvență LZ77. Lungimea și distanța fiecărui pachet sunt codificate implicit sau explicit.

Cele șapte tipuri de pachete sunt următoarele ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Cod împachetat (secvență de biți) |Numele pachetului |Descrierea pachetului|
---|---|---|
|0 + byteCode| LIT| Un singur octet codificat folosind un codificator de interval binar adaptiv.|
|1+0 + len + dist| MECI| O secvență tipică LZ77 care descrie lungimea și distanța secvenței.|
|1+1+0+0| SHORTREP| O secvență LZ77 de un octet. Distanța este egală cu ultima distanță LZ77 utilizată.|
|1+1+0+1 + len| LONGREP[0]| O secvență LZ77. Distanța este egală cu ultima distanță LZ77 utilizată.|
|1+1+1+0 + len| LONGREP[1]| O secvență LZ77. Distanța este egală cu ultima distanță LZ77 utilizată.|
|1+1+1+1+0 + len| LONGREP[2]| O secvență LZ77. Distanța este egală cu ultima distanță LZ77 utilizată.|
|1+1+1+1+1 + len| LONGREP[3]| O secvență LZ77. Distanța este egală cu ultima distanță LZ77 utilizată.|


## Referințe

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

