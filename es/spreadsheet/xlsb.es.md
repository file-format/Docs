{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "archivo", "extensión", "formato de archivo", "Archivo de hoja de cálculo binario de Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tu guía de formato de archivo para saber qué es un archivo XLSB y las API que puedes crear y abrir",
  "title" :"¿Qué es un archivo XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo XLSB?

El formato de archivo XLSB especifica el formato de archivo binario de Excel, que es una colección de registros y estructuras que especifican el contenido del libro de Excel. El contenido puede incluir tablas no estructuradas o semiestructuradas de números, texto o números y texto, fórmulas, conexiones de datos externos, gráficos e imágenes. A diferencia de [XLSX](/es/spreadsheet/xlsx/) (que se basa en el formato de archivo Open XML), el XLSB representa un archivo de libro de Excel binario. Los archivos XLSB se pueden leer y escribir más rápido, lo que los hace útiles para trabajar con archivos grandes. XLSB rara vez se usa para almacenar libros de trabajo, ya que XLSX (y anteriormente [XLS](/es/spreadsheet/xls/)) son los formatos de archivo más comunes seleccionados por el usuario para guardar libros de trabajo. Se puede abrir con Microsoft Office 2007 y superior.

## Especificaciones del formato de archivo XLSB ##

Las especificaciones de formato de archivo para el formato de archivo XLSB se hicieron públicas en 2008 como versión 1.0. Desde entonces, las especificaciones se han revisado varias veces y la última versión de las especificaciones (v 10.0) se publicó en abril de 2018. Las especificaciones están disponibles públicamente por Microsoft como [[MS-XLSB] - especificaciones de formato de archivo binario de Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) y debe ser consultado por cualquiera para leer o escribir archivos en formato de archivo XLSB.

## Estructura del archivo XLSB ##

Un archivo XLSB es un paquete que consta de una colección de partes. Estas partes contienen información sobre el contenido de un libro de trabajo, incluidos los datos del libro de trabajo y la estructura del paquete. Algunas partes contienen información almacenada mediante registros binarios, algunas como XML, mientras que otras contienen información almacenada como un flujo binario de bytes. Cada registro binario contiene cero o más campos estructurados que contienen los datos del libro.

#### Paquete ####

Un paquete XLSB es un archivo [ZIP](/es/compression/zip/) que debe contener exactamente una parte del libro de trabajo. Esta parte debe ser el destino de una relación en esta parte de relación de paquete. La parte del libro de trabajo es la parte inicial del documento XLSB.

#### Parte ####

Una parte es un flujo de bytes que tiene un tipo de contenido asociado que especifica la naturaleza y el tipo de contenido almacenado en la parte. Algunas partes almacenan información en formato binario, mientras que otras almacenan información como XML. La sección [enumeración de partes](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) del documento de especificaciones enumera las partes válidas, los tipos de contenido y las relaciones requeridas/opcionales entre todas las piezas en un paquete.

#### Relación ####

Un recurso de origen y de destino están conectados por una relación. Una relación puede ser:

**Relación del paquete:** donde el destino es una parte y el origen es el paquete como un todo

**Relación de parte a parte:** donde el objetivo es una parte y el origen es una parte en el paquete

**Relación explícita:** donde se hace referencia a un recurso desde el contenido de una parte de origen al hacer referencia al valor del atributo ID de un elemento de relación

**relación implícita** es una relación que no es explícita

**Relación interna:** donde el objetivo es una parte del paquete

**Relación externa:** donde el destino es un recurso externo que no está en el paquete

#### Registro ####

Un registro es el componente básico que se utiliza para almacenar información sobre las funciones de un libro de trabajo. Cada registro binario es una secuencia de bytes de longitud variable. Un registro binario consta de tres componentes:

* un tipo de registro
* un tamaño récord, y
* los datos de registro que son específicos de ese tipo de registro.

**Tipo de registro:** El tipo de registro muestra el tipo de registro especificado por el registro. También especifica la estructura de los datos de registro específicos de este registro. Los tipos de registros válidos se enumeran en la sección [Enumeración de registros](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) del documento de especificaciones. El tipo de registro debe ser de uno o dos bytes y debe ser mayor o igual a 128 y menor a 16384.

**Tamaño del registro:** El tamaño del registro especifica el conteo de bytes que especifica el tamaño total de los datos del registro. Este valor DEBE ser de uno a cuatro bytes. Este valor DEBE ser un byte si el bit alto en el byte bajo es igual a 0; de lo contrario, este valor DEBE ser mayor que un byte. Si el recuento de bytes es superior a un byte, el bit alto de cada byte sucesivo especifica si se utiliza un byte adicional. Si el bit alto del segundo byte es igual a 1, entonces este valor DEBE usar un tercer byte adicional. Si el bit alto del tercer byte es igual a 1, entonces este valor DEBE usar un cuarto byte adicional. El bit alto del cuarto byte DEBE ignorarse. El valor consta de los siete bits bajos de cada byte combinados. Los bits bajos, menos significativos, están contenidos dentro del primer byte, y cada byte sucesivo contiene bits de mayor orden que el byte anterior.

**Datos de registro:** El componente de datos de registro contiene campos que corresponden a un tipo de registro en particular y comprenden el resto del registro. El orden y la estructura de los campos para un tipo de registro determinado enumerados en Enumeración de registros se especifican en la sección correspondiente para ese tipo de registro en Registros. El tamaño total del componente de datos del registro DEBE ser igual al tamaño del registro. Los campos en el componente de datos de registro pueden contener valores simples, matrices de valores, estructuras de varios campos, matrices de campos y matrices de estructuras.

#### Ejemplo de registro XLSB ####

El siguiente tipo de registro y tamaño de registro especifican un registro **BrtCommentText** con un tamaño de 200 bytes:

11111101 00000100 11001000 00000001 [Campos de registro]

El primer byte es 11111101, especificando un valor bajo de 125 y que el tipo de registro requiere un segundo byte. El segundo byte es 00000100, que especifica un valor alto de 4 * 128, que equivale a 512. El valor del tipo de registro es 125 + 512 o 637, que corresponde a un tipo de registro **BrtCommentText**. El siguiente byte es 11001000, especificando un valor bajo de 72 y que el tamaño del registro requiere un segundo byte. El segundo byte es 00000001, especificando un valor mayor de 1 * 128 y que el tamaño del registro no requiere un byte adicional. El tamaño del registro es 72 + 128, o 200, que especifica el tamaño total, en bytes, del componente de datos del registro. Los campos en el componente de datos de registro se especifican mediante **BrtCommentText**.

## Referencias ##

* [[MS-XLSB] - Formato de archivo binario de Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

