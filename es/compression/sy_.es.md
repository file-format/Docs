{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo SY_ - Archivo SYS comprimido",
  "description":"Obtenga información sobre el formato de archivo SY_ y las API que pueden crear y abrir archivos SY_",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## ¿Qué es un archivo SY_?

Un archivo SY_ es un archivo .sys comprimido que utilizan los instaladores de software para reducir el tamaño de los archivos de instalación empaquetados dentro del instalador. Esto reduce el tamaño total del instalador. Los archivos SY_ se pueden expandir usando la utilidad de línea de comando Microsoft Expand que expande uno o más archivos comprimidos.

## Formato de archivo SY_ - Más información

Los archivos SY_ se guardan en el disco como archivos binarios comprimidos. Sin embargo, su formato de archivo interno no está disponible públicamente. La utilidad de línea de comando Microsoft Expand puede expandir archivos SY_ usando una de las siguientes líneas de comando.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Cuando se expanden, los archivos SY_ se convierten en un archivo [SYS](https://docs.fileformat.com/system/sys/).

Los archivos SY_ son similares a los archivos EX_ y DL_.

## Referencias

* [StuffIt - Por Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Expandir de Microsoft](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

