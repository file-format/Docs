{
  "date" : "2021-07-30",
  "keywords" :[ "archivo dlg", "formato de archivo dlg", "qué es un archivo dlg", "archivo", "ejemplo de dlg", "extensión de archivo dlg","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Formato de índice de forma de archivo Shapefile",
  "description":"Obtenga más información sobre el formato de archivo DLG y las API que pueden crear y abrir archivos DLG",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## ¿Qué es un archivo DLG?
Un archivo con extensión .dlg contiene el gráfico lineal digital, que es una característica de mapa cartográfico que se muestra en forma de vector digital y que es administrado por el Servicio Geológico de EE. UU. (USGS). Los archivos DLG están disponibles en dos formatos diferentes:
1. **Formato opcional**: un formato fácil de usar que incorpora una longitud de registro lógico de 80 bytes, el sistema de coordenadas terrestres UTM y enlaces de topología contenidos en elementos de línea, nodo y área.
2. **Formato estándar de transferencia de datos espaciales (SDTS)**: un formato que facilita la transferencia de datos espaciales entre diferentes sistemas informáticos.

## Formato de archivo DLG
El formato de archivo DLG está diseñado para mapas USGS y se transmiten en escala grande, intermedia y pequeña con hasta nueve categorías diferentes de características. Los archivos DLG vienen en formatos opcionales y estándar de transferencia de datos espaciales (SDTS) que tienen una estructura topológica para su uso en aplicaciones GIS y de mapeo.
### Especificaciones del formato de archivo DLG
Los archivos DLG se distribuyen en tres escalas diferentes:

1. **Gran escala** - normalmente corresponde a:
- El USGS 7,5 por 7,5 minutos
- Serie de mapas cuadrangulares topográficos a escala 1:24 000 y 1:25 000
- Escala 1:63,360 para Alaska
- Escala 1:30,000 para Puerto Rico
 

2. **Escala intermedia** - derivada del USGS:

- 30 por 60 minutos

- Serie de mapas a escala 1:100.000
3. **Pequeña escala**: derivado de los mapas seccionales a escala 1:2,000,000 del USGS del Atlas Nacional de los Estados Unidos
### Categorías de datos
Nueve categorías diferentes de capas o funciones están disponibles en los archivos DLG:
1. Sistema de Topografía de Tierras Públicas (PLSS)
2. Límites (BD)
3. Transporte (TR)
4. Hidrografía (HY)
5. Hipsografía (HP)
6. Rasgos no vegetativos (NV)
7. Control de levantamiento y marcadores (SM)

8. Características artificiales (MS)

9. Cobertura superficial vegetal (SC)

Los archivos DLG a gran escala ofrecen las nueve capas, mientras que los de escala intermedia ofrecen las cinco capas de PLSS, BD, TR, HY y HP. Los DLG a pequeña escala ofrecen las cinco capas de PLSS, BD, TR, HY y MS.

## Referencias

* [Gráfico lineal digital - por Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


