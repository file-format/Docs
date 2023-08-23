{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "archivo", "extensión", "formato", "Audio", "Sistema global para audio móvil", "extensión gsm", "archivos gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo GSM y las API que pueden crear y abrir archivos GSM",
  "title" :"GSM - Sistema global para formato de archivo de audio móvil",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## ¿Qué es un archivo GSM?

GSM es una extensión de archivo asociada con el sistema global para archivos de formato de audio móvil. Los archivos que contienen extensiones GSM se pueden abrir en plataformas Linux, Windows y Mac OS. El formato de archivo GSM pertenece a la categoría de archivos de audio.

Un archivo GSM está codificado con un códec de compresión de sonido CBR (tasa de bits constante) con pérdidas. La tasa de muestreo en un archivo de audio GSM es de 8000 muestras/segundo, mientras que la tasa de datos es de alrededor de 13 kbps. La tasa de bits dentro de los archivos GSM garantiza la calidad durante la grabación de voz. Además, el formato de archivo GSM también se conoce como el formato estándar global que se usa en teléfonos móviles y los archivos WAV también se pueden codificar fácilmente usando un formato de archivo GSM. Cualquier problema con un archivo GSM puede ser resuelto fácilmente por el propio usuario sin acudir a un experto.

Los usuarios también pueden convertir archivos GSM a formatos [MP3](/es/audio/mp3/) y [MP4](/es/video/mp4/).

## Breve historia del formato de archivo GSM

GSM es un formato de archivo de audio que se creó para la telefonía por Internet en Europa. Fue desarrollado por el Instituto Europeo de Normas de Telecomunicaciones (ETSI) para ser utilizado como un celular digital 2G utilizado en teléfonos móviles y tabletas. Hoy en día se utiliza para almacenar grabaciones de conversaciones telefónicas y mensajes de voz.

## Especificaciones del formato de archivo GSM ##

GSM trabaja sobre una red estructurada que consta de las siguientes secciones:

- **Modulación**: es un proceso de transformación de datos de entrada en un formato que se puede transmitir fácilmente. Los datos transmitidos se demodulan en el extremo receptor.
- **Tasa de transmisión**: GSM es un sistema digital que tiene una tasa de bits superior a 270 kbps
- **Rango de frecuencia de enlace ascendente**: 933-960 MHz
- **Rango de frecuencia de enlace descendente**: 890 - 915 MHz
- **Espaciado de canales** : Significa el espaciado entre barreras adyacentes que debe ser de unos 200 kHz
- **Distancia dúplex**: Es el espacio entre las frecuencias de enlace ascendente y descendente que debe ser de 80 MHz
- **Codificación de voz**: GSM utiliza codificación predictiva lineal (LPC). LPC comprime la tasa de bits. Cuando la señal de audio pasa por un filtro e imita el tracto vocal. Codificación de voz GSM a 13 kbps

| Formato de compresión de audio | Algoritmo | Tasa de muestreo | Transformación de tasa de bits | Latencia | RBC | VBR | Estéreo | Multicanal |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8kHz | 5,6 kbit/s | 25 ms | Sí | No | No | No |
| GSM-FR | LTP-RPE | 8kHz | 13 kbit/s | 20–30ms | Sí | No | No | No |
| GSM-EFR | ACELP | 8kHz | 12,2 kbit/s | 20–30ms | Sí | No | No | No |

## Referencias ##

* [GSM - Por Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

