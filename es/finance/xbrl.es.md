{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl","archivo xbrl", "formato de archivo xbrl", "tipo de archivo xbrl", "archivo", "tipo", "qué es un archivo xbrl"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Formato de archivo de informes comerciales y financieros",
  "description":"Obtenga más información sobre el formato de archivo XBRL y las API que pueden crear y abrir archivos XBRL",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## ¿Qué es un archivo XBRL?

Un archivo con la extensión .xbrl (lenguaje extensible de informes comerciales) es un marco global y disponible gratuitamente para intercambiar información comercial. Ahora se usa ampliamente como uno de los formatos estándar que ha reemplazado a los antiguos informes en papel con registros digitales más útiles y precisos. Los datos intercambiados mediante los archivos XBRL incluyen libros de contabilidad, detalles financieros y balances. Admite etiquetas de datos que permiten el procesamiento de datos desde la preparación hasta la etapa de análisis de información comercial de todo tipo. Los archivos XBRL se pueden abrir con software como Rivet Software Dragon View XBRL Viewer y API como [Aspose.Finance](https://products.aspose.com/finance/).

## Formato de archivo XBRL

XBRL es un estándar internacional abierto para informes comerciales digitales que se usa ampliamente en todo el mundo. Es un lenguaje basado en [XML](/es/web/xml/) que utiliza elementos XBRL, conocidos como etiquetas, para describir cada elemento de los datos comerciales para formular datos para la clasificación y el análisis de informes. Las especificaciones del formato de archivo XBRL son desarrolladas y publicadas por XBRL International, Inc, con [XBRL versión 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) actualmente disponible para los usuarios.

### Estructura del documento XBRL

Información completa sobre las [etiquetas XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) puede ser referido por los programadores para escribir aplicaciones para trabajar con este formato de archivo. Un XBRL consiste en una instancia de XBRL y una colección de taxonomías.

**`XBRL Instance`**: la instancia XBRL comienza con el<xbrl> elemento raíz. Un documento XML grande puede contener más de una instancia XBRL incrustada.

**`Taxonomía XBRL`** - La [Taxonomía XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 +errata-corregida-2013-02-20.html#_5) se define como una estructura de esquema XML y un conjunto de elementos de enlaces externos referenciados directamente. Un esquema de taxonomía escalable que muestra las referencias de la base de enlaces es el siguiente.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Referencias ##

* [XBRL - Por Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Lenguaje extensible de informes comerciales (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

