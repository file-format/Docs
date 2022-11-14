{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST: formato de archivo del almacén de información personal de Outlook",
  "description":"Obtenga información sobre el formato de archivo PST y las API que pueden crear y abrir archivos PST",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PST?

Los archivos con extensión .pst representan archivos de almacenamiento personal de Outlook (también llamados tablas de almacenamiento personal) que almacenan una variedad de información del usuario. La información del usuario se almacena en carpetas de diferentes tipos que incluyen correos electrónicos, elementos de calendario, notas, contactos y varios otros formatos de archivo. Los archivos PST se utilizan para archivar datos de correo electrónico sin conexión que luego se pueden cargar y ver en varias aplicaciones.

## Especificaciones del formato de archivo PST

El formato de archivo PST [especificaciones] (https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) están disponibles en Microsoft como licencia de patente gratuita e irrevocable a través de Open Specification Promise .

### Tipo de formatos PST

Los formatos de archivo PST se clasifican en dos tipos según la codificación del tipo de archivo. Los archivos PST con codificación ANSI son formatos de archivo más antiguos y sólo son compatibles con Outlook 2002 y versiones anteriores. Dichos archivos tienen un límite de tamaño máximo de 2 GB (2^^31^^ Bytes) y no son compatibles con Unicode. Un tipo de formato de archivo más moderno, basado en la codificación Unicode, elimina la limitación de tamaño de archivo y puede alcanzar un tamaño máximo de datos de 50 GB.

### Organización lógica del formato de archivo PST

En la base del formato de archivo PST se encuentra B-Tree que mantiene los datos ordenados y permite búsquedas, acceso secuencial, inserciones, eliminaciones, etc. en tiempo logarítmico. La estructura general de un archivo PST está organizada en tres capas.

![Logical layers of a PST file](/es/email/PST-1.png "Logical layers of a PST file")

`Capa de base de datos de nodo (NDB)`: la capa de base de datos de nodo se encuentra en el nivel inferior de un archivo PST e incluye la base de datos de nodos. Estos nodos en realidad representan instalaciones de almacenamiento de nivel inferior del formato de archivo PST. La capa NDB se compone de encabezado, información de asignación de archivos, bloques y BTrees (Node BTree y Block BTree) desde el punto de vista del almacenamiento. Los nodos y bloques de la capa NDB están vinculados a través de Data BID, que es una de las cuatro propiedades de la referencia de nodo, es decir, NID (ID de nodo), NID principal, BID de datos (BID de bloque) y BID de subnodo.

`Capa de listas, tablas y propiedades -` La capa LTP proporciona la comprensión lógica de los conceptos de nivel superior además de NDB. Además de otros elementos, la capa LTP se compone principalmente de contexto de propiedad (PC) y contexto de tabla (TC). PC es una colección de propiedades, mientras que TC representa una matriz bidimensional de colección de propiedades vs. la presencia de estas. Implementación eficiente de PC y TC, la capa LTP utiliza los siguientes dos tipos de estructuras de datos sobre el nodo NDB:

* Heap On Node (HN): permite subasignar el flujo de datos de un nodo en pequeños fragmentos de tamaño variable.
* BTree on Heap (BTH): BTH proporciona una forma conveniente y práctica de buscar a través de los datos. Las PC, descritas anteriormente, se implementan como BTH y es por eso que se implementan al construir dentro de una estructura HN.

`Capa de mensajes -` En esta capa se implementan reglas de nivel superior y lógica comercial para trabajar con archivos PST. La salida lógica de esta capa da como resultado objetos de carpeta, objetos de mensaje, objetos de archivo adjunto y propiedades, lo que es posible gracias a la combinación de capas LTP y NDB. Las reglas y los requisitos que deben seguirse al modificar los contenidos de PST también se definen en esta capa.

### Organización física del formato de archivo PST

El alto nivel de organización de archivos del archivo PST se muestra en la siguiente figura. Esta es solo una descripción general de los diferentes conceptos de los elementos lógicos del archivo PST.

![Physical organization of the PST file format](/es/email/PST-2.png "Physical organization of the PST file format")


#### Información del encabezado PST

La estructura HEADER del archivo PST se encuentra al principio del archivo en el desplazamiento 0. Contiene información de metadatos sobre el archivo PST y la información de la RAÍZ para acceder a las estructuras de datos de la capa NDB descritas anteriormente. La estructura HEADER difiere para las versiones Unicode y ANSI del formato de archivo PST.

El encabezado comienza con una palabra mágica de 4 bytes **!BDN** representada por bytes (0x21, 0x42, 0x44, 0x4E). Otro número mágico de 2 bytes, **SM** (0x53, 0x4D), se encuentra en el desplazamiento 8 desde el inicio del archivo. La información de la versión (ANSI o Unicode) se encuentra en un desplazamiento de 10 desde el inicio del archivo. El valor hexadecimal (0x17) especifica el archivo PST Unicode mientras que 0x0E o 0x0F representa el formato de archivo ANSI.

|Campo|Descripción
---|---|
|dwMagic (4 bytes)|DEBE ser "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|El valor CRC de 32 bits de los 471 bytes de datos a partir de wMagicClient (0ffset 0x0008)
|wMagicClient (2 bytes)|DEBE ser "{ 0x53, 0x4D }".
|wVer (2 bytes)|Versión del formato del archivo. Este valor DEBE ser 14 o 15 si el archivo es un archivo PST ANSI y DEBE ser 23 si el archivo es un archivo PST Unicode.
|wVerClient (2 bytes)|Versión del formato de archivo del cliente. La versión que corresponde al formato descrito en este documento es 19. Los creadores de un nuevo archivo PST basado en este documento DEBERÍAN inicializar este valor en 19.
|bPlatformCreate (1 byte)|Este valor DEBE establecerse en 0x01.
|bPlatformAccess (1 byte)|Este valor DEBE establecerse en 0x01.
|dwReservado (8 bytes)|
|bidUnused (solo Unicode de 8 bytes)|Relleno no utilizado agregado cuando se creó el formato de archivo PST Unicode.
|bidNextP (Unicode: 8 bytes; ANSI: 4 bytes)|Página siguiente BID. Las páginas tienen un contador especial para asignar valores de bidIndex. El valor de bidIndex para BID para páginas se asigna a partir de este contador.
|bidNextB (solo ANSI de 4 bytes): |Next BID. Este valor es el contador monótono que indica el BID a asignar para el próximo bloque asignado. Los valores de BID avanzan en incrementos de 4. Para más detalles, consulte la sección 2.2.2.2.
|dwUnique (4 bytes)|Este es un valor que aumenta monótonamente y que se modifica cada vez que se modifica la estructura HEADER del archivo PST. La función de este valor es proporcionar un valor único y garantizar que los CRC de HEADER sean diferentes después de cada modificación de encabezado.
|rgnid[] (128 bytes)|Una matriz fija de 32 NID, cada uno correspondiente a uno de los 32 NID_TYPE posibles (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 bytes)|Espacio no utilizado; DEBE ponerse a cero. Solo formato de archivo PST Unicode.
|root (Unicode: 72 bytes; ANSI: 40 bytes)|Una estructura ROOT (sección 2.2.2.5).
|dwAlign (4 bytes)|Bytes de alineación no utilizados; DEBE ponerse a cero. Solo formato de archivo PST Unicode.
|rgbFM (128 bytes)|FMap obsoleto. Esto ya no se usa y DEBE completarse con 0xFF. Los lectores DEBEN ignorar el valor de estos bytes.
|rgbFP (128 bytes)|FPMap obsoleto. Esto ya no se usa y DEBE completarse con 0xFF. Los lectores DEBEN ignorar el valor de estos bytes.
|bSentinel (1 byte)|DEBE establecerse en 0x80.
|bCryptMethod (1 byte)|Indica cómo se codifican los datos dentro del archivo PST. DEBE establecerse en uno de los valores predefinidos (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReservado (2 bytes)| Reservado; DEBE ponerse a cero.
|bidNextB (8 bytes)|Indica el siguiente valor de BID disponible. Solo formato de archivo PST Unicode.
|bidNextB (UNIcode SOLAMENTE: 8 bytes)|Próxima OFERTA. Este valor es el contador monótono que indica el BID a asignar para el próximo bloque asignado. Los valores de BID avanzan en incrementos de 4. Para más detalles, consulte la sección 2.2.2.2.
|dwCRCFull (4 bytes)|El valor CRC de 32 bits de los 516 bytes de datos desde wMagicClient hasta bidNextB, inclusive. Solo formato de archivo PST Unicode.
|ullReservado (8 bytes)|Reservado; DEBE ponerse a cero. Solo formato de archivo ANSI PST.
|dwReservado (4 bytes)|Reservado; DEBE ponerse a cero. Solo formato de archivo ANSI PST.
|rgbReservado2 (3 bytes)|
|bReservado (1 byte) |
|rgbReservado3 (32 bytes) |

### Protección de Datos ###

Por seguridad, los archivos PST también se pueden proteger con contraseña, lo que requiere que la aplicación de carga aplique una contraseña antes de poder verlos. La contraseña aplicada al archivo PST se almacena en el almacén de mensajes. Sin embargo, esto no proporciona una protección sólida de los datos, ya que las herramientas disponibles pueden eliminar la contraseña. Además, la contraseña especificada por el usuario no se usa como parte de la clave para codificar y decodificar algoritmos de cifrado. Por lo tanto, no hay ningún beneficio de proteger los datos para que accedan personas no autorizadas. El almacenamiento de la contraseña como hash CRC-32 de la cadena original también lo convierte en un método débil para la seguridad de los datos contra el enfoque de fuerza bruta.

## Referencias ##

* [Formato de archivo de carpetas personales de Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Especificaciones de formato de archivo de carpeta personal](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

