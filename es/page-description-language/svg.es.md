{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "archivo", "formato de archivo", "Lenguaje de descripción de página", "Escalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo SVG y las API que pueden crear y abrir archivos SVG",
  "title" :"¿Qué es un archivo SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## ¿Qué es un archivo SVG? ##

Un archivo SVG es un archivo de gráficos vectoriales escalares que utiliza un formato de texto basado en XML para describir la apariencia de una imagen. La palabra escalable se refiere al hecho de que el SVG se puede escalar a diferentes tamaños sin perder calidad. La descripción basada en texto de tales archivos los hace independientes de la resolución. Es uno de los formatos más utilizados para construir un sitio web e imprimir gráficos para lograr escalabilidad. Sin embargo, el formato solo se puede usar para gráficos bidimensionales. Los archivos SVG se pueden ver/abrir en casi todos los navegadores modernos, incluidos Chrome, Internet Explorer, Firefox y Safari.

## Breve historia ##

Las especificaciones SVG están disponibles como estándar abierto por World Wide Web Consortium (W3C) desde 1999. Antes de esto, se enviaron al W3C especificaciones de formato de archivo similares en seis formatos diferentes hasta 1998. Se aplicó una actualización a las especificaciones en 2011 y se realizó la versión 1.1 . En 2016, SVG 2 se publicó como una versión más nueva que incluye funciones adicionales a las de SVG 1.1.

## Especificaciones de formato de archivo ##

El Modelo de Objetos de Documento (DOM) SVG sienta las bases para todas las especificaciones e interfaces que corresponden a las secciones particulares de las especificaciones. Los visores de SVG deben implementar las interfaces SVG DOM como se define en las especificaciones del W3C. Su DOM expone varias interfaces para diferentes tipos de datos y elementos.

### formas SVG ###

SVG tiene algunos elementos de forma predefinidos que los desarrolladores pueden usar:

* Rectángulo<rect>
* Circulo<circle>
* Elipse<ellipse>
* Línea<line>
* Polilínea<polyline>
* Polígono<polygon>
* Sendero<path>

Según estas formas y especificaciones, las áreas funcionales de SVG son las siguientes.

**Rutas**: las rutas se utilizan para representar contornos de formas simples y compuestas. Los códigos se utilizan para definir la naturaleza de la operación. Por ejemplo, M se usa para Mover a, L se usa para Línea a, Z se usa para cerrar una ruta, etc.

**Formas básicas**: se pueden dibujar rutas en línea recta y rutas formadas por una serie de segmentos de línea recta conectados (polilíneas), así como polígonos cerrados, círculos y elipses. Los rectángulos y los rectángulos de esquinas redondeadas también son elementos estándar.

**Texto**: la representación de texto se expresa como datos de caracteres XML donde se pueden aplicar muchos efectos visuales al texto. Las especificaciones permiten manejar texto bidireccional, texto vertical y caracteres a lo largo de una ruta curva.

**Pintura**: las formas se pueden rellenar y/o delinear con un color, un degradado o un patrón, lo que permite volverlas opacas o tener algún grado de transparencia. Las características de final de línea, como puntas de flecha o símbolos que aparecen en los vértices de un polígono, se representan mediante marcadores.

**Color**: las especificaciones de SVG permiten aplicar colores a todos los elementos SVG visibles, ya sea directamente o mediante relleno, trazo y otras propiedades. Se pueden usar diferentes códigos de color para especificar como negro o azul, representación hexadecimal, decimal o como porcentajes de la forma RGB.

**Degradados y patrones**: las formas en un archivo SVG se pueden rellenar o delinear con colores sólidos, degradados o patrones repetitivos.

**Efectos de filtro**: en realidad, se trata de una serie de operaciones gráficas que se aplican a un gráfico vectorial de origen dado para producir un resultado modificado.

**Interactividad**: los usuarios pueden interactuar con archivos SVG cambiando el enfoque, haciendo clic con el mouse, desplazando o haciendo zoom en la imagen. La interactividad permite que las imágenes SVG interactúen con los usuarios de muchas maneras diferentes, como se mencionó anteriormente.

**Enlaces**: es posible que las imágenes SVG tengan hipervínculos a otros documentos. Esto se logra a través del lenguaje de vinculación XML o XLink. Esto permite crear estados de vista específicos que se utilizan para acercar o alejar un área específica o para limitar la vista a un elemento específico.

**Secuencias de comandos**: similar a HTML, todos los aspectos de un documento SVG son accesibles para su manipulación mediante secuencias de comandos. Los objetos SVG DOM proporcionan la guía para lograr esto usando el elemento y atributo SVG. Los scripts están encerrados en elementos de etiqueta `script` y pueden ejecutarse en respuesta a eventos de puntero, teclado o documento según sea necesario.

**Animación** - Los elementos DOM<animate> ,<animateMotion> y<animateColor> le permite incluir animación para contenidos SVG. Por supuesto, esto no se puede lograr sin usar scripts y temporizadores integrados. Estas animaciones pueden ser continuas y pueden ponerse en bucle, así como repeticiones, al mismo tiempo que responden a los eventos del usuario.

**Fuentes**: el texto en SVG puede hacer referencia a archivos de fuentes externas, como fuentes del sistema. En ausencia de dichas fuentes, el texto en SVG no se representará en la salida. Esto se puede solucionar incorporando los glifos requeridos en un archivo como una fuente que luego se renderiza usando el<text> elemento.

## Ejemplos ##
Las siguientes líneas muestran cómo se representa un círculo utilizando el script SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Las siguientes líneas de código muestran cómo usar el<text> bloque para renderizar texto a SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referencias ##

* [Especificaciones W3C SVG](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

