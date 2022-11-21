{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo CPG - Arquivo de página de código ESRI",
  "description":"Saiba mais sobre o formato de arquivo CPG e APIs que podem criar e abrir arquivos CPG.",
  "linktitle" : "CPG",
  "menu" : {
    "docs" : {
      "identifier":"system-cpg",
      "parent" : "system"
}
},
  "lastmod" : "2022-09-01"
}

## O que é um arquivo CPG?

Um arquivo CPG é um arquivo opcional necessário ao ESRI Shapefile que é usado para especificar a página de código para identificar o conjunto de caracteres a ser usado. Estes são armazenados em formato de arquivo de texto simples e contém informações sobre a codificação aplicada para criar o shapefile. Caso um arquivo CPG não esteja disponível, o shapefile usa a codificação padrão do sistema. Um arquivo CPG, se presente, deve ter o mesmo prefixo do arquivo [SHP](/pt/gis/shp/), por exemplo, estradas.shp, estradas.cpg.

Os arquivos CPG podem ser abertos com o ESRI ArcGIS Pro.

### Formato de arquivo CPG - Mais informações

Ao visualizar um shapefile no ArcCatalog ou qualquer outro aplicativo ArcGIS, você vê apenas o shapefile. Mas, na realidade, o shapefile usa outros arquivos associados que são lidos ao lado do arquivo de forma principal. O arquivo CPG também é um deles se estiver presente ao lado do arquivo SHP principal.

## Referências

* [Extensões de arquivo Shapefile
](https://desktop.arcgis.com/en/arcmap/10.3/manage-data/shapefiles/shapefile-file-extensions.htm)

