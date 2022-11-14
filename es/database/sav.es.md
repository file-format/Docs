{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extensión", "archivo sav", "formato de archivo sav", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "qué es un archivo sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo SAV y las API que pueden crear y abrir archivos SAV",
  "title" :"SAV - Archivo de datos SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## ¿Qué es un archivo SAV?
El archivo SAV es un archivo de datos creado por el paquete estadístico para las ciencias sociales (SPSS), que es una aplicación ampliamente utilizada por investigadores de mercado, investigadores de salud, empresas de encuestas, gobierno, investigadores de educación, organizaciones de marketing, mineros de datos para análisis estadístico. El SAV se guarda en un formato binario patentado y consta de un conjunto de datos y un diccionario que representa el conjunto de datos, guarda los datos en filas y columnas.

## Formato de archivo SAV
El formato de archivo SAV se ha vuelto relativamente estable, pero no podemos decir que sea estático. La compatibilidad con versiones anteriores y posteriores está disponible opcionalmente cuando sea necesario, pero no se mantiene adecuadamente. Los datos en un archivo SAV se clasifican en las siguientes secciones:

### Encabezado del archivo
Consta de 176 bytes. Los primeros 4 bytes indican la cadena **$FL2** o **$FL3** en la codificación de caracteres utilizada para el archivo. Los últimos tres bytes representan que los datos en el archivo están comprimidos usando **ZLIB**. La siguiente cadena de 60 bytes comienza con **@(#) SPSS DATA FILE** y también determina el sistema operativo y la versión de SPSS que creó el archivo. Luego, el encabezado continúa con campos de seis dígitos, que contienen el número de variables por observación y un código de dígitos para la compresión, y termina con datos de caracteres que indican la fecha y hora de creación y una etiqueta de archivo.
### Registros de descriptores de variables
El registro contiene una secuencia fija de campos, clasificando el tipo y el nombre de la variable junto con la información de formato utilizada por SPSS. Cada registro de variable puede contener opcionalmente una etiqueta de variable de hasta 120 caracteres y hasta tres especificaciones de valores perdidos.
### Etiquetas de valor
Las etiquetas de valor son opcionales y se almacenan en pares de registros con etiquetas de números enteros 3 y 4. El primer registro, que es la etiqueta 3, tiene una secuencia de pares de campos, cada par contiene un valor y la etiqueta de valor asociada. El segundo registro, que es la etiqueta 4, representa a qué variables se aplica el conjunto de valores/etiquetas.
### Documentos
Registros únicos o múltiples con etiqueta de número entero 6. Documentación opcional. contiene líneas de 80 caracteres.
### Registros de extensión
Registros únicos o múltiples con etiqueta de número entero 7. Los registros de extensión brindan información que puede ignorarse de manera segura, pero conservarse, en muchas situaciones, permite que los archivos escritos por software más nuevo conserven la compatibilidad con versiones anteriores. Los registros de extensión tienen etiquetas de subtipo entero.
### Terminador de diccionario
Solo registre con la etiqueta entera 999. Separa el diccionario de las observaciones de datos.
### Observaciones de datos
Se considera que los datos están en orden de observación, por ejemplo, todos los valores de las variables para la primera observación, seguidos de todos los valores para la segunda observación, etc. El formato del registro de datos varía según el código de compresión en el registro del encabezado del archivo. La porción de datos de un archivo .sav se puede descomprimir:
- **código 0**: comprimido por bytecode
- **código 1**: comprimido usando compresión ZLIB
 







## Referencias ##

* [Familia de formatos de archivos de datos del sistema SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

