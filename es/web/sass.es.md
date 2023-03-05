---
date: 2019-10-11
keywords: sass, .sass, formato de archivo sass, cómo abrir archivos sass, hoja de estilo sintácticamente impresionante, preprocesador css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo Sass
linktitle: Sass
description: "Obtenga información sobre el formato de archivo Sass y las API que pueden crear y abrir archivos Sass."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## ¿Qué es un archivo SASS? ##

Sass (hojas de estilo sintácticamente asombrosas) es un lenguaje de secuencias de comandos de preprocesador. Se compila en [CSS](/es/web/css/) y se almacena con la extensión .sass. Sass consta de dos sintaxis, la original basada en sangrías que usa la extensión .sass y la SCSS más nueva con formato de bloque como CSS que usa la extensión .scss.

## Por qué usar Sass ##

Sass es realmente útil para mantener estilos, ya que proporciona muchas funciones, como la introducción de variables, anidamiento, mezclas, importaciones y herencia de selectores que hacen que trabajar con estilos sea divertido.

## Cómo usar archivos SASS ##

Los archivos SASS no se incluyen directamente en el documento [HTML](/es/web/html/), sino que se convierten en archivos CSS que se incluyen en los archivos HTML. Puede instalar Sass en su sistema siguiendo las instrucciones proporcionadas en el [sitio oficial de Sass](https://sass-lang.com/install).

Sass se puede convertir a CSS ya sea convirtiendo un archivo SASS ya guardado o observando los cambios y convirtiendo a medida que se guarda el archivo. Los comandos para ambos se dan a continuación.

### Convertir una vez ###

El primer parámetro del comando es el archivo SASS de origen y el segundo parámetro es el archivo CSS de salida.

```cmd
sass main.sass main.css
```

### Esté atento a los cambios ###

El comando anterior se puede ejecutar con un indicador *watch* adicional que mantiene el comando en ejecución y tan pronto como se guarda el archivo Sass, se genera el CSS de salida.

```cmd
sass --watch main.sass main.css
```

## Sass Sintaxis ##

Sass admite variables, anidamiento, mezclas, importaciones, herencia de selectores, etc. A continuación se muestran ejemplos de estas características.

### Variables ###

Las variables se pueden usar para establecer información reutilizable, como el color principal o el relleno de un botón. Esto puede resultar útil si en el futuro necesita cambiar esa información, simplemente cámbiela en una ubicación y se actualiza en todas partes.

**Hablar con descaro a**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS generado**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Anidamiento ###

Los selectores de CSS se pueden anidar de forma similar a la jerarquía de HTML. En el siguiente ejemplo, el tramo está anidado dentro del bloque h1.

**Hablar con descaro a**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
```

**CSS generado**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### Mezclas ###

Los mixins se usan para agrupar propiedades similares que se usan en varios lugares. Los mixins también admiten parámetros.

**Hablar con descaro a**

**Declarando una mezcla**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**Usando una mezcla**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
```

**CSS generado**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### Extender ###

Extend/Inheritance puede resultar útil en los casos en que las propiedades de un selector deben compartirse con otro selector. En el siguiente ejemplo, el selector *.error-notice* toma todas las propiedades del selector *.error-text* y agrega propiedades de borde y relleno.

**Hablar con descaro a**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
```

**CSS generado**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### Importar ###

La importación puede ser útil si estructura sus estilos en diferentes archivos según la funcionalidad o cualquier otra estructura que siga. Puede importar todos estos archivos en un archivo SASS principal que luego se convierte a CSS. Durante la importación, no necesita especificar la extensión del archivo en las instrucciones de importación. Sass compila todos los archivos SASS directamente. Para evitar que los archivos de importación se compilen directamente, puede hacerlos parciales agregando un guión bajo (_) al comienzo de su nombre. Los parciales se importan de forma similar a los archivos Sass normales.

**Hablar con descaro a**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

El CSS de salida tendrá los estilos de todos los archivos importados.

## Referencias ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

