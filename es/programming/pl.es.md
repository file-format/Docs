{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "archivo", "extensión", "formato", "Perl", "lenguaje Perl", "archivos PL", "programación"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo PL y las API que pueden crear y abrir archivos PL",
  "title" :"Archivo PL - Formato de archivo de script Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## ¿Qué es un archivo PL?

Un archivo con extensión .pl es un archivo Perl Script que es un lenguaje de secuencias de comandos. Estos se compilan y ejecutan con el software Perl Interpreter. Un archivo de script PL contiene líneas de código, variables y comentarios. Los lenguajes de secuencias de comandos son comparativamente difíciles de
comprender otros formatos de archivo de programación como [PHP](/es/programming/php/). Los archivos PL se pueden crear y son compatibles con Windows, macOS y Linux.

## Breve historia del lenguaje de secuencias de comandos Perl

Este lenguaje se mantuvo en uso por primera vez en 1987, por lo que estos archivos tuvieron su origen en ese año. En 1989 se lanzó Perl 2. Posteriormente, se actualizó y se modificó hasta la versión 5.35, y se espera que la próxima versión se lance el próximo año.

En cada actualización, se han agregado herramientas sobre la funcionalidad, el rendimiento y el aspecto del idioma y los archivos. Ha habido muchas revisiones sobre las versiones en estos años. Originalmente era un lenguaje de secuencias de comandos básico, pero ahora también incluye muchos otros módulos. Originalmente, era un lenguaje muy simple, pero las escrituras de este lenguaje eran bastante difíciles de entender ya que eran compactas.

## Especificaciones de la extensión de formato de archivo Perl

Existen algunas propiedades o especificaciones de estos archivos de programación, algunas de ellas son las siguientes:

* El código incluido en estos archivos está en formato de texto sin formato y se utiliza para el desarrollo de scripts
* La secuencia de comandos del servidor, el análisis de texto y la administración del servidor son los aspectos principales que cubre la secuencia de comandos de este lenguaje.
* Muchos programas populares asociados con este lenguaje son Active state Active Perl y Bare Bones BBEdit (compatible con Mac OS)
* Este lenguaje se considera un lenguaje de alto nivel
* Para Win32, es posible que el usuario deba instalar una distribución binaria nativa del idioma
* Requiere algunas herramientas de secuencias de comandos para convertirse en ejecutable en varios kits de recursos de Windows
* Visual Studio .NET es un marco famoso para el desarrollo de lenguajes de programación. La herramienta Active State conocida como Visual Perl se usa para agregar Perl a Visual Studio
* En los archivos, la primera línea del código fuente describe la información del intérprete que se está utilizando. Los archivos PL generalmente comienzan con la línea **#!/usr/bin/perl** que le dice a su computadora que ejecute este script usando un intérprete de Perl instalado en la computadora.


## Ejemplos de secuencias de comandos PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Esto se imprimirá

```
Hello, World
```

### Comentario de una sola línea ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Comentario de varias líneas ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Asignación de variables ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Asignación de variables escalares ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Operaciones escalares simples ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referencias ##

- [Python (lenguaje de programación) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

