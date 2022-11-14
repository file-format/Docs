{
  "date" : "2021-08-24",
  "keywords" :[ "archivo wdb", "formato de archivo wdb", "qué es un archivo wdb", "archivo", "ejemplo de wdb", "extensión de archivo wdb","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo WDB y las API que pueden crear y abrir archivos WDB",
  "title" :"WDB: archivo de seguimiento de SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## ¿Qué es un archivo WDB?
Un archivo con la extensión .wdb es en realidad un archivo de base de datos creado por Microsoft Works que se utilizó para realizar funciones como un sistema de administración de bases de datos. El archivo WDB es similar al archivo Access Database ([MDB](/es/database/mdb/)), pero menos eficiente y con mayores limitaciones. Los archivos WDB no se pueden abrir con Microsoft Access. Sin embargo, puede abrir el archivo WDB en Microsoft Works y luego exportarlo a un archivo MDB para abrir un archivo WDB en MS Access.

## formato de archivo WDB
Microsoft Works Database es el formato de base de datos nativo de la suite ofimática Microsoft Works. Debido a la naturaleza propietaria del formato y algunas limitaciones. Los archivos WDB no se pueden abrir en ningún otro software que no sea Microsoft Works. En el formato de archivo, se puede encontrar un encabezado recurrente de 10 bytes antes de cada una de las cadenas de texto ASCII que representan los valores de los campos que terminaron con un valor NULL. El encabezado generalmente comienza con un byte **\x0f** y NULL, seguido de 4 bytes de datos alternados con NULL.

### Estructura del archivo

La estructura del archivo WDB se muestra a continuación:
- **1er encabezado**: desde el principio del archivo, terminando en \x25\x00\xf2 y 244 bytes NULL
- **Segundo encabezado**: comienza con \xffT, es decir, \xff\x54 y se extiende hasta 4096 bytes, que contiene nombres de columna/campo y otras cosas, y parece comenzar en la posición de byte 6144.
- **Campo**: el valor tiene un encabezado de 10 bytes, con el siguiente formato: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , parte 2} {db 4} \x00. el byte de datos 2 es el número de campo, el byte de datos 3 es el número de registro (agregando el byte de datos 3, parte 2 cuando supera los 256 registros).


## Referencias ##

* [Usuario:JesseW/formato wdb](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

