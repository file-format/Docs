{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo GDOC - Acceso directo a Google Docs",
  "description":"Obtenga información sobre qué es un archivo GDOC y las API que pueden crear y abrir archivos GDOC",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## ¿Qué es un archivo GDOC?

Un archivo GDOC es un archivo de acceso directo que apunta a un archivo ubicado en Google Drive, un servicio de almacenamiento de documentos basado en la nube. Cuando el cliente de Google Drive está instalado en una computadora y se crea un documento en su interior, la unidad crea un documento en el almacenamiento en la nube en línea y escribe la [URL](/es/web/url/) de este documento en el archivo GDOC en Google local. Carpeta de unidad. Cuando se hace doble clic en este archivo de acceso directo, el navegador web predeterminado abre el documento desde la ubicación [URL](/es/web/url/). Si este archivo de acceso directo se saca de esta carpeta, el enlace al documento en línea se rompe.

## Formato de archivo GDOC - Más información

El archivo GDOC contiene un acceso directo al documento en línea escrito en formato de archivo [JSON](/es/web/json/). El navegador que abre los archivos GDOC lee la información de la URL y abre el documento vinculado para mostrarlo, siempre que el usuario haya iniciado sesión en esta cuenta de Google donde se almacena el documento. Los archivos GDOC no contienen el contenido del documento.

### Ejemplo de archivo GDOC

El archivo GDOC se puede abrir en un editor de texto y su contenido se parece a lo siguiente.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Como se puede ver, los contenidos están formateados en JSON con la URL de un documento y la identificación del documento asociado.

## Referencias

* [Google Docs no abre archivos gdoc o docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

