{
  "date" : "2019-12-09",
  "keywords" :[ "archivo 3mf", "formato de archivo 3mf", "qué es un archivo 3mf", "archivo", "ejemplo 3mf", "extensión de archivo 3mf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Obtenga más información sobre el formato de archivo 3MF y las API que pueden abrir y crear archivos 3MF",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## ¿Qué es un archivo 3MF?

3MF, formato de fabricación 3D, es utilizado por aplicaciones para representar modelos de objetos 3D en una variedad de otras aplicaciones, plataformas, servicios e impresoras. Fue creado para evitar las limitaciones y problemas de otros formatos de archivo 3D, como [STL](/es/cad/stl/), para trabajar con las últimas versiones de impresoras 3D. 3MF es un formato de archivo relativamente nuevo que ha sido desarrollado y publicado por el consorcio 3MF. Es lo suficientemente rico como para describir completamente un modelo, conservando la información interna, el color y otras características que lo hacen extensible para admitir nuevas innovaciones en la impresión 3D. El formato es extensible, capaz de ser ampliamente adoptado y libre de problemas que acosan a otros formatos de archivo ampliamente utilizados.

## Breve historia del formato de archivo 3MF

Las limitaciones existentes en los formatos de archivos descriptivos de modelos disponibles, como STL y otros, llevan a las marcas líderes a unirse y formular un formato de archivo más extensible para la impresión 3D. Una consideración importante fue cómo las aplicaciones deberían pasar los datos del modelo a las impresoras 3D. El consorcio 3MF, por lo tanto, nació para respaldar un nuevo formato de archivo 3D llamado 3MF con el objetivo de hacerlo lo suficientemente extensible para satisfacer las necesidades de la impresión 3D. Varias empresas formaron parte de este consorcio, incluidas Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP y otras. Microsoft donó su trabajo en curso de formato de archivo 3D como punto de partida para el desarrollo colaborativo de la especificación del Consorcio 3MF.

## Formato de archivo 3MF - Más información

3MF es un formato de datos basado en XML (XML comprimido legible por humanos) que incluye definiciones de datos relacionados con la fabricación en 3D, incluida la extensibilidad de terceros para datos personalizados. El formato de archivo 3MF se diseñó teniendo en cuenta las limitaciones y los problemas que enfrentan otros formatos de archivo 3D. Esto condujo a la formulación del formato de archivo 3MF que es:

* **Completo:** Contiene toda la información necesaria sobre modelos, materiales y propiedades en un solo archivo
* **Legible por humanos:** Uso de estructuras comunes como OPC, [ZIP](/es/compression/zip/) y XML para facilitar el desarrollo
* **Simple:** Una especificación breve y clara que facilita el desarrollo y agiliza la validación
* **Extensible:** aprovechar los espacios de nombres XML permite extensiones públicas y privadas manteniendo la compatibilidad
* **Sin ambigüedades:** El lenguaje claro y las pruebas de conformidad garantizan que un archivo sea siempre coherente de lo digital a lo físico
* **Gratis:** El acceso y la implementación de la especificación 3MF están y estarán siempre libres de regalías, patentes y licencias.

Las especificaciones para el formato de archivo 3MF están alojadas en [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) para acceso público y actualizaciones continuas. La versión publicada actual es 1.2.3 que describe el conjunto de convenciones para el uso de XML y otras tecnologías ampliamente disponibles para describir el contenido y la apariencia de uno o más modelos 3D. Los desarrolladores que deseen crear sistemas para procesar formatos de archivo 3MF pueden consultar estas especificaciones con fines de implementación.

## Especificaciones del formato de archivo 3MF

El formato de archivo 3MF utiliza las especificaciones de Open Packaging en forma de archivo ZIP para su modelo físico. Incluye un conjunto bien definido de partes y relaciones que cumplen un propósito particular en el documento. Esto también hace que el formato siga la característica del paquete, incluidas las firmas digitales y las miniaturas.

### El documento 3MF: una descripción general

Un documento 3MF típico tiene el siguiente aspecto:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

La carga útil incluye el conjunto completo de piezas necesarias para procesar la pieza del modelo 3D. Todo el contenido que se utilizará para fabricar un objeto descrito en la carga útil 3D DEBE estar contenido en el Documento 3MF. La descripción de cada parte del documento junto con su estado como requerido u opcional se encuentra en la siguiente tabla.


|**Nombre**|**Descripción**|**Origen de la relación**|**Obligatorio/Opcional**
--- | --- | --- | ---
|Modelo 3D|Contiene la descripción de uno o más objetos 3D para la fabricación.|Paquete|REQUERIDO
|Propiedades principales|La parte OPC que contiene varias propiedades del documento.|Paquete|OPCIONAL
|Origen de la firma digital|La parte OPC que es la raíz de las firmas digitales en el paquete.|Paquete|OPCIONAL
|Firma digital|Partes OPC que contienen cada una una firma digital.|Origen de la firma digital|OPCIONAL
|Certificado de firma digital|Piezas OPC que contienen un certificado de firma digital.|Firma digital|OPCIONAL
|PrintTicket|Proporciona la configuración que se utilizará al generar los objetos 3D en la pieza del modelo 3D.|Modelo 3D|OPCIONAL
|Miniatura|Contiene una pequeña imagen JPEG o PNG que representa los objetos 3D en el paquete o el paquete como un todo.|Paquete|OPCIONAL
|Textura 3D|Contiene una textura utilizada para aplicar color a un objeto 3D en la parte Modelo 3D (disponible para extensiones)|Modelo 3D|OPCIONAL
|Piezas personalizadas|Piezas OPC que están asociadas con metadatos|Paquete|OPCIONAL

Las [Partes y relaciones](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Modelos 3D](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Recursos de objetos](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Recursos materiales](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) y [Características del paquete](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) secciones de especificaciones documento dar información detallada sobre el documento 3MF.

## Referencias ##

* [Especificaciones de formato de archivo 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Por Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

