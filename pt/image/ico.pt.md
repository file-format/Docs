{
  "date" : "2019-10-11",
  "keywords" :[ "ico file", "ico file format", "o que é um ico file", "file", "ico example", "ico file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo ICO e APIs que podem criar e abrir arquivos ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo ICO?

Arquivos com extensão ICO são tipos de arquivos de imagem usados como ícone para representação de um aplicativo no [Microsoft Windows](https://www.microsoft.com/en-us/windows). Eles vêm em diferentes tamanhos, suporte a cores e resolução para atender aos requisitos da tela. Outro formato de arquivo de imagem semelhante no Microsoft Windows é [CUR](/pt/image/cur/) para representação do cursor e define um ponto de acesso no cabeçalho da imagem. No MacOS, os formatos de arquivo ICNS têm a mesma finalidade dos arquivos ICO. Vários sites on-line, bem como aplicativos, fornecem o recurso de criar esses arquivos e converter outros formatos de imagem, como [BMP](/pt/image/bmp/), [PNG](/pt/image/png/), etc. para o formato de arquivo de ícone. O tipo de mídia oficial da Internet registrado pela IANA para arquivos ICO é image/vnd.microsoft.icon.

## Breve história ##

Os ícones foram introduzidos com o lançamento do Microsoft Windows 1.0. Estes eram 32x32 em tamanho e eram monocromáticos. Com a chegada do win32, foi introduzido suporte para imagens de ícones em cores verdadeiras com até 256x256 pixels de dimensão. O Windows XP foi o primeiro a fornecer suporte para imagens de ícones coloridos de 32 bits, permitindo que áreas semitransparentes como sombras, anti-aliasing e efeitos semelhantes a vidro fossem adicionados ao ícone. A Microsoft só recomendou tamanhos de ícone de até 48×48 pixels para Windows XP. O Windows Vista adicionou uma visualização de ícone de 256 × 256 pixels ao Windows Explorer, bem como suporte para o formato compactado [PNG](/pt/image/png/). Com usuários usando resoluções mais altas e modos de alta DPI, formatos de ícone maiores (como 256×256) são recomendados.

## Formato de arquivo ICO ##

Um único arquivo ICO consiste em uma ou mais imagens pequenas de vários tamanhos e profundidades de cor. A presença de imagens de vários tamanhos é para dimensionamento apropriado em diferentes resoluções de tela. Todos os valores nos arquivos ICO/CUR são representados na ordem de bytes [little-endian](https://en.wikipedia.org/wiki/Little-endian).

O arquivo ICO consiste em um cabeçalho de ícone, um diretório de ícones,

|Campo|Descrição
---|---|
|Icon Header|Armazena informações gerais sobre o arquivo ICO.
|Diretório[1..n]|Armazena informações gerais sobre cada imagem no arquivo.
|Ícone #1|Os "dados" reais para a primeira imagem no formato antigo AND/XOR DIB ou PNG mais recente
|...|
|Ícone #n|Dados para a última imagem do ícone

### Cabeçalho ###

|Deslocamento|Tamanho (em bytes)|Propósito
---|---|---|
|0|2|Reservado. Deve ser sempre 0.
|2|2|Especifica o tipo de imagem: 1 para imagem de ícone (.ICO), 2 para imagem de cursor (.CUR). Outros valores são inválidos.
|4|2|Especifica o número de imagens no arquivo.

### Diretório ###

O diretório contido em um arquivo ICO, representado como estrutura ICONDIR, contém uma estrutura ICONDIRECTORY para cada imagem no arquivo. O mesmo é seguido por um bloco contíguo de todos os dados de bitmap de imagem. Isto é como mostrado abaixo.

|Deslocamento|Tamanho|Descrição
---|---|---|
|0 (0)|1|Largura, deve ser 0 se 256 pixels
|1 (1)|1|Altura, deve ser 0 se 256 pixels
|2 (2)|1|Contagem de cores, deve ser 0 se mais de 256 cores
|3 (3)|1|Reservado, deve ser 0
|4 (4)|2|Planos de cor quando em formato .ICO, devem ser 0 ou 1, ou o hotspot X quando em formato .CUR
|6 (6)|2|Bits por pixel quando em formato .ICO, ou o hotspot Y quando em formato .CUR
|8 (8)|4|Tamanho dos dados de bitmap em bytes.
|12 (C)|4|Deslocamento no arquivo.

## Referências ##

* [ICO - Por Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

