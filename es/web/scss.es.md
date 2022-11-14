---
date: 2019-10-11
keywords: scss, .scss, formato de archivo scss, cómo abrir archivos scss, hoja de estilo sintácticamente impresionante, preprocesador css, sass
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo SCSS - Hoja de estilo en cascada Sass
linktitle: SCSS
description: "Obtenga información sobre el formato de archivo SCSS y las API que pueden crear y abrir archivos SCSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## ¿Qué es un archivo SCSS? ##

SCSS es la segunda sintaxis de Sass (Syntactically Awesome Stylesheet) que utiliza corchetes en lugar de sangrías. SCSS se diseñó de tal manera que un archivo CSS3 válido también es un archivo SCSS válido. Los archivos SCSS se almacenan con la extensión .scss.

## Por qué usar SCSS ##

A medida que los diseños de los sitios web se vuelven complejos, se generan archivos [CSS](/es/web/css/) de gran tamaño. Dichos archivos son más difíciles de mantener. Aquí es donde entra en juego SCSS. SCSS introduce variables, anidamiento, mezclas, importaciones y herencia de selectores en el desarrollo de CSS. Estas adiciones hacen que trabajar con el diseño sea mucho más divertido.

## Cómo usar archivos SCSS ##

Los archivos SCSS no se incluyen directamente en el documento [HTML](/es/web/html/) como CSS. En su lugar, los archivos SCSS se convierten en archivos CSS que se incluyen en los archivos HTML. Para instalar SCSS en su sistema, siga las instrucciones proporcionadas en el [sitio oficial de Sass] (https://sass-lang.com/install).
Para convertir SCSS a CSS, puede convertir un archivo SCSS ya guardado o buscar cambios y convertir a medida que se guarda el archivo. Los comandos para ambos se dan a continuación.

### Convertir una vez ###

El primer parámetro es el archivo SCSS de origen y el segundo parámetro es el archivo CSS de salida.

```cmd
sass main.scss main.css
```

### Esté atento a los cambios ###

El comando tiene un indicador *watch** adicional que mantiene el comando en ejecución y tan pronto como se guarda el archivo SCSS, se genera el CSS de salida.

```cmd
sass --watch main.scss main.css
```

## Sintaxis SCSS ##

SCSS admite variables, anidamiento, mezclas, importaciones, herencia de selectores, etc. A continuación se muestran ejemplos de estas características.

### Variables ###

Mediante el uso de variables, puede establecer información reutilizable, como el color principal o el color de fondo, para el botón Guardar. Esto es útil si necesita cambiar esa información, simplemente cámbiela en una ubicación y se actualiza donde sea que se use.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Puede anidar los selectores de CSS de forma similar a la jerarquía de HTML. En el ejemplo que se muestra a continuación, el tramo está anidado dentro del bloque h1.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
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

Los mixins se pueden usar para agrupar propiedades similares que se usan juntas en varios lugares. También puede pasar parámetros a mixins.

**SCSS**

**Declarando una mezcla**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**Usando una mezcla**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
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

Extend/Inheritance es útil en los casos en que las propiedades de un selector deben compartirse con otro selector. En el siguiente ejemplo, el selector *.error-notice* toma todas las propiedades del selector *.error-text* y agrega propiedades de borde y relleno.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
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

La importación puede ser útil en la separación de preocupaciones. Puede dividir los estilos de tal manera que los estilos de encabezado estén en un archivo separado, los estilos de pie de página estén en un archivo separado, todas las variables de color utilizadas en los estilos puedan estar en un archivo separado, etc. Usando esta técnica, el los estilos se mantienen organizados. Simplemente importe los archivos en su archivo SCSS principal como se muestra en el ejemplo a continuación. No necesita especificar la extensión del archivo en la instrucción de importación. Sass compila todos los archivos SCSS directamente. Para evitar que los archivos de importación se compilen directamente, puede hacerlos parciales agregando un guión bajo (_) antes de su nombre. Puede importar parciales similares a los archivos SCSS normales sin el guión bajo.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

El CSS de salida tendrá los estilos de todos los archivos importados.

## Referencias ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [Sass](https://sass-lang.com/)

