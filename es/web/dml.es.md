{
  "date" : "2021-05-25",
  "keywords" :[ "DML", "archivo DML", "formato de archivo DML", "tipo de archivo DML", "archivo", "tipo", "qué es un archivo DML" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DML - Archivo HTML de DynaScript",
  "description":"Obtenga información sobre el formato de archivo DML y las API que pueden crear y abrir archivos DML",
  "linktitle" : "DML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-25"
}

## ¿Qué es un archivo DML?

Un archivo con extensión .dml es un archivo de código de página de script web creado con DyanScript. DynaScript es un lenguaje de secuencias de comandos [HTML](/es/web/html/) dinámico que es compatible con ECMAScript y proporciona la mayoría de las mismas características que otros lenguajes de secuencias de comandos. Es similar al código ColdFusion y al código de Microsoft Active Server Pages (ASP). Los archivos DML se pueden abrir y ver en navegadores web estándar similares a otras páginas HTML.

## Formato de archivo DML

Los archivos DML se crean en formato de archivo de texto sin formato y se pueden abrir con un editor de texto para ver el código. La escritura de código mediante el lenguaje de secuencias de comandos DML se puede utilizar para generar HTML de forma dinámica en páginas DML alojadas en el lado del servidor. Los DynaScripts se crean a partir de los siguientes elementos del lenguaje:


* Etiqueta SCRIPT: están incrustadas en los documentos como comentarios HTML. Un comentario HTML se marca con \ <!-- tag.
* Literales: estos son valores fijos en los archivos de DynaScript. Ejemplos de estos incluyen números enteros como s 123 , 0x3F , 0123, números de punto flotante como 456.789 , 3.2e-8, booleanos como verdadero o falso y cadenas como "La lluvia en España".
* Variables: no es necesario definir las variables de DynaScript ni asignarlas a un tipo de datos fijo. Una variable debe tener un valor antes de usarla en una expresión; de lo contrario, se genera una advertencia de tiempo de ejecución.
* Expresiones: son combinaciones de variables, valores literales, operadores y otras expresiones. El lado derecho de una instrucción de asignación es una expresión.
* Operadores - Estos operan en una o más expresiones llamadas operandos. Estos pueden ser ternarios, binarios o unarios: los operadores ternarios actúan sobre tres expresiones, los operadores binarios actúan sobre dos expresiones y los operadores unarios actúan sobre una.
* Declaraciones: controlan el flujo de scripts, manipulan objetos y programan en general. En general, estas declaraciones siguen la sintaxis estándar de C y Java. Los ejemplos son if-else, do-while loops, switch, break, continue, etc. como cualquier otro lenguaje de scripting.
* Funciones: las funciones, como cualquier otro lenguaje de secuencias de comandos, le permiten encapsular un conjunto de instrucciones una vez en un documento como una función y luego usarlo varias veces a lo largo del documento (llamando a la función). DynaScript también admite funciones.
* Objetos: DynaScript está orientado a objetos y admite `objetos` y los conceptos fundamentales orientados a objetos de encapsulación, polimorfismo y herencia.

