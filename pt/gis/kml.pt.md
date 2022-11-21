{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo kml", "o que é um arquivo kml", "arquivo", "exemplo kml", "extensão de arquivo kml", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Linguagem de marcação Keyhole",
  "description":"Saiba mais sobre o formato de arquivo KML e as APIs que podem criar e abrir arquivos KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo KML?

KML, Keyhole Markup Language) contém informações geoespaciais em notação XML. Os arquivos salvos como KML podem ser abertos em aplicativos do Sistema de Informações Geográficas (GIS), desde que sejam compatíveis. Muitos aplicativos começaram a fornecer suporte para o formato de arquivo KML depois que ele foi adotado como padrão internacional. O KML usa uma estrutura baseada em tags com elementos e atributos aninhados. Todas as tags diferenciam maiúsculas de minúsculas e é importante seguir a ordem dessas tags, conforme a referência [KML](https://developers.google.com/kml/documentation/kmlreference).

## Breve história ##

O KML foi originalmente desenvolvido para uso com o Google Earth, originalmente conhecido como Keyhole Earth Viewer. O KLM foi adotado como padrão internacional em 2008 pelo Open Geospatial Consortium em 2008. Como o formato foi desenvolvido para uso com o Google Earth, ele tem a distinção de ser o primeiro a visualizar e editar arquivos KML. Com o passar do tempo, agora há cada vez mais projetos que oferecem suporte para formatos de arquivo KML, incluindo várias APIs em diferentes idiomas.

## Especificações de formato de arquivo KML ##

A Referência KML é um guia completo de referência para ter as especificações completas de formato de arquivo. Um arquivo KML padrão consiste em:

* Marcadores
* HTML descritivo em marcadores
* Sobreposições de solo
* Caminhos
* Polígonos

Além disso, uma versão avançada do arquivo KML pode ter:

* Estilos para geometria
* Estilos para ícones destacados
* Sobreposições de tela
* Links de rede

Cada elemento KML tem informações de longa duração que localizam geograficamente as informações presentes no arquivo. No entanto, pode haver parâmetros adicionais, como direção, altitude e inclinação.

### Marcas de lugar ###

É usado para representar uma posição na superfície da Terra e é identificado pela<Point> elemento. Veja a seguir um exemplo de como um marcador é representado no arquivo KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML descritivo em marcadores ###

Informações adicionais podem ser associadas a um marcador que aprimora ainda mais a representação do marcador. Essas informações incluem links, tamanhos de fonte, estilos e cores. Além disso, também inclui alinhamento de texto e tabelas para fazer parte do marcador.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Sobreposições de solo ###

Estes representam as camadas de uma imagem na superfície da Terra. o<icon> elment contém o link para o arquivo de imagem de sobreposição.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Caminhos ###

Os caminhos são representados por<LineString> elemento que é uma coleção de pares lat-long. Com eles, muitos tipos diferentes de caminhos podem ser criados no Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Referência espacial no arquivo KML ##

As informações contidas em qualquer arquivo geoespacial sobre geolocalizações podem ter significados diferentes sem informações de referência espacial. Por padrão, as referências espaciais do arquivo KML são definidas pelo World Geodetic System de 1984, WGS84.

## Referências ##

* [Referência KML](https://developers.google.com/kml/documentation/kmlreference)
* [Tutorial do desenvolvedor do Google para KML](https://developers.google.com/kml/documentation/kml_tut)
* [Formato de arquivo KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

