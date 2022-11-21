{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extensão", "arquivo", "formato", "imagem", "Imagem do ícone da Apple", "macOS", "Apple", "Ícone" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Imagem do ícone da Apple",
  "description":"Saiba mais sobre o formato de arquivo ICNS e APIs que podem criar e abrir arquivos ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo ICNS? ##

Um formato de ícone usado por programas macOS é chamado de arquivo ICNS. Permite bandas alfa de 1 e 8 bits e salva uma ou mais imagens, geralmente feitas de documentos [PNG](/pt/image/png). O ícone do programa no navegador e na interface do macOS é exibido usando arquivos ICNS.

Com base na localização, o mesmo ícone de estilo pode ter várias configurações. O formato ICNS sofreu inúmeras alterações e evoluiu até o ponto em que agora pode ser usado como base para vários formatos compatíveis. Aqui estão alguns outros pontos importantes que você precisa saber:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource e Mac OS icons Resource são alguns dos outros nomes.
* Para informações de ícone, é usada uma fonte na ramificação de recursos.
* Na maioria dos casos, um arquivo contém várias imagens. 1612 pixels quadrados e 1024, 512, 256, 128, 48, 32 e 16 pixels quadrados são tamanhos de imagem suportados.


## Formato de arquivo ICNS ##

O formato de dados ICNS é uma cápsula para uma ou mais imagens, suportando bandas de 1 bit e vários estados de imagem.
O sistema operacional pode redimensionar imagens de ícones para caber no tamanho de exibição necessário. As imagens de ícones maiores são normalmente salvas como arquivos [JPEG](/pt/image/jpeg/) 2000 ou [PNG](/pt/image/png). Um tipo de arquivos ICNS compactados e não compactados é possível.

Um cabeçalho e dados de ícone binário compõem a estrutura de um arquivo ICNS. O cabeçalho contém 8 bytes de dados, quatro dos quais são o literal mágico e quatro são o comprimento do arquivo. O tipo e o tamanho de cada imagem de ícone são armazenados na seção de dados de ícone, que é seguida pelos dados de imagem binária. O tamanho da imagem determina o tamanho da seção binária.

## Especificação Técnica ##

### Cabeçalho ###

|Deslocamento|Tamanho|Objetivo
---|---|---|
|0|4|Literal mágico, deve ser "icns" (0x69, 0x63, 0x6e, 0x73)
|4|4|Comprimento do arquivo, em bytes, msb primeiro


### Dados do ícone ###

|Deslocamento|Tamanho|Objetivo
---|---|---|
|0|4|Tipo de ícone
|4|4|Comprimento dos dados, em bytes (incluindo tipo e comprimento), msb primeiro
|8|Variável|Dados do ícone

### Compressão ###

Os dados de pixel são compactados até certo ponto. Os pixels de 32 bits ("is32", "il32", "ih32", "it32") e ARGB ("ic04", "ic05") geralmente são compactados (por canal) de maneira semelhante aos PackBits.

|Valor do Lead|Tail Bytes|Resultado (descompactado)
---|---|---|
|0 - 127|1 - 128|1 - 128 Bytes
|128 - 255|1 Byte|3 - 130 Cópias

## Referência ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

