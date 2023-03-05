{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Obtenga información sobre el formato de archivo TNEF y las API que pueden crear y abrir archivos TNEF",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo TNEF?

El formato de encapsulación neutral para el transporte (TNEF) es propiedad de Microsoft, para encapsular archivos adjuntos de correo electrónico basados en la interfaz de programación de aplicaciones de mensajería (**MAPI**). Microsoft Outlook y Microsoft Exchange Server son totalmente compatibles con TNEF, mientras que más tarde decodifica TNEF en MAPI y muestra los correos formateados. Un archivo adjunto de correo electrónico con codificación TNEF tiene un tipo MIME de MS-TNEF y se almacena como winmail/win.dat. El archivo adjunto en winmail .dat encapsula la siguiente información:


|Mensaje|Objetos OLE|Características de Outlook
---|---|---|
|<ul><li> Archivos adjuntos del mensaje original</li><li> Versión formateada original</li><li> fuentes, tamaños de texto y colores de texto</li></ul> |<ul><li> imágenes incrustadas</li><li> documentos de Office incrustados</li></ul> |<ul><li> formularios personalizados</li><li> botones de votacion</li><li> solicitudes de reunión</li></ul>


Otros servicios de correo electrónico que no son compatibles con TNEF presentan texto sin formato para los mensajes con formato TNEF. Outlook incrusta un formato enriquecido del mensaje en archivos TNEF (OLE) o características particulares de Outlook (formularios, botones de sondeo y solicitudes de conferencia). No es posible sancionar la codificación TNEF explícita dentro del cliente de correo electrónico de Outlook, sin embargo, optar por el formato RTF para enviar un correo electrónico facilita implícitamente la codificación TNEF.

## Formato de archivo TNEF

El algoritmo de datos TNEF establece una estructura plana a partir de ricas propiedades jerárquicas de mensajes. Estas estructuras aplanadas luego se utilizan para representar un flujo de datos en serie compuesto por propiedades particulares.

En algunas situaciones, donde las propiedades ocurren en grupos o tienen valores múltiples, la transmisión puede incluir recuentos y rellenos para aplicar alineaciones de datos específicas. Una situación distintiva en la que el uso de este algoritmo es ventajoso es en un entorno de mensajería poco compatible. En dichos entornos, un escritor TNEF codifica una propiedad de mensaje enriquecido en un flujo de datos en serie. Además, las propiedades que no pertenecen al TNEF subyacente pueden encapsularse durante la transmisión. Estas propiedades encapsuladas luego se ponen a disposición mediante la decodificación a través de un TNEF para garantizar la disponibilidad de todas las propiedades del mensaje original para la aplicación cliente.

En TNEF todos los tipos de datos numéricos son little-endian y su tamaño es superior a un byte. El manejo de estos valores numéricos en plataformas que no son de Little Endian requiere realizar las transformaciones adecuadas para obtener los valores correctos. Los valores de cadena se representan en formato de formulario de Backus-Naur aumentado (ABNF) de acuerdo con las especificaciones [RFC5234]. Cuando la cadena termina con un carácter nulo, también se incluye; por ejemplo, "trabajador@espécimen.com" %x00.

{{< figure src="../TNEF.png" alt="Formato de archivo TNEF" >}}

## Atributos TNEF y reglas de procesamiento ##

El flujo de datos en TNEF comienza con un número de versión heredado, una firma, un valor de clave primitivo y una página de códigos de representación de atributos. Esta página de códigos se genera cuando el codificador registra atributos y propiedades ANSI. Después de eso, la transmisión se convirtió en una serie de atributos en los que los atributos del mensaje se alineaban primero y luego seguían los atributos del archivo adjunto. Las diferentes características de mensajes y archivos adjuntos están contenidas en atributos especiales como attMsgProps, attAttachment y attRecipTable. Los atributos que aparecen en la secuencia TNEF contienen la estructura, las propiedades del mensaje y las conversiones necesarias para relacionarlos con las propiedades del mensaje. Cada atributo consta de un ID, tamaño y datos del atributo, un checksum y un nivel de acuerdo a su aplicación.

## Relación con protocolos y otros algoritmos ##

Los sistemas que tienen un mecanismo deficiente para mostrar un formato de mensaje enriquecido de forma nativa necesitan un algoritmo de datos TNEF para el transporte. Usando el tipo de medio ms-TNEF, la salida del algoritmo consiste en un archivo adjunto (winmail.dat) y una parte del cuerpo de MIME especificada en [RFC2045]. El cuerpo del mensaje de texto sin formato se transmite utilizando UUENCODE de acuerdo con la especificación [MSDN-UAF] y este cuerpo del mensaje o método equivalente se descodifica en el extremo del destinatario. Además, TNEF puede transmitir datos de mensajes utilizando diferentes protocolos de Internet como SMTP, POP3, IMAP4 y los que integran MIME de acuerdo con el estándar RFC2045.

## Declaración de aplicabilidad ##

Además de la transmisión de mensajes simples, la aplicación original de TNEF debía crearse para usar clases de mensajes y admitir características adicionales que no tienen soporte original en el protocolo de transporte. Esta aplicación se perfeccionó aún más para la transmisión de propiedades de mensajes enriquecidos y propiedades con nombre que los clientes de mensajería modernos utilizan hoy en día. Para cumplir con la implementación original, se mantiene la sintaxis de atributo original y un atributo especial contiene las propiedades del nuevo mensaje por separado.

## Referencias

* [Formato de encapsulación de transporte neutral](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Direcciones de correo electrónico y libretas de direcciones en Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: Algoritmo de datos de formato de encapsulación neutral de transporte (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

