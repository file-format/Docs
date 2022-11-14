{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DDL y las API que pueden crear y abrir archivos DDL",
  "title" :"Formato de archivo DDL: un archivo de lenguaje de definición de datos",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## ¿Qué es un archivo DDL?

Un archivo con extensión .ddl es un archivo de lenguaje de definición de datos que se utiliza para definir el esquema de una base de datos. Contiene sentencias/comandos para trabajar con estructuras de bases de datos como tablas, columnas, registros y otros campos. Los comandos en un archivo DDL están escritos en [SQL](/es/database/sql/) y pueden realizar operaciones como crear una tabla en la base de datos, soltar y actualizar. Un esquema de base de datos es propiedad de su creador y todas las operaciones CRUD se pueden realizar en él. Las aplicaciones populares que pueden crear y abrir archivos DDL son Windows Text Editor, Jetbrains Intellij Idea y EclipseLink.

## Comandos DDL

Un solo archivo DDL puede contener varios comandos que, debido a la sintaxis correcta, se ejecutarán en secuencia y realizarán cambios en el esquema, como la creación de conjuntos de caracteres y tablas, la eliminación de tablas, el cambio de nombre y la modificación de tablas. Los siguientes comandos DDL se usan comúnmente al trabajar con el esquema de la base de datos.

`CREATE`: se utiliza para crear la base de datos o sus objetos (como tabla, índice, función, vistas, procedimiento de almacenamiento y disparadores).

`DROP`: se utiliza para eliminar objetos de la base de datos.

`ALTER`: se utiliza para modificar la estructura de la base de datos.

`TRUNCATE`: se utiliza para eliminar todos los registros de una tabla, incluidos todos los espacios asignados para que se eliminen los registros.

`COMENTARIO`: agrega comentarios al diccionario de datos.

`RENAME`: cambia el nombre de un objeto existente en la base de datos.

## Ejemplo DDL

El siguiente ejemplo muestra la instrucción DDL para el comando CREAR que crea una tabla y define sus campos.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referencias ##

* [DDL de Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

