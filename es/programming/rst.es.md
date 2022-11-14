{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo RST: archivo de texto reestructurado",
  "description":"Obtenga información sobre el formato de archivo RST y las API que pueden crear y abrir archivos RST",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## ¿Qué es un archivo RST?

Un archivo RST es un formato de archivo de documentación técnica, utilizado principalmente en la comunidad de programación de Python. Es un archivo de texto escrito en el lenguaje de marcado reStructuredText que aplica estilos y formato a documentos de texto sin formato para la generación de documentación. Los archivos RST usan los comentarios y otra información en el código de los programas de Python para crear documentación técnica de la aplicación. Sin embargo, estos también pueden contener texto que se puede convertir en páginas web simples y [eBooks](/es/ebook/). Se pueden usar editores de texto como Github Atom, GNU Emacs (multiplataforma), Microsoft Notepad (Windows), Apple TextEdit (Mac) y Vim (Linux) para abrir archivos RST.

## Formato de archivo RST

Los archivos RST contienen código escrito en lenguaje de marcado reStructuredText. Forma parte del proyecto Docutils de Python Doc-SIG (Documentation Special Interest Group) que proporciona un conjunto de herramientas para Python similar a Javadoc para Java. El analizador para el formato de archivo RST está integrado en Docutils y puede extraer información de los programas de Python para formatearlos en la documentación del programa.

### Ejemplo de RST de texto reestructurado

Tomemos un texto de ejemplo escrito en formato de archivo RST de la siguiente manera.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Cuando este texto se ingresa en un procesador rST como Docutils, el resultado es el siguiente.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referencia ##

* [ReStructuredText - por Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

