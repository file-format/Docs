{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "archivo", "extensión", "formato de archivo", "implementación de hta", "Guía de programación", "ejemplo de hta", "Aplicación HTML", "Aplicación de lenguaje de marcado de hipertexto", "Archivos HTA", "Aplicación HTML de Microsoft"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - Archivos de aplicación HTML",
  "description":"Obtenga información sobre el formato de archivo HTA y las API que pueden crear y abrir archivos HTA",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## ¿Qué es un archivo HTA?

HTMLA significa **Aplicación de lenguaje de marcado de hipertexto** y es un programa compatible con Microsoft Windows. El código fuente de este programa incluye más de un lenguaje de secuencias de comandos como [HTML](/es/web/html/) y [JavaScript](/es/web/js/). Para la interfaz de usuario, se prefiere una aplicación HTML, mientras que para cumplir con los requisitos de la lógica del programa se utiliza cualquier otro lenguaje de secuencias de comandos.

Una aplicación HTML es independiente del modelo de seguridad del navegador de Internet y se ejecuta como una aplicación totalmente confiable. La extensión utilizada para los archivos relacionados con estas aplicaciones es HTA. Estas aplicaciones incluyen funciones de HTML junto con las propiedades de otros lenguajes de secuencias de comandos.


## Breve historia ##

El HTA fue introducido por primera vez en 1999 por Microsoft junto con el lanzamiento de Internet Explorer 5. Era compatible con Internet Explorer y, por lo tanto, solo podía ejecutarse en el sistema operativo Windows. Esta tecnología fue patentada en 2003. Los archivos HTA se ejecutan de forma similar a cualquier otro archivo .exe. Los archivos HTA también son compatibles con la versión actualizada actual de Windows 11.


## Especificación técnica ##

Las HTA tienen el mismo formato que cualquier otra página HTML, mientras que algunos atributos se utilizan para controlar los estilos de los bordes o los iconos de los programas. Además, se proporcionan argumentos para el lanzamiento de HTA. Estas aplicaciones se pueden ejecutar usando un programa llamado mshta.exe. Se puede acceder simplemente haciendo doble clic en el archivo. Estos programas se ejecutan automáticamente junto con Internet Explorer. Además de otras especificaciones, estas no son independientes del motor de navegación Trident sino de Internet Explorer. Significa que estos se pueden ejecutar sin utilizar Internet Explorer.

Las etiquetas se utilizan para personalizar la apariencia de estas aplicaciones. La conversión de la aplicación HTML de Microsoft al formato HTA es más fácil, es decir, solo necesita cambiar la extensión. Como sabemos que estas aplicaciones son totalmente confiables, comprenden más funciones y ventajas en comparación con los archivos HTML simples. Los editores de texto se pueden utilizar para crear HTA. Estos editores pueden ser adquiridos por Microsoft o cualquier otra fuente confiable.


## Ejemplo de formato de archivo HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Referencia ##

* [HTA - por Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



