{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo OAM: formato de archivo del widget Adobe Edge Animate",
  "description" :"Obtenga información sobre qué es un archivo OAM y las API que pueden crear y abrir archivos OAM.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## ¿Qué es un archivo OAM?

Un archivo .oam y un archivo de widget animado exportado desde Adobe Edge Animate Widget. Las animaciones exportadas como formato de archivo de widget OAM se pueden insertar en otras aplicaciones de Adobe, como InDesign Documents ([archivo INDD](/es/page-description-language/indd/), Dreamweaver y Muse. Los archivos OAM son como paquetes de implementación que se pueden implementar fácilmente. insertado en otros proyectos de Adobe para utilizarlos. Los archivos OAM contienen información sobre los activos, comportamientos y código ActionScript de la animación. Puede crear un archivo OAM publicando un proyecto de Adobe Animate [archivo .AN](/es/web/an/) .
Los usuarios pueden crear archivos OAM publicándolos desde un proyecto de Edge Animate (archivo .AN).

## Formato de archivo OAM

Un archivo OAM se guarda en el disco como archivo comprimido [ZIP](/es/compression/zip/). Esto implica que puede cambiar el nombre de la extensión del archivo a .zip y extraerlo con cualquier utilidad de compresión como WinZIP o WinRAR. El tamaño reducido del archivo hace que sea más fácil transferir y compartir la animación con otros usuarios a través de Internet.

### Estructura de archivos OAM

La estructura de archivos interna de un archivo .oam es propietaria y Adobe no la documenta públicamente. Sin embargo, se sabe que los archivos .oam contienen una colección de archivos y recursos (como gráficos, audio y código ActionScript) empaquetados en un solo archivo. El contenido de un archivo .oam puede incluir archivos [XML](/es/web/xml/), archivos SWF y otros archivos de recursos. La estructura exacta del archivo .oam depende de la versión específica de Adobe Animate utilizada para crearlo, así como del tipo de animación y recursos incluidos en el archivo.

Un archivo OAM contiene la siguiente información.

`Activos:` Información sobre los recursos de gráficos, audio y video utilizados en la animación.

`Comportamientos:` Descripciones de las acciones e interacciones que ocurren en la animación.

`Código ActionScript:` El código utilizado para controlar el comportamiento y la interactividad de la animación.

`Configuración de publicación:` Información sobre la plataforma y formato en el que se publicará la animación, como HTML5 o AIR.

`Metadatos:` Información adicional como el autor de la animación, la fecha de creación y el número de versión.

## ¿Cómo abrir un archivo OAM?

Puede utilizar las siguientes aplicaciones para abrir archivos OAM.

* Adobe Edge Animate CC (descontinuado)
* Adobe Animar 2023
*Adobe InDesign 2023
*Adobe Dreamweaver 2021

## Referencias

* [Publicación OAM](https://helpx.adobe.com/animate/using/OAM-publishing.html)

