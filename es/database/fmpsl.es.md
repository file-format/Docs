{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo FMPSL y las API que pueden crear y abrir archivos FMPSL",
  "title" :"Formato de archivo FMPSL - FileMaker Pro 12 Snapshot Link File",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## ¿Qué es un archivo FMPSL?

Un archivo FMPSL es un archivo de instantánea de la base de datos creado con FileMaker Pro 12. Almacena los resultados consultados de la base de datos junto con otra información, como el diseño visual y la información visible. El archivo FMPSL se puede utilizar para restaurar todos estos datos en otra instancia de la base de datos de FileMaker Pro. Este formato de archivo se introdujo con el lanzamiento de FileMaker Pro v 12. Antes de esta versión, los enlaces de instantáneas se introdujeron como formato de archivo FPSL en FileMaker Pro v 11. Los archivos FMPSL se pueden abrir con el software FileMaker Pro Advanced. Otros formatos de archivo compatibles con FileMaker Pro incluyen [FP5](/es/database/fp5/), [FP7](/es/database/fp7/) y [FMP12](/es/database/fmp12/).

## Formato de archivo FMPSL

Los detalles del formato de archivo interno de los archivos FMPSL no están disponibles públicamente para referencia del desarrollador.

### ¿Cómo guardar registros como archivo FMPSL?

Los datos de la base de datos de FileMaker Pro se pueden guardar como un archivo de enlace de instantánea siguiendo los siguientes pasos.

1. Busque los registros de la base de datos que deben guardarse como un archivo de enlace de instantánea.
1. Con la opción Enviar registro como vínculo de instantánea del menú, guarde el archivo ingresando un nombre de archivo.
1. Utilice los registros que se están examinando para guardar todo el conjunto de registros encontrados.

El archivo de instantánea generado se guardará en el disco con el nombre especificado.

## Referencias

* [Convertir versiones anteriores de formatos de archivo de FileMaker Pro al formato de archivo FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Guardar registros como archivo de enlace de instantánea](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

