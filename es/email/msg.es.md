{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Formato de correo electrónico de Microsoft Outlook",
  "description":"Obtenga información sobre el formato de archivo MSG y las API que pueden crear y abrir archivos MSG",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo MSG?

MSG es un formato de archivo utilizado por [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) y Exchange para almacenar mensajes de correo electrónico. , contacto, cita u otras tareas. Dichos mensajes pueden contener uno o más campos de correo electrónico, con el remitente, el destinatario, el asunto, la fecha y el cuerpo del mensaje, o información de contacto, detalles de la cita y una o más especificaciones de tareas. Las propiedades que constituyen el objeto Mensaje, incluido, también forman parte del archivo MSG. El archivo MSG tiene encabezados, cuerpo del mensaje principal e hipervínculos como texto ASCII sin formato. Los archivos MSG también son adecuados con los programas que necesitan la interfaz de programación de aplicaciones de mensajería (MAPI) de Microsoft.

## Estructura del archivo MSG

El formato CFB_3 es la base del archivo MSG. El paradigma se basa en los conceptos de almacenamientos y flujos, bastante cercano a los directorios y archivos. Por lo tanto, una gran diferencia en el primero es la jerarquía completa, empaquetada en un archivo distinto, llamado archivo compuesto. Los objetos constituyen los archivos de mensajes y consisten en una sola propiedad o sus colecciones. Esta capacidad facilita que las aplicaciones almacenen datos estructurados e intrincados en un solo archivo. Este formato también especifica múltiples almacenamientos, cada almacenamiento representa el objeto Mensaje como un componente principal. Estos almacenamientos contienen una serie de flujos que representan una propiedad de ese componente. También es posible anidar el almacenamiento.

## Mapi Propiedades

En el nivel superior del archivo .msg, los almacenamientos contienen secuencias que almacenan propiedades en ellos. Las propiedades se pueden clasificar de la siguiente manera:

* Propiedades de longitud fija
* Propiedades de longitud variable
* Propiedades de valores múltiples

Independientemente de la categoría, una propiedad está etiquetada o nombrada. Sin embargo, se requiere información de mapeo adecuada para las propiedades con nombre según lo especificado por su almacenamiento de mapeo.

## Almacenamientos

Los almacenamientos constituyen los componentes clave del objeto Message. El formato de archivo MSG establece los siguientes almacenamientos:

## Estructura de nivel superior

El objeto de mensaje representa todo el nivel superior del formato de archivo MSG. Según el tipo, las propiedades, la cantidad de destinatarios y los objetos adjuntos, un objeto de mensaje puede tener diferentes almacenamientos de flujo en su archivo .MSG correspondiente.

### Relación con otras estructuras

El formato de archivo Msg tiene las siguientes relaciones con otras estructuras:

* La base de .msg es el formato de archivo binario de archivo compuesto.
* Este formato utiliza las propiedades utilizadas por Message and Attachment Object Protocol.

## Escenarios para evitar los formatos MSG

El objeto de mensaje se puede compartir entre clientes o almacenes de mensajes que utilizan el sistema de archivos .msg. Hay algunas circunstancias en las que almacenar un objeto Mensaje en el formato de archivo .msg no sería apropiado. Por ejemplo:

* En caso de mantener un gran archivo independiente, es mejor usar un formato con todas las funciones en el que las vistas se puedan representar con mayor precisión.
* Si el receptor es desconocido, es posible que el formato no sea compatible con el extremo del receptor y que se entregue algo privado o irrelevante.

## Ejemplo de archivo MSG

Para tener una idea de cómo se ve un archivo MSG, puede descargar un [archivo MSG de muestra](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) y abrirlo en su computadora para ver su contenido.

## Referencias

* [[MS-OXMSG]: Formato de archivo MSG de Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

