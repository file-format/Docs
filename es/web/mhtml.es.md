{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","archivo mhtml", "formato de archivo mhtml", "tipo de archivo mhtml", "archivo", "tipo", "qué es un archivo mhtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Archivo MIME HTML",
  "description":"Obtenga información sobre el formato de archivo MHTML y las API que pueden crear y abrir archivos MHTML",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo MHTML?

Los archivos con extensión MHTML representan un formato de archivo de página web que puede ser creado por varias aplicaciones diferentes. El formato se conoce como formato de archivo porque guarda el código web **[HTML](/es/web/html/)** y los recursos asociados en un solo archivo. Estos recursos incluyen todo lo relacionado con la página web, como imágenes, applets, animaciones, archivos de audio, etc. Los archivos MHTML se pueden abrir en una variedad de aplicaciones como Internet Explorer y Microsoft Word. Microsoft Windows utiliza el formato de archivo MHTML para registrar escenarios de problemas observados durante el uso de cualquier aplicación en Windows que plantee problemas. El formato de archivo MHTML codifica el contenido de la página de forma similar a las especificaciones definidas en message/rfc822, que son especificaciones relacionadas con el correo electrónico de texto sin formato. Las especificaciones reales del formato se detallan en [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Formato de archivo MHTML

MHTML también se conoce como encapsulación MIME de documentos HTML agregados por su capacidad para codificar páginas web HTML junto con sus recursos en un único archivo web. Según las especificaciones RFC 2557, un documento agregado es un mensaje codificado en MIME que contiene un recurso raíz (objeto), así como otros recursos vinculados a él a través de URI. Tales otros recursos pueden ser la representación de imágenes en línea, hojas de estilo, applets, etc. Además, estos pueden ser la raíz de otros documentos multimedia. Las especificaciones completas del documento para el formato de archivo MHTML se detallan en [RFC 2557](https://tools.ietf.org/html/rfc2557) y deben consultarse para cualquier tipo de desarrollo de aplicaciones para leer/escribir este formato de archivo. El estándar especifica que las partes del cuerpo a las que se hace referencia pueden identificarse mediante un ID de contenido o una ubicación de contenido.

### Encabezados de contenido MIME

Se define un encabezado de contenido MIME, Content-Location, para resolver las referencias URI a los recursos en otras partes del cuerpo. Este encabezado puede aparecer en cualquier mensaje o encabezado de contenido.

### Encabezado de ubicación de contenido

Una ubicación de contenido es una representación de un URI que etiqueta el contenido de una parte del cuerpo donde se coloca. Su valor puede ser un URI absoluto o relativo. Se puede utilizar para etiquetar un recurso que no es recuperable por algunos o todos los destinatarios de un mensaje. Se permite que un solo mensaje tenga un solo encabezado de ubicación de contenido. Ejemplo de una estructura multiparte/relacionada que contiene partes del cuerpo con etiquetas Content-Location y Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI de agregados MHTML

El URI del agregado MHTML es diferente al de su URI raíz. El campo de encabezado Ubicación de contenido debe aplicarse a todo el agregado si se usa en el encabezado de un encabezado relacionado o de varias partes. De manera similar, el conjunto de recursos recuperados puede ser diferente del conjunto de recursos recuperados usando las ubicaciones de contenido de sus partes cuando el URI que hace referencia al agregado MHTML se usa para recuperar este agregado. Por ejemplo, recuperar un agregado MHTML puede devolver una versión anterior, mientras que recuperar el URI raíz y sus objetos vinculados en línea puede devolver una versión más nueva.

## Referencias

* [Encapsulación MIME de documentos agregados - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Formato de archivo MHTML: por Wikipedia](https://en.wikipedia.org/wiki/MHTML)

