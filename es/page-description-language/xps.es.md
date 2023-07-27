{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Especificaciones de papel XML", "Archivo", "Extensión", "Formato de archivo", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Formato de archivo de diseño de página",
  "description":"Obtenga información sobre el formato de archivo XPS y las API que pueden crear y abrir archivos XPS",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo XPS? ##

Un archivo XPS representa archivos de diseño de página que se basan en las especificaciones de papel XML creadas por Microsoft. Fue desarrollado como reemplazo del formato de archivo EMF y es similar al formato de archivo [PDF](/es/pdf/), pero usa XML en el diseño, la apariencia y la información de impresión de un documento. De hecho, está más justificado decir que XPS es un intento de PDF, pero no pudo obtener suficiente popularidad como propiedad de PDF por muchas razones. Microsoft proporciona XPS Document Writer de forma predeterminada desde Windows 7 en adelante para la creación de archivos XPS. Los archivos XPS se pueden generar seleccionando "Microsoft XPS Document Writer" como impresora mientras se imprime el documento.

Los visores XPS vienen integrados como parte de Windows Vista, Windows 7, Windows 8 e Internet Explorer 6 o posterior. Los archivos XPS se vuelven de solo lectura una vez que se generan. Esto se suma a la confianza del usuario en los documentos recibidos enviados como XPS para la autenticidad del documento. Un documento XPS puede contener una o más páginas convertidas del documento original.

## Breve historia ##

Microsoft envió la especificación XPS a Ecma International. En junio de 2007, se creó el Comité Técnico 46 de Ecma (TC46) para desarrollar un estándar basado en las especificaciones de papel de OpenXPS. Ecma International aprobó el estándar Ecma (ECMA-388) [especificaciones XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) en junio de 2009 en la 97.ª Asamblea General.

## Formato de archivo XPS ##

El formato XPS consta de marcado XML que define la composición de un documento y la apariencia visual de cada página junto con reglas de representación para mostrar o imprimir el documento. Conserva toda la información para volver a crear un documento en cualquier sistema, lo que lo hace independiente de los recursos disponibles en ese sistema. El formato es esencialmente un archivo ZIP y si cambia el nombre de la extensión del archivo a ZIP, verá los archivos constituyentes que contienen los datos del documento. Estos documentos incluyen:

* Archivos de página de documento (.fpage): contiene el contenido del documento y la configuración del formato del documento. Cada página del documento XPS tiene un archivo FPAGE.
* archivo de configuración del documento (.fdoc): almacena la configuración incluida en el archivo XPS.
* Archivos de fragmentos de documentos (.frag): define la configuración del archivo XPS real y cada página del documento tiene su propio archivo .frag.

{{< figure src="../XPS-1.png" alt="Formato de archivo XPS" >}}

Estos archivos retienen el contenido del documento de tal manera que si, por ejemplo, alguien no tiene las mismas fuentes instaladas en su máquina, el visor XPS seguirá representando esas fuentes originales. Esto implica la inclusión de un archivo de marcado XML para cada uno:

* Página
* Texto
* Fuentes incrustadas
* Imágenes de trama
* Gráficos vectoriales 2D
* Gestión de derechos digitales

El formato del documento XPS incluye un conjunto bien definido de partes y relaciones, cada una de las cuales cumple un propósito particular en el documento. El formato también amplía las funciones del paquete, incluidas las firmas digitales, las miniaturas y el intercalado.

Un documento XPS típico tiene el siguiente aspecto y se puede analizar a la luz del formato de archivo XPS [especificaciones](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="Formato de archivo XPS" >}}


## Referencias ##

* [Especificaciones del formato de archivo XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Por Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

