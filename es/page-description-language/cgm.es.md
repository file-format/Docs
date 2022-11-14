{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Metarchivo de gráficos de computadora", "Archivo", "Extensión", "Formato de archivo", "Gráficos vectoriales", "Descriptor de metarchivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo CGM",
  "description":"Obtenga información sobre el formato de archivo CGM y las API que pueden crear y abrir archivos CGM",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo CGM? ##

Computer Graphics Metafile (CGM) es un formato de metarchivo estándar internacional gratuito, independiente de la plataforma para almacenar e intercambiar gráficos vectoriales (2D), gráficos rasterizados y texto. CGM utiliza un enfoque orientado a objetos y muchas funciones para la producción de imágenes. CGM utiliza estas características orientadas a objetos para remodelar elementos gráficos para representar una imagen. Un metarchivo contiene la información necesaria que define otros archivos. En CGM, un archivo fuente basado en texto contiene todos los elementos gráficos que luego se pueden compilar en un archivo binario. Básicamente, CGM es una forma de facilitar el intercambio de datos gráficos 2D, independientemente de cualquier plataforma o dispositivo en particular.

El formato CGM proporciona diferentes elementos para realizar funciones y significar objetos para ajustar primitivas geométricas e información gráfica. Aunque CGM ha sido reemplazado por otros formatos para mostrar artes gráficas en páginas web, ya que no es compatible con páginas web, sigue siendo muy popular entre aplicaciones industriales, aeronáuticas y otras aplicaciones técnicas. Aunque World Wide Web Consortium ha desarrollado WebCGM, un enfoque alternativo para el uso de CGM en la Web. La implementación principal de CGM fue una ilustración de la secuencia de operaciones básicas del Sistema de Kernel Gráfico (GKS). No se ha adoptado mucho en los diseños profesionales, pero ha sido reemplazado en gran medida por otros formatos como DXF y SVG.

## Historia ##

CGM resultó ser un estándar internacional en 1987 (ISO 8632-1987) y también fue adoptado como estándar nacional en el Reino Unido por BSI y en EE. UU. por ANSI. Después de una serie de modificaciones en 1991, se publicó una norma revisada de CGM en 1992 (ISO 8632:1992). En 2001, World Wide Web Consortium desarrolló WebCGM con capacidad mejorada para ser utilizado con las páginas web. En 2007 se lanzó la segunda versión de WebCGM y la tercera versión se lanzó en 2010 con capacidades mejoradas.

## Formato de archivo CGM ##

Los metarchivos de gráficos por computadora son básicamente bases de datos para información gráfica y proporcionan los medios para la captura, el almacenamiento y la transmisión de datos gráficos. En consecuencia, debe haber un componente de sistema gráfico para crear la base de datos simultáneamente con la ejecución de una aplicación en un formato de metarchivo. En la mayoría de los casos, este componente es el generador de metarchivos. Además, existe la necesidad de otro componente que pueda obtener, interpretar y representar datos gráficos en un metarchivo. Esta necesidad se satisface con la presencia de un intérprete de metarchivo. La figura siguiente representa el entorno de trabajo del metarchivo gráfico.

La relación de CGM con otros componentes de un sistema gráfico típico se ilustra en la figura anterior. También es evidente a partir de la figura que la funcionalidad del metarchivo no depende de la salida del dispositivo final.

Generalmente, hay dos categorías de metarchivo: **captura de sección** y **captura de imagen**. La funcionalidad principal del metarchivo de captura de imágenes es la captura de múltiples definiciones de imágenes independientes del dispositivo. Mientras que los metarchivos de captura de sesión utilizan la interfaz del sistema para capturar el diálogo de salida en un sistema gráfico. CGM pertenece a la categoría de metarchivos de captura de imágenes estáticas. CGM proporciona una disposición bien organizada de componentes con una estructura de dos niveles.

1. Descriptor de metarchivo
1. Un conjunto de imágenes lógicamente independientes

Cada imagen es una colección de descriptores de imagen y un cuerpo de imagen que incluye una definición de imagen. El descriptor de metarchivo define información descriptiva que se aplica por igual a todas las imágenes de ese metarchivo. Esta información ayuda al intérprete a analizar correctamente un metarchivo y reconocer los recursos necesarios para la representación correcta de una imagen. Aunque el descriptor de la imagen también encierra la información descriptiva, solo puede reconocer la imagen en la que reside el descriptor. En este formato de archivo, cada definición de imagen es autónoma y lógicamente soberana. Son independientes de todas las demás definiciones de imagen en un archivo. Inmediatamente después de la interpretación del metadescriptor, se puede acceder a las imágenes e interpretarlas aleatoriamente. El cambio en el estado de las imágenes anteriores no tiene efecto en sus sucesoras. Esta independencia de imagen es otra característica destacada de CGM. CGM consiste en un espacio de coordenadas que son coordenadas cartesianas 2D llamadas coordenadas de dispositivo virtual y se pueden representar a través de números o precisión que representan el rango y la granularidad. CGM especifica tanto la selección directa de colores como la selección basada en índices. En el primero, el especificador de color consta de un triple RGB, mientras que más tarde, el especificador de color indica un índice en una tabla de colores.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
