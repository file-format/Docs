{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo HAML - Archivo de código fuente Haml",
  "description":"Obtenga información sobre el formato de archivo HAML y las API que pueden crear y abrir archivos HAML",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## ¿Qué es un archivo HAML?

Un archivo HAML es un archivo de lenguaje de marcado de abstracción HTML que contiene código fuente escrito en lenguaje [Haml](https://haml.info/). Se puede usar como reemplazo del ERB (scripts de plantilla de Ruby). El archivo HAML contiene el código fuente de la plantilla para generar el HTML de un documento web. Los archivos ERB se pueden reemplazar simplemente reemplazando estos archivos en la carpeta de aplicaciones/vistas a Haml cambiando la extensión del archivo. Los archivos HAML se pueden abrir con cualquier editor de texto, como Microsoft Notepad, Notepad ++, Apple TextEdit,

## Formato de archivo HAML

Los archivos HAML son archivos de origen guardados en el disco como archivos de texto sin formato. Contiene código escrito en sintaxis HAML. HAML reemplaza las etiquetas **<>** con el signo **%** para simplificar y simplificar el código. Los archivos ERB son reemplazables directamente por HAML como se muestra en el siguiente ejemplo simple.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Ejemplo de HAML

El siguiente es un ejemplo de Hello World de HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
que representa la siguiente salida HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referencias

* [HAML - Github](https://github.com/haml/haml)

