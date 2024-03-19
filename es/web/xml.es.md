{
  "date" : "2019-10-11",
  "keywords" :["xml", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "lenguaje de marcado extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo XML",
  "description":"Obtenga información sobre el formato de archivo XML y las API que pueden crear y abrir archivos XML",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo XML?

XML significa Lenguaje de marcado extensible que es similar a **[HTML](/es/web/html/)** pero diferente en el uso de etiquetas para definir objetos. La idea detrás de la creación del formato de archivo XML era almacenar y transportar datos sin depender de herramientas de software o hardware. Su popularidad se debe a que es legible tanto por humanos como por máquinas. Esto le permite crear protocolos de datos comunes en forma de objetos para ser almacenados y compartidos a través de una red como la World Wide Web (WWW). La "X" en XML es extensible, lo que implica que el lenguaje se puede extender a cualquier número de símbolos según los requisitos del usuario. Es por estas funciones que muchos formatos de archivo estándar lo utilizan, como Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/es/web/xhtml/)** y **[SVG](/es/page-description-language/svg/)**.

## Formato de archivo XML

El formato de archivo XML se basa en el modelo de objeto de documento XML (DOM), que es una API de programación para documentos HTML y XML. El DOM XML define un método estándar para acceder y manipular los elementos del documento XML. Hace una vista de estructura de árbol de un documento XML que se puede usar para acceder a todos los elementos a través del árbol DOM. Los elementos existentes se pueden modificar/eliminar, así como se pueden crear nuevos elementos en el árbol XML. Cada elemento de un documento XML se denomina nodo. El XML DOM es como se muestra en la siguiente imagen.

{{< figure src="../XML DOM.png" alt="DOM XML" >}}

### Enfoque universal de XML

El poder de XML lo convierte en un lenguaje universal para la comunicación de datos a través de la red al simplificar el transporte de datos y los cambios de plataforma. Esto también asegura que sea posible el intercambio de datos entre sistemas incompatibles mediante el almacenamiento de datos en formato de texto sin formato. HTML es para la representación de datos en la web, mientras que XML es para el intercambio de datos. Los pares de etiquetas de marcado utilizados dentro de XML definen los elementos clave de la estructura que utilizarán las aplicaciones de lectura.

## Ejemplo XML

El siguiente es un ejemplo simplificado de un catálogo de CD donde cada registro contiene información sobre los CD como artista, país, compañía, precio y año de producción.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referencias

* [XML - Por Wikipedia](https://en.wikipedia.org/wiki/XML)

