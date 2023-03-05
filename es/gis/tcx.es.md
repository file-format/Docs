{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo TCX: archivo XML del centro de capacitación",
  "description":"Obtenga información sobre el formato de archivo TCX y las API que pueden crear y abrir archivos TCX",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## ¿Qué es un archivo TCX?

Un archivo TCX (Training Center XML) es un formato de intercambio de datos que se utiliza para compartir datos entre dispositivos de fitness. Se introdujo en 2008 con el producto Training Center de Garmin. Los datos de entrenamiento, como la frecuencia cardíaca, la cadencia de carrera, la cadencia de bicicleta, las calorías y el tiempo de vuelta, se almacenan en formato [XML](/es/web/xml/) dentro del archivo TCX. Además, los datos de resumen sobre la pista de entrenamiento también se incluyen en el archivo TCX. Los archivos TCX son similares a los archivos [FIT](/es/gis/fit/) que se crean con los dispositivos portátiles deportivos de Garmin.

## Formato de archivo TCX - Más información

Los archivos TCX se guardan en el disco como archivos XML y cada registro se guarda como una actividad. Una actividad comprende todos los datos de un entrenamiento, como tiempo, tiempo de vuelta, Id, frecuencia cardíaca, intensidad, cadencia e información de seguimiento que contiene los pares de posición junto con la marca de tiempo para esa posición lat-long similar al [GPX](/es/gis/gpx/) archivos.

### Versiones de formato de archivo TCX

Existen dos versiones de este formato con sus propios esquemas XML alojados por Garmin. Los siguientes son algunos de ellos:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protocolo de datos TCX

Una versión rápida del formato TCX XML está disponible en Github como [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referencias ##

* [Centro de formación XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Visor TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

