{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo BML - Archivo de lenguaje de marcado Bean",
  "description":"Obtenga información sobre el formato de archivo BML y las API que pueden crear y abrir archivos BML",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## ¿Qué es un archivo BML?

Un archivo con extensión .bml es un archivo de Bean Markup Language que almacena clases de Java para admitir aplicaciones de Java. Esto permite el acceso a objetos y métodos de Java, y no necesita crear nuevas funciones usando clases de Java. Especifica cómo se conectan los componentes entre sí para realizar tareas útiles. BML fue desarrollado por IBM alphaWorks para describir las estructuras y las relaciones de los componentes. Los archivos BML se pueden abrir y visualizar con cualquier editor de texto, como navegadores web, Microsoft Notepad y Notepad++.

## Formato de archivo BML

El sitio web de IBM alphaworks ha proporcionado dos implementaciones de BML. La primera implementación es un intérprete que 'reproduce' un script BML para generar la jerarquía de beans deseada. La segunda implementación es un compilador que compila cualquier script BML en código Java sin reflejos. Esto es ventajoso en el sentido de que permite capturar la estructura entre componentes de la aplicación utilizando un lenguaje diseñado para este propósito específico con la capacidad adicional de compilarlo en código Java 'normal'.

## Etiquetas BML

La siguiente es una explicación de algunas de las etiquetas utilizadas en el lenguaje BML:

### Los<bean> etiqueta:

los<bean> El elemento se usa para crear nuevos beans o para buscar beans por nombre. los<bean> la etiqueta tiene el formato:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
El "id" en la etiqueta está asociado con el registro de objetos para el JavaBean.

### Los<string> etiqueta

Hay dos formas en que se puede usar la etiqueta de cadena:

1. Para crear una cadena no vacía:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Para crear una cadena vacía:

```
<string/>
```
## Referencias

* [Mensajería orientada a objetos con XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [El lenguaje de marcado físico](http://web.mit.edu/mecheng/pml/standards.htm)


