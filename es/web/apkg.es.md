{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","archivo apkg", "formato de archivo apkg", "tipo de archivo apkg", "archivo", "tipo", "¿Qué es un archivo APKG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Formato de archivo de la baraja de tarjetas Flash de Anki",
  "description" :"Aprenda qué es un archivo APKG y las API que pueden crearlos y abrirlos",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## ¿Qué es un archivo APKG?

Un archivo con la extensión .apkg es una baraja de tarjetas flash generadas para usarse en la aplicación de software [Anki](https://ankiweb.net/about) que es un programa de aprendizaje basado en tarjetas flash. Contiene texto [HTML](/es/web/html/) que se cargará y mostrará en la aplicación Anki y, además, puede tener imágenes y sonidos para el aprendizaje visual y auditivo. Anki permite a los usuarios crear sus propios mazos de tarjetas flash de Anki, así como importar los mazos de tarjetas flash de otros usuarios.

## Formato de archivo APKG

Los mazos de cartas de Anki se crean a partir de plantillas escritas en HTML, un lenguaje famoso y común para crear páginas web. El estilo de las cartas de mazo se realiza mediante CSS, que es el lenguaje utilizado para diseñar páginas web. El estilo incluye modificaciones a:

* font-family: el nombre de la fuente que se utilizará en la tarjeta.
* font-size - El tamaño de la fuente en píxeles.
* text-align: define si el texto debe alinearse en el centro, a la izquierda o a la derecha.
* color: define el color del texto, que puede ser un nombre de color simple como "azul", "rojo", etc. o códigos de color HTML.
* background-color - Define el color de fondo de la tarjeta

La información de estilo se comparte entre todas las tarjetas y afecta a todas las tarjetas cuando se realiza un cambio. El siguiente ejemplo usará un fondo amarillo en todas las tarjetas excepto en la primera:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

El cambio de tamaño de las imágenes en una tarjeta Anki se puede controlar de la siguiente manera.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Incrustar Javascript en tarjetas Anki

Es posible incrustar [Javascript](/es/web/js/) en una tarjeta Anki usando las plantillas de tarjeta. Sin embargo, debido al nivel avanzado de Javascript, no se brinda soporte. Además, los dispositivos de representación pueden mostrar los efectos de implementación de Javascript en la tarjeta de manera diferente, lo que genera la necesidad de probar la implementación en todos los dispositivos. Ciertas funciones de Javascript, como window.alert, dificultan la depuración del código Javascript que ha escrito.

## Referencias ##

* [Documentación Anki](https://docs.ankiweb.net/intro.html)

