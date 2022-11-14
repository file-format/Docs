---
date: 2019-10-11
keywords: js, .js, formato de archivo js, cómo abrir archivos js, archivos javascript
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo JS
linktitle: JS
description: "Obtenga información sobre el formato de archivo JS y las API que pueden crear y abrir archivos JS."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## ¿Qué es un archivo JS? ##

JS (JavaScript) son archivos que contienen código JavaScript para su ejecución en páginas web. Los archivos JavaScript se almacenan con la extensión .js. Dentro del documento [HTML](/es/web/html/), puede incrustar el código JavaScript usando el \ <script>\</script> etiquetas o incluir un archivo JS. Al igual que los archivos [CSS](/es/web/css/), los archivos JS se pueden incluir en varios documentos HTML para la reutilización del código. JavaScript se puede utilizar para manipular el HTML DOM.

## Breve historia ##

JavaScript se envió por primera vez como parte del navegador Navigator en septiembre de 1995 con el nombre LiveScript de Netscape. Fue rebautizado como JavaScript tres meses después. En 1996, Microsoft realizó ingeniería inversa del intérprete de Navigator para crear JScript. JScript se lanzó con Internet Explorer y era muy diferente a JavaScript.

Netscape envió JavaScript a ECMA International que condujo al lanzamiento oficial de la primera especificación de ECMAScript en 1997. ECMAScript 2 se lanzó en 1998, ECMAScript 3 en 1999 y el trabajo en ECMAScript 4 comenzó en 2000 pero nunca llegó a buen término.

Jesse James Garrett en 2005 publicó un libro blanco donde acuñó el término *Ajax*. Esto usó JavaScript como columna vertebral para crear aplicaciones web que cargaban datos en segundo plano y evitaban recargas de páginas completas. Esto resultó en la creación de bibliotecas como JQuery, Prototype, Dojo, etc.

Google lanzó el navegador Chrome con el motor JavaScript V8 en 2008. A principios de 2009, se llegó a un acuerdo para combinar todo el trabajo relevante e impulsar JavaScript. Esto resultó en el lanzamiento del estándar ECMAScript 5 en diciembre de 2009.

## Cómo usar archivos JS ##

Para usar un archivo JS, inclúyalo en el documento HTML. Utilice la etiqueta de enlace para incluir el archivo como se muestra a continuación.

```html
<script src="site.js"></script>
```

El atributo *src* de la etiqueta *script* contiene la ruta al archivo JS. Al hacer esto, la funcionalidad JS se agrega al documento HTML.

## Sintaxis JS ##

Los archivos de JavaScript pueden contener variables, operadores, funciones, condiciones, bucles, matrices, objetos, etc. A continuación se ofrece una breve descripción general de la sintaxis de JavaScript.

- Cada comando termina con un punto y coma (;).
- Utilice la palabra clave *var* para declarar variables.
- Admite operadores aritméticos ( + - * / ) para calcular valores.
- Los comentarios de una sola línea se agregan con // y los comentarios de varias líneas están rodeados por /* y */.
- Todos los identificadores distinguen entre mayúsculas y minúsculas, es decir, *modelNo* y *modelno* son dos variables diferentes.
- Las funciones se definen mediante la palabra clave *función*.
- Las matrices se pueden definir usando corchetes [].
- JS admite operadores de comparación como ==, != , >=, !==, etc.
- Las clases se pueden definir usando la palabra clave *clase*.

## Ejemplo de uso de JS ##

A continuación se muestra un archivo JavaScript de ejemplo de uso simple.

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### Código JS ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## Referencias ##

- [JS - Wikipedia](https://en.wikipedia.org/wiki/JavaScript)

