{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo qlr", "formato de arquivo qlr", "o que é um arquivo qlr", "arquivo", "exemplo qlr", "extensão de arquivo qlr", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - Arquivo de definição de camada QGIS",
  "description":"Saiba mais sobre o formato de arquivo QLR e APIs que podem criar e abrir arquivos QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## O que é um arquivo QLR?

Um arquivo com .qlr é um arquivo de definição de camada que contém um ponteiro para a fonte de dados da camada. Isso é um acréscimo às informações de estilo do [QGIS](https://www.qgis.org/en/site/) para a camada. Tendo referências a todos os estilos relacionados, este arquivo é usado como uma única fonte de dados a serem usados para obter as informações de estilo. Usando os arquivos QLR, as informações para as fontes de dados podem ser colocadas nesse único arquivo que pode ser lido por outros aplicativos para carregar as informações de estilo. Os arquivos QLR podem ser abertos com qualquer editor de texto, como o Notepad++.

## Formato de arquivo QLR

QLR, semelhante a [QGS](/pt/gis/qgs/), é um arquivo XML que contém ponteiros para fonte de dados de camada na forma de tags XML. É semelhante ao arquivo .lyr do ArcGIS. As tags de nível superior de um arquivo QML são mostradas na imagem abaixo.

{{< figure src="../qlr.png" title="" >}}

## Referências

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

