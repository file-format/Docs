{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo lz", "formato de arquivo lz", "o que é um arquivo lz", "arquivo", "exemplo lz", "extensão de arquivo lz", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Formato de arquivo compactado Lzip",
  "description":"Saiba mais sobre o formato de arquivo LZ e APIs que podem criar e abrir arquivos LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## O que é um arquivo LZ?

Um arquivo com extensão .lz é um arquivo compactado criado com Lzip, que é uma ferramenta de linha de comando gratuita para compactação. Ele suporta concatenação para compactar arquivos de suporte. Os arquivos LZ têm o tipo de mídia application/lzip e suportam taxas de compactação mais altas que [BZ2](/pt/compression/bz2/). LZ são baseados no algoritmo LZMA (cadeia de Lempel-Ziv-Markov) e incluem uma soma de verificação CRC de 32 bits e bytes de identificação para verificar a integridade do arquivo.

## Formato compactado LZMA

O formato compactado LZMA consiste em um fluxo compactado de bits que é codificado usando o codificador de intervalo binário adaptável. O fluxo é dividido em pacotes. Cada pacote descreve um único byte ou uma sequência LZ77. O comprimento e a distância de cada pacote são codificados implícita ou explicitamente.

Os sete tipos de pacotes são os seguintes ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Código empacotado (sequência de bits) |Nome do pacote |Descrição do pacote|
---|---|---|
|0 + byteCode| LIT| Um único byte codificado usando um codificador de intervalo binário adaptável.|
|1+0 + len + dist| CORRESP| Uma sequência LZ77 típica descrevendo o comprimento e a distância da sequência.|
|1+1+0+0| CURTO| Uma sequência LZ77 de um byte. A distância é igual à última distância LZ77 usada.|
|1+1+0+1 + len| LONGO[0]| Uma sequência LZ77. A distância é igual à última distância LZ77 usada.|
|1+1+1+0 + len| LONGO[1]| Uma sequência LZ77. A distância é igual à penúltima distância LZ77 usada.|
|1+1+1+1+0 + len| LONGO[2]| Uma sequência LZ77. A distância é igual à terceira última distância LZ77 usada.|
|1+1+1+1+1 + len| LONGO[3]| Uma sequência LZ77. A distância é igual à quarta última distância LZ77 usada.|


## Referências

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

