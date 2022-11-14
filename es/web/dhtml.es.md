{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","archivo dhtml", "formato de archivo dhtml", "tipo de archivo dhtml", "archivo", "tipo", "qué es un archivo dhtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Formato de archivo HTML dinámico",
  "description":"Obtenga más información sobre el formato de archivo DHTML y las API que pueden crear y abrir archivos DHTML",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DHTML?

Un archivo con extensión .dhtml es un archivo [HTML](/es/web/html/) dinámico que se utiliza para crear contenido dinámico de una página web. Un elemento web creado en DHTML se basa en eventos y no requiere recargar la página. En la mayoría de los casos, se usa un archivo DHTML para crear el contenido dinámico de una página web, como menús desplegables, capas flotantes, botones de rollover y otro contenido dinámico. Te encuentras con elementos html dinámicos casi a diario en tu vida cuando pasas el mouse sobre un elemento del menú y abre más opciones de submenú. DHTML utiliza tecnologías web como [HTML](/es/web/html/), [Javascript](/es/web/js/), HTML DOM, HTML Events y [CSS](/es/web/css/) para lograr la dinámica. comportamiento de los elementos.

## Formato de archivo DHTML

Los archivos DHTML son archivos de texto sin formato que contienen código DHTML para implementar el comportamiento dinámico de los elementos web.


### DOM DHTML

El modelo de objeto de documento DHTML (DOM) se basa en el DOM HTML que es una estructura de árbol con elementos, atributos y texto como se muestra en la siguiente imagen.

{{< figure src="../dhtml.png" alt="DOM HTML" >}}

El nodo 'Documento' se puede usar para llamar a varias funciones para implementar diferentes funcionalidades. El siguiente ejemplo simplemente usa el método document.write() de JavaScript en DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Este código escribe el texto "Hello World" para generar en el navegador.

### Eventos DHTML

|S.Nro.|Evento|Ocurrencia|
---|---|---|
|1|onabort|Ocurre cuando el usuario cancela la carga de la página o del archivo multimedia.|
|2|onblur|Ocurre cuando el usuario abandona un objeto HTML.|
|3|onchange|Ocurre cuando el usuario cambia o actualiza el valor de un objeto.|
|4|onclick|Ocurre o se desencadena cuando cualquier usuario hace clic en un elemento HTML.|
|5|ondblclick|Ocurre cuando el usuario hace clic en un elemento HTML dos veces seguidas.|
|6|onfocus|Ocurre cuando el usuario enfoca un elemento HTML. Este controlador de eventos funciona de forma opuesta a onblur.|
|7|onkeydown|Se activa cuando un usuario presiona una tecla en un dispositivo de teclado. Este controlador de eventos funciona para todas las claves.|
|8|onkeypress|Se dispara cuando los usuarios presionan una tecla en un teclado. Este controlador de eventos no se activa para todas las claves.|
|9|onkeyup|Ocurre cuando un usuario suelta una tecla de un teclado luego de presionar sobre un objeto o elemento.|
|10|onload|Ocurre cuando un objeto está completamente cargado.|
|11|onmousedown|Ocurre cuando un usuario presiona el botón de un mouse sobre un elemento HTML.|
|12|onmousemove|Ocurre cuando un usuario mueve el cursor sobre un objeto HTML.|
|13|onmouseover|Ocurre cuando un usuario mueve el cursor sobre un objeto HTML.|
|14|onmouseout|Ocurre o se activa cuando el puntero del mouse se mueve fuera de un elemento HTML.|
|15|onmouseup|Ocurre o se desencadena cuando se suelta el botón del ratón sobre un elemento HTML.|
|16|onreset|Es utilizado por el usuario para resetear el formulario.|
|17|onselect|Se produce después de seleccionar el contenido o texto en una página web.|
|18|onsubmit|Se activa cuando el usuario hace clic en un botón después de enviar un formulario.|
|19|onunload|Se activa cuando el usuario cierra una página web.|

## Referencias

* [HTML dinámico - Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

