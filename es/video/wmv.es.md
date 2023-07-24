{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo WMV",
  "description":"Obtenga información sobre el formato de archivo WMV y las API que pueden crear y abrir archivos WMV",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## ¿Qué es un archivo WMV?

El formato de sistemas avanzados (ASF) es un contenedor multimedia digital diseñado principalmente para almacenar y transmitir flujos de medios. Microsoft Windows Media Video (WMV) es el formato de video comprimido y Microsoft Windows Media Audio (WMA) es el formato de audio comprimido junto con metadatos adicionales en el contenedor ASF desarrollado por Microsoft. Una vez que los archivos WMV o WMA se codifican con los códecs de Windows Media Video y Windows Media Audio, se representan con la extensión .asf. WMV comprime archivos grandes para una mejor tasa de transmisión a través de una red mientras mantiene la calidad del video. WMV está específicamente diseñado para ejecutarse en todos los dispositivos Windows. Después de la estandarización de la Society of Motion Picture and Television Engineers (SMPTE), ahora se considera que WMV es un formato de estándar abierto.

## Historia ##

Con la ayuda de los códecs propietarios de Microsoft, en 1999 se desarrolló un nuevo formato de video comprimido conocido como WMV7, basado en MPEG-4 Parte 2. Se agregaron mejoras en otras dos versiones, es decir, WMV8 y 9. Microsoft presentó una versión 9^^th^^ de WMV a SMPTE para su estandarización en 2003, que finalmente se estandarizó en 2006 como SMPTE 421M, también conocido como VC-1. La idea detrás de WMV era desarrollar un formato de medios que pudiera ser compatible con todo el hardware y software compatibles con Microsoft. Además, otro propósito importante era transmitir secuencias de video a través de Internet en un escenario óptimo. Después de la estandarización de SMPTE, WMV también se convirtió en un formato de video para discos Blu-ray.

## Especificaciones de formato de archivo

### Envase

Generalmente, WMV se empaqueta en un contenedor ASF pero, además, el contenedor Matroska o AVI también puede admitirlo con extensiones de .mkv y .avi, respectivamente.

### Vídeo de Windows Media 9

Aunque hay varios códecs de audio y video disponibles en la serie Windows Media Video 9 para la creación y reproducción de medios digitales, el códec WMV-9 es el mejor y más reciente códec de video, ya que puede lograr la compresión óptima desde velocidades de bits muy bajas, es decir, 160 x 120 a 10 Kbps a 1920 x 1080 a 4-8 Mbps para una variedad de videos HD.

### Estructura del códec

WMV-9 tiene un formato de color interno de 8 bits 4:2:0. Al igual que todos los demás estándares populares de compresión de video MPEG-1 y H.261, WMV-9 utiliza un esquema de transformación espacial y compensación de movimiento basado en bloques. En general, podemos decir que estos estándares realizan una compensación de movimiento bloque por bloque a partir del cuadro reconstruido anterior con la ayuda de una cantidad 2-D llamada vector de movimiento (MV) para señalar el desplazamiento espacial. El bloque actual se forma con la ayuda de la predicción de los valores del marco reconstruido anterior del mismo tamaño que se desplaza de la posición actual por el vector de movimiento. Eventualmente, el error residual se calcula como la diferencia entre el bloque predicho con compensación de movimiento y el bloque real. Este error residual se transforma utilizando una transformación de compactación de energía lineal, luego se cuantifica y se codifica en entropía.

Los coeficientes de transformación cuantificados se decodifican por entropía, se descuantifican y se transforman inversamente para producir una aproximación del error residual en el lado del decodificador, que luego se agrega a la predicción con compensación de movimiento para generar la reconstrucción. La descripción de alto nivel del códec se muestra en la siguiente imagen.

El resto de la sección discutirá las nuevas mejoras en WMV-9 que lo diferencian del resto de las soluciones de codificación de video como los estándares MPEG. WMV-9 tiene tramas intra (I), predichas (P) y predichas bidireccionalmente (B). Los intraframes son aquellos que se codifican de forma independiente y no dependen de otros frames. Los fotogramas predichos son fotogramas que dependen de un fotograma en el pasado. La decodificación de un cuadro predicho puede ocurrir solo después de que se hayan decodificado todos los cuadros de referencia anteriores al cuadro actual a partir del cuadro más reciente (I). Los marcos B son marcos que tienen dos referencias: una en el pasado temporal y otra en el futuro temporal. Los cuadros B se transmiten después de sus referencias, lo que significa que los cuadros B se envían desordenados para garantizar que sus referencias estén disponibles en el momento de la decodificación. Los fotogramas B en WMV-9 no se utilizan como referencia para fotogramas posteriores. Esto coloca los fotogramas B fuera del bucle de decodificación, lo que permite tomar atajos durante la decodificación de fotogramas B sin desviaciones ni artefactos visuales a largo plazo. La definición anterior de fotogramas I, P y B es válida tanto para secuencias progresivas como entrelazadas.

El rendimiento de los códecs de video se compara con su trama de distorsión de velocidad (RD). Es una curva 2-D que muestra la distorsión producida por la compresión a una determinada tasa de bits.

WMV-9 ha abordado este problema con la introducción de una variedad de técnicas que se enumeran a continuación:

1. Transformación de tamaño de bloque adaptable

2. Conjunto de transformación de precisión limitada

3. Compensación de movimiento

4. Cuantización y descuantificación

5. Codificación de entropía avanzada

6. Filtrado de bucles

7. Codificación avanzada de cuadros B

8. Codificación entrelazada

9. Suavizado de superposición

10. Herramientas de bajo costo

11. Compensación de desvanecimiento

## Referencias ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)

