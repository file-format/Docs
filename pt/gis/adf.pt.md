{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - Formato de Grade Binária ESRI ArcInfo",
  "description":"Saiba mais sobre o formato de arquivo ADF e APIs que podem criar e abrir arquivos ADF.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## O que é um arquivo ADF?

Um arquivo com extensão .adf é um formato de arquivo de dados raster usado por aplicativos de software ESRI, como ArcGIS, ArcView e ArcInfo. Os dados espaciais são armazenados como uma grade binária nativa do ESRI. A grade é composta de linhas e colunas de células que podem ser inteiras ou de ponto flutuante. Grades inteiras em um arquivo ADF representam dados discretos e grades de ponto flutuante representam dados contínuos. Outro formato de arquivo ESRI popular é o arquivo [SHP](/pt/gis/shp/) que representa informações geoespaciais na forma de dados vetoriais a serem usados por aplicativos de Sistemas de Informação Geográfica (GIS).

## Formato de arquivo ADF - Mais informações

Os arquivos ADF são salvos como arquivos binários no disco em uma grade binária. As grades inteiras têm atributos que são armazenados em uma tabela de atributos de valor (VAT). Cada valor único na grade tem um registro no IVA onde o registro armazena o valor único e o número de células na grade é representado por esse valor.

As grelhas de ponto flutuante não têm IVA.

### Estrutura de grade

Dentro do arquivo ADF, as grades são implementadas usando uma estrutura de dados raster lado a lado. A unidade básica dentro dessa estrutura de dados raster é um bloco retangular de células. Cada bloco é armazenado em disco e compactado em uma estrutura de arquivo de tamanho variável, chamada de bloco. Cada bloco é armazenado como um registro de comprimento variável.

Os rasters GRID são armazenados em áreas de trabalho, onde uma área de trabalho contém um subdiretório info e um subdiretório para cada GRID. Existem vários arquivos que atribuem dados de localização geográfica e dados para a grade correspondente. O subdiretório Info contém vários arquivos que mantêm certas informações sobre o GRID e outros conjuntos de dados, como coberturas, no espaço de trabalho.

## Referências ##

* [Formato de grade ESRI](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [FAQ: Qual é a estrutura do arquivo de um Arc/INFO Grid?](https://support.esri.com/en/technical-article/000008526)

