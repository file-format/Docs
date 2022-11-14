{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Lenguaje maya incrustado", "archivo", "extensión", "formato de archivo", "Maya 3D", "Guía de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Formato de archivo de idioma incrustado maya",
  "description":"Obtenga información sobre el formato de archivo MEL y las API que pueden crear y abrir archivos MEL",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## ¿Qué es un archivo MEL?

Un archivo con la extensión .mel (Maya Embedded Language) es un lenguaje de secuencias de comandos que utiliza Autodesk Maya para crear interfaces gráficas. Le permite automatizar la creación de elementos gráficos usando scripts ejecutables además de la interfaz gráfica de Maya. MEL le permite crear interfaces gráficas sin aprender a programar. Esto se logra mediante la creación de macros y acciones personalizadas que aceleran las tareas repetitivas. Estos procedimientos y scripts le permiten crear modelado personalizado, animaciones, dinámicas y representación de tareas. Autodesk Maya 2020 se puede utilizar para abrir y ver el contenido de un archivo EML.

## Formato de archivo MEL - Más información

El [manual de referencia] de un programador (https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) está disponible para desarrolladores en la sección de documentación de Maya. MEL se basa en comandos de secuencias de comandos de shell, similares a UINX, para lograr cosas. Los comandos basados en secuencias de comandos lo hacen irrelevante para la programación convencional y orientada a objetos (POO), lo que da como resultado que no se utilicen estructuras de datos, llamadas a funciones o uso de OOP como en otros lenguajes.

Algunos puntos clave sobre MEL son los siguientes.

`Comentarios` - Cada declaración en MEL debe terminar con un punto y coma (;), incluso al final de un bloque.

`Valores devueltos`: declarar una expresión que devuelve un valor no imprime automáticamente el valor en MEL. En su lugar, provoca un error.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Comandos para Crear, Editar y Eliminar` - El mismo comando se usa para crear cosas, editar cosas o consultar información sobre cosas existentes. Sin embargo, un indicador controla lo que hace el comando (crear, editar o consultar).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Valor devuelto de la función`: la sintaxis de la función devuelve automáticamente un valor. Para obtener un valor de retorno usando la sintaxis del comando, debe encerrar el comando entre comillas invertidas.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referencias

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

