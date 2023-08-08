{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "archivo", "extensión", "formato de archivo", "Word", "Documento" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Archivo de documento de Microsoft Word",
  "description":"Obtenga información sobre el formato de archivo DOC y las API que pueden crear y abrir archivos DOC",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## ¿Qué es un archivo DOC?

Los archivos con extensión .doc representan documentos generados por Microsoft Word u otros documentos de procesamiento de texto en formato de archivo binario. La extensión se usó inicialmente para la documentación de texto sin formato en varios sistemas operativos diferentes. Puede contener varios tipos diferentes de datos, como imágenes, texto formateado y sin formato, gráficos, tablas, objetos incrustados, enlaces, páginas, formato de página, configuraciones de impresión y muchos otros. El formato fue popular para todo tipo de documentación debido a la variedad de opciones que ofrece a los usuarios para escribir manuales, propuestas, especificaciones, currículos, artículos o cualquier documento similar. La versión actualizada de DOC es [DOCX](/es/word-processing/docx/) que se basa en Office OpenXML cuyas especificaciones están disponibles abiertamente.

## Breve historia ##

WordPerfect, un producto de [Corel](https://www.corel.com/en/), usó DOC como la extensión de su formato patentado. En la década de 1980, WordPerfect siguió siendo la opción de uso en la mayoría de las computadoras debido a su fácil disponibilidad, conformidad con la mayoría de las computadoras y sistemas operativos. Sin embargo, WordPerfect vio su caída en el sistema operativo Windows cuando Microsoft presentó Microsoft Word como su producto para el formato de archivo de documentos y eligió la extensión DOC para su formato patentado. A medida que Microsoft Word se hizo cada vez más popular, el formato de archivo DOC experimentó varias revisiones desde Microsoft Word 97 - 2003. Fue en 2007 cuando el formato de archivo DOC predeterminado fue reemplazado por el formato Office Open XML (conocido como DOCX) y las nuevas versiones de Microsoft Word ahora usa esta nueva extensión como formato de archivo predeterminado.

## Especificaciones del formato de archivo DOC - Más información

Microsoft no publicó las especificaciones de formato de archivo DOC durante mucho tiempo hasta 2008. En febrero de 2008, se publicaron las especificaciones de formato para el formato de archivo .doc bajo la Promesa de especificación abierta de Microsoft. Aunque la especificación no describe todas las funciones utilizadas por el formato DOC, brinda amplia información sobre los conocimientos necesarios para trabajar con este formato de archivo. Aún así, se requiere ingeniería inversa para hacer uso de la información disponible. Las especificaciones se han actualizado varias veces y la última [revisión](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) es 8.0, que se actualizó en agosto de 2018 .

### Algunos conceptos fundamentales ###

Antes de entrar en detalles sobre las especificaciones de formato de archivo para DOC, es necesario comprender algunos conceptos fundamentales para poder trabajar con este formato de archivo.

**Base de información de archivo (Fib):** La estructura Fib contiene información sobre el documento y especifica los punteros de archivo a varias partes que componen el documento.
El Fib es una estructura de longitud variable. Con la excepción de la parte base que tiene un tamaño fijo, cada sección va precedida de un campo de recuento que especifica el tamaño de la siguiente sección.

**Posición del carácter:** CP o Posición del carácter representa un número entero de 32 bits sin signo que sirve como índice basado en cero de un carácter en el texto del documento. La ubicación y el tamaño de cada carácter en el archivo no se pueden recuperar directamente y deben calcularse utilizando un algoritmo preespecificado. Los personajes incluyen:

* Texto del documento
* Anclajes de objetos como notas al pie o cuadros de texto
* Caracteres de control como marcas de párrafo y marcas de celda de tabla

**PLC:** La estructura del PLC es una matriz de CP seguida de una matriz de elementos de datos. Los elementos de datos para cualquier PLC deben tener el mismo tamaño de cero o más bytes, por lo que el número de CP debe ser uno más que el número de elementos de datos. Las estructuras de PLC son de diferentes tipos, donde cada tipo especifica si se permiten CP duplicados para ese tipo o no. Una estructura de PLC consta de:

* **aCP (longitud variable):** Una matriz de elementos CP. Cada tipo de estructura **PLC** especifica el significado de los elementos CP y el rango permitido.
* **aData (longitud variable):** Cada tipo de estructura de **PLC** especifica la estructura y el significado de los elementos de datos, cualquier restricción sobre la cantidad de elementos de datos y cualquier restricción sobre los datos contenidos en ellos. También especifica la relación entre los elementos de datos y los CP correspondientes.

**Selección válida:** Las construcciones del archivo .DOC se describen principalmente mediante una variedad de CP. Hay una serie de [reglas](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) especificadas por Microsoft que deben seguirse en tal caso.

**STTB:** El STTB es una tabla de cadenas que se compone de un encabezado seguido de una matriz de elementos. El valor **cData** especifica el número de elementos que están contenidos en la matriz.

**Almacenamiento de propiedades:** Un archivo de Word puede tener diferentes elementos, como texto, párrafos, tablas, imágenes y secciones, donde cada uno puede tener sus propias propiedades. Las propiedades de estos se almacenan en el archivo de Word como diferencias con respecto a las predeterminadas. Tales diferencias son especificadas por PRl que consiste en un Modificador de Propiedad Única (Sprm) y su operando. Una aplicación puede determinar el conjunto final de propiedades mediante la aplicación de listas de **Prl**s.

**Protección con contraseña:** Los archivos de Word también se pueden proteger con contraseña, para lo cual se puede utilizar uno de los siguientes mecanismos.

* Ofuscación XOR
* Cifrado RC4 de documentos binarios de Office
* Documento binario de Office Cifrado RC4 CryptoAPI

Si FibBase.fEncrypted y FibBase.fObfuscation son ambos 1, el archivo se ofusca mediante la ofuscación XOR.

Si FibBase.fEncrypted es 1 y FibBase.fObfuscation es 0, el archivo se cifra mediante el uso de Office Binary Document RC4 Encryption o Office Binary Document RC4 CryptoAPI Encryption, con EncryptionHeader almacenado en los primeros bytes de FibBase.lKey del flujo de tabla. EncryptionHeader.EncryptionVersionInfo especifica qué mecanismo de cifrado se usó para cifrar el archivo.

### Estructura del archivo ###

Un archivo de Word binario en su originalidad es un archivo compuesto OLE que se compone de varios almacenamientos y flujos. Estos almacenamientos y flujos tienen su propia estructura y tamaño, que especifican los parámetros de escritura y lectura. Estos son:

#### Flujo de documento de Word ####

Esta secuencia contiene el texto del documento y otra información a la que se hace referencia en otras partes del archivo. La transmisión no tiene una estructura predefinida que no sea la FIB al principio, que es obligatoria y debe estar en el desplazamiento 0. Esta transmisión no debe tener más de 2147 MB.

#### 1TableStream o 0TableStream ####

Un archivo binario de Word puede contener Table Streams conocidos como 1Table stream o 0Table stream. Al menos uno de estos debe estar presente en el documento. Sin embargo, si un documento contiene secuencias 1Table y 0Table, solo se utiliza la secuencia referenciada por base.fWhichTblStm. El flujo sin referencia DEBE ser ignorado.
El Table Stream NO DEBE tener más de 2147 MB.

#### Flujo de datos ####

El flujo de datos no tiene una estructura predefinida. Contiene datos a los que se hace referencia desde la FIB o desde otras partes del archivo. Esta secuencia no necesita estar presente si no hay referencias a ella. El flujo de datos NO DEBE tener más de 2147 MB.

#### Almacenamiento de grupos de objetos ####

El almacenamiento de Object Pool contiene almacenamientos para objetos OLE incrustados. Este almacenamiento no necesita estar presente si no hay objetos OLE incrustados en el documento.

#### Almacenamiento de datos XML personalizados ####

El almacenamiento de datos XML personalizados es un almacenamiento opcional cuyo nombre DEBE ser "MsoDataStore".

#### Flujo de información resumida ####

El flujo de información resumida es un flujo opcional cuyo nombre DEBE ser "\005SummaryInformation", donde \005 es el carácter con valor 0x0005, y no el literal de cadena "\005".

#### Flujo de información resumida del documento ####

El flujo de información de resumen del documento es un flujo opcional cuyo nombre DEBE ser "\005DocumentSummaryInformation", donde \005 es el carácter con valor 0x0005, no el literal de cadena "\005".

#### Flujo de cifrado ####

El flujo de cifrado es un flujo opcional cuyo nombre DEBE ser "cifrado". Esta transmisión NO DEBE estar presente a menos que se cumplan las dos condiciones siguientes:

* El documento está cifrado con Office Binary Document RC4 CryptoAPI Encryption.
* El valor de fDocProps se establece en EncryptionHeader.Flags.

#### Almacenamiento de macros ####

El almacenamiento de macros es un almacenamiento opcional que contiene las macros del archivo. Si está presente, DEBE ser un almacenamiento raíz del proyecto.

#### Almacenamiento de firmas XML ####

El almacenamiento de firmas XML es un almacenamiento opcional cuyo nombre DEBE ser "_xmlsignatures".

#### Flujo de firmas ####

El flujo de firmas es un flujo opcional cuyo nombre DEBE ser "_signatures". Esta secuencia contiene firmas digitales.

#### Gestión de derechos de información Almacenamiento de espacio de datos ####

El almacenamiento del espacio de datos de Information Rights Management es un almacenamiento opcional cuyo nombre DEBE ser "\006DataSpaces", donde \006 es el carácter con el valor 0x0006, y no el literal de cadena "\006". Si este almacenamiento está presente, el flujo de contenido protegido también DEBE estar presente.
Si este almacenamiento está presente, todos los flujos y almacenamientos especificados que no sean este almacenamiento y el Flujo de contenido protegido DEBERÍAN leerse del Flujo de contenido protegido como se especifica en [MS-OFFCRYPTO] y si alguno de esos flujos y almacenamientos existen fuera del Contenido protegido Stream, DEBEN ser ignorados.

#### Flujo de contenido protegido ####

El flujo de contenido protegido es un flujo opcional cuyo nombre DEBE ser "\009DRMContent", donde \009 es el carácter con valor 0x0009 y no el literal de cadena "\009".
Si este flujo está presente, el almacenamiento del espacio de datos de gestión de derechos de información también DEBE estar presente.

## Referencias ##

* [Especificaciones de formación de archivos MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Informática Doc](https://en.wikipedia.org/wiki/Doc_(computing))

