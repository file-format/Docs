{
  "date" : "2020-08-20",
  "keywords" :[ "archivo cff", "formato de archivo cff", "qué es un archivo cff", "archivo", "ejemplo cff", "extensión de archivo cff","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Formato de archivo de fuente compacto",
  "description":"Obtenga más información sobre el formato de archivo CFF y las API para crear y abrir archivos CFF",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## ¿Qué es un archivo CFF?

Un archivo con la extensión .cff es un formato de fuente compacto y también se conoce como PostScript Tipo 1 o CIDFont. CFF actúa como un contenedor para almacenar varias fuentes juntas en una sola unidad conocida como FontSet. El diseño de fuentes CFF permite incrustar código de lenguaje PostScript que permite mayor flexibilidad y extensibilidad del formato para su uso con entornos de impresión. Los archivos de fuentes CFF se pueden abrir y convertir mediante API como [Aspose.Font](https://products.aspose.com/font).

## Formato de archivo CFF

Los archivos CFF son archivos binarios que contienen un diseño de datos estructurados, tienen tipos de datos definidos, un encabezado, organización de glifos y diccionarios de tablas. Se pueden encontrar más detalles sobre estos en las [especificaciones de formato de fuente compacta] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Diseño de datos
El diseño de datos del formato de archivo CFF se muestra a continuación.

|Entrada|Comentarios|
---|---|
|Encabezado|–|
|NombreINDEX|–|
|Arriba ÍNDICE DICT|–|
|Cadena ÍNDICE|–|
|ÍNDICE Global Subr|–|
|Codificaciones–Juegos de caracteres|–|
|FDSeleccionar|CIDFuentes solamente|
|CharStrings ÍNDICE|por-fuente|
|Fuente DICT INDEX|por fuente, solo CIDFonts|
|DICT privado|por fuente|
|ÍNDICE Subr local|por fuente o por DICT privado para CIDFonts|
|Avisos de derechos de autor y marcas registradas|–|

### Tipos de datos

Los tipos de datos CFF son los que se muestran en la siguiente tabla.

|Nombre|Rango|Descripción|
---|---|---|
|Card8|0 –255|número sin firmar de 1 byte|
|Card16|0 – 65535|número sin firmar de 2 bytes|
|Offset|varía|1, 2, 3 o 4 bytes de desplazamiento (especificado por el campo OffSize)|
|OffSize|1–4|número sin signo de 1 byte especifica el tamaño de un campo o campos de compensación|
|SID|0 – 64999|identificador de cadena de 2 bytes|

### Encabezado

Los datos binarios comienzan con un encabezado que tiene el formato que se muestra en la siguiente tabla.

|Tipo|Nombre|Descripción|
---|---|---|
|Tarjeta8|mayor|Formatear versión mayor (a partir de 1)|
|Card8|menor|Formatear versión menor (a partir de 0)|
|Card8|tamaño hdr| Tamaño del encabezado (bytes) |
|OffSize|offSize|Desplazamiento absoluto (0) tamaño|

## Referencias

* [Tabla de formato de fuente compacta](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Formato de archivo CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Conjunto de gráficos CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

