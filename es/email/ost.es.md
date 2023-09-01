{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Formato de archivo de almacenamiento de Outlook",
  "description":"Obtenga información sobre el formato de archivo OST y las API que pueden crear y abrir archivos OST",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo OST?

Los archivos de almacenamiento fuera de línea o OST representan los datos del buzón del usuario en modo fuera de línea en la máquina local al registrarse con Exchange Server usando Microsoft Outlook. Se crea automáticamente en el primer uso de Microsoft Outlook al conectarse con el servidor. Una vez que se crea el archivo, los datos se sincronizan con el servidor de correo electrónico para que también estén disponibles sin conexión en caso de desconexión del servidor de correo electrónico. Los archivos OST pueden usar elementos del buzón como correos electrónicos, contactos, información de calendario, notas, tareas y otros datos similares. Los usuarios pueden crear correos electrónicos y otros elementos de datos en el archivo OST incluso en ausencia de conexión al servidor, pero estos no se sincronizarán con el servidor. Una vez que se establece la conexión, el archivo local se sincroniza nuevamente con el servidor para que tanto el servidor como la copia local estén en el mismo nivel de información.

## Formato de archivo OST

El formato de archivo OST (tabla de almacenamiento fuera de línea) y [PST](/es/email/pst/) (tabla de almacenamiento personal) consisten en el formato de archivo de carpeta personal (PFF) que corresponde al almacenamiento de correos electrónicos, contactos y citas del usuario. Los datos en un archivo PFF se almacenan en little-endian con todas las fechas y horas representadas como FILETIME en UTC. [MS-PST] define dos tipos de PFF:

* Formato ANSI de 32 bits
* Formato Unicode de 64 bits

Las [especificaciones](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) del formato de archivo PST, disponibles en Microsoft, también se aplican al formato de archivo OST de forma gratuita y gratuita. licencia de patente irrevocable a través de la Promesa de Especificación Abierta. Consta de los siguientes elementos diferenciables:

* Encabezado de archivo
* Datos del encabezado del archivo
* Nodo de rama de índice
* Nodo de hoja de índice
* (Archivo) índice de compensación
* (Artículo) índice descriptor
* Descriptores locales
* Tipo de tabla de elementos

### Información del encabezado

La estructura HEADER del archivo OST se encuentra al principio del archivo en el desplazamiento 0. Contiene información de metadatos sobre el archivo OST y la información de la RAÍZ para acceder a las estructuras de datos de la capa NDB descritas anteriormente. La estructura HEADER difiere para las versiones Unicode y ANSI del formato de archivo OST.

El encabezado comienza con una palabra mágica de 4 bytes **!BDN** representada por bytes (0x21, 0x42, 0x44, 0x4E). Otro número mágico de 2 bytes, **SM** (0x53, 0x4D), se encuentra en el desplazamiento 8 desde el inicio del archivo. La información de la versión (ANSI o Unicode) se encuentra en un desplazamiento de 10 desde el inicio del archivo. El valor hexadecimal (0x17) especifica el archivo OST Unicode mientras que 0x0E o 0x0F representa el formato de archivo ANSI.

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
|rgnid[]   (128 bytes)|Una matriz fija de 32 NID, cada uno correspondiente a uno de los 32 NID_TYPE posibles (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
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

## Referencias

* [Formato de archivo de carpetas personales de Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Especificaciones de formato de archivo de carpeta personal](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

