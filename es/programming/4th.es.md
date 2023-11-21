
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Cuarto archivo: formato de archivo del cuarto idioma",
  "description":"Obtenga información sobre qué es el formato de archivo .4th con ejemplos y API que pueden crear y abrir archivos 4th.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## ¿Qué es un cuarto archivo?

Un archivo con extensión de archivo .4th es un archivo de programación creado para el **Forth Programming Language**. Contiene código fuente para programas escritos en el lenguaje de programación Forth y genera la salida cuando se ejecuta el programa. Es solo otro archivo de lenguaje de programación similar al archivo fuente [C](/es/programming/c/) y [C++](/es/programming/cpp/).

## Cuarto formato de archivo: más información


### Cuarto ejemplo de código de lenguaje de programación

Aquí hay un ejemplo de un programa simple escrito en Forth que calcula el factorial de un número dado:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

En este ejemplo, la palabra factorial toma un único argumento n y devuelve su factorial. La palabra dup duplica el valor en la parte superior de la pila, drop descarta el valor en la parte superior de la pila y * multiplica los dos valores en la parte superior de la pila. Las construcciones if y start/hasta controlan el flujo del programa.

Para usar este programa, debe ingresar la definición en el intérprete de Forth y luego llamar a la palabra factorial con el número cuyo factorial desea encontrar:

```
10 factorial .
```
Esto daría como resultado el resultado 3628800, que es el factorial de 10.

## Referencias

* [Cuarto lenguaje de programación](https://en.wikipedia.org/wiki/Forth_(programming_language))

