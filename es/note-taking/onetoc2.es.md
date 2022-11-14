{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Formato de archivo de Microsoft OneNote",
  "description":"Obtenga información sobre el formato de archivo ONETOC2 y las API que pueden crear y abrir archivos ONETOC2",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es ONETOC2? ##

Aquellos que han trabajado con la aplicación [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-take-app) pueden haber notado la presencia de archivos .onetoc2 en la carpeta del cuaderno. Microsoft OneNote crea un archivo binario .onetoc2 como tabla de contenido para mantener un índice sobre el orden de las diferentes secciones para tomar notas en un cuaderno. Un cuaderno es una colección de archivos de sección que se almacenan en el mismo directorio. El archivo .onetoc2 usa una colección de propiedades para especificar configuraciones como el orden de las secciones dentro del cuaderno y el color del cuaderno.

Cuando crea un bloc de notas en OneNote 2016, se guarda automáticamente en el nuevo formato de archivo 2010-2016. Necesitará este formato si desea que todas las características de OneNote 2016, como ecuaciones matemáticas y notas vinculadas, funcionen correctamente.

## Formato de archivo ONETOC2 ##

El formato de archivo .onetoc2 se representa como formato de archivo de almacenamiento de revisión de OneNote y es una colección de estructuras que especifican un almacenamiento de revisión organizado en espacios de objetos con referencias cruzadas, que contienen objetos con conjuntos de propiedades y contienen un registro de transacciones para garantizar la integridad del archivo en entornos asincrónicos. escribe Las especificaciones completas para el formato de archivo .onetoc2 están disponibles [en línea] (https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) y se pueden consultar para el desarrollo de aplicaciones .

### Estructura del archivo ###

Un archivo de almacenamiento de revisión DEBE comenzar con una estructura de **Encabezado**. El resto del archivo se divide en bloques de bytes, donde el tamaño y la estructura de cada bloque se especifican en el campo que hace referencia a él. Se puede acceder a un bloque si se hace referencia a él mediante la estructura **Encabezado**, o si se hace referencia a él mediante un campo en otro bloque accesible. Los datos fuera de la estructura del **Encabezado** y cualquier bloque accesible DEBEN ser ignorados.

Todas las estructuras están alineadas en límites de 1 byte. Todos los números enteros están firmados a menos que se especifique lo contrario. Todos los campos son [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) a menos que se especifique lo contrario.

#### Encabezado ####

El encabezado del archivo .ONE se compone de fragmentos que contienen diferentes ID y campos únicos para la representación de la información del archivo de la siguiente manera:

`guidFileType (16 bytes):` un GUID que especifica el tipo del archivo de almacenamiento de revisión. DEBE ser uno de los valores de la siguiente tabla.

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
:


|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Un entero sin signo. DEBE ser uno de los valores de la siguiente tabla, según el formato de este archivo.


|Formato de archivo|Valor
--- | --- |
|.uno|0x0000002A
|.onetoc2|0x0000001B

## Referencias ##

* [[MS-ONESTORE] - Formato de archivo de OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

