{
  "date" : "2019-10-11",
  "keywords" :[ "archivo dng", "formato de archivo dng", "qué es un archivo dng", "archivo", "ejemplo dng", "extensión de archivo dng","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Formato de archivo de imagen de cámara digital",
  "description":"Obtenga información sobre el formato de archivo DNG y las API que pueden crear y abrir archivos DNG",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DNG?

DNG es un formato de imagen de cámara digital utilizado para el almacenamiento de archivos sin procesar. Ha sido desarrollado por Adobe en septiembre de 2004. Fue desarrollado básicamente para fotografía digital. DNG es una extensión del formato estándar [TIFF](/es/image/tiff/)/EP y utiliza metadatos de manera significativa. Para manipular los datos sin procesar de las cámaras digitales con la facilidad de la flexibilidad y el control artístico, los fotógrafos optan por los archivos sin formato de cámara. Los formatos JPEG y TIFF almacenan imágenes que son procesadas por la cámara, por lo tanto, no hay mucho espacio para la alteración disponible en dichos formatos.

## Historia y versiones del formato de archivo DNG

Hasta ahora ha habido 5 versiones de la especificación DNG. La versión 1.0.0.0 se lanzó en septiembre de 2004 junto con el lanzamiento de "2.3" (ACR y DNG Converter). En febrero de 2005 se publicó la versión 1.1.0.0. En mayo de 2008 se lanzó la versión 1.2.0.0 y se usó en "4.4". La versión 1.3.0.0 se publicó en junio de 2009. La versión 1.4.0.0 apareció en 2012.

## Formato de archivo DNG

Mientras que los archivos RAW de cámara capturan datos sin procesar o poco procesados directamente desde el sensor. Como son similares a los negativos de película, los formatos RAW de cámara también se conocen como "negativos digitales". El beneficio de los formatos sin formato es el mayor control artístico para el usuario final. El usuario puede ajustar varios rangos de parámetros según los requisitos, como el balance de blancos, el mapeo de tonos, la reducción de ruido, la nitidez, etc. Por otro lado, el archivo RAW de cámara debe procesarse para cualquier uso a través de cualquier software o mediante un convertidor.

Como no había un formato estándar disponible para los archivos RAW de cámara, creaba múltiples problemas para el usuario final. Adobe abordó estos problemas y definió un formato no propietario para los archivos RAW de cámara. El formato se conoce como Negativo Digital o DNG. DNG puede ser utilizado por una amplia gama de hardware y software para el procesamiento de archivos sin formato. Además, DNG también se puede usar como un formato intermedio para almacenar imágenes que fueron capturadas originalmente por cámaras que tienen sus propios formatos sin procesar patentados.

### Especificaciones del formato de archivo DNG

En esta sección describiremos el formato DNG como una extensión de TIFF 6.0.

* **Extensiones de archivo**: DNG usa extensiones “.DNG” o “.TIF”.
* **Árboles SubIFD**: DNG no es compatible con cadenas SubIFD, en su lugar DNG recomienda el uso de árboles SubIFD como se menciona en las especificaciones TIFF-EP. La calidad y resolución más altas pueden usar NewSubFileType de 0, mientras que las miniaturas de calidad reducida deben usar NewSubFileType igual a 1. También se recomienda, aunque no es obligatorio, que el primer IFD tenga una miniatura de baja calidad o resolución.
* **Orden de bytes**: el orden de bytes debe ser compatible con lectores DNG, también para archivos de un modelo de cámara en particular.
* **Píxeles enmascarados**: la mayoría de los sensores de la cámara calculan los píxeles completamente enmascarados en el borde del sensor a través de la codificación negra. Estos píxeles se pueden incluir o recortar antes de que la imagen se almacene en formato DNG. Si los píxeles enmascarados no se recortan, el área de estos píxeles debe mencionarse en la etiqueta ActiveArea. La información recopilada de estos píxeles sobre el nivel de codificación de negro debe usarse antes de que se almacenen los datos sin procesar o puede incluirse en el archivo DNG que especifica el nivel de negro.
* **Píxeles defectuosos**: antes de almacenar datos sin procesar como DNG, se deben excluir los píxeles defectuosos.
* **Metadatos**: los metadatos se pueden incluir en DNG de cualquiera de las siguientes maneras:
** Mediante el uso de etiquetas de metadatos TIFF-EP o EXIF
** A través de la etiqueta de metadatos IPTC (33723)
** Usando la etiqueta de metadatos XMP (700)
* **Datos de propiedad**: normalmente, los proveedores incluyen datos de propiedad en un archivo sin formato para que los utilicen sus propios convertidores. DNG almacena sus datos de propiedad en etiquetas privadas, IFD privados y en una MakerNote privada. Los proveedores deben usar las etiquetas DNGPrivateData y MakerNoteSafety para asegurarse de que las aplicaciones que editan archivos DNG conserven estos datos de propiedad.

A continuación se presentan algunas restricciones importantes y extensiones de etiquetas TIFF.

**Bits por muestra**

Se admiten de 8 a 32 bits/muestra. Debe haber la misma profundidad para cada muestra cuando SamplesPerPixel no es igual a 1. Pero si BitsPerSample no es igual a 8, 16 o 32, entonces los bits deben empaquetarse en bytes usando el FillOrder predeterminado de TIFF de 1 (big-endian).

**Compresión**

Se admiten dos valores de etiquetas de compresión:

* Valor #1: Datos sin comprimir.
* Valor n.º 7: datos comprimidos en JPEG, ya sea DCT JPEG de referencia o compresión JPEG sin pérdidas.

**Interpretación fotométrica**

Los siguientes valores son compatibles solo con miniaturas y vistas previas de IFD:

* 1 = NegroEsCero. Se supone que está en un espacio de color gamma 2.2.
* 2 = RGB. Se supone que está en el espacio de color sRGB.
* 6 = YCbCr. Se utiliza para imágenes de vista previa codificadas en JPEG.

Los siguientes valores son compatibles con el IFD sin formato y se supone que son el espacio de color nativo de la cámara:

* 32803 # CFA (matriz de filtros de color).
* 34892 # LinealRaw.

**Orientación**

La etiqueta de orientación se utiliza para los exploradores de archivos para que puedan realizar una rotación sin pérdidas de archivos DNG. Los lectores de DNG deben admitir todas las orientaciones posibles, incluidas las orientaciones reflejadas.

## Características en la última versión de DNG

La versión 1.4 de DNG de octubre de 2012 tiene las siguientes características avanzadas.

* Recorte de usuario predeterminado
* Transparencia
* Punto flotante (HDR)
* Compresión con pérdida
* apoderados

## Referencias ##

* [Especificaciones DNG - Por Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Negativo digital - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG: el formato de archivo público para datos sin procesar de cámaras digitales](https://helpx.adobe.com/photoshop/digital-negative.html)

