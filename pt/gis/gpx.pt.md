{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo gpx", "o que é um arquivo gpx", "arquivo", "exemplo gpx", "extensão de arquivo gpx", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Formato de arquivo de troca GPX",
  "description":"Saiba mais sobre o formato de arquivo GPX e APIs que podem criar e abrir arquivos GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GPX?

Arquivos com extensão GPX representam o formato GPS Exchange para troca de dados GPS entre aplicativos e serviços web na internet. É um formato de arquivo XML leve que contém dados de GPS, ou seja, waypoints, rotas e trilhas a serem importadas e vermelhas por vários programas. O formato de arquivo GPX é aberto e é suportado por vários aplicativos e dispositivos GPS. Os dados de GPS desses arquivos podem ser carregados para exibição em aplicativos de mapeamento para fins geoespaciais.

## Formato de arquivo GPX ##

Um arquivo GPX consiste em dados de localização de latitude e longitude, valores de elevação e outras informações possivelmente descritivas. Os dados de localização são expressos em graus decimais e a elevação é expressa em metros. A hora em um arquivo GPX está em Tempo Universal Coordenado (UTC) usando o formato ISO 8601. Os benefícios de usar um arquivo GPX são os seguintes:

* GPX permite trocar dados com uma lista crescente de programas para Windows, MacOS, Linux, Palm e PocketPC.
* GPX pode ser transformado em outros formatos de arquivo usando uma simples página da web ou programa conversor.
* GPX é baseado no padrão XML, então muitos dos novos programas que você usa (Microsoft Excel, por exemplo) podem ler arquivos GPX.
* O GPX torna fácil para qualquer pessoa na web desenvolver novos recursos que funcionarão instantaneamente com seus programas favoritos.

O [GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) mostra a representação do formato de arquivo GPX para referência.

### Dados essenciais ###

A seguir estão dados essenciais que fazem parte de um arquivo GPX para representação de dados GPS.

* **Waypoints**: Um waypoint é uma coordenada WGS84 (GPS) de um ponto e representa uma camada de feições do tipo OGR wkbPoint
* **Rotas**: representam uma camada de feições do tipo OGR wkbLineString. Inclui uma lista de pontos de trilha, que são waypoints que mostram uma curva ou pontos de estágio que levam a um destino
* **Tracks**: Tracks representam a camada de feições do tipo OGR wkbMultiLineString. É composto por pelo menos um segmento contendo waypoints em uma lista ordenada de pontos que descrevem um caminho. Consiste em uma lista de pontos de trilha que representam uma trilha GPS contínua.

### Arquivo de exemplo GPX ###

O arquivo GPX a seguir mostra a organização dos dados GPS em um arquivo GPX e pode dar uma boa ideia sobre o conteúdo de um arquivo GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Referências ##

* [Formato de arquivo GPX](https://www.topografix.com/gpx.asp)
* [GPX - Por Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

