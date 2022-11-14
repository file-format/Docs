---
date: 2019-10-11
keywords: css, .css, formato de archivo css, cómo abrir archivos css, hojas de estilo en cascada
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo CSS
linktitle: CSS
description: "Obtenga información sobre el formato de archivo CSS y las API que pueden crear y abrir archivos CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ¿Qué es un archivo CSS? ##

CSS (hojas de estilo en cascada) son archivos que describen cómo se muestran los elementos HTML en la pantalla, el papel, etc. Con HTML, puede tener estilos incrustados o definir estilos en una hoja de estilo externa. Para incrustar los estilos, el \ <style>\</style> se utilizan etiquetas. Las hojas de estilo externas se almacenan en archivos con la extensión .css. Con el CSS externo, puede incluirlo en varias páginas HTML para actualizar el estilo de esas páginas. Incluso un solo archivo CSS se puede usar para diseñar un sitio web completo.

## Breve historia ##

CSS1 se lanzó en 1996 con Bert Bos como coautor. El Grupo de Trabajo de CSS comenzó a trabajar en los temas que no se abordaron en CSS1. Esto resultó en la creación de CSS2 en noviembre de 1997 que se publicó como una recomendación del W3C el 12 de mayo de 1998. Esta versión agregó soporte para dispositivos específicos de medios como impresoras, fuentes descargables, tablas y posicionamiento de elementos. En junio de 1999, CSS3 se convirtió en la recomendación de W3C. Esto dividió la documentación en módulos donde cada módulo tenía características de extensión definidas en CSS2.

## Cómo usar archivos CSS ##

Para usar un archivo CSS, inclúyalo en la sección de encabezado del documento HTML. Utilice la etiqueta de enlace para incluir el archivo como se muestra a continuación.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

el atributo *href* de la etiqueta de enlace contiene la ruta al archivo CSS. Al hacer esto, los estilos aplicables contenidos en el archivo CSS incluido se aplican al documento HTML.

## Sintaxis CSS ##

Una regla CSS se compone de dos componentes, un selector y una declaración. Un selector apunta a un elemento en el documento HTML. Puede ser una etiqueta de elemento, un nombre de clase, un nombre de identificación, múltiples etiquetas que muestren la jerarquía, etc. Una declaración contiene la definición de estilo que comprende la propiedad y el valor. La propiedad identifica la propiedad del elemento que desea cambiar y el valor define su nuevo valor. Cada regla CSS puede tener múltiples declaraciones. El siguiente es un ejemplo de una regla CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

En el ejemplo anterior, tenemos **h1** como un selector que selecciona todas las etiquetas h1 en el documento HTML. La regla tiene dos declaraciones, una para font-weight y otra para color. *font-weight* y *color* son propiedades y *700* y *forestgreen* son sus valores respectivamente.

## Ejemplo de uso de CSS ##

A continuación se muestra el documento HTML de ejemplo y la hoja de estilo utilizada para diseñarlo. La imagen de comparación también se agrega para comparar los documentos HTML con estilo y sin formato.

### Documento HTML ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### Hoja de estilo CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Comparación de salida ###

El lado izquierdo de la imagen muestra el documento HTML sin los estilos aplicados y el lado derecho muestra el documento HTML con los estilos aplicados.

{{< figure src="../CssExample.jpg" alt="Imagen de ejemplo" >}}

## Referencias ##

- [CSS - Wikipedia](https://en.wikipedia.org/wiki/CSS)

