{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","qué es un archivo jar","cómo abrir un archivo jar", "extensión", "archivo", "archivo jar","formato de archivo jar", "extensión .jar " ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Formato de archivo de archivo de Java",
  "description":"Obtenga información sobre el formato de archivo JAR y las API que pueden crear y abrir un archivo JAR",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo JAR?

Un archivo con la extensión .jar es un archivo Java Archive que contiene muchos archivos diferentes relacionados con aplicaciones como un solo archivo. Este formato de archivo se creó para reducir la velocidad de carga de un subprograma Java descargado en el navegador a través de una transacción HTTP, evitando crear múltiples conexiones HTTP. Un solo archivo JAR puede contener archivos de clase Java ([.clase](/es/programming/clase/)), [imágenes](/es/image/) y [sonidos](/es/audio/). El desarrollador de la aplicación puede firmar digitalmente elementos individuales dentro de un archivo JAR para autenticar su origen. Los archivos JAR se usan regularmente para crear API funcionales que contienen funciones específicas relacionadas con esa API.

## Formato de archivo JAR

Los archivos JAR se basan en el popular [formato de archivo ZIP](/es/compression/zip/) que archiva sus archivos de contenido individuales en un solo archivo. El formato de archivo JAR admite compresiones, lo que da como resultado un tamaño de archivo más pequeño para la descarga y, por lo tanto, mejora aún más el tiempo de descarga. El artículo [Especificaciones del archivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) de Oracle brinda detalles completos sobre las especificaciones internas de los archivos JAR.

### El archivo de manifiesto

Cuando se crea un archivo JAR, se crea automáticamente un archivo de manifiesto en su interior que contiene la información de metadatos sobre el contenido del archivo JAR. Este archivo muestra el contenido que se empaqueta dentro del archivo JAR. Un archivo de Manifiesto típico tiene el siguiente aspecto, que muestra las carpetas y clases incluidas en el archivo JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Especificaciones del manifiesto

Oracle define las especificaciones del manifiesto de la siguiente manera.

`manifest-file`: sección principal nueva línea \*sección-individual

`sección-principal`: versión-info nueva línea \*atributo-principal

`version-info`: Manifiesto-Versión: versión-número

`número-de-versión` : digit+{.digit+}*

`atributo principal`: (cualquier atributo principal legítimo) salto de línea

`sección-individual`: Nombre: valor nueva línea \*perentry-attribute

`perentry-attribute`: (cualquier atributo de perentry legítimo) salto de línea

`nueva línea` : CR LF | FL | CR (no seguido de LF)

`digit`: {0-9}

### JAR ejecutable

Los archivos JAR también pueden formar parte de una aplicación que puede ser ejecutada por Java Virtual Machine (JVM) similar a cualquier otra aplicación en el sistema operativo Microsoft Windows. En este caso, la JVM necesita conocer el punto de entrada de la aplicación, que es cualquier clase con un método principal vacío estático público. El archivo de manifiesto identifica dicha clase con el encabezado `Main-Class` en el siguiente formato:

```
Main-Class: com.example.MyClassName
```



## Referencias

* [Descripción general del archivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Formato de archivo JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

