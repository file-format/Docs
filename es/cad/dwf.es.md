{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Formato de archivo", "Abrir", "Leer", "Crear", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DWF y las API que pueden crear y abrir archivos DWF",
  "title" :"Formato de archivo DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DWF?

Design Web Format (DWF) representa dibujos 2D/3D en formato comprimido para ver, revisar o imprimir archivos de diseño. Contiene gráficos y texto como parte de los datos de diseño y reduce el tamaño del archivo debido a su formato comprimido. El tamaño de archivo reducido hace que la distribución y comunicación de datos de diseño enriquecidos sea eficiente. DWF no requiere que el destinatario conozca el uso del software CAD que creó el dibujo original. El contenido del formato de archivo DWF puede ser simple e incluir solo una hoja o lo suficientemente complejo como para tener fuentes, colores e imágenes.

## Breve historia ##

Autodesk introdujo el formato de archivo DWF en 1995 como parte del complemento de navegación de Netscape, WHIP. El formato evolucionó desde el formato solo 2D para incluir contenidos 3D con el paso del tiempo. Muchas de las aplicaciones de terceros también utilizan este formato.

## Formato de archivo DWF ##

DWF es un formato abierto y seguro diseñado específicamente para compartir datos completos de diseño de ingeniería. Es independiente del software de la aplicación, el hardware y el sistema operativo originales utilizados para crear esos datos de diseño. Esto permite que los miembros del equipo que no utilizan aplicaciones CAD participen en los procesos digitales mediante la visualización de diseños de edificios, GIS o productos. Un archivo DWF consta de varios archivos XML y binarios que se empaquetan juntos en un archivo comprimido creado con compresión [ZIP](/es/compression/zip/). Puede cambiar el nombre de una extensión de archivo DWF a ZIP y ver el contenido del archivo. El paquete DWF puede contener muchos tipos de datos de diseño, como gráficos 2D, gráficos 3D, metadatos de paquetes y secciones, y otros archivos de recursos.

**Archivos de metadatos DWF**: archivos XML que contienen información relacionada con los metadatos y la estructura (autor, título, hora de creación, dependencias de la sección, orden de la sección, descripciones del archivo de recursos, funciones, tipos MIME, etc.) y relacionada con la sección (página información, metadatos de diseño, etc.). Los metadatos estructurales se utilizan para crear objetos lógicos (colecciones de archivos para representar una parte o una página, etc.).

**Archivos de recursos**: medios u otros archivos de contenido a los que se hace referencia desde los metadatos del paquete/sección y, por lo general, son presentaciones de datos de diseño en varios formatos (ZGL, W2D, [JPG](/es/image/jpeg/), [PNG](/es/imagen/png/), AVI, XML, [TXT](/es/procesador de textos/txt/), [DOC](/es/procesador de textos/doc/), etc.)

### Detalles del formato de archivo ###

Los archivos DWF están organizados en tres secciones principales, como se muestra a continuación.

* Cabecera de identificación del archivo
* Bloque de datos de archivo
* Tráiler de terminación de archivos

#### Encabezado de identificador de archivo ####

El encabezado del identificador de archivo permite que las aplicaciones identifiquen los archivos DWF. También identifica qué versión de las especificaciones DWF se utilizó para codificar el archivo. Es un encabezado de 12 bytes que se organiza de la siguiente manera:


|Byte|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Carácter|(|D|W|F|(espacio)|V|0|0|.|3|0|)

He aquí un resumen de esta tabla:

* Los primeros seis bytes del encabezado siempre representan caracteres ASCII "(DWF V"
* Los siguientes 5 bytes contienen información sobre el número de versión, por ejemplo, "00.30" con el valor de versión mayor y menor del formato

Las aplicaciones que crean un archivo DWF deben especificar el número de versión más bajo posible que una aplicación de lectura debe admitir para usar correctamente los datos.

#### Bloque de datos de archivo ####

El bloque de datos del archivo comienza en el byte 13 de un archivo DWF y es una serie de pares de códigos de operación y operandos, como se muestra en la siguiente tabla.

|Campo 1|Campo 2|Campo 3|Campo 4|Campo 5|Campo 5
--- | --- |--- | --- |--- | --- |
|código de operación|operando|código de operación|operando|código de operación|operando

Un archivo DWF puede contener pares de código de operación-operando como ASCII legible, así como código binario o una combinación de ambos. Todas las operaciones de DWF tienen un código de operación/operando ASCII legible, y la mayoría de las operaciones también tienen un código de operación/operando binario codificado. Los códigos de operación están en un solo byte, lo que permite más de 200 operaciones. El ASCII extendido y el binario extendido son casos excepcionales. Los valores de los códigos de operación pueden oscilar entre 0 y 255, con algunas excepciones. Excepto por los dos tipos especiales de códigos de operación ASCII extendido y binario extendido, un lector de archivos debe saber cómo calcular la longitud del operando.

##### Códigos de operación prohibidos #####

Las representaciones ASCII para lo siguiente no se pueden usar como códigos de operación:

Las siguientes representaciones ASCII no se pueden usar como códigos de operación:

* Espacio (0x20)
* Pestaña (0x09)
* Guión (0x2D)
* Dígitos ASCII 0-9 (0x30 - 0x39)
* Retorno de carro (0x0D)
* Avance de línea (0x0A)
* Comillas simples (0x27)
* Comillas dobles (0x22)
* Punto (0x2E)
* Paréntesis (0x28 y 0x29)
* Corchetes (0x7B y 0x7D)
* Corchetes (0x5B y 0x5D)
* Barra inclinada hacia atrás (0x5C)

#### Tráiler de terminación de archivo ####

El tráiler de terminación de archivo para DWF es simplemente un código de operación especial que indica el final del archivo. Algunas aplicaciones pueden almacenar datos que no son DWF siguiendo el código de operación de terminación. El avance es como se muestra a continuación:


|Byte|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Carácter|(|E|n|d|0|f|D|W|F|)

## Referencias ##

* [DWF - Por Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Formato de datos WHIP](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

