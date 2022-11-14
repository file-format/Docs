{
  "date" : "2021-05-24",
  "keywords" :["xul", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "Idioma de interfaz de usuario XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Archivo de idioma de interfaz de usuario XML",
  "description":"Obtenga información sobre el formato de archivo XUL y las API que pueden crear y abrir archivos XUL",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ¿Qué es un archivo XUL?

Un archivo con una extensión .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) significa Lenguaje de interfaz de usuario XML) es un archivo de lenguaje de marcado basado en [XML](/es/web/xml/) para creación de interfaces de usuario. Fue desarrollado por Mozilla para que los desarrolladores crearan elementos de interfaz gráfica de usuario similares a otros lenguajes de marcado utilizados para crear páginas web. XUL ha sido ampliamente utilizado por Mozilla en su navegador Firefox, donde utilizó el código base de Mozilla. La representación XUL se lleva a cabo utilizando el
[Motor Gecko](https://en.wikipedia.org/wiki/Gecko_(software)). Las bifurcaciones de Firefox como Pale Moon, Basilisk y Waterfox conservan la compatibilidad con los complementos XUL. Los archivos XUL se identifican con el tipo MIME: application/vnd.mozilla.xul+xml.

## Formato de archivo XUL

Los archivos XUL se escriben en texto plano basado en el formato de archivo XML y se procesan utilizando el motor Gecko. Las tres partes principales de una estructura XUL son:

* `Contenido` - Esto incluye las declaraciones de la ventana y los elementos de la interfaz de usuario contenidos dentro de ellos.
* `Skin`: incluye hojas de estilo, imágenes y otros archivos relacionados con el tema. La apariencia de una ventana se describe en las hojas de estilo.
* `Configuración regional`: el texto que se muestra dentro de una ventana se almacena por separado y los usuarios pueden utilizar varios conjuntos de archivos de idioma.

### Ejemplo de XUL

El siguiente ejemplo crea tres botones que se apilan uno encima del otro en dirección vertical.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referencias

* [XUL - Por Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Documentación archivada de XUL - Por Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

