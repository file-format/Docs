{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo de lenguaje de marcado de dispositivo portátil",
  "description":"Obtenga más información sobre el formato de archivo HDML y las API que pueden crear y abrir archivos HDML",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## ¿Qué es un archivo HDML?

Un archivo con la extensión .hdml (Lenguaje de marcado de dispositivos portátiles) es un lenguaje de marcado para crear páginas web para dispositivos electrónicos portátiles, como computadoras portátiles, teléfonos inteligentes y dispositivos de visualización de información. Se dice que HDML es una extensión del lenguaje [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML es similar a HTML pero para dispositivos inalámbricos y de mano que tienen pantallas pequeñas como PDA, teléfonos móviles, etc. Fue reemplazado por WML para el cual actuó como una influencia importante.

## Formato de archivo HDML - Más información

HDML es un lenguaje de marcado para dispositivos portátiles que se basa en etiquetas de marcado similares a HTML. HDML se envió al W3C para su estandarización, pero nunca se convirtió en un estándar. Sin embargo, sus especificaciones de formato de archivo están disponibles en el [sitio web de W3] (https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) como referencia. La [sintaxis para lenguaje HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) está disponible para referencia del desarrollador y se puede usar para el desarrollo de aplicaciones de muestra.

## Elementos HDML

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

