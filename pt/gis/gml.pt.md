{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo gml", "o que é um arquivo gml", "arquivo", "exemplo gml", "extensão de arquivo gml", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Formato de arquivo de linguagem de marcação geográfica",
  "description":"Saiba mais sobre o formato de arquivo GML e as APIs que podem criar e abrir arquivos GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GML?

GML significa Geography Markup Language que é baseada em especificações XML desenvolvidas pelo Open Geospatial Consortium (OGC). O formato é usado para armazenar recursos de dados geográficos para intercâmbio entre diferentes formatos de arquivo. Ele serve como uma linguagem de modelagem para sistemas geográficos, bem como um formato de intercâmbio aberto para transações geográficas na internet.

## Formato de arquivo GML ##

Como na maioria das gramáticas baseadas em XML, há duas partes na gramática – o esquema que descreve o documento e o documento de instância que contém os dados reais. Um documento GML é descrito usando um esquema GML. Isso permite que usuários e desenvolvedores descrevam conjuntos de dados geográficos genéricos que contêm pontos, linhas e polígonos. Usando esquemas de aplicativos, os usuários podem se referir a estradas, rodovias e pontes em vez de pontos, linhas e polígonos.

Vale a pena notar que GML não deve ser interpretado para representação de dados espaciais em mapas. A representação do conteúdo GML é diferente da finalidade para a qual o GML foi criado. Em resumo, GML é semelhante ao XML, pois é usado apenas para conter o conteúdo espacial que pode ser usado por aplicativos de mapeamento para fins de exibição.

### Formação de conteúdo em GML ###

GML representa dados espaciais usando recursos que são uma lista de propriedades e geometrias. Uma Propriedade tem um nome, tipo e descrição de valor. As geometrias são compostas de blocos de construção de geometria básica, como:

* pontos
* linhas
* curvas
*superfícies e
* polígonos

As futuras versões do GML estão planejadas para suportar geometria 3D, bem como relacionamentos topológicos entre recursos.

A codificação GML já permite recursos bastante complexos. Um recurso pode, por exemplo, ser composto de outros recursos. Um único recurso como um aeroporto pode, assim, ser composto por outros recursos, como pistas de táxi, pistas, hangares e terminais aéreos. A geometria de uma feição geográfica também pode ser composta por muitos elementos geométricos. Um recurso geometricamente complexo pode, portanto, consistir em uma mistura de tipos de geometria, incluindo pontos, sequências de linhas e polígonos.

### Exemplos ###

GML 1.0 e 2.0 codificam objetos Polygons, Points e LineString da seguinte forma:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referências ##

* [Especificações GML](https://www.ogc.org/standard/gml/)
* [GML - Por Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

