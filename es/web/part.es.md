{
  "date" : "2021-06-24",
  "keywords" :[ "PARTE", "parcial", "extensión", "archivo", "formato", "web", "descargado"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - Archivo parcialmente descargado",
  "description":"Obtenga información sobre el formato de archivo PART y las API que pueden crear y abrir archivos PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## ¿Qué es un archivo PARTE? ##

Un archivo parcial o extensión .part es un archivo descargado parcialmente. Se utiliza cuando las descargas están en curso o se han interrumpido debido a algún problema, lo que le da al administrador de descargas la oportunidad de reanudar la descarga siempre que sea posible.
Esto significa que el navegador, como Firefox o los programas de transferencia de archivos como eMule, eMule plus, FlashGet, etc., almacena una parte del archivo, llamado Part file, mientras se realiza la descarga en su dispositivo. Este archivo parcial le mostrará si la descarga está en curso o se ha interrumpido antes de completarse. No solo esto, sino que el archivo PART almacena todos los datos hasta que se completa la descarga, por lo que algunos de ellos se pueden reanudar más tarde si desea iniciar la descarga nuevamente.

## PARTE Formato de archivo ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
