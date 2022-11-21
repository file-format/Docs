{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo kmz", "o que é um arquivo kmz", "arquivo", "exemplo kmz", "extensão de arquivo kmz","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Formato de arquivo compactado KML",
  "description":"Saiba mais sobre o formato de arquivo KMZ e APIs que podem criar e abrir arquivos KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo KMZ?

O arquivo KMZ (KML Zipped) é uma representação do arquivo compactado [KML](/pt/gis/kml/) que contém informações geoespaciais visíveis em aplicativos GIS como o Google Earth. As informações sobre marcadores são representadas no arquivo como latitude e longitude junto com um nome personalizado. O único arquivo KMZ empacotado pode ser facilmente compartilhado com outros usuários. Os arquivos KMZ podem incluir dados de modelo 3D também para representação geográfica do modelo. Um arquivo KMZ pode ser aberto no Google Maps salvando o arquivo em um local online e digitando o URL na caixa Pesquisa do Google Maps.

## Estrutura do arquivo ##

O conteúdo de um arquivo MKZ consiste em um arquivo KML principal e zero ou mais arquivos associados. Ele pode ser extraído usando um utilitário de descompactação padrão como o WinZIP. O formato de arquivo KMZ também é compactado em um arquivo com taxa de compactação de 10:1. Você pode exportar dados do Google Earth como aplicativos diretamente para o formato de arquivo KMZ. O arquivo KML principal é denominado **doc.kml**. Ao empacotar um arquivo KMZ, mais de um arquivo KML pode ser adicionado a ele, mas isso não trará nenhum benefício, pois o Google Earth pesquisa o primeiro arquivo KML ao abrir o arquivo KMZ e o lê. Ele ignora quaisquer outros arquivos KML encontrados no arquivo. Para garantir que o arquivo KML desejado seja lido pelo Google Earth, recomenda-se colocar apenas um único arquivo KML dentro do arquivo KMZ.

As imagens, modelos, texturas, arquivos de som e outros recursos referenciados no arquivo doc.kml são colocados em outra subpasta dentro da pasta principal. Isso também pode envolver alguma complexidade, dependendo do número de arquivos de suporte. Links para esses recursos constituintes podem ser referência relativa ou por meio de referência absoluta.

### Referência relativa ###

Quando os recursos são colocados ao lado do doc.kml principal dentro de uma subpasta dentro da pasta principal, a referência relativa pode apontar para esses arquivos de suporte conforme mostrado no exemplo a seguir (apenas para ícone).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Referência absoluta ###

Os recursos também podem ser referenciados absolutamente. As referências absolutas contêm o URL completo do arquivo vinculado. Quando os arquivos são postados em um servidor central, a referência absoluta garante que eles permaneçam inequívocos em comparação com a referência relativa. O arquivo local não é recomendado para ser referenciado absolutamente, pois esses links serão quebrados quando os arquivos forem movidos para um novo sistema. Um exemplo de referência absoluta é o seguinte:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Veja também ##

* [GeoJSON](/pt/gis/geojson/)

## Referências ##

* [Arquivos do Google Earth e KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

