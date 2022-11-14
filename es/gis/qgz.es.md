{
  "date" : "2021-03-18",
  "keywords" :[ "archivo qgz", "formato de archivo qgz", "qué es un archivo qgz", "archivo", "ejemplo de qgz", "extensión de archivo qgz","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Proyecto Comprimido Quantum GIS",
  "description":"Obtenga información sobre el formato de archivo QGZ, que es solo un QGS comprimido y las API que pueden crear y abrir archivos QGZ",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## ¿Qué es un archivo QGZ?

El formato de archivo **QGZ** es un archivo comprimido que contiene un archivo [QGS](https://docs.fileformat.com/gis/qgs/) y un archivo QGD. Mientras que el archivo QGD es la base de datos sqlite del proyecto qgis que consta de datos auxiliares para el proyecto. Si no hay datos auxiliares, el archivo QGD permanecerá vacío.

## Detalles sobre el formato de archivo QGZ

El QGZ se introdujo como una nueva variante del **formato de archivo de proyecto QGIS 3**. Este formato es un contenedor comprimido para el archivo xml de QGS. Si los usuarios eligen QGD que es un formato opcional, en este caso el contenedor es beneficioso para almacenar la base de datos de almacenamiento auxiliar.

En el modo clásico, la base de datos auxiliar se guarda como un archivo con extensión .qgd junto con el archivo xml. Al elegir el contenedor comprimido, el archivo .qgd se incluye en el .qgz. Simplemente facilita a los usuarios sin ningún problema, ¡los usuarios no pueden eliminarlo u olvidarse de copiarlo al compartir archivos de proyecto!


## Referencias

* [QGZ – Un nuevo formato de archivo de proyecto predeterminado para QGIS](https://oslandia.com/es/2018/06/01/qgz-un-nuevo-formato-de-archivo-de-proyecto-predeterminado-para-qgis/)
* [Formatos de archivo QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

