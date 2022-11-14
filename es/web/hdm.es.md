{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM File - Handheld Device Markup Language File",
  "description":"Obtenga información sobre el formato de archivo HDM y las API que pueden crear y abrir archivos HDM",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## ¿Qué es un archivo HDM?

Un archivo HDM es un archivo de página web de lenguaje de marcas que se crea en el Lenguaje de marcas de dispositivos portátiles (HDML). Contiene etiquetas de marcado similares al lenguaje [HTML](/es/web/html/), pero está diseñado para dispositivos electrónicos portátiles como teléfonos inteligentes y PDA. Las [especificaciones del formato de archivo HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) se enviaron al W3C para su estandarización, pero no pudieron convertirse en un estándar. HDM se basa en las especificaciones de formato de archivo [HDML](/es/web/hdml/) disponibles en el sitio web de W3.

## Formato de archivo HDM - Más información

El archivo HDM consta de etiquetas de marcado que se representan en un sitio web diseñado visualmente en dispositivos portátiles. Los archivos HDM se copian en dispositivos que utilizan el protocolo HDTP (Protocolo de transporte de dispositivos portátiles) en lugar del protocolo HTTP que se utiliza para las páginas HTML.

## Elementos del archivo HDML

A continuación se muestra una lista de elementos que proporcionan un entorno de tiempo de ejecución para HDML y se denomina agente de usuario.

|Elemento|Descripción|
---|---|
|Tarjetas|Este es el bloque de construcción fundamental de HDML, y muestra y permite al usuario interactuar con tarjetas de información. |
|Mazos|Las tarjetas HDML se agrupan en mazos. Una plataforma HDML es similar a una página HTML en que se identifica por URL [RFC1738] y es la unidad de contenido solicitada de un servidor y almacenada en caché por el agente de usuario.|
|Acciones|Las acciones pueden ser de tipo PREV, SOFT1-SOFT8 y HELP. Estos son abstractos y se admiten en la interfaz de usuario de una manera específica de agente de usuario.|
|Actividades|Una actividad es como un grupo de tarjetas relacionadas que realizan una función lógica. Estos pueden abarcar una o más cubiertas. El modelo de estado y navegación HDML está estructurado en torno a actividades.|
|Navegación basada en historial|El agente de usuario mantiene un historial de las tarjetas mostradas al usuario. Cada tarjeta a la que se accede se agrega al historial de tarjetas. El agente de usuario permite que el usuario vuelva fácilmente a la tarjeta anterior en el historial.|

## Referencias

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Especificaciones HDML - Escuelas W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

