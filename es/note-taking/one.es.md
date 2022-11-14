{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"UNO - Formato de archivo de Microsoft OneNote",
  "description":"Obtenga información sobre el formato de archivo ONE y las API que pueden crear y abrir archivos ONE",
  "linktitle" : "ONE",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo .ONE? ##

Los archivos representados por la extensión .ONE son creados por la aplicación Microsoft OneNote. OneNote le permite recopilar información usando la aplicación como si estuviera usando su bloc de notas para tomar notas. Los archivos de OneNote pueden contener diferentes elementos que se pueden colocar en ubicaciones no fijas en las páginas del documento. Estos elementos pueden contener texto, escritura a mano digitalizada y objetos copiados de otras aplicaciones, incluidas imágenes, dibujos y clips multimedia (audio/video). Microsoft ahora ofrece una versión en línea de OneNote como parte de Office365 donde las notas se pueden compartir con otros usuarios de OneNote a través de Internet.

## Especificaciones del formato de archivo .ONE ##

El formato de archivo de OneNote proporciona una forma eficaz de representar notas digitales como conjuntos jerárquicos de secciones y páginas. Cada página contiene contenido definido por el usuario en una estructura específica para su representación mediante el formato de archivo Modelo de objetos de documento (DOM). El modelo de datos de este formato es como se ilustra a continuación.

### Descripción general de la estructura ###

Como se ilustra en el modelo de datos para el formato de archivo de OneNote, un documento de OneNote consta de diferentes elementos.

#### Sección ####

Una sección es el contenedor superior en un archivo de OneNote que además contiene diferentes elementos como:

* Paginas
* Metadatos
* Propiedades

Los metadatos y las propiedades incluyen el nombre de la sección, la identificación de las páginas contenidas en la sección y el orden en que aparecen esas páginas. El término "sección" hace referencia a todas las páginas que se encuentran en una sección y la representación de esos datos en un archivo de almacenamiento de revisión de OneNote®, que tiene una extensión de nombre de archivo .one.

#### Página ####

El contenido definido por el usuario en un documento de OneNote se encuentra dentro de una página. La información de la página incluye texto, listas, tablas, títulos de página, imágenes y etiquetas de notas. Una página consta de objetos de contorno a los que se añaden la mayoría de los objetos contenidos. A cada página se le puede asignar un nombre para una representación significativa y también se pueden agregar objetos directamente a las páginas. Una página puede contener además subpáginas en un sistema jerárquico.

#### Propiedades y conjuntos de propiedades ####

El contenido de OneNote consta de propiedades, conjuntos de propiedades y objetos de datos de archivos. Un conjunto de propiedades es una colección de propiedades que representa algún tipo de contenido. Un objeto de datos de archivo es un bloque de datos binarios que contiene imágenes, archivos incrustados o contenido de audio/video.

#### Bloc de notas de OneNote ####

Un cuaderno es una colección de archivos de sección que se almacenan en el mismo directorio. Se utiliza una colección de propiedades para especificar configuraciones como el orden de las secciones dentro del cuaderno y el color del cuaderno.

### Estructura del archivo ###

Un archivo de almacenamiento de revisión DEBE comenzar con una estructura de **Encabezado**. El resto del archivo se divide en bloques de bytes, donde el tamaño y la estructura de cada bloque se especifican en el campo que hace referencia a él. Se puede acceder a un bloque si se hace referencia a él mediante la estructura **Encabezado**, o si se hace referencia a él mediante un campo en otro bloque accesible. Los datos fuera de la estructura del **Encabezado** y cualquier bloque accesible DEBEN ser ignorados.

Todas las estructuras están alineadas en límites de 1 byte. Todos los números enteros están firmados a menos que se especifique lo contrario. Todos los campos son [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) a menos que se especifique lo contrario.

#### Encabezado ####

El encabezado del archivo .ONE se compone de fragmentos que contienen diferentes ID y campos únicos para la representación de la información del archivo de la siguiente manera:

`guidFileType (16 bytes):` un GUID que especifica el tipo del archivo de almacenamiento de revisiones. DEBE ser uno de los valores de la siguiente tabla.


|Formato de archivo|Valor
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` un GUID que especifica la identidad de este archivo de almacenamiento de revisión. DEBERÍA ser globalmente único.

`guidLegacyFileVersion (16 bytes):` DEBE ser "{00000000-0000-0000-0000-000000000000}" y DEBE ignorarse.

`guidFileFormat (16 bytes):` un GUID que especifica que el archivo es un archivo de almacenamiento de revisiones. DEBE ser "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 bytes):` Un entero sin signo. DEBE ser uno de los valores de la siguiente tabla, según el tipo de archivo.

|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` Un entero sin signo. DEBE ser uno de los valores de la siguiente tabla, según el formato de este archivo.


|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Un entero sin signo. DEBE ser uno de los valores de la siguiente tabla, según el formato de este archivo.

|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un entero sin signo. DEBE ser uno de los valores de la siguiente tabla, según el formato de este archivo.

|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 bytes):` Una estructura **FileChunkReference32** que DEBE tener un valor de "fcrZero".

`fcrLegacyTransactionLog (8 bytes):` Una estructura **FileChunkReference32** que DEBE ser "fcrNil".

`cTransactionsInLog (4 bytes):` Un entero sin signo que especifica el número de transacciones en el registro de transacciones. NO DEBE ser cero.

`cbLegacyExpectedFileLength (4 bytes):` Un entero sin signo que DEBE ser cero y DEBE ignorarse.

`rgbPlaceholder (8 bytes):` Un entero sin signo que DEBE ser cero y DEBE ignorarse.

`fcrLegacyFileNodeListRoot (8 bytes):` Una estructura **FileChunkReference32** que DEBE ser "fcrNil".

`cbLegacyFreeSpaceInFreeChunkList (4 bytes):` Un entero sin signo que DEBE ser cero y DEBE ignorarse.

`fNeedsDefrag (1 byte):` DEBE ignorarse.

`fRepairedFile (1 byte):` DEBE ignorarse.

`fNeedsGarbageCollect (1 byte):` DEBE ignorarse.

`fHasNoEmbeddedFileObjects (1 byte):` Un entero sin signo que DEBE ser cero y DEBE ignorarse.

`guidAncestor (16 bytes):` un GUID que especifica el campo **Header.guidFile** del archivo de la tabla de contenido, dado por la siguiente tabla:


|Formato de archivo de tabla de contenido|Ubicación del archivo de tabla de contenido
--- | --- |
|Archivo de sección: .One|El archivo de tabla de contenido se encuentra en el mismo directorio que este archivo.
|Archivo de tabla de contenido: .onetoc2|El archivo de tabla de contenido se encuentra en el directorio principal de este archivo.

Si el GUID es {00000000-0000-0000-0000-000000000000}, este campo no hace referencia a un archivo de tabla de contenido.

`crcName (4 bytes):` Un entero sin signo que especifica el valor CRC del nombre de este archivo de almacenamiento de revisiones. El nombre es la representación Unicode del nombre del archivo con su extensión y un carácter nulo adicional al final. Este CRC siempre se calcula utilizando el algoritmo CRC para el archivo .one, independientemente de este formato de archivo de almacenamiento de revisión.

`fcrHashedChunkList (12 bytes):` Una estructura **FileChunkReference64x32** que especifica una referencia al primer **FileNodeListFragment** en una lista de fragmentos con hash. Si el valor de la estructura **FileChunkReference64x32** es "fcrZero" o "fcrNil", la lista de fragmentos con hash no existe.

`fcrTransactionLog (12 bytes):` Una estructura **FileChunkReference64x32** que especifica una referencia a la primera estructura **TransactionLogFragment** en un registro de transacciones. El valor del campo **fcrTransactionLog** NO DEBE ser "fcrZero" y NO DEBE ser "fcrNil".

`fcrFileNodeListRoot (12 bytes):` Una estructura **FileChunkReference64x32** que especifica una referencia a una lista de nodos de archivo raíz. El valor del campo **fcrFileNodeListRoot** NO DEBE ser "fcrZero" y NO DEBE ser "fcrNil".

`fcrFreeChunkList (12 bytes):` Una estructura **FileChunkReference64x32** que especifica una referencia a la primera estructura **FreeChunkListFragment**. Si el valor de la estructura **FileChunkReference64x32** es "fcrZero" o "fcrNil", la lista de fragmentos libres no existe.

`cbExpectedFileLength (8 bytes):` Un entero sin signo que especifica el tamaño, en bytes, de este archivo de almacenamiento de revisiones.

`cbFreeSpaceInFreeChunkList (8 bytes):` Un entero sin signo que DEBERÍA especificar el tamaño, en bytes, del espacio libre especificado por la lista de fragmentos libres.

`guidFileVersion (16 bytes):` UN GUID. Cuando se cambia el valor del campo **cTransactionsInLog** o el campo **guidDenyReadFileVersion**, **guidFileVersion** DEBE cambiarse a un nuevo GUID.

`nFileVersionGeneration (8 bytes):` Un entero sin signo que especifica el número de veces que ha cambiado el archivo. DEBE incrementarse cuando cambia el campo **guidFileVersion**.

`guidDenyReadFileVersion (16 bytes):` un GUID. Cuando se cambia el contenido existente del archivo, excluyendo la estructura **Encabezado** del archivo y los bloques de almacenamiento no utilizados, **guidDenyReadFileVersion** DEBE cambiarse a un nuevo GUID.

`grfDebugLogFlags (4 bytes):` DEBE ser cero. DEBE ser ignorado.

`fcrDebugLog (12 bytes):` Una estructura **FileChunkReference64x32** que DEBE tener un valor "fcrZero". DEBE ser ignorado.

`fcrAllocVerificationFreeChunkList (12 bytes):` Una estructura **FileChunkReference64x32** que DEBE ser "fcrZero". DEBE ser ignorado.

`bnCreated (4 bytes):` Un entero sin signo que especifica el número de compilación de la aplicación que creó este archivo de almacenamiento de revisiones. DEBE ser ignorado.

`bnLastWroteToThisFile (4 bytes):` Un entero sin signo que especifica el número de compilación de la aplicación que escribió por última vez en este archivo de almacenamiento de revisiones. DEBE ser ignorado.

`bnOldestWritten (4 bytes):` Un entero sin signo que especifica el número de compilación de la aplicación más antigua que escribió en este archivo de almacenamiento de revisiones. DEBE ser ignorado.

`bnNewestWritten (4 bytes):` Un entero sin signo que especifica el número de compilación de la aplicación más reciente que escribió en este archivo de almacenamiento de revisiones. DEBE ser ignorado.

`rgbReserved (728 bytes):` DEBE ser cero. DEBE ser ignorado.

## Referencias ##

* [[MS-ONESTORE] - Formato de archivo de OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

