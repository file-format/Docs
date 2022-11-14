{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","archivo ixbrl", "formato de archivo ixbrl", "tipo de archivo ixbrl", "archivo", "tipo", "qué es un archivo ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Formato de archivo de informes comerciales y financieros",
  "description":"Obtenga información sobre el formato de archivo IXBRL y las API que pueden crear y abrir archivos IXBRL",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## ¿Qué es un archivo iXBRL?

El formato de archivo iXBRL (ilnine XBRL) permite que los datos [XBRL](/es/web/xbrl/) se incrusten en un archivo HTML para que sea legible tanto por máquina como por humanos. En realidad, es un archivo [xHTML](/es/web/xhtml/) que usa las etiquetas XBRL y fue desarrollado por XBRL International para cumplir con los requisitos de HMRC del Reino Unido. Con iXBRL, se pueden crear estados financieros manteniendo intacto el diseño del documento original. Los archivos iXBRL se pueden abrir en cualquier editor de texto, como Notepad en el sistema operativo Windows y TextEdit en MacOS.

## Formato de archivo iXBRL

Dentro de iXBRL, los contenidos de XBRL están envueltos en un formato de archivo xHTML que utiliza etiquetas XML. como XBRL,<xbrl> es el elemento raíz de los archivos iXBRL. El formato XHTML representa su contenido como una colección de diferentes tipos de documentos y módulos. Todos los archivos en XHTML se basan en el formato de archivo XML y se ajustan a los estándares de documentos XML. XHTML es el formato de uso esencial para la utilización operativa del modelo de objeto de documento (DOM) [HTML](/es/web/html/) dependiente o del modelo de objeto de documento [XML](/es/web/xml/). Para el mundo exterior, iXBRL sigue las especificaciones de formato de archivo [xHTML](/es/web/xhtml/).

### iXBRL frente a XBRL

XBRL se puede comparar con iXBRL según los siguientes factores:

* Complejidad
* Opciones de formato
* Tipos de archivos/Extensiones
* Opción de renderizado
* Proceso de presentación

La siguiente tabla ilustra estas diferencias.

|Parámetro|XBRL|iXBRL|
---|---|---|
|Complejidad|Más complejo que iXBRL|Menos complejo debido al esquema de organización existente de XHTML|
|Opciones de formato|Flexibilidad limitada|Alta flexibilidad para formatear contenidos|
|Tipos de archivo/extensión|Guardado formalmente con extensión .xml|Generalmente guardado como extensión .html o .xhtml|
|Opciones de representación|Visores XBRL necesarios para ver estos|contenido legible por humanos que se puede ver en navegadores|
|Proceso de presentación| Los documentos de instancia XBRL (legible por máquina) y HTML (legible por humanos) se archivarán por separado. Tanto los formatos legibles por humanos como los legibles por máquina están disponibles en un único documento de instancia.

## Referencias

* [XBRL - Por Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

