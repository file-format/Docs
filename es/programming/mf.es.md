{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Formato de archivo de manifiesto de Java",
  "description":"Obtenga información sobre el formato de archivo MF y las API que pueden crear y abrir archivos MF",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo MF?

Un archivo con la extensión .mf es un archivo de manifiesto de Java que contiene información sobre las entradas individuales del archivo [JAR](/es/programming/jar/). El archivo MF en sí está contenido dentro del archivo JAR y proporciona toda la definición relacionada con la extensión y el paquete. Los archivos JAR se pueden producir para usarse como un archivo ejecutable. En tal caso, el archivo mainfest especifica la clase principal de la aplicación que contiene la declaración **`public static void main`**. Los archivos de manifiesto se denominan MANIFEST.MF y se pueden abrir con cualquier editor de texto en los sistemas operativos Windows, MacOS y Linux.

## Especificaciones de formato de archivo de manifiesto

Las [especificaciones de formato de archivo de manifiesto] (https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) están disponibles en Oracle en su guía para el formato de archivo JAR. Un archivo de manifiesto se compone de secciones principales seguidas de una lista de secciones para entradas de archivos JAR individuales. Cada sección sigue algunas reglas y restricciones.

### Secciones principales

Una sección principal:

* contiene información sobre seguridad y configuración sobre el archivo JAR
* contiene información sobre la aplicación o extensión de la que forma parte el archivo JAR
* define los atributos principales para cada elemento de manifiesto individual

**Nota**: Ningún atributo en esta sección puede llamarse "Nombre".

### Secciones individuales

Una sección individual define varios atributos para paquetes o archivos de un archivo JAR. Cada sección debe comenzar con un atributo llamado "Nombre" cuyo valor debe ser una ruta relativa al archivo o una URL absoluta que haga referencia a datos fuera del archivo.

### Especificaciones del manifiesto

|Atributos|Descripción|
---|---|
|archivo-manifiesto|sección principal nueva línea *sección-individual|
|sección-principal|versión-info nueva línea *atributo-principal|
|información-versión|Versión-manifiesto: número-versión|
|número-versión|dígito+{.dígito+}*|
|atributo principal|(cualquier atributo principal legítimo) salto de línea|
|sección-individual|Nombre: valor nueva línea *perentry-attribute|
|perentry-attribute|(cualquier atributo de perentry legítimo) nueva línea|
|nueva línea|CR LF | FL | CR (no seguido de LF)|
|dígito|{0-9}|

## Referencias

* [Oracle - Formato de archivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Formato de archivo JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Ellos%20están%20construidos%20en%20la,jar%20archivo%20extensión.)

