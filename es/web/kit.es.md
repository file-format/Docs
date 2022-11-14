{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo KIT y las API que pueden crear y abrir archivos KIT",
  "title" :"Formato de archivo KIT - Archivo CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## ¿Qué es un archivo KIT?

Un archivo con extensión .kit es un archivo HTML que se crea con la aplicación de lenguaje de programación [CodeKit](https://codekitapp.com/). Contiene `importaciones` y `variables` además de los archivos [HTML](/es/web/html/) existentes, lo que lo hace ideal para sitios estáticos. CodeKit compila archivos KIT en HTML que se pueden usar fácilmente como archivos de sitios web estáticos.

## Formato de archivo KIT

Los archivos KIT son archivos HTML que además incluyen importaciones y variables. Estos se almacenan como archivos de texto sin formato y se pueden abrir con cualquier editor de texto o editores de archivos web.

### Importaciones de archivos KIT

Casi cualquier tipo de archivo se puede importar a un archivo de kit. A continuación se muestra la sintaxis de importación utilizada para importar archivos a un archivo .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Cuando se agrega una importación a un archivo KIT y se guarda, se reemplaza con el texto del archivo que se está importando. También puede usar @include en lugar de @import.

### Importaciones múltiples en un archivo KIT

También puede importar más de un archivo a la vez utilizando una lista separada por comas:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referencias

* [¿Qué es Kit?](https://codekitapp.com/help/kit/)

