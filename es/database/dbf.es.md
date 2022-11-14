{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extensión", "archivo dbf", "formato de archivo dbf", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "qué es un archivo dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo DBF y las API que pueden crear y abrir archivos DBF",
  "title" :"DBF - Archivo de base de datos dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## ¿Qué es un archivo DBF?
El archivo con extensión .dbf es un archivo de base de datos utilizado por una aplicación de sistema de gestión de base de datos denominada **dBASE**. Inicialmente, la base de datos dBASE se denominó Project Vulcan; iniciado por **Wayne Ratliff** en 1978. El tipo de archivo DBF se introdujo con dBASE II en 1983. Organiza múltiples registros de datos con campos de tipo Array. El software de base de datos **xBase** que es popular debido a su compatibilidad con una amplia gama de formatos de archivo; también es compatible con los archivos DBF.

## Formato de archivo DBF
El formato de archivo DBF pertenece al sistema de administración de bases de datos dBASE, pero puede ser compatible con xBase u otros software DBMS. La versión inicial del archivo dbf consistía en una tabla simple en la que se podían agregar, modificar, eliminar o imprimir datos utilizando el conjunto de caracteres ASCII. Con el paso del tiempo, se mejoró .dbf y se agregaron archivos adicionales para aumentar las características y capacidades del sistema de base de datos.

En la dBASE moderna, un archivo DBF consta de un encabezado, los registros de datos y el marcador EOF (fin de archivo).

- El encabezado contiene información sobre el archivo, como la cantidad de registros y la cantidad de tipos de campos utilizados en los registros.
- Los registros contienen los datos reales.
- El final del archivo está marcado por un solo byte, con valor 0x1A.

### Encabezado del archivo
El diseño del encabezado del archivo en dBase se proporciona en la siguiente tabla:

| byte | Contenidos | significado |
---|---|---|
| 0 | 1 byte | dBASE válido para archivo DOS; los bits 0–2 indican el número de versión, el bit 3 indica la presencia de un archivo memo de dBASE para DOS, los bits 4–6 indican la presencia de una tabla SQL, el bit 7 indica la presencia de cualquier archivo memo (ya sea dBASE m PLUS o dBASE para DOS) |
| 1–3 | 3 bytes | Fecha de la última actualización; formateado como AAMMDD |
| 4–7 | número de 32 bits | Número de registros en el archivo de la base de datos |
| 8–9 | número de 16 bits | Número de bytes en el encabezado |
| 10–11 | número de 16 bits | Número de bytes en el registro |
| 12–13 | 2 bytes | Reservado; llenar con 0 |
| 14 | 1 byte | Bandera que indica transacción incompleta [nota 1] |
| 15 | 1 byte | Indicador de cifrado[nota 2] |
| 16–27 | 12 bytes | Reservado para dBASE para DOS en un entorno multiusuario |
| 28 | 1 byte | Indicador de archivo .mdx de producción; 1 si hay un archivo .mdx de producción, 0 si no |
| 29 | 1 byte | Id. de controlador de idioma |
| 30–31 | 2 bytes | Reservado; llenar con 0 |
| 32–n [nota 3][nota 4] | 32 bytes cada uno | matriz de descriptores de campo (consulte a continuación el diseño de los descriptores) |
| norte + 1 | 1 byte | 0x0D como terminador de matriz de descriptor de campo |

- La función ISMARKEDO verifica este indicador (BEGIN TRANSACTION lo establece en 1, END TRANSACTION y ROLLBACK lo restablece en 0).
- Si este indicador se establece en 1, aparece el mensaje Base de datos cifrada.
- El número máximo de campos es 255.
- n significa el último byte en la matriz de descriptores de campo.

### Matriz de descriptores de campo
Diseño de descriptores de campo en dBASE:

| byte | Contenidos | significado |
---|---|---|
| 0–10 | 11 bytes | Nombre de campo en ASCII (completado con ceros) |
| 11 | 1 byte | Tipo de campo. Valores permitidos: C, D, F, L, M o N (consulte la siguiente tabla para conocer los significados) |
| 12–15 | 4 bytes | Reservado |
| 16 | 1 byte | Longitud de campo en binario (máximo 254 (0xFE)). |
| 17 | 1 byte | Recuento decimal de campo en binario |
| 18–19 | 2 bytes | Identificación del área de trabajo |
| 20 | 1 byte | Ejemplo |
| 21–30 | 10 bytes | Reservado |
| 31 | 1 byte | Indicador de campo MDX de producción; 1 si el campo tiene una etiqueta de índice en el archivo MDX de producción, 0 en caso contrario |

### Registros de la base de datos
Cada registro comienza con un indicador de eliminación (1 byte). Los campos se envuelven en registros sin separadores de campo. Todos los datos de campo son ASCII. Dependiendo del tipo de campo, la aplicación impone más restricciones. Estos son los tipos de campo en dBase:

| Tipo de campo | Mnemónico | Lo que acepta |
-------|-----|----|
| C | Personaje | Cualquier texto ASCII (rellenado con espacios hasta la longitud del campo) |
| D | Fecha | Números y un carácter para separar el mes, el día y el año (almacenados internamente como 8 dígitos en formato AAAAMMDD) |
| F | punto flotante | -, ., 0–9 (justificado a la derecha, relleno con espacios en blanco) |
| L | lógico | Y, y, N, n, T, t, F, f o ? (cuando no está inicializado) |
| m | Nota | Cualquier texto ASCII (almacenado internamente como 10 dígitos que representan un número de bloque .dbt, justificado a la derecha, relleno con espacios en blanco) |
| norte | numérico | -, ., 0–9 (justificado a la derecha, relleno con espacios en blanco) |









## Referencias ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

