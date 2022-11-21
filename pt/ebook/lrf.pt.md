{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "arquivo", "extensão", "formato", "eBook", "livro digital" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo LRF e APIs que podem criar e abrir arquivos LRF.",
  "title" :"Formato de arquivo LRF - Um arquivo de leitor portátil da Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## O que é um arquivo LRF?

Um arquivo com extensão .lrf é um arquivo eBook de banda larga (BBeB) que contém dados para um Sony BBeB, incluindo texto, imagens e dados de paginação. O arquivo é salvo em um formato binário compactado que contém um cabeçalho, um número especificado de objetos e um índice de objeto. Os arquivos LRF e LRX incluem os dois formatos de livro BBeB disponíveis. Os arquivos LRF não são criptografados e podem ser compilados a partir de arquivos [LRX](/pt/ebook/lrf/). Os arquivos LRF podem ser convertidos de vários outros tipos de arquivos, incluindo PDF e HTML. Se o seu computador não conseguir abrir o arquivo LRF, provavelmente você não possui o software instalado para abrir ou editar os arquivos LRF. Os programas que podem abrir arquivos LRF são Caliber, BookDesigner, Makelrf e Canon Book Creator para Windows, Calibre para Linux, Calibre e Sony Reader para Macintosh.

## Breve história

O tipo de arquivo LRF é principalmente associado ao Line Rider por [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). O Line Rider é um brinquedo de física da internet e foi inventado em setembro de 2006 por um estudante universitário esloveno, Boštjan Čadež. Os eBooks da marca Sony (como leitores Sony PRS-500 e Sony Librie) utilizam a extensão de arquivo LRF para seus documentos e textos. Esse tipo de arquivo proprietário agora está obsoleto, assim como os arquivos LRS e LRX relacionados. Esses três tipos de arquivos compuseram o eBook BroadBand (BBeB), que foi descontinuado em 2010, quando a Sony começou a vender seus ebooks no formato EPUB.

## Formato de arquivo LRF

Especificações detalhadas do formato de arquivo LRF estão disponíveis em [arquivo da web](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Um arquivo LRF consiste em:
* um cabeçalho
* vários objetos
* um índice de objeto.

Todos esses valores estão na ordem Intel (LSB primeiro).

### Cabeçalho LRF

|Deslocamento (hex) |Tamanho(bytes) |Nome/significado| Valor de exemplo|
---|---|---|---|
|0 |8| Assinatura LRF| 4C 00 52 00 46 00 00 00 = "LRF" em Unicode|
|8 |2| versão?| 999 na maioria dos arquivos|
|A |2| "Psuedo-Criptografia" |key byte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NúmeroDeObjetos |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| desconhecido| 0|
|24 |1| Bandeiras| (16 - de trás para frente, 1 = de frente para trás) 16|
|25 |1| desconhecido |(preenchimento?) 0|
|26 |2| desconhecido| 1600|
|28 |2| desconhecido| (preenchimento?) 0|
|2A |2| Altura?| 600|
|2C |2| Largura?| 800|
|2E |1| desconhecido| 24|
|2F |1| desconhecido |(preenchimento?) 0|
|30 |0x14| desconhecido| zeros|
|44 |4| ID do objeto apenas do objeto PlaneStream (0x1E)| 0x0042|
|48 |4| desconhecido |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referências

* [Formato de arquivo LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Por Wikipedia](https://en.wikipedia.org/wiki/BBeB)

