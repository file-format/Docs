{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo BCP y las API que pueden crear y abrir archivos BCP",
  "title" :"BCP: formato de archivo de copia masiva de SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo BCP?

BCP (formato de copia masiva) es el formato de datos técnicos de Microsoft SQL Server que define estructuras de datos para almacenar diferentes valores de tipos de datos de bases de datos para importar/exportar. El formato define completamente la interpretación de cada columna de datos para que se pueda leer el conjunto de valores especificado en el archivo de datos. La utilidad [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) usa el formato de archivo BCP para leer datos de dicho archivo e identificarlo.


## Formato de archivo BCP

El archivo de formato BCP es un documento XML que define el orden de las columnas, el nombre y el tipo de datos. Permite a los usuarios importar/exportar una gran cantidad de datos desde un archivo de datos especificando estos campos. Esto es útil en la importación masiva de valores de datos desde archivos de datos. El número y el orden de los campos de datos en el archivo de datos pueden ser diferentes a los de las columnas de la tabla de destino. Aquí es cuando el archivo de formato de datos BCP ayuda al especificar el orden y el tipo de columnas para importar los datos.

La estructura del archivo de formato se representa en el siguiente formato.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Tipos de datos BCP

|Tipo de datos|Rango|Representación|
---|---|---|
|BigInt|-263 (-9,223,372,036,854,775,808) a 263-1 (9,223,372,036,854,775,807)|`BigInt = ["-"]1*19DIGIT`|
|Binario|1 a 8000 bytes|formato de cadena Unicode con codificación hexadecimal `Binary = 32000OCTET`|
|Bit|0 o 1|cadena Unicode simple Bit = "0" / "1"|
|Char|1 a 8000|Formato de cadena Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET con n = 4 x (2,147,483,647)|
|Fecha|0001-01-01 a 9999-12-31|formato de cadena AAAA-MM-DD|
|DateTime|1753-01-01 00:00:00.000 hasta 9999-12-31 23:59:59.997| Unicode AAAA-MM-DD hh:mm:ss[.nnn] formato de cadena|
|DateTime2|0001-01-01 00:00:00.0000000 hasta 9999-12-31 23:59:59.9999999.| Unicode YYYY-MM-DD hh:mm:ss[.nnnnnnn] formato de cadena|
|DateTimeOffset|0001-01-01 00:00:00.0000000 hasta 9999-12-31 23:59:59.9999999 en la zona horaria de tiempo universal coordinado (UTC)| Unicode AAAA-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] formato de cadena|
|Decimal|-1038 + 1 a 1038 – 1|Formato de cadena Unicode `Decimal = ["-"] 0*38DIGIT ["."0*38DIGIT]`|
|Flotante|-1.79E+308 a -2.23E-308; 0; de 2.23E-308 a 1.79E+308|formato de cadena Unicode|
|Imagen|secuencia de bytes que van desde 0 hasta 231 – 1 (2,147,483,647)|formato de cadena Unicode con codificación hexadecimal|
|Int|-231 (-2,147,483,648) a 231 – 1 (2,147,483,647)|Formato de cadena Unicode|

## Referencias

* [Formato BCP - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

