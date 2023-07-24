{
  "date" : "2019-10-11",
  "keywords" :[ "archivo dcm", "formato de archivo dcm", "qué es un archivo dcm", "archivo", "ejemplo de dcm", "extensión de archivo dcm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo DCM - Archivo de información médica digital",
  "description":"Obtenga más información sobre el formato de archivo DCM y las API que pueden crear y abrir archivos DCM",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## ¿Qué es un archivo DCM?

Los archivos con extensión .dcm representan imágenes digitales que almacenan información médica de pacientes, como resonancias magnéticas, tomografías computarizadas e imágenes de ultrasonido. Los archivos DCM usan el formato de archivo de imagen [DICOM](/es/image/dicom) (Imágenes digitales y comunicaciones en medicina) y pueden incluir información del paciente como referencia. Fue desarrollado por la [Asociación Nacional de Fabricantes Eléctricos](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) y estaba destinado a estandarizar el formato de archivo de imágenes para la distribución y visualización de imágenes médicas.

## Formato de archivo DCM

Los archivos DCM almacenan información en formato de imagen DICOM. Estos archivos almacenan el conjunto de datos, que es información del mundo real, que representa una instancia de SOP relacionada con un DICOM IOD. La metainformación del archivo DICOM se almacena en el archivo seguido del flujo de bytes del conjunto de datos real.

### Metainformación del archivo DICOM ##

Cada archivo DICOM incluye un encabezado de información de identificación para el conjunto de datos encapsulados que consta de:
* Un preámbulo de archivo de 128 bytes
* Prefijo DICOM de 4 bytes
* Metaelementos de archivo

Este encabezado es imprescindible para todos los archivos DICOM.

### Elementos meta del archivo ###
|Nombre de atributo|Etiqueta|Tipo| Descripción del atributo
---|---|---|---|
|Preámbulo del archivo|Sin campos de etiqueta o longitud|1|Un campo fijo de 128 bytes disponible para el perfil de aplicación o el uso especificado por la implementación. Si no lo utiliza un perfil de aplicación o una implementación específica, todos los bytes se establecerán en 00H. Los lectores o actualizadores de conjuntos de archivos no se basarán en el contenido de este preámbulo para determinar si este archivo es o no un archivo DICOM.
|Prefijo DICOM|Sin campos de etiqueta o longitud|1|Cuatro bytes que contienen la cadena de caracteres "DICM". Este prefijo está diseñado para reconocer si este archivo es o no un archivo DICOM.
|Longitud del grupo de metainformación del archivo|(0002,0000)|1|Número de bytes que siguen a este metaelemento del archivo (final del campo Valor) hasta el último metaelemento del archivo del grupo 2, inclusive.
|Versión de metainformación de archivo|(0002,0001)|1|Este es un campo de dos bytes donde cada bit identifica una versión de este encabezado de metainformación de archivo. En la versión 1, el valor del primer byte es 00H y el valor del segundo byte es 01H. Las implementaciones que leen archivos con metainformación donde este atributo tiene el bit 0 (lsb) del segundo byte establecido en 1 pueden interpretar la metainformación del archivo como se especifica en este versión de PS3.10. Todos los demás bits no se verificarán.
|UID de clase de SOP de almacenamiento de medios|(0002,0002)|1|Identifica de forma exclusiva la clase de SOP asociada con el conjunto de datos. Los UID de clase SOP permitidos para el almacenamiento de medios se especifican en PS3.4 - Perfiles de aplicación de almacenamiento de medios.
|UID de instancia de SOP de almacenamiento de medios|(0002,0003)|1|Identifica de forma exclusiva la instancia de SOP asociada con el conjunto de datos colocado en el archivo y siguiendo la metainformación del archivo.
|UID de sintaxis de transferencia|(0002,0010)|1|Identifica de forma exclusiva la sintaxis de transferencia utilizada para codificar el siguiente conjunto de datos. Esta sintaxis de transferencia no se aplica a la metainformación del archivo.
|UID de clase de implementación|(0002,0012)|1|Identifica de forma exclusiva la implementación que escribió este archivo y su contenido. Proporciona una identificación inequívoca del tipo de implementación que escribió por última vez el archivo en caso de problemas de intercambio.
|Nombre de versión de implementación|(0002,0013)|3|Identifica una versión para un UID de clase de implementación (0002,0012) usando hasta 16 caracteres del repertorio.
|Título de entidad de aplicación de origen|(0002,0016)|3|El título de entidad de aplicación DICOM (AE) del AE que escribió el contenido de este archivo (o lo actualizó por última vez). Si se utiliza, permite rastrear la fuente de errores en caso de problemas de intercambio de medios.
|UID del creador de información privada|(0002,0100)|3|El UID del creador de la información privada (0002,0102).
|Información privada|(0002,0102)|1C|Contiene información privada colocada en la metainformación del archivo. El creador se identificará en (0002,0100). Obligatorio si el UID del creador de información privada (0002,0100) está presente.

### Encapsulación de conjuntos de datos ###

Un archivo DICOM contiene un solo conjunto de datos que representa una sola instancia de SOP relacionada con una sola clase de SOP. El UID de sintaxis de transferencia de la metainformación del archivo DICOM definirá la sintaxis de transferencia utilizada para codificar el conjunto de datos.

### Compatibilidad con información de gestión de archivos ###

La capa de formato de medios proporciona la siguiente información de administración de archivos si es necesario para un perfil de aplicación DICOM determinado.

* Identificación del propietario del contenido del archivo

* Estadísticas de acceso a archivos (por ejemplo, fecha y hora de creación)

* Control de acceso a archivos de aplicaciones

* Control de acceso a medios físicos (p. ej., protección contra escritura)

## Referencias ##
* [Estándar DICOM](https://www.dicomstandard.org/current/)
* [Formato de archivo DICOM](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

