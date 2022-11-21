{
  "date" : "2019-12-09",
  "keywords" :[ "arquivo zl", "formato de arquivo zl", "o que é um arquivo zl", "arquivo", "exemplo zl", "extensão de arquivo zl", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - Formato de arquivo compactado ZLIP",
  "description":"Saiba mais sobre o formato de arquivo ZL e APIs que podem criar e abrir arquivos ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## O que é um arquivo ZL?

Um arquivo com extensão .zl é um formato de arquivo compactado ZLIP que usa uma variante do algoritmo de compactação DEFLATE para compactar arquivos. É independente do tipo de CPU, sistema operacional, sistema de arquivos e conjunto de caracteres e, portanto, pode ser usado para troca de informações. As especificações técnicas da compactação ZLIP estão disponíveis no [site da IETF](https://tools.ietf.org/html/rfc1950) e podem ser consultadas do ponto de vista do desenvolvedor.

## Formato de arquivo ZL

Um fluxo zlib tem a seguinte estrutura:

* `CMF (Compression Method and flags)` - Este byte é dividido em um método de compressão de 4 bits e um campo de informação de 4 bits dependendo do método de compressão.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Método de compressão)` - Identifica o método de compressão utilizado no arquivo. Seus valores e o método de compactação correspondente são os seguintes.

| Valor CM| Compressão|
|---|---|
|CM = 8|DEFLATE com tamanho de janela de até 32K|
|CM = 15|Reservado|

* `CINFO (Informações de compressão)` - Para CM = 8, CINFO é o logaritmo de base 2 do tamanho da janela LZ77, menos oito (CINFO=7 indica um tamanho de janela de 32K).

* `FLG (FLaGs)` - Este byte de flag é dividido da seguinte forma:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referências ##

* [Especificações de formato de arquivo Zlib](https://tools.ietf.org/html/rfc1950)

