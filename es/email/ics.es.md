{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Formato de archivo iCalendar",
  "description":"Obtenga información sobre el formato de archivo ICS y las API que pueden crear y abrir archivos ICS",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo ICS?

La Especificación de objeto principal de calendario y programación de Internet (iCalendar) es un estándar de Internet (RFC 2445) para intercambiar e implementar eventos de calendario y programación. El formato iCalendar es interoperable, lo que garantiza el intercambio de información de calendario entre los usuarios que tienen diferentes aplicaciones de correo electrónico. iCalendar da formato a los datos de entrada como extensiones de correo de Internet multipropósito (MIME) y facilita el intercambio de objetos a través de diferentes protocolos de transporte. Estos protocolos de transporte pueden ser SMTP, HTTP, comunicación asíncrona punto a punto y transporte de red basado en medios físicos.

iCalendar permite a los usuarios compartir eventos, tareas dependientes de la fecha/hora e información de disponibilidad a través de correos electrónicos con otros usuarios que pueden responder. Los archivos de iCalendar se almacenan con los sufijos ".ics", ".iCalendar" o ".ifb" con un tipo MIME de "texto/calendario". iCalendar se mantiene para ser autosuficiente sin ninguna dependencia del protocolo de transporte. Los servidores web (con protocolo HTTP) pueden transportar información de iCalendar y las páginas web pueden contener datos de iCalendar en forma incrustada utilizando iCalendar.

## Breve historia del formato de archivo ICS

En 1998, el Grupo de Trabajo de Ingeniería de Internet (IETF) definió iCalendar como un estándar (RFC 2445). El estándar fue documentado por Frank Dawson (Lotus Notes Corporation) y Derik Stenerson (Microsoft). En 2009, el estándar fue refinado nuevamente por Bernard Desruisseaux (Oracle) como RFC 5545. Esta vez se agregaron algunas características nuevas y algunas características obsoletas quedaron obsoletas. En 2016, se lanzó RFC 7986 y se amplió a iCalendar RFC original. RFC 7986 agregó nuevas características al objeto principal VCALENDAR y también se introdujeron nuevas características de apoyo para los sistemas de conferencias.

## Formato de archivo ICS ##

El tipo MIME utilizado por los datos de iCalendar es "texto/calendario". El conjunto de caracteres predeterminado para iCalendar es UTF-8; sin embargo, al proporcionar parámetros en MIME, se puede usar un conjunto de caracteres diferente. Un archivo iCalendar contiene secciones, entre estas secciones "VCALENDAR", es la sección global que encapsula todas las demás secciones. La sección VEVENT define eventos, VTODO enumera todos los elementos pendientes, VJOURNAL contiene entradas de diario y VTIMEZONE especifica información de la zona horaria. Se permiten varias secciones de categoría similar. Para numerosos eventos, múltiples secciones VEVENT pueden estar presentes en un archivo iCalendar.

### Líneas de contenido ###

Los objetos de iCalendar se organizan en distintas líneas de texto "líneas de contenido". En este formato de archivo, la secuencia CRLF termina una línea, mientras que la longitud de la línea está limitada a 75 octetos, excluyendo el salto de línea. Un elemento de datos largo puede abarcar muchas líneas.

### Separadores de listas y campos ###

Las propiedades y los parámetros especifican una lista de valores que están separados por un carácter COMA. Las cadenas entrecomilladas se utilizan para valores de parámetros basados en URI. La lista de parámetros se puede construir por el valor de la propiedad. Cada parámetro de propiedad en esta lista debe estar separado por un PUNTO Y COMA.

En una lista de valores, un PUNTO Y COMA aísla los parámetros de propiedad y una COMA separa los valores de propiedad. El ejemplo se da a continuación:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Valores múltiples

Algunas propiedades pueden tener varios valores. Simplemente generar una nueva línea de contenido con el nombre de la propiedad es la regla básica para las propiedades de varios valores. Sin embargo, para un solo valor con múltiples variaciones de idioma, no debe usar propiedades de varios valores.

### Contenido binario

Dentro de un objeto iCalendar, el valor de propiedad puede hacer referencia a datos de contenido binario colocados en una entidad MIME externa mediante un URI. El contenido binario en línea se puede usar en situaciones especiales con el parámetro "CODIFICACIÓN", donde la aplicación necesita expresar un objeto iCalendar como una sola entidad. El siguiente ejemplo explica una propiedad "ATTACH" con una referencia URI:

ADJUNTAR: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Conjunto de caracteres

Aunque el esquema de juego de caracteres predeterminado para un iCalendar es UTF-8, no se especifica ningún parámetro de propiedad para definir el juego de caracteres de un valor de propiedad. en las transferencias MIME, el parámetro "juego de caracteres" DEBE usarse para el juego de caracteres existente.

## Referencias

* [Especificación de objeto principal de calendario y programación de Internet] (https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)] (https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#Historia_y_diseño)

