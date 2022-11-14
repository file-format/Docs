{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MPG",
  "keywords" :[ "MPG", "archivo", "extensión", "formato", "formato de video", "qué es un formato de archivo mpg", "formato de archivo mpg", "reproductor de archivos mpg", "compresión mpeg", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Obtenga información sobre el formato de archivo MPG y las API que pueden crear y muestre cómo abrir los archivos MPG",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## ¿Qué es un formato de archivo MPG? ##

El archivo con extensión .mpg pertenece al grupo de extensiones de archivo para compresión de audio y video MPEG-1 o MPEG-2. El video MPEG-1 Parte 2 no está fácilmente disponible, y esta extensión (formato de archivo MPG) generalmente apunta a un flujo de programa MPEG que se define en MPEG-1 y MPEG-2, o un flujo de transporte MPEG que se define en MPEG-2. . También existen otras extensiones, como .m2ts, que especifican el contenedor preciso, en este caso, MPEG-2 TS, pero esto tiene poca relevancia para los medios MPEG-1. El [.mp3](https://docs.fileformat.com/audio/mp3/) es la extensión más común para archivos que contienen audio MP3. Un archivo MP3 es un flujo típico de audio sin procesar; la forma tradicional de etiquetar archivos MP3 es escribir datos de transmisión en segmentos "basura" de cada fotograma, que guardan la información multimedia pero son descartados por el **reproductor de archivos mpg**. Esta es una técnica similar que se usa para etiquetar los archivos AAC, pero menos compatible hoy en día.

## Compresión MPEG ##

El nombre MPEG significa Grupo de expertos en imágenes en movimiento. MPEG es una herramienta para la compresión de video, que implica la compresión de imágenes y sonidos, así como la sincronización de los dos.
Actualmente existen varios estándares MPEG.

- Se propone MPEG-1 para velocidades de datos intermedias, del orden de 1,5 Mbit/seg.
- MPEG-2 se propone para altas velocidades de datos de al menos 10 Mbit/seg.
- Se propuso MPEG-3 para la compresión de HDTV, pero se descubrió que era redundante y se fusionó con MPEG-2.
- MPEG-4 se propone para velocidades de datos muy bajas de menos de 64 Kbit/seg.


## Flujo de programa de formato de archivo MPG ##

El flujo de programa es un contenedor para multiplexar audio digital, video y más. El formato del flujo de programa se especifica en la primera parte de MPEG-1 (ISO/IEC 11172-1) y la primera parte de MPEG-2, Sistemas (estándar ISO/IEC 13818-1/ITU-T H.222.0). El flujo de programa MPEG-2 tiene base analógica y es similar a la capa de sistemas ISO/IEC 11172 y es compatible con versiones posteriores.

### Detalles de codificación ###

Estos son los detalles de codificación del formato de encabezado del paquete MPEG-2 Program Stream parcial:

| Nombre | Número de bits | Descripción |
---|---|---|
| sincronizar bytes | 32 | 0x000001BA |
| puntas de marcador | 2 | 01b para la versión MPEG-2. Los bits de marcador para la versión MPEG-1 son 4 bits con valor 0010b. |
| Reloj del sistema [32..30] | 3 | Referencia de reloj del sistema (SCR) bits 32 a 30 |
| punta de marcador | 1 | 1 bit siempre establecido. |
| Reloj del sistema [29..15] | 15 | Bits de reloj del sistema 29 a 15 |
| punta de marcador | 1 | 1 bit siempre establecido. |
| Reloj del sistema [14..0] | 15 | Bits de reloj del sistema 14 a 0 |
| punta de marcador | 1 | 1 bit siempre establecido. |
| Ampliación del SCR | 9 | |
| punta de marcador | 1 | 1 bit siempre establecido. |
| tasa de bits | 22 | En unidades de 50 bytes por segundo. |
| puntas de marcador | 2 | 11 Bits siempre establecidos. |
| reservado | 5 | reservado para uso futuro |
| longitud de relleno | 3 | |
| bytes de relleno | 8*longitud del relleno | |
| encabezado del sistema (opcional) | 0 o más | si el código de inicio del encabezado del sistema sigue: 0x000001BB |

La siguiente tabla muestra el formato de encabezado del sistema parcial:

| Nombre | Número de bytes | Descripción |
---|---|---|
| sincronizar bytes | 4 | 0x000001BB |
| longitud del encabezado | 2 | |
| velocidad límite y bits de marcador | 3 | |
| audio encuadernado y banderas | 1 | |
| banderas, bit de marcador y enlace de video | 1 | |
| Restricción de tasa de paquete y byte reservado | 1 | |


## Referencias ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



