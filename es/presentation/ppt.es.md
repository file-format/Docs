{
  "date" : "2019-12-13",
  "keywords" :[ "archivo ppt", "formato de archivo ppt", "qué es un archivo ppt", "archivo", "ejemplo de ppt", "extensión de archivo ppt","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo PPT y las API que pueden crear y abrir archivos PPT",
  "title" :"PPT - Formato de archivo de PowerPoint",
  "linktitle" : "PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PPT?

Un archivo con extensión PPT representa un archivo de PowerPoint que consta de una colección de diapositivas para mostrar como presentación de diapositivas. Especifica el formato de archivo binario utilizado por Microsoft PowerPoint 97-2003. Un archivo PPT puede contener varios tipos diferentes de información, como texto, viñetas, imágenes, multimedia y otros objetos OLE incrustados. Microsoft presentó un formato de archivo más nuevo para PowerPoint, conocido como [PPTX](/es/presentation/pptx/), a partir de 2007 que se basa en Office OpenXML y es diferente de este formato de archivo binario. Varios otros programas de aplicación como OpenOffice Impress y Apple Keynote también pueden crear archivos PPT.

## Breve historia ##

Microsoft introdujo el formato de archivo PPT con el lanzamiento de PowerPoint en 1987. El formato binario estable se compartió como predeterminado en PowerPoint 97-2003 para Windows. El formato de archivo binario es compatible para leer y escribir en las versiones más recientes de PowerPoint, incluido PowerPoint 2016.

## Especificaciones de formato de archivo ##

Desde su introducción, el formato de archivo PPT ha pasado por varias revisiones para incorporar nuevas características y mejoras. Las especificaciones de la última versión disponible son las de la revisión 6.0 que se publicaron en agosto de 2018, que no deben mezclarse con el número de producto real del formato de archivo PPT, ya que Microsoft ya no proporciona modificaciones para este formato.

### Descripción general del formato de archivo ###

Algunos de los componentes clave de un formato de archivo PPT son los siguientes:

#### Diapositivas ####

Los datos de usuario, como formas, texto, animaciones y medios, se agregan a una presentación dentro de una diapositiva. Una presentación puede contener una o más diapositivas que se muestran como una presentación de diapositivas cuando se ejecuta una presentación. Una presentación contiene diapositivas maestras y diapositivas maestras de título que actúan como plantilla para las propiedades visuales comunes de las diapositivas de presentación. También hay una diapositiva maestra de notas y una diapositiva maestra de documentos que tienen un propósito similar y proporcionan propiedades visuales comunes para todas las diapositivas de notas y todos los documentos impresos.

#### Formas ####

Las formas son objetos que permiten a los usuarios agregar una variedad de contenido a una diapositiva en forma de formas, imágenes y gráficos de marcador de posición. Las formas en una diapositiva maestra definen datos comunes para grupos de formas.

#### Marcadores de posición Formas ####

Estos son marcadores de posición especiales que sirven como contenedores para una variedad de objetos. Se pueden usar diferentes formas de marcador de posición para proporcionar pistas para insertar tipos específicos de formas, como tablas o gráficos. Dentro de una diapositiva, una forma de marcador de posición adopta las propiedades visuales de una diapositiva maestra principal, una diapositiva maestra de título o una diapositiva maestra de notas.

#### Objetos externos ####

Los objetos externos como el audio incrustado y vinculado, el video vinculado, los objetos OLE incrustados y vinculados y los hipervínculos se pueden incrustar en una diapositiva. Estos objetos se pueden usar para activar objetos vinculados para acceder a recursos externos durante una presentación de diapositivas.

### Estructuras de formato de archivo ###

Los formatos de archivos binarios de PowerPoint consisten en los siguientes flujos para representar la estructura y los datos generales del documento.

* Flujo de usuario actual
* Flujo de documentos de PowerPoint
* Corriente de imágenes
* Información resumida e Información resumida del documento (Opcional)

Las especificaciones completas para el formato de archivo DOC se pueden encontrar proporcionadas por [Microsoft] (https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) y deben consultarse en referencia a las secciones mencionadas en los siguientes detalles.

#### Flujo de usuario actual ####

Mantiene un registro del último usuario que abrió el documento y su nombre debe ser "Usuario actual".

#### Flujo de documentos de PowerPoint ####

Mantiene un registro de toda la información sobre una presentación de PowerPoint y explica su diseño y contenido. Es un flujo obligatorio cuyo nombre DEBE ser "Documento de PowerPoint". El contenido de este flujo se especifica mediante una secuencia de registros de nivel superior. Las restricciones de orden parcial en la secuencia de registros se especifican en los registros PersistDirectoryAtom y UserEditAtom.

Como registros contenedores, los registros DocumentContainer, MainMasterContainer (sección 2.5.3), HandoutContainer (sección 2.5.8), SlideContainer (sección 2.5.1) y NotesContainer (sección 2.5.6) son la raíz de un árbol de registros contenedores. y registros atómicos. Dentro de cualquier registro contenedor, pueden existir otros registros que no se enumeran explícitamente como registros secundarios. Los registros desconocidos se identifican cuando el campo recType de la estructura RecordHeader (sección 2.3.1) contiene un valor no especificado por la enumeración RecordType (sección 2.13.24). Estos registros desconocidos, si se encuentran, DEBEN ignorarse y PUEDEN <1> conservarse. Los registros desconocidos se pueden ignorar buscando bytes recLen hacia adelante desde el final de la estructura RecordHeader.

Cada vez que se escribe este flujo, se pueden agregar nuevos registros de nivel superior, una edición del usuario, al flujo existente, o se puede reemplazar todo el contenido del flujo con una secuencia actualizada de registros de nivel superior. Si no se reemplaza todo el flujo, cualquier registro de nivel superior existente anteriormente que comprendiera cualquier edición de usuario anterior puede volverse obsoleto por los registros de nivel superior agregados posteriormente que comprenden la edición de usuario actual.

#### Transmisión de imágenes ####

Este es un flujo opcional que contiene datos sobre las imágenes contenidas en una presentación de PowerPoint. Su nombre DEBE ser "Imágenes". El contenido de este flujo está especificado por el registro OfficeArtBStoreDelay como se especifica en [MS-ODRAW] sección 2.2.21.

#### Flujo de información resumida ####

Mantiene estadísticas sobre el documento siguiendo el estándar de Microsoft Office. El nombre del flujo de información de resumen debe ser "\005SummaryInformation", donde \005 es el carácter con valor 0x0005, no el literal de cadena "\005". Este flujo DEBE omitirse para documentos encriptados. El contenido de este flujo se especifica en la sección 2.3.3.2.1 de [MS-OSHARED].

#### Flujo de información resumida del documento ####

Una secuencia opcional cuyo nombre DEBE ser "\005DocumentSummaryInformation", donde \005 es el carácter con valor 0x0005, no el literal de cadena "\005". Este flujo PUEDE <2> omitirse para documentos cifrados. El contenido de este flujo se especifica en la sección 2.3.3.2.2 de [MS-OSHARED].

#### Flujo de información resumida cifrada ####

Un flujo opcional cuyo nombre DEBE ser "EncryptedSummary". Este flujo solo existe en un documento cifrado. El contenido de este flujo se especifica en la sección 2.3.5.4 de [MS-OFFCRYPTO].

#### Almacenamiento de firmas digitales ####

Un almacenamiento opcional cuyo nombre DEBE ser "_xmlsignatures". PUEDE ser omitido y PUEDE ser ignorado. El contenido de este almacenamiento se especifica en [MS-OFFCRYPTO] sección 2.5.2.

#### Almacenamiento de datos XML personalizados ####

Un almacenamiento opcional cuyo nombre DEBE ser "MsoDataStore". El contenido del almacenamiento se especifica en [MS-OSHARED] sección 2.3.6.

#### Flujo de firmas ####

Un flujo opcional cuyo nombre DEBE ser "_signatures". DEBE ser omitido y PUEDE ser ignorado. El contenido de este flujo se especifica en la sección 2.5.1 de [MS-OFFCRYPTO].

## Referencias ##

* [Especificaciones del formato de archivo PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Estructuras de objetos y tipos de datos comunes de Office](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Estructura de criptografía de documentos de Office](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [Formatos de archivo de PowerPoint] (https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

