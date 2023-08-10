{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Base de datos Sqlite del proyecto QGIS", "extensión", "formato", "QGIS", "Base de datos auxiliar", "¿Qué es un archivo QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Base de datos Sqlite del Proyecto QGIS",
  "description":"Obtenga más información sobre QGD, que es una base de datos sqlite del proyecto QGIS y las API que pueden crear y abrir archivos QGD",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## ¿Qué es un archivo QGD?

El archivo con extensión .QGD es en realidad la base de datos sqlite asociada del proyecto **QGIS** que alberga los datos auxiliares del proyecto. El archivo QGD permanecerá vacío, si no habrá datos auxiliares para el proyecto.

## Detalles sobre el formato de archivo QGD

En el modo clásico, la base de datos auxiliar se guarda como un archivo con extensión .qgd junto con el archivo xml. El sistema de **Base de Datos Auxiliar** permite leer y escribir datos en el sistema como una forma alternativa. Al crear el QGZ, que es un contenedor comprimido, el archivo .qgd se incluye en el .qgz.

## ¿Qué es la base de datos auxiliar?
La base de datos auxiliar es en realidad un sistema de base de datos en espera que se crea como respuesta a la duplicación de la base de datos de destino. La base de datos auxiliar es en realidad un caso de una base de datos duplicada que sería la base de datos en la que se está duplicando. Por ejemplo, si configura una base de datos en espera utilizando una base de datos duplicada, la base de datos de origen será el destino y la base de datos en espera se conocerá como auxiliar.


## Referencias

* [QGZ – Un nuevo formato de archivo de proyecto predeterminado para QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formatos de archivo QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

