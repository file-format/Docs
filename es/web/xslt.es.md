{
  "date" : "2021-01-20",
  "keywords" :["xslt", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "Lenguaje de hoja de estilo extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo XSLT",
  "description":"Obtenga más información sobre el formato de archivo XSLT y las API que pueden crear y abrir archivos XSLT",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## ¿Qué es un archivo XSLT?

Un archivo con una extensión .xslt es un archivo de transformación de lenguaje de hoja de estilo extensible que se usa para transformar y aplicar estilo a un archivo XML usando instrucciones XSL. El formato se utiliza para transformar documentos XML en formatos de salida estándar, como un documento de texto o una página web .html. Esta transformación crea un nuevo documento basado en el contenido del documento XML existente. XSLT lo hace teóricamente capaz de realizar cálculos arbitrarios.

## Formato de archivo XSLT

El formato de archivo XLST contiene instrucciones de transformación en formato de texto sin formato que se pueden ver en cualquier editor de texto. Ha habido tres revisiones al lenguaje.

* `XSLT 1.0`: XSLT 1.0 se publicó como recomendación del W3C en noviembre de 1999.
* `XSLT 2.0`: incluye modificaciones como la manipulación de cadenas mediante expresiones regulares, funciones y operadores para manipular fechas, horas y duraciones, múltiples documentos de salida, agrupación y un sistema de tipos más rico y una verificación de tipos más sólida.
* `XSLT 3.0`: se convirtió en parte de la recomendación W3C el 8 de junio de 2017 y las principales funciones nuevas incluyen transformación de transmisión, paquetes para mejorar la modularidad de hojas de estilo grandes, manejo mejorado de errores dinámicos con, por ejemplo, una instrucción xsl:try, y soporte para mapas y matrices, lo que permite que XSLT maneje JSON y XML.

### Ejemplo XSLT

El siguiente ejemplo está tomado de [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Referencias ##

* [XSLT - Por Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [Elementos XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

