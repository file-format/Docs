{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Archivo de plantilla de correo electrónico de Microsoft Outlook",
  "description":"Obtenga información sobre el formato de archivo OFT y las API que pueden crear y abrir archivos OFT",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo OFT?

Los archivos con la extensión .oft son archivos de plantilla que se crean con Microsoft Outlook. El conjunto de diseños preformateados para plantillas de mensajes se usa para enviar correos electrónicos con información común para ahorrar tiempo. Dichos archivos se pueden generar creando un nuevo correo electrónico, agregando la información necesaria y luego usando el menú desplegable Guardar como plantilla de Office (.oft) de Microsoft Outlook. Los usuarios pueden abrir los archivos OFT haciendo doble clic en él y se abrirá en la aplicación asociada en ese sistema en particular.

## Estructura del archivo OFT ##

El formato de archivo .OFT utiliza el formato de archivo [MSG](/es/email/msg/) en su base. La única diferencia es que los archivos OFT tienen CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) como clase de almacenamiento (WriteClassStg), mientras que los archivos MSG usan CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

El formato CFB_3 es la base del archivo MSG. El paradigma se basa en los conceptos de almacenamientos y flujos, bastante cercano a los directorios y archivos. Por lo tanto, una gran diferencia en el primero es la jerarquía completa, empaquetada en un archivo distinto, llamado archivo compuesto. Los objetos constituyen los archivos de mensajes y consisten en una sola propiedad o sus colecciones. Esta capacidad facilita que las aplicaciones almacenen datos estructurados e intrincados en un solo archivo. Este formato también especifica múltiples almacenamientos, cada almacenamiento representa el objeto Mensaje como un componente principal. Estos almacenamientos contienen una serie de flujos que representan una propiedad de ese componente. También es posible anidar el almacenamiento.

### Propiedades OFT

En el nivel superior del archivo .msg, los almacenamientos contienen secuencias que almacenan propiedades en ellos. Las propiedades se pueden clasificar de la siguiente manera:

* Propiedades de longitud fija
* Propiedades de longitud variable
* Propiedades de valores múltiples

Independientemente de la categoría, una propiedad está etiquetada o nombrada. Sin embargo, se requiere información de mapeo adecuada para las propiedades con nombre según lo especificado por su almacenamiento de mapeo.

### Almacenamientos OFT

Los almacenamientos constituyen los componentes clave del objeto Message. El formato de archivo MSG establece los siguientes almacenamientos:

### Estructura de nivel superior

El objeto de mensaje representa todo el nivel superior del formato de archivo Msg. Según el tipo, las propiedades, la cantidad de destinatarios y los objetos adjuntos, un objeto de mensaje puede tener diferentes almacenamientos de flujo en su archivo .MSG correspondiente.

#### Relación con otras estructuras

El formato de archivo MSG/OFT tiene las siguientes relaciones con otras estructuras:

* La base de .msg es el formato de archivo binario de archivo compuesto.
* Este formato utiliza las propiedades utilizadas por Message and Attachment Object Protocol.

## Referencias

* [[MS-OXMSG]: Formato de archivo MSG de Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

