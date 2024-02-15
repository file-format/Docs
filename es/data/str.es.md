{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo STR - Archivo de objetos de lista de estructura de dBASE - ¿Qué es el archivo .str y cómo abrirlo?",
  "description" : "Obtenga más información sobre el archivo de objetos de lista de estructuras STR dBASE y cómo abrirlo.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-es-str",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## ¿Qué es un archivo STR?

El formato de archivo STR se asocia comúnmente con dBASE, un sistema de gestión de bases de datos. En dBASE, un archivo .str normalmente representa un archivo de objeto de lista de estructura. Este archivo contiene la estructura de una tabla de base de datos, incluida información sobre campos (columnas) y sus propiedades.

El archivo de objetos de lista de estructura (.str) contiene metadatos como nombres de campos, tipos de datos, longitudes de campos y cualquier otra propiedad asociada con cada campo en la tabla de la base de datos. Se utiliza para definir la estructura de la tabla de la base de datos sin contener registros de datos reales.

Programas como dBASE u otras herramientas de administración de bases de datos pueden utilizar este archivo para comprender el diseño de la tabla de la base de datos y realizar operaciones como consultar, actualizar o crear nuevos registros basados en esta estructura.

A continuación se muestra un ejemplo básico de lo que puede contener un archivo STR:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Este ejemplo describe una tabla con cuatro campos: ID, nombre, edad y fecha de nacimiento, junto con sus respectivos tipos de datos y longitudes.

## ¿Cómo abrir el archivo STR?

La forma principal de abrir archivos .str es mediante el propio dBASE, especialmente en los sistemas operativos Windows. dBASE es capaz de leer e interpretar el contenido de estos archivos, permitiendo a los usuarios ver y trabajar con la estructura de la base de datos.

Dado que los archivos .str son esencialmente archivos de texto sin formato que contienen información sobre la estructura de la base de datos, también puedes abrirlos usando un editor de texto. Ejemplos de editores de texto incluyen Microsoft Notepad en Windows y Apple TextEdit en Mac. Cuando se abre en un editor de texto, podrá ver el contenido del archivo, incluidos los nombres de los campos, los tipos de datos y otra información estructural, en un formato legible por humanos.

## Referencias
* [dBase](https://en.wikipedia.org/wiki/DBase)


