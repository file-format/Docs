{
  "date" : "2020-01-10",
  "keywords" :[ "archivo otg", "formato de archivo otg", "qué es un archivo otg", "archivo", "ejemplo otg", "extensión de archivo otg","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG: formato de archivo de plantilla de dibujo de OpenDocument",
  "description":"Obtenga información sobre el formato de archivo OTG y las API que pueden crear y abrir archivos OTG",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## ¿Qué es un archivo OTG?

Un archivo OTG es una plantilla de dibujo que se crea utilizando el estándar OpenDocument que sigue las aplicaciones de Office OASIS [especificación 1.0](http://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0 -os.pdf). Representa la organización predeterminada de elementos de dibujo para una imagen vectorial que se puede utilizar para mejorar aún más el contenido del archivo. Los archivos OTF son como cualquier otro archivo basado en formato OpenDocument que se basa en formato XML para representar el contenido del documento. Los archivos OTF se pueden ver abriéndolos en cualquier editor de texto o XML estándar.

## Especificaciones de formato de archivo OTG ##

El formato de archivo OTG se basa en el formato XML de OpenDocument que tiene un esquema bien establecido. La estructura de cada componente de un formato OpenDocument está representada por un elemento que tiene atributos asociados y es común para todos los tipos de documentos, como un documento de texto, una hoja de cálculo o un archivo de dibujo. OTG, al ser una plantilla de dibujo, utiliza ampliamente las especificaciones de contenido de gráficos que incluyen:

* Funciones de página mejoradas para aplicaciones gráficas
* Formas de dibujo
* Marcos
* Formas 3D
* Forma personalizada
* Formas de presentación
* Animaciones de presentación
* Animaciones de presentación SMIL
* Eventos de presentación
* Presentar campos de texto
* Contenido del documento de presentación

### Funciones de página mejoradas para aplicaciones gráficas ###
#### Patrón de folletos ####

El elemento principal de folletos es una plantilla para generar automáticamente las páginas de folletos para aplicaciones que admiten la impresión de dichas páginas.
Los atributos que se pueden asociar con `<style:handout-master> ` elemento son:

|Diseño|Atributo|Descripción
---|---|---|
|Diseño de página de presentación|presentación:presentation-page-layout-name|Enlaces a `<style:presentation-page-layout> ` atributo
|Diseño de página|`estilo:nombre-diseño-de-página` | Especifica un diseño de página que contiene los tamaños, el borde y la orientación de la página maestra del documento.
|Estilo de página|`draw:style-name`|Asigna atributos de formato adicionales a la página maestra de un documento mediante la asignación de un estilo de página de dibujo.|
|Declaración de cabecera| `presentación:use-header-name`| Especifica el nombre de la declaración del campo de encabezado que se utiliza para todos los campos de encabezado que se muestran en la página maestra del documento.
|Declaración de pie de página| presentación:use-footer-name|Especifica el nombre de la declaración del campo de pie de página que se usa para todos los campos de pie de página que se muestran en la página maestra del documento.
|Declaración de fecha y hora|use-date-time-name|Especifica el nombre de la declaración de campo de fecha y hora que se usa para todos los campos de fecha y hora que se muestran en la página maestra del documento.

### Dibujar formas ###
El formato OpenDocument admite varias formas de dibujo que pueden ser utilizadas por cualquier tipo de documento.

|Forma|Atributos asociados| elementos
---|---|---|
Rectángulo - `<draw:rect> `|Posición, Tamaño, Estilo, Capa, Índice Z, Id., Id. de subtítulos, Anclaje de texto, fondo de tabla, Posición final del dibujo, Esquinas redondeadas|Título, Descripción larga, Oyentes de eventos, Puntos de unión, Texto
Línea `<draw:line> `|Estilo, Capa, Índice Z, Id., Id. de subtítulos y transformación, Ancla de texto, fondo de tabla, posición final del dibujo, Punto de inicio, Punto final|Título, Descripción larga, Oyentes de eventos, Puntos de unión, Texto
Polilínea `<draw:polyline> `| Posición, tamaño, cuadro de vista, estilo, capa, índice Z, ID, ID de título y transformación, anclaje de texto, fondo de tabla, posición final del dibujo, puntos | Título, descripción larga, detectores de eventos, puntos de unión, texto
Polígono `<draw:polygon> `|Posición, tamaño, cuadro de visualización, estilo, capa, índice Z, ID, ID de título y transformación, anclaje de texto, fondo de tabla, posición final del dibujo, puntos|Título, descripción larga, detectores de eventos, puntos de unión, texto
|Polígono regular `<draw:regular-polygon> `|Posición, tamaño, estilo, capa, índice Z, ID, ID de título y transformación, anclaje de texto, fondo de tabla, posición final del dibujo, cóncavo, esquinas, nitidez|Título, descripción larga, detectores de eventos, puntos de unión, texto
|Ruta `<draw:path> `|Posición, tamaño, cuadro de vista, estilo, capa, índice Z, ID, ID de título y transformación, ancla de texto, fondo de tabla, posición final del dibujo, datos de ruta| Título, descripción larga, detectores de eventos, puntos de unión, texto

### Marcos ###
Un marco, en un documento de dibujo, es un contenedor rectangular que contiene cuadros de texto, imágenes u objetos. Los marcos admiten características adicionales, como contornos, mapas de imágenes e hipervínculos. Un marco puede contener tanto un objeto como una imagen, lo que permite tener múltiples representaciones de un objeto. Las aplicaciones representan el elemento respectivo basado en el mejor soporte.

Los marcos pueden contener:
* Cajas de texto
* Objetos representados en formato OpenDocument o en un formato binario específico de objeto
* Imágenes
* applets
* Complementos
* Marcos flotantes

Un marco está contenido en un documento como se muestra a continuación.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Referencias ##
* [Formato de documento abierto de OASIS para aplicaciones de Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formato OpenDocument - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

