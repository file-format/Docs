{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo FZP y las API que pueden crear y abrir archivos FZP",
  "title" :"Formato de archivo FZP: archivo de descripción de pieza XML Fritzing",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## ¿Qué es un archivo FZP?

Un archivo FZP es un archivo XML creado por [Fritzing](https://fritzing.org/) aplicación de diseño y creación de prototipos de circuitos electrónicos. Contiene información sobre las propiedades, los conectores y los buses de la pieza en formato de archivo [XML](/es/web/xml/). Los archivos FPZ no se pueden usar de forma independiente en Fritzing. En su lugar, se importan como parte del archivo de almacenamiento FZPZ.

## Formato de archivo FZP - Más información

Los archivos FZP son archivos XML que contienen información sobre las propiedades, los conectores y los buses de la pieza. Además de estos, los archivos FZP también contienen información sobre el título, la descripción, el autor y la fecha de publicación del archivo FZP. Cuando se exporta un archivo de pieza de Fritzing, la aplicación Fritzing crea un archivo comprimido [FZPZ](/es/compression/fzpz/) que contiene un archivo FZP y cuatro archivos [SVG](/es/image/svg/).

Las [especificaciones de formato de archivo FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) están disponibles en Github by Fritzing.

## Ejemplo de estructura de archivo FZP

Un archivo FZP típico tiene la siguiente estructura XML.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Referencias

* [Especificaciones del formato de archivo FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nuevas piezas con extensión fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

