{
  "date" : "2021-12-09",
  "keywords" :[ "aro","archivo .aro", "formato de archivo aro", "un tipo de archivo", "archivo", "tipo", "qué es un archivo .aro"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ARO - Archivo de aplicación web SteelArrow",
  "description" :"Obtenga información sobre qué es un archivo ARO y las API que pueden crear y abrir archivos ARO",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## ¿Qué es un archivo ARO?

Un archivo ARO es un archivo de página web del lado del servidor que se genera con la aplicación web SteelArrow. Contiene etiquetas y scripts [HTML](/es/web/html/) y SteelArrow. Estos se ejecutan en el servidor para generar una página de respuesta completa antes de enviarlos al navegador del usuario. Los archivos ARO contienen casi el 95% del contenido HTML, mientras que el resto consiste en código SteelArrow. Para que los archivos ARO funcionen para usted, el servidor de aplicaciones web SteelArrow debe estar instalado y ejecutándose en la máquina del servidor web.

## Formato de archivo ARO

Los archivos ARO están escritos en un archivo de lenguaje de marcado HTML con código JavaScript incrustado y applets de Java. [Etiquetas SteelArrow](http://www.steelarrow.com/docs/basics1.aro) son los componentes básicos para el desarrollo de páginas web. Aunque estos no cambian la visualización de la página, se utilizan para llenar la página con datos. Además, también se pueden usar para controlar la salida con declaraciones condicionales.

### Ejemplo de etiqueta ARO

los<SAOUTPUT> La etiqueta ARO permite a los desarrolladores generar valores de datos en cualquier lugar dentro de un script. Por ejemplo, se puede utilizar para obtener la salida de la tabla PARAM con<SAOUTPUT VALUE=PARAM[]> que se puede mostrar dentro del HTML<BODY> etiqueta.

## Referencias

* [Etiquetas SteelArrow](http://www.steelarrow.com/docs/basics.aro)

