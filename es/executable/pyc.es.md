{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo PYC y las API que pueden crear y abrir archivos PYC",
  "title" :"Formato de archivo PYC: archivo compilado de Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## ¿Qué es un archivo PYC?

Un archivo PYC es un archivo de salida compilado generado a partir del código fuente escrito en el lenguaje de programación Python. Cuando el archivo PY se ejecuta con el intérprete de Python, se convierte en código de bytes para su ejecución. Al mismo tiempo, el código de bytes compilado también se guarda como archivo .pyc para reutilizarlo desde la memoria caché en un momento posterior, si corresponde.

## Estructura del formato de archivo PYC

Los archivos PYC están en código de bytes y sus especificaciones de formato de archivo no están disponibles públicamente. Sin embargo, la investigación de algunas fuentes muestra que la [estructura de un archivo PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) consta de:

* `Un número mágico de cuatro bytes`r: simplemente dos bytes que cambian con cada cambio en el código de clasificación y luego dos bytes de 0d0a.
* `Una marca de tiempo de modificación de cuatro bytes`: marca de tiempo de modificación de Unix del archivo fuente que generó el .pyc, para que pueda volver a compilarse si la fuente cambia.
* `Un objeto de código ordenado`: la salida de marshal.dump del objeto de código que es el resultado de compilar el archivo fuente.

## Referencias

* [La estructura de los archivos .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

