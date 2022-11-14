{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo TPSR - Archivo de informe de sesión piloto de TeamViewer",
  "description":"Obtenga información sobre el formato de archivo TPSR y las API que pueden crear y abrir archivos TPSR",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## ¿Qué es un archivo TPSR?

Un TPSR es un archivo de protocolo de conexión utilizado por TeamViewer Assist AR (anteriormente conocido como TeamViewer Pilot). La información almacenada en un archivo TPSR se almacena en formato de archivo comprimido [ZIP](/es/compression/zip/). TPSR contiene un historial detallado de la conexión de TeamViewer entre un experto y un técnico para resolver problemas y fines de revisión. La información contenida dentro de un archivo TPSR incluye el tipo de dispositivo, el nombre, la ID de Assist AR, la ID de experto, la fecha y la hora, y la duración de la conexión. Estos datos se almacenan en un archivo [JSON](/es/web/json/) dentro del archivo TPSR comprimido.

## Formato de archivo TPSR

Un archivo TPSR se almacena en un disco en formato de archivo ZIP donde el contenido se almacena dentro de un archivo JSON. Se genera automáticamente después de completar la conexión de Assist AR siempre que la opción de informes de conexión esté habilitada en TeamViewer.

TeamViewer Assist AR permite que los expertos se conecten con los técnicos para obtener una transmisión EN VIVO del extremo remoto a través de la cámara móvil. Pueden ayudar a los técnicos a resolver el problema por teléfono.

## Abrir archivos TPSR

Puede abrir archivos TPSR utilizando la versión de escritorio del software TeamViewer. Si está instalado en su computadora, al hacer doble clic en el archivo TPSR se abrirá en el software TeamViewer. Los archivos TPSR también se pueden exportar a archivos [PDF](/es/pdf/) o se pueden imprimir para tener una copia impresa del archivo de protocolo.

## Referencias ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

