{
  "date" : "2021-05-24",
  "keywords" :["zul", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "abrir"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - Archivo de interfaz de usuario ZK",
  "description":"Obtenga información sobre el formato de archivo ZUL y las API que pueden crear y abrir archivos ZUL",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## ¿Qué es un archivo ZUL?

Un archivo con extensión .zul es un archivo web creado con el lenguaje de marcado de la interfaz de usuario (ZUML) y contiene definiciones para los elementos de la interfaz de usuario. Las clases Ajax y Java admiten el uso de ZUML basado en [XML](/es/web/xml/) para desarrollar archivos del lado del servidor. El formato de archivo ZUL fue desarrollado por ZK, un marco de interfaz de usuario que le permite crear aplicaciones web y móviles sin el conocimiento de JavaScript o AJAX.

## Formato de archivo ZUL

Los archivos ZUL están basados en XML y constan de diferentes elementos para construir la interfaz de usuario. El cargador ZK usa cada elemento XML para crear un componente. El procesamiento general de los elementos de la página, como el título de la página, la descripción, etc., se describen en cada instrucción de procesamiento XML de ZUML.

### Ejemplo ZUL

En el siguiente ejemplo de código ZUML, la primera línea especifica el título de la página, la segunda línea crea un componente raíz con título y borde, y la tercera línea crea un botón con etiqueta y un detector de eventos.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
El esquema ZUL se puede descargar desde http://www.zkoss.org/2005/zul/zul.xsd.
## Referencias

* [ZUL - Por ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Esquema ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

