{
  "date" : "2019-10-11",
  "keywords" :[ "archivo jp2", "formato de archivo jp2", "qué es un archivo jp2", "archivo", "ejemplo jp2", "extensión de archivo jp2","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Formato de archivo de imagen",
  "description":"Obtenga información sobre el formato de archivo JP2 y las API que pueden crear y abrir archivos JP2",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## ¿Qué es un archivo JP2? ##

JPEG 2000 (**JP2**) es un sistema de codificación de imágenes y un estándar de compresión de imágenes de última generación. Utiliza tecnología wavelet para codificar contenido sin pérdidas en cualquier calidad a la vez. Además, sin ninguna penalización sustancial en la eficiencia de la codificación, JPEG 2000 tiene la capacidad de acceder y decodificar el mismo contenido de manera eficaz en una variedad de otras resoluciones y calidades. Los flujos de código en JPEG 2000 son significativamente escalables y tienen regiones de interés que brindan la posibilidad de acceso aleatorio espacial.

JPEG 2000 destaca por ser uno de los estándares más escalables. Se pueden almacenar diferentes partes de una imagen usando diversas calidades. Se puede lograr una escalada de rendimiento notable ordenando el flujo de código en una variedad de formas. Sin embargo, JP2 requiere codificadores/decodificadores complejos y computacionalmente desafiantes, como resultado de esta flexibilidad. En comparación con JPEG, JPEG 2000 solo produce artefactos de timbre que forman anillos cerca del borde de la imagen y pueden verse borrosos, mientras que JPEG usa bloques de artefactos visuales de 8 × 8 que pueden ser artefactos de timbre y de bloqueo. Posee hasta 16384 componentes diversos con las dimensiones en terapixels y una precisión que puede llegar a 38 bits/muestra.

## Historia ##

En 2000, el comité del Grupo Conjunto de Expertos Fotográficos diseñó JP2 con el objetivo de mejorar su propio estándar JPEG basado en la transformada de coseno discreta con este nuevo método basado en wavelet. El comité de JPEG tenía como objetivo proporcionar sus métodos de referencia libres de tarifas de licencia. En la competencia de la licencia JP2 entre 20 empresas, ganaron por un pelo. JPEG 2000 se ha declarado como un estándar ISO, aunque la mayoría de los navegadores web no están listos para ayudar a JPEG 2000 desde 2017.

## Partes del sistema de codificación de imágenes JPEG 2000 ##

Las siguientes son las partes principales que constituyen el conjunto completo de estándares para JPEG 2000.


|Parte|Título|Descripción|Número
---|---|---|---|
|Parte 1|Sistema de codificación central| Define la sintaxis del flujo de código. Diferentes etapas involucradas en la decodificación de imágenes JPEG 2000. Explica el formato de archivo básico JP2, los metadatos y los derechos de propiedad intelectual que se deben proporcionar.|ISO/IEC 15444-1
|Parte 2|Extensiones|Define extensiones para flujo de código de formato de archivo y permite demostraciones de muestra HDR, especificación de espacio de color, recorte, transformaciones geométricas; diversas animaciones, metadatos y flujo de código múltiple.|ISO/IEC 15444-2
|Parte 3|Motion JPEG 2000 (MJ2 o MJP2)|Introduzca un formato de archivo para secuencias de movimiento, codificando imágenes en un flujo de código independiente.|ISO/IEC 15444-3
|Parte 4|Conformidad|Establece técnicas de prueba para codificar y decodificar y verifica archivos tanto para flujos de código desnudo como para archivos JP2.|ISO/IEC 15444-4
|Parte 5|Software de referencia|Se compone de dos paquetes de código fuente (Java, C) que implementan el sistema de codificación Core y están disponibles bajo licencias de código abierto.|ISO/IEC 15444-5
|Parte 6|Formato de archivo de imagen compuesto|Define el formato de archivo JPM y permite la creación de imágenes de documentos de varias páginas para aplicaciones similares a fax. Admite el uso de JBIG2 y JPEG.|ISO/IEC 15444-6
|Parte 8|JPEG 2000 Secured (JPSEC)|Garantiza la seguridad de las transacciones, los contenidos y las tecnologías, y permite flujos de bits JPEG 2000 seguros.|ISO/IEC 15444-8
|Parte 9|JPIP|Define herramientas en un entorno de red para acceder a metadatos e imágenes, y establece protocolos interactivos y eficientes|ISO/IEC 15444-9
|Parte 10|JP3D|Extensión volumétrica de la Parte 1 e introduce la dimensión Z. Amplía el concepto de teselas, bloques de código, recintos y características de accesibilidad de regiones de interés 3D.|ISO/IEC 15444-10
|Parte 11|JPWL|Trata de una transmisión bien organizada a través de una red inalámbrica propensa a errores. Esta extensión es compatible con decodificadores|ISO/IEC 15444-11
|Parte 13|Codificador de nivel de entrada|Define una implementación de codificador de nivel de entrada del sistema de codificación Core.|ISO/IEC 15444-13
|Parte 14|JPXML|Una representación en XML y explica los segmentos de marcador y los métodos para acceder a los datos internos de las imágenes.|ISO/IEC 15444-14
|Parte 15|HTJ2K (en desarrollo)|Especifica un algoritmo de codificación de bloques alternativo. Algorithm ofrece un rendimiento multiplicado por diez y codificación/descodificación sin pérdidas.|

## Formato de archivo JP2 ##

JPEG 2000 define el formato de archivo y el flujo de código de la misma manera que JPEG-1. Aunque las muestras de imágenes se describen exclusivamente en JPEG 2000, JPEG-1 incluye otra información adicional sobre el espacio de color y la resolución de lo esencial para codificar la imagen. Si una imagen se almacena como archivo JPEG 2000, **.jp2** se utiliza como extensión. Este formato de archivo mejora aún más con la extensión JPEG 2000 parte 2, que define los mecanismos de animación y la configuración de numerosos flujos de código en una sola imagen. La extensión **.jpx** se usa cuando las imágenes se guardan usando este formato de archivo extendido. Como no se considera que los datos del flujo de código se guarden principalmente en archivos, no se define una extensión estándar para este fin. Aunque para fines de prueba, con frecuencia obtiene la extensión **.jpc** o **.j2k**. A diferencia de JPEG-1, JPEG 2000 elige una forma diferente de codificar metadatos en formato XML. El estándar 12234-1.4 (del comité ISO TC42) se utiliza como referencia entre las etiquetas Exif y los componentes XML. JPEG 2000 puede contener un estándar ISO, XMP dentro.

### Trozos ###
Los archivos JPEG 2000 constan de fragmentos consecutivos. Cada fragmento tiene un encabezado de 8 bytes: tamaño de fragmento de 4 bytes (big-endian, byte alto primero) y tipo de fragmento de 4 bytes: una de las firmas predefinidas: "jP" o "jP2".

El segundo fragmento debe ser del tipo "ftyp" y tiene un subtipo en el desplazamiento 8. JPEG 2000 definido por subtipo que debe ser uno de los valores: "jp2" (tipo de archivo \*.JP2), "jp20" (archivo tipo \*.JPA), "jpm" (tipo de archivo \*.JPM), "jpx" (tipo de archivo \*.JPX).

Iterando fragmentos, hasta que se detecta un tipo desconocido, creamos un archivo de imagen/video JPEG 2000.

### Transformación de color ###

Inicialmente, se requiere la transformación de imágenes del espacio de color RGB a otro espacio de color. Para ello, existen dos formas: la Transformación de Color Irreversible (ICT) y la Transformación de Color Reversible (RCT). El primero usa espacio de color YC,,B,,C,,R, y tiene que implementarse en punto fijo/flotante, mientras que más tarde usa un espacio de color YUV modificado y de naturaleza reversible.// //No restringido al modelo RGB, JPEG El lenguaje 2000 utiliza la transformación de múltiples componentes.

### Embaldosado ###

Cuando se realiza la transformación de color, la imagen se convierte en regiones rectangulares llamadas mosaicos que se pueden transformar y codificar por separado. El tamaño de todos los mosaicos será el mismo o la imagen completa se puede considerar como un solo mosaico. El decodificador aprovecha el mosaico y consume menos memoria o puede codificar parcialmente algunos mosaicos. Aunque esta técnica tiene la desventaja de la degradación de la calidad de la imagen.

### Transformada wavelet ###

La imagen después del mosaico se transforma en wavelet que puede ser irreversible o reversible y se implementa mediante el uso del esquema de convolución o elevación.

### Índice de compresión ###

Dependiendo de las características físicas de una imagen, se obtiene una ganancia de compresión del 20% La predicción de redundancia espacial de JPEG 2000 juega un papel vital en el proceso de compresión y las imágenes de alta resolución tienden a obtener la mayor ventaja.

## Aplicaciones servidas por el estándar ##

* Grabación, edición y almacenamiento de videos HD basados en cuadros
* Imágenes médicas y biometría
* imágenes satelitales, teledetección y detección de movimiento
* Comunicación cliente/servidor, distribución y almacenamiento en red.
* Cine digital, contribución de alimentación de HDTV en vivo, material audiovisual digitalizado

## Referencias ##

* [Resumen de JPEG 2000](https://jpeg.org/jpeg2000)
* [Sistema de codificación de imágenes JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

