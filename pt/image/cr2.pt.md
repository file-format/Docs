{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo CR2 - arquivo de imagem Canon Raw 2",
  "description":"Saiba mais sobre o formato de arquivo CR2 e APIs que podem criar e abrir arquivos CR2.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## O que é um arquivo CR2?

Um arquivo CR2 (Camera RAW 2) é um arquivo de imagem RAW criado por câmeras digitais Canon. Ele armazena os dados de imagem sem perdas originais não processados capturados pela câmera. O formato de arquivo CR2 foi desenvolvido pela Canon para suas câmeras digitais e pode gravar imagens de alta qualidade de até 14 bits de RGB. Isso produz imagens de alta qualidade com espaço suficiente para pós-processamento. O formato de imagem CR2 tem sido usado pela Canon em seus modelos de câmera 350D, 20D e 1D. Os arquivos CR2 são arquivos RAW e contêm informações de metadados adicionais, como informações da câmera, informações da lente, informações de bracketing, balanço de branco e outras configurações.

## Formato de arquivo CR2

Os arquivos CR2 são armazenados no cartão de memória da câmera como arquivos binários no formato de arquivo proprietário da Canon. O formato de arquivo CR2 substituiu o formato de arquivo CRW usado inicialmente e foi substituído pelo formato de arquivo Canon RAW 3 posteriormente. O formato de arquivo CR2 é baseado nas especificações [TIFF](/pt/image/tiff/) que possui 4 Diretórios de Arquivos de Imagem (IFDs).

|Deslocamento |Conteúdo |Comentário|
---|---|---|
|0x0000 |Cabeçalho |contém a ordenação dos bytes, a versão e o deslocamento para a imagem RAW|
|calculado |IFD#0 |esta parte contém a seção Exif, que contém a seção Makernotes.
Informações sobre a imagem#0|
|computado |imagem#0 |versão pequena da imagem (um quarto do tamanho da original), compactada em Jpeg|
|calculado |IFD#1 |Informações sobre a imagem#1.|
|computado |imagem#1 |versão pequena da imagem, compactada em Jpeg|
|calculado |IFD#2 |Informações sobre a imagem#2.|
|computado |imagem#2 |versão pequena da imagem, não compactada|
|no cabeçalho| IFD#3| Informações sobre a imagem nº 3, a imagem RAW de dimensão total|
|computado |imagem#3 |Dados de imagem RAW, compactados sem perdas em Jpeg (não dados RGB!)|

## Vantagem do formato de arquivo CR2

Armazenar imagens no formato RAW permite muito pós-processamento para a fotografia, como o ajuste do Balanço de Branco. Isso é muito mais difícil e com uma grande perda de qualidade com outros formatos de arquivo de imagem, como [JPEG](/pt/image/jpeg/).

## O CR2 é melhor que o JPEG?

Os arquivos CR2 são arquivos brutos sem perda de dados e, portanto, sem perda de qualidade. JPEG, por outro lado, é um formato de arquivo de imagem com perdas, pois perde alguns dados para reduzir o arquivo. Assim, os arquivos CR2 são de alta qualidade e mais adequados para retoques e aprimoramentos.

## Referências

* [Formato de arquivo CR2](http://lclevy.free.fr/cr2/)

