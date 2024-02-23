{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo BIF - Formato de imagem de slide inteiro Ventana",
  "description":"Saiba mais sobre o formato de arquivo BIF e APIs que podem criar e abrir arquivos BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-pt",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## O que é um arquivo .BIF?

Um arquivo BIF é um arquivo de imagem raster que contém a imagem da amostra da lâmina. Consiste em várias imagens TIFF que são combinadas por aplicativos de visualização de slides em uma única imagem composta. Os arquivos BIF são criados pelo scanner digital de slides da Ventana Medical Systems e são totalmente compatíveis com a variante BigTIFF da definição [TIFF](/image/tiff/) v 6.0.

## Formato de arquivo BIF

Um arquivo BIF é salvo como um arquivo de imagem binário e consiste em até 200.000 x 200.000 pixels. Isso pode levar a arquivos grandes, quebrando o limite de tamanho de 4 GB imposto pelos ponteiros de arquivo de 32 bits definidos pelo padrão TIF. Com ponteiros de arquivo de 64 bits, entretanto, essa barreira de tamanho de arquivo é superada pela variante BigTIFF do padrão TIFF.

### Quem usa o arquivo BIF?

Os arquivos BIF são usados por scanners digitais de lâminas para digitalizar e criar cópias digitais de amostras de lâminas. Se você for patologista, poderá abrir esses arquivos BIF em aplicativos de visualização de slides. Com grande nível de detalhes e dados de alta resolução, você pode ampliar e reduzir uma imagem de slide para visualizar seções de amostra com mais ou menos detalhes. O arquivo de metadados [XML](/web/xml/) presente nesses arquivos define como as imagens devem ser combinadas e a imagem que deve ser usada como miniatura do arquivo.

## Como abrir o arquivo BIF?

Você pode abrir arquivos BIF com:

 * OpenSlide (plataforma cruzada)
 * ImageJ (plataforma cruzada)
 * Visualizador NetScope (Windows)

## Referências ##

 * [Documento técnico BIF da Roche Digital Pathology](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

