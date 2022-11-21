{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "arquivo", "extensão", "formato de arquivo", "Localização GPS", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Formato de arquivo de localização GPS",
  "description":"Saiba mais sobre o formato de arquivo LOC e APIs que podem criar e abrir arquivos LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## O que é um arquivo LOC?

Um arquivo com extensão .loc é um arquivo de localização GPS que contém localizações geoespaciais como waypoints. Um waypoint é um par de valores de Latitude-Longitude que se refere a um local usado por aplicativos do Sistema de Informações Geográficas (GIS). Programas de mapeamento GPS, como o DeLorme Topo, usam arquivos LOC para ler e exibir informações contidas nesses arquivos LOC como camadas selecionáveis pelos usuários finais. Além disso, eles são usados para trocar dados de GPS entre aplicativos. Os arquivos LOC podem ser abertos usando aplicativos como o [TopoGrafix EasyGPS](https://www.easygps.com/) que exibe o conteúdo desses arquivos como camadas e dados plotados no mapa na respectiva geolocalização.

## Formato de arquivo LOC - Mais informações

Os arquivos LOC têm semelhanças com os arquivos [GPX](/pt/gis/gpx/), mas são salvos em formatos diferentes. Estes são salvos como arquivos [XML](/pt/web/xml/) onde o conteúdo dos waypoints e informações associadas estão contidos em tags estruturadas. Como XML é uma linguagem generalizada para troca de dados entre diferentes aplicativos, isso facilita a troca de dados de LOC com outros aplicativos.

## Formato de arquivo LOC - Exemplo

A seguir está o cabeçalho e o texto de um waypoint de um arquivo LOC. Como pode ser visto, as informações do cabeçalho contêm a fonte de localização dos dados. O waypoint contém informações como o 'ID' e os dados de conteúdo associados ao waypoint. Finalmente, o waypoint é uma coleção de valores de latitude e longitude e o texto associado a este waypoint específico.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Referências

* [TopGraphic EasyGPS](https://www.easygps.com/)

