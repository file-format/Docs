{
  "date" : "2022-02-16",
  "keywords" :[ "archivo obb", "formato de archivo obb", "qué es un archivo obb", "archivo", "ejemplo de obb", "extensión de archivo obb","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo OBB: archivo de blob binario opaco de Android",
  "description":"Obtenga información sobre el formato de archivo OBB y las API que pueden crear y abrir archivos OBB",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## ¿Qué es un archivo OBB?

Un archivo OBB es un archivo de expansión que contiene datos adicionales además del archivo [APK](/es/compression/apk/) de Android. La tienda Google Play no permite tener un archivo APK de Android con un tamaño superior a 100 MB. Sin embargo, algunas aplicaciones pueden requerir el alojamiento de gráficos de alta definición, archivos multimedia u otros activos grandes además de los archivos APK. Ahí es donde entran los tipos de archivos OBB. Google Play permite adjuntar estos archivos de expansión como complemento del archivo APK.

## Formato de archivo OBB

Los archivos OBB se guardan como archivos binarios junto con los archivos APK. Cuando un APK acompaña a los archivos OBB, Google Play aloja los archivos de expansión en su servidor y no se le cobra ningún costo adicional al desarrollador. Estos archivos adicionales se almacenan en el almacenamiento compartido del dispositivo en la tarjeta SD o en la partición que se puede montar en USB cuando se descarga la aplicación para su instalación.

Los archivos OBB se descargan e instalan al realizar la descarga. Pero en algunos casos, estos se descargan para su instalación cuando se ejecuta la aplicación por primera vez.

### Tamaño máximo de archivo OBB

Google Play Store le permite cargar archivos de expansión OBB de hasta 2 GB. Se recomienda cargar archivos de gran tamaño como archivos comprimidos [ZIP](/es/compression/zip/) para una carga eficiente a través de Internet.

Estos archivos de expansión se pueden alojar como archivo de expansión primario **principal** para recursos adicionales requeridos por la aplicación o como un archivo de expansión de parche opcional destinado a pequeñas actualizaciones del archivo de expansión principal.

## Referencias

* [Desarrolladores de Android - Archivos de expansión](https://developer.android.com/google/play/expansion-files)

