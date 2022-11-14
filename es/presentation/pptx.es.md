{
  "date" : "2019-12-13",
  "keywords" :[ "archivo pptx", "formato de archivo pptx", "qué es un archivo pptx", "archivo", "ejemplo de pptx", "extensión de archivo pptx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo PPTX y las API que pueden crear y abrir archivos PPTX",
  "title" :"PPTX - Formato de archivo de presentación de PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PPTX?

Los archivos con la extensión PPTX son archivos de presentación creados con la popular aplicación Microsoft PowerPoint. A diferencia de la versión anterior del formato de archivo de presentación PPT, que era binario, el formato PPTX se basa en el formato de archivo de presentación XML abierto de Microsoft PowerPoint. Un archivo de presentación es una colección de diapositivas donde cada diapositiva puede incluir texto, imágenes, formato, animaciones y otros medios. Estas diapositivas se presentan a la audiencia en forma de presentaciones de diapositivas con configuraciones de presentación personalizadas.

## Breve historia

El formato de archivo PPTX se introdujo en 2007 y utiliza el estándar Open XML adaptado por Microsoft en 2000. Antes de PPTX, el formato de archivo común utilizado era PPT, que era un formato de archivo binario puro. El nuevo tipo de archivo ha agregado ventajas de tamaño de archivo pequeño, menos cambios de corrupción y representación de imágenes bien formateadas. Fue a principios de 2000 cuando Microsoft decidió apostar por el cambio para adaptarse al estándar de **Office Open XML**. En 2007, este nuevo formato de archivo pasó a formar parte de Office 2007 y también se mantiene en las nuevas versiones de Microsoft Office.

## Especificaciones del formato de archivo PPTX

Los archivos generados con el formato de archivo Office Open XML son una colección de archivos XML junto con otros archivos que proporcionan vínculos entre todos los archivos constituyentes. Esta colección es en realidad un archivo comprimido que se puede extraer para ver su contenido. Para hacerlo, simplemente cambie el nombre de la extensión de archivo PPTX con zip y extráigalo para observar su contenido (consulte [Especificaciones de formato de archivo PPTX] (https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) de Microsoft).

Las siguientes secciones arrojan algo de luz sobre cada uno de estos.

### [Tipos_de_contenido].xml

Este es el único archivo que se encuentra en el nivel base cuando se extrae el zip. Enumera los tipos de contenido de las partes dentro del paquete. Todas las referencias a los archivos XML incluidos en el paquete se mencionan en este archivo XML. El siguiente es un tipo de contenido para una parte de diapositiva:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Si es necesario agregar piezas nuevas al paquete, puede hacerlo agregando la pieza nueva y actualizando cualquier relación dentro de los archivos .rels. Hay que tener en cuenta que para tal cambio, también se debe actualizar el Content_Types.xml.

### \_rels (Carpeta) ###

Las relaciones entre las otras partes y recursos fuera del paquete son mantenidas por la parte de relaciones. La carpeta Relaciones contiene un único archivo XML que almacena las relaciones a nivel de paquete. Los enlaces a las partes clave de los archivos PPTX se encuentran en este archivo como URI. Estos URI identifican el tipo de relación de cada parte clave con el paquete. Esto incluye la relación con el documento de oficina principal ubicado como ppt/presentation.xml y otras partes dentro de docProps como propiedades principales y extendidas.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Cada parte del documento que es el origen de una o más relaciones tendrá su propia parte de relaciones donde cada parte de relación se encuentra dentro de una subcarpeta \_rels de la parte y se nombra agregando '.rels' al nombre de la parte. parte. La parte de contenido principal (presentation.xml) tiene su propia parte de relaciones (presentation.xml.rels). Contiene relaciones con otras partes del contenido, como slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, así como los URI para enlaces externos.

#### Relación explícita ####

Para una relación explícita, se hace referencia a un recurso utilizando el atributo Id de un<Relationship> elemento. Es decir, el Id en el origen se asigna directamente a un Id de un elemento de relación, con una referencia explícita al destino.

Por ejemplo, una diapositiva puede contener un hipervínculo como este:

```
<a:hlinkClick r:id#"rId2">
```

El r:id#"rId2" hace referencia a la siguiente relación dentro de la parte de relaciones de la diapositiva (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Relación implícita ####

Para una relación implícita, no existe tal referencia directa a un `<Relationship> Identificación`. En cambio, la referencia se entiende.

### Carpeta ppt ###

Esta es la carpeta principal que contiene todos los detalles sobre el contenido de la Presentación. Por defecto, tiene las siguientes carpetas:

* \_rels
* tema
* diapositivas
* diseños de diapositivas
* maestros de diapositivas

y siguientes archivos xml:

* presentación.xml
* presProps.xml
* TableStyles.xml
* viewProps.xml

## Referencias ##

* [[MS-PPTX] - Formato de archivo PPTX](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

