{
  "date" : "2021-02-15",
  "keywords" :[ "archivo vp6", "formato de archivo vp6", "qué es un archivo vp6", "archivo", "ejemplo de vp6", "extensión de archivo vp6","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Archivo de vídeo TrueMotion",
  "description":"Obtenga información sobre el formato de archivo VP6 y las API que pueden crear y abrir archivos VP6",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## ¿Qué es un archivo VP6?

VP6 es un formato de video de compresión con pérdida que On2 Technologies introdujo en mayo de 2003. Forma parte de una serie de códecs de video desarrollados por TrueMotion, incluidos V3, V4 y V5. El formato se utilizó en breve en el campo de la radiodifusión, como con los informes de la BBC y el software QuickLink. VP6 fue reemplazado por VP7 Codec en enero de 2005 con una mejor compatibilidad de compresión.

## Formato de archivo VP6

Las especificaciones completas para los archivos V6 no están disponibles públicamente. On2 hizo públicas las especificaciones inicialmente, pero pronto dejaron de estar disponibles para los usuarios generales. Una documentación no oficial del formato de archivo VP6 está disponible en [wiki multimedia] (https://wiki.multimedia.cx/index.php?title=On2_VP6) que se puede consultar para referencia del desarrollador.

### Macrobloques (MB)

Al igual que MPEG-2, MPEG-4 partes 2 y 10, cada cuadro de video de un archivo VP6 se compone de una matriz de macrobloques (MB) de 16x16. Cada MB puede estar en uno de los siguientes modos:

* MB intra
* Inter MB, MV nulo, referencia de cuadro anterior
* Inter MB, MV diferencial, referencia de cuadro anterior
* Inter MB, cuatro MV, referencia de cuadro anterior
* Inter MB, MV 1, referencia de cuadro anterior
* Inter MB, MV 2, referencia de cuadro anterior
* Inter MB, MV nulo, referencia de cuadro marcado
* Inter MB, diferencial MV, marco de referencia marcado
* Inter MB, MV 1, referencia de cuadro marcado
* Inter MB, MV 2, referencia de cuadro marcado

### Encabezado de cuadro

El encabezado de la trama de un VP6 se muestra a continuación y sigue el empaquetamiento de bits big-endian.

|Sintaxis|Número de bits|Tipo|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 significa un intraframe|
|qp |6 |Sin signo |Parámetro de cuantificación rango válido 0..63|
|marcador| 1| Constante| 0=VP61/62, 1=VP60|
|si (modo_marco == 0) { | 0 | |igual a INTRA_FRAME|
|versión |5| Constante| 6=VP60/61, 7=VP60(Artes electrónicas), 8=VP62|
|versión2 |2| Constante |0=VP60, 3=VP61/62|
|entrelazar |1| Booleano |verdadero (1) significa que se usará entrelazado|
|si (marcador==1 o versión2==0) {||||
|desplazamiento |16 |Sin firmar| desplazamiento del búfer secundario (bytes relativos al inicio del búfer) |
|}||||
|dim_y |8| Sin firmar| Altura de macrobloque de video|
|dim_x |8| Sin firmar| Ancho de macrobloque de video |
|render_y |8 |Sin firmar |Altura de visualización del vídeo|
|render_x |8 |Sin firmar |Ancho de visualización del vídeo|
|}más{||||
|si (marcador==1 o versión2==0) {||||
|desplazamiento |16 |Sin signo |Desplazamiento del búfer secundario (bytes relativos al inicio del búfer)|
|}||||
|}||||

## Referencias

* [Wikipedia VP6](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

