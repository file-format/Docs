{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo FIT: archivo de actividad de Garmin",
  "description":"Obtenga más información sobre el formato de archivo FIT y las API que pueden crear y abrir archivos FIT",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## ¿Qué es un archivo FIT?

Un archivo FIT es un archivo GIS creado por los dispositivos portátiles deportivos de Garmin. Se utiliza para registrar las actividades de la persona cuando se desplaza portando estos dispositivos. Los datos de actividad incluyen la ubicación y la hora registradas por el dispositivo GPS. Los archivos FIT también se utilizan para transferir los datos de actividad registrados mediante las API web. Esa es la razón por la que los archivos FIT son el formato de archivo más utilizado para compartir datos de fitness con otras plataformas de fitness. Otros formatos de archivo comunes incluyen [GPX](/es/gis/gpx/), TCX y [KML](/es/gis/kml/).

## Formato de archivo FIT - Más información

Los archivos FIT se guardan en el disco como archivos binarios con la información registrada por los dispositivos Garmin para la actividad. La información almacenada dentro de un archivo FIT incluye:

* Fecha y hora
* Tipos de deporte
* Datos de vuelta y división
* Rastreo de GPS
* Datos del sensor
* Eventos para sesión activa

Los datos de actividad se pueden registrar en el archivo en tiempo real o exportar una vez que se completa el registro de actividad.

### Mensajes de actividad FIT

Un archivo de actividad FIT puede incluir algunos tipos de mensajes requeridos. Los siguientes son los mensajes necesarios para un archivo de actividad.

|Mensaje|Propósito|
---|---|
|Id. de archivo| Todos los tipos de archivos FIT requieren el mensaje de ID de archivo y se espera que sea el primer mensaje en el archivo. Para los archivos de actividad, la propiedad Tipo debe establecerse en 4.|
|Actividad| Se requiere un solo mensaje de actividad en un archivo de actividad FIT. En el mensaje de actividad se incluyen las propiedades Local Timestamp y Session Count. La marca de tiempo local se utiliza para determinar el desplazamiento de la zona horaria que se puede aplicar a todas las marcas de tiempo del archivo. La mayoría de los dispositivos graban archivos FIT en tiempo real y el recuento de sesiones se desconocerá hasta el final de la grabación. Por este motivo, el mensaje de actividad suele ser el último mensaje del archivo.|
|Sesión| Los archivos de actividad contendrán uno o más mensajes de sesión. Un mensaje de sesión es un tipo de mensaje de resumen. Hora de inicio, Tiempo total transcurrido, Tiempo total del temporizador y Marca de tiempo son campos obligatorios para todos los mensajes de resumen.|
|Vuelta| Los mensajes de vuelta representan vueltas o intervalos dentro de la sesión. Un mensaje de vuelta es un tipo de mensaje de resumen. Hora de inicio, Tiempo total transcurrido, Tiempo total del temporizador y Marca de tiempo son campos obligatorios para todos los mensajes de resumen.|
|Grabar| Los mensajes de registro incluyen coordenadas GPS, velocidad, distancia, frecuencia cardíaca, potencia, etc.|

## Archivo FIT Recursos útiles

* [Descodificación de archivos de actividad FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Codificación de archivos de actividad FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referencias ##

* [Archivo de actividad FIT](https://developer.garmin.com/fit/file-types/activity/)

