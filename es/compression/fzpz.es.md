{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo FZPZ - Archivo de pieza Fritzing",
  "description":"Obtenga información sobre qué es un archivo FZPZ y las API que pueden crear y abrir archivos FZPZ",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## ¿Qué es un archivo FZPZ?

Un archivo FZPZ es un componente o pieza que se utiliza en el diseño de un circuito electrónico creado con la aplicación de diseño y creación de prototipos de circuitos **Fritzing**. Es un archivo comprimido que contiene un archivo [FZP](/es/cad/fzp/) y cuatro imágenes [SVG](/es/image/svg/) que describen la parte general de Fritzing. La ventaja de usar estos archivos es que los usuarios pueden compartir sus archivos FZPZ con cada uno desde el punto de vista de la reutilización. Compartir partes de FZPZ ayuda a integrar partes de circuitos para crear diseños de PCB más grandes de manera rápida.

## Formato de archivo FZPZ - Más información

Los archivos FZPZ se guardan en el disco como archivos comprimidos [ZIP](/es/compression/zip/). Puede cambiar el nombre de la extensión de .fzpz a .zip y usar cualquier utilidad de descompresión estándar como WinZIP para extraer los archivos del archivo.

### Información de la estructura del archivo FZPZ

Como se mencionó, un archivo FZPZ es un archivo de almacenamiento que contiene múltiples archivos para la representación de una parte utilizada en la placa de circuito impreso. El FZPZ contiene los siguientes archivos:

* `Cuatro archivos SVG` - que representan la placa de pruebas, el esquema, la placa de circuito impreso y las imágenes de iconos de la pieza
* `Archivo FZP`: un archivo XML que contiene información sobre las propiedades, los conectores y los buses de la parte

Los archivos generalmente se nombran de la siguiente manera.

* parte.archivo.fzp
* svg.breadboard.archivo.svg
* svg.icono.archivo.svg
* svg.pbc.archivo.svg
* svg.schematic.file.svg

## Referencias ##

* [Nuevas piezas con extensión fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

