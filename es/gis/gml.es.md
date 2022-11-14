{
  "date" : "2019-10-11",
  "keywords" :[ "archivo gml", "qué es un archivo gml", "archivo", "ejemplo gml", "extensión de archivo gml","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Formato de archivo de lenguaje de marcado de geografía",
  "description":"Obtenga más información sobre el formato de archivo GML y las API que pueden crear y abrir archivos GML",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GML?

GML significa Geography Markup Language que se basa en especificaciones XML desarrolladas por Open Geospatial Consortium (OGC). El formato se utiliza para almacenar características de datos geográficos para el intercambio entre diferentes formatos de archivo. Sirve como un lenguaje de modelado para sistemas geográficos, así como un formato de intercambio abierto para transacciones geográficas en Internet.

## Formato de archivo GML ##

Como ocurre con la mayoría de las gramáticas basadas en XML, la gramática consta de dos partes: el esquema que describe el documento y el documento de instancia que contiene los datos reales. Un documento GML se describe mediante un esquema GML. Esto permite a los usuarios y desarrolladores describir conjuntos de datos geográficos genéricos que contienen puntos, líneas y polígonos. Usando esquemas de aplicación, los usuarios pueden hacer referencia a carreteras, autopistas y puentes en lugar de puntos, líneas y polígonos.

Vale la pena notar que GML no debe interpretarse para la representación de datos espaciales en mapas. La representación del contenido GML es diferente al propósito para el que se creó GML. En resumen, GML es similar a XML en el sentido de que solo se usa para contener los contenidos espaciales que pueden usar las aplicaciones de mapeo con fines de visualización.

### Formación de contenido en GML ###

GML representa datos espaciales utilizando características, que es una lista de propiedades y geometrías. Una propiedad tiene una descripción de nombre, tipo y valor. Las geometrías se componen de bloques de construcción básicos de geometría, tales como:

* puntos
* líneas
* curvas
* superficies y
* polígonos

Las versiones futuras de GML están planificadas para admitir geometría 3D, así como relaciones topológicas entre entidades.

La codificación GML ya permite funciones bastante complejas. Una característica puede, por ejemplo, estar compuesta de otras características. Por lo tanto, una característica única como un aeropuerto podría estar compuesta por otras características, como calles de rodaje, pistas, hangares y terminales aéreas. La geometría de una característica geográfica también puede estar compuesta por muchos elementos geométricos. Por lo tanto, una característica geométricamente compleja puede consistir en una combinación de tipos de geometría, incluidos puntos, cadenas de líneas y polígonos.

### Ejemplos ###

GML 1.0 y 2.0 codifican los objetos Polygons, Points y LineString de la siguiente manera:

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

## Referencias ##

* [Especificaciones GML](http://www.opengeospatial.org/standards/gml)
* [GML - Por Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

