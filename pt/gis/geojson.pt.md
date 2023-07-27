{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo geojson", "o que é um arquivo geojson", "arquivo", "exemplo geojson", "extensão de arquivo geojson","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Formato de arquivo geográfico baseado em JSON",
  "description":"Saiba mais sobre o formato de arquivo GeoJSON e APIs que podem criar e abrir arquivos GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GeoJSON?

GeoJSON é um formato baseado em JSON projetado para representar os recursos geográficos com seus atributos não espaciais. Este formato define diferentes objetos JSON (JavaScript Object Notation) e sua forma de junção. O formato JSON representa uma informação coletiva sobre os recursos geográficos, suas extensões espaciais e propriedades. Um objeto deste arquivo pode indicar uma geometria (Point, LineString, Polygon), uma feature ou coleção de features. Os recursos refletem endereços e lugares como ruas de pontos, estradas principais e fronteiras como sequências de linhas e países, províncias e regiões terrestres como polígonos. Usando o GeoJSON, diferentes aplicativos móveis de roteamento e navegação podem indicar a cobertura de seus serviços. Uma extensão do GeoJSON é o TopoJSON que é menor em tamanho e codifica a topologia geoespacial.

## Breve história ##

A Internet Engineering Task Force (IETF), em associação com os autores do formato, formou um [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) para lançar o GeoJSON em abril de 2015. Substituindo o 2008 Especificação GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), a nova especificação padrão do formato GeoJSON publicada em agosto de 2016.

## Formato de arquivo GeoJSON ##

### Coordenar ###

A coordenada é o elemento básico de qualquer dado geográfico. Esta é uma dimensão única (Longitude, latitude) que representa um único número (formato decimal) e às vezes também grava uma coordenada para elevação. O tempo também é uma dimensão, mas sua complexidade torna difícil registrá-lo como coordenado. As coordenadas em JSON GeoJSON são formatadas como números.

### Posição ###

Uma matriz ordenada de coordenadas representa a [posição](https://geojson.org/geojson-spec.html#positions). Esta é a menor unidade que pode indicar um ponto na Terra.

`[Longitude, latitude, elevação]`

Antes do lançamento da especificação atual, o GeoJSON permitia gravar três coordenadas por posição, mas não é permitido pela nova especificação.

### Geometria ###

Geometrias são formas simples (pontos, curvas e superfícies) em GeoJSON que consistem em um tipo e uma coleção de coordenadas. Ponto é a geometria mais simples que representa uma única posição

`{ "tipo": "Ponto", "coordenadas": [0, 0] }`

### LineStrings ###

Pelo menos dois lugares conectados são usados para representar uma linha.

`{ "type": "LineString", "coordinates": [[10, 30], [10, 10]] }`

Strings de ponto e linha são as duas categorias mais simples de geometria. Ambos os tipos de geometria não incomodam muitas regras geométricas. Um ponto pode ser representado em um lugar em qualquer lugar, e uma linha pode ter mais de um ponto, mesmo que os pontos sejam auto-cruzados.

### Polígonos ###

As geometrias GeoJSON parecem significativamente mais complexas em polígonos. Os polígonos têm áreas internas e externas e podem possuir buracos nesse interior.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

Em comparação com LineStrings, em polígonos, a lista de coordenadas é mais um nível aninhado e pode ter recortes como rosquinhas.

### Nível de coordenadas ###

No formato GeoJSON, para a propriedade de coordenadas, existem quatro níveis de profundidade.

### Características ###

As geometrias são a parte central do GeoJSON, portanto, os dados do mundo real são mais do que essas formas simples com identidade e atributos. Os recursos registram a geometria, bem como suas propriedades.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

As propriedades de um recurso podem ser um tipo de objeto [JSON](http://json.org/) contendo mapeamentos de valor-chave de profundidade única.

### Coleção de recursos ###

No nível superior dos arquivos GeoJSON, FeatureCollection é a coisa mais comum que se parece com:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Muitos pacotes de software de mapeamento e GIS suportam GeoJSON, incluindo GeoDjango, OpenLayers e software Geoforge. Também é compatível com PostGIS e Mapnik. Os serviços de API dos mapas do Google, yahoo e Bing também suportam GeoJSON.

## Referências ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Por Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

