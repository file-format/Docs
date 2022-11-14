{
  "date" : "2019-10-11",
  "keywords" :[ "archivo qgs", "formato de archivo qgs", "qué es un archivo qgs", "archivo", "ejemplo de qgs", "extensión de archivo qgs","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Formato de archivo de proyecto QGIS",
  "description":"Obtenga información sobre el formato de archivo QGS y las API que pueden crear y abrir archivos QGS",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo QGS?

Un archivo con extensión .qgs es un archivo de proyecto creado con [QGIS](https://www.qgis.org/en/site/), que es una aplicación SIG multiplataforma de código abierto. Todas las configuraciones del proyecto, como propiedades de capa y datos auxiliares para el proyecto. Se crea cuando un proyecto de mapa se guarda en un disco. En realidad, es un archivo de configuración que conserva información como punteros a los datos GIS, información de estilo sobre las capas y el título del proyecto. Los archivos QGS se pueden abrir con el software QGIS que está disponible gratuitamente para descargar.

## Formato de archivo QGS

Los archivos QGS están en formato [XML](/es/web/xml/) y almacenan datos de proyectos como etiquetas XML. Un archivo QGS contiene información como:

* Título del Proyecto
* proyecto SRC
* el árbol de capas
* ajustes de ajuste
* relaciones
* la extensión del lienzo del mapa
* modelos de proyecto
* leyenda
* muelles mapview (2D y 3D)
* las capas con enlaces a los conjuntos de datos subyacentes (fuentes de datos) y otras propiedades de la capa, incluida la extensión, SRS, uniones, estilos, renderizador, modo de fusión, opacidad y más.
* propiedades del proyecto

### Etiquetas XML de nivel superior de QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Etiquetas de capa de proyecto de nivel superior extendidas

{{< figure src="../qgstoplevel.png" title="" >}}

## Referencias

* [QGIS](https://www.qgis.org/en/site/)

