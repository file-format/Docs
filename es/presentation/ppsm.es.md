{
  "date" : "2019-10-11",
  "keywords" :[ "archivo ppsm", "formato de archivo ppsm", "qué es un archivo ppsm", "archivo", "ejemplo de ppsm", "extensión de archivo ppsm","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - Archivo de presentación de PowerPoint habilitado para macros",
  "description":"Obtenga más información sobre el formato de archivo PPSM y las API que pueden crear y abrir archivos PPSM",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo PPSM?

Los archivos con la extensión PPSM representan un formato de archivo de presentación de diapositivas habilitado para macros creado con Microsoft PowerPoint 2007 o superior. Otro formato de archivo similar es [PPTM](/es/presentation/pptm/), que difiere en abrirse con Microsoft PowerPoint en formato editable en lugar de ejecutarse como presentación de diapositivas. Cuando se ejecuta como presentación de diapositivas, el archivo PPSM muestra las diapositivas de la presentación con el contenido intacto en la presentación de diapositivas y está en modo de solo lectura de forma predeterminada. Los archivos PPSM aún se pueden editar en Microsoft PowerPoint abriéndolos en PowerPoint.

## Formato de archivo ##

El formato de archivo PPSM se introdujo con PowerPoint 2007 y se basa en el formato de archivo OpenXML que utiliza una combinación de XML y [ZIP](/es/compression/zip/) para almacenar su contenido. Los archivos generados con el formato de archivo Office Open XML son una colección de archivos XML junto con otros archivos que proporcionan vínculos entre todos los archivos constituyentes. Esta colección es en realidad un archivo comprimido que se puede extraer para ver su contenido. Para hacerlo, simplemente cambie el nombre de la extensión del archivo PPSM con zip y extráigalo para observar su contenido.

Las siguientes secciones arrojan algo de luz sobre cada uno de estos.

### [Tipos_de_contenido].xml ###

Este es el único archivo que se encuentra en el nivel base cuando se extrae el zip. Enumera los tipos de contenido de las partes dentro del paquete. Todas las referencias a los archivos XML incluidos en el paquete se mencionan en este archivo XML. El siguiente es un tipo de contenido para una parte de diapositiva:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Si es necesario agregar piezas nuevas al paquete, puede hacerlo agregando la pieza nueva y actualizando cualquier relación dentro de los archivos .rels. Hay que tener en cuenta que para tal cambio, también se debe actualizar el Content_Types.xml.

### \_rels (Carpeta) ###

Las relaciones entre las otras partes y recursos fuera del paquete son mantenidas por la parte de relaciones. La carpeta Relaciones contiene un único archivo XML que almacena las relaciones a nivel de paquete. Los enlaces a las partes clave de los archivos de presentación se encuentran en este archivo como URI. Estos URI identifican el tipo de relación de cada parte clave con el paquete. Esto incluye la relación con el documento de oficina principal ubicado como ppt/presentation.xml y otras partes dentro de docProps como propiedades principales y extendidas.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
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
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
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

* [Formato de archivo de presentación OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

