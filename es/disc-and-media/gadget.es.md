{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo GADGET y las API que pueden crear y abrir archivos GADGET",
  "title" :"GADGET - Archivo de CD virtual",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## ¿Qué es un archivo GADGET?

Un archivo GADGET consiste en un pequeño programa de software que se ejecuta dentro de la barra lateral de Windows Vista o Windows 7. Comprime varios archivos basados en web y los archivos pueden comprender los archivos [.html](/es/web/html), [.css](/es/web/css) o [.js](/es/web/js/), así como otros archivos web. Los archivos GADGET se utilizan para componentes pequeños, como herramientas de búsqueda, fuentes de noticias, utilidades del sistema y juegos pequeños. Aunque los GADGET están alojados en la barra lateral, no son específicos del área de la barra lateral; estos se pueden desacoplar y mover al escritorio como se desee.

## Formato de archivo GADGET

El archivo GADGET es un archivo [ZIP](/es/compression/zip/) renombrado que contiene una colección de archivos HTML, XML, JScript y CSS (hojas de estilo en cascada). La instalación incluye descargar el archivo .gadget y habilitar el proceso de descarga para instalar el componente o guardar el archivo .gadget en el sistema local y hacer doble clic para iniciar el proceso de instalación.

Básicamente, un GADGET contiene dos archivos:

1. **Gadget.xml**: el manifiesto, un archivo XML que contiene información general de presentación y configuración del gadget.
2. **nombre.html**: un archivo HTML, en el que el nombre se especifica en el<name> etiqueta del manifiesto del gadget asociado, que proporciona el envoltorio para la interfaz de usuario del gadget y comprende la funcionalidad principal del gadget.

Se pueden ejecutar varias instancias de un archivo GADGET simultáneamente. Por ejemplo, si alguien quiere saber la hora en varias zonas horarias, puede ejecutar varias instancias del dispositivo de reloj configurando cada reloj en una zona horaria particular.

### Suspensión de GADGET

Dado que la plataforma Windows Sidebar en Windows 7 tiene vulnerabilidades graves, los Gadgets ya no están disponibles en el sitio web oficial de Microsoft. Posteriormente, Microsoft retiró esta función en versiones más recientes de Windows. GADGET podría explotarse para acceder a los archivos de una computadora, dañar una computadora, revelar contenido objetable o cambiar su comportamiento en cualquier momento.

## Referencias

* [Barra lateral de Windows: de Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Desarrollo de un gadget para Windows Sidebar Parte 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

