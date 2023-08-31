{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Mensaje de correo electrónico",
  "description":"Obtenga información sobre el formato de archivo EML y las API que pueden crear y abrir archivos EML",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## ¿Qué es un archivo EML?

El formato de archivo EML representa los mensajes de correo electrónico guardados con Outlook y otras aplicaciones relevantes. Casi todos los clientes de correo electrónico admiten este formato de archivo para cumplir con el estándar de formato de mensajes de Internet RFC-822. Microsoft Outlook es el software predeterminado para abrir tipos de mensajes EML. Los archivos EML se pueden usar para guardarlos en un disco, así como para enviarlos a destinatarios mediante protocolos de comunicación.

## Breve historia de EML

Las especificaciones de formato de archivo EML están disponibles según el formato estándar [RFC 822](https://www.ietf.org/rfc/rfc0822.txt). Antes del RFC-822, el RFC-733 regía las reglas del intercambio de mensajes de red hasta que en 1982 se creó el primero como una mejora del lateral al establecer los estándares ARPA. Al mismo tiempo, Microsoft creó sus propios módulos COM para el desarrollo de su propio cliente de correo electrónico, es decir, Outlook Express. RFC-822 tomó el camino para establecerse como un formato propietario cuando Microsoft se desvió del estándar abierto y creó el formato de archivo [PST](/es/email/pst/) donde los correos electrónicos se guardan en un formato de base de datos altamente estructurado. Esto generaba problemas para los usuarios de clientes de correo electrónico que no eran de Microsoft cuando los correos electrónicos se reenviaban desde Microsoft Outlook.

Fue en 2001 cuando el estándar 822 se mejoró a 2822 - Formato de mensajes de Internet que se utiliza actualmente para crear, leer y enviar mensajes EML en formato MIME RFC-822.

## Especificaciones del formato de archivo EML

Los archivos EML se componen de dos secciones distinguidas:

* Encabezados: contiene información sobre el encabezado del mensaje
* Cuerpo del mensaje: contiene una serie de información que puede incluir contenido del mensaje, imágenes incrustadas y archivos adjuntos

### Información de encabezados ###

Un archivo EML consta de información de encabezados y, opcionalmente, del cuerpo del mensaje. Cada línea de encabezado en la EML tiene dos partes separadas por dos puntos ":". El primero se llama Nombre del encabezado y el que sigue a los dos puntos es el cuerpo del encabezado. Por ejemplo, tales encabezados incluyen:

* Dirección de correo electrónico del remitente
* Dirección de Correo Electrónico del Destinatario
* Asunto del correo electrónico
* Sello de fecha y hora del mensaje

**Ejemplo de encabezado**

```
De:<John@bmw.eml.light.com>

A:<Andy@fileformat.com>

Fecha: jueves, 8 de marzo de 2018 10:43:37 +0100

Asunto: luz bmw eml
```

### Cuerpo del mensaje ###

El cuerpo del mensaje EML contiene la información principal del correo electrónico en forma de texto, hipervínculos y archivos adjuntos. El cuerpo del correo electrónico puede contener texto legible sin formato, pero no es necesario. En este caso, el cuerpo del mensaje puede estar vacío o contener datos adjuntos codificados.

El contenido del cuerpo del mensaje se describe por su tipo de contenido, lo que permite que las aplicaciones de lectura lean la información en los formatos respectivos. En realidad, representa la naturaleza y el formato de un documento. La estructura de un tipo MIME o tipo de contenido es muy simple; consta de un tipo y un subtipo, dos cadenas, separadas por un '/'. No se permite espacio. El `tipo` representa la categoría y puede ser un tipo discreto o de varias partes. El `subtipo` es específico de cada tipo. La lista de tipos, que caen en la categoría de tipo de contenido, es larga, pero algunos tipos de contenido importantes son los siguientes:


|**Tipo**|**Descripción**|**Ejemplo de subtipos**
---|---|---|
|texto|Representa un formato legible por humanos|texto/sin formato, texto/html, texto/css, texto/javascript
|image|Representa imágenes de cualquier tipo excepto videos|image/bmp, image/png, image/jpg, image/gif
|audio|Representa cualquier formato de archivo de audio|audio/mdi, audio/wav
|aplicación|Representa cualquier tipo de datos binarios|aplicación/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Representación del archivo adjunto en el cuerpo EML ###

El cuerpo de EML contiene límites para cada tipo de contenido que contiene. El archivo adjunto en el cuerpo del mensaje se identifica por su tipo de contenido y disposición de contenido, como se muestra en el siguiente ejemplo:

Tipo de contenido: texto/simple; juego de caracteres#"windows-1252"; nombre#"tienda de aplicaciones de Apple.txt"
Contenido-Disposición: archivo adjunto; nombre de archivo#"tienda de aplicaciones de Apple.txt"
Codificación de transferencia de contenido: base64
X-Adjunto-Id: f_jkhztmd02

Como puede verse, la disposición de contenido configurada como archivo adjunto permite que las aplicaciones de lectura obtengan información del archivo adjunto, como el nombre del archivo adjunto y la codificación de la transferencia. La información del encabezado del archivo adjunto va seguida del contenido codificado del archivo adjunto que debe leerse.

#### Ejemplo de hoja de cálculo como archivo adjunto ####

Tipo de contenido: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; nombre#"english_spodr.xlsx"
Contenido-Disposición: archivo adjunto; nombre de archivo#"english_spodr.xlsx"
Codificación de transferencia de contenido: base64
X-Adjunto-Id: f_jkhztmd43

## Referencias

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

