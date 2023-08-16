{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Archivo", "Extensión", "Formato de archivo", "Formato de video", "Video TrueMotion", "VPX", "Tecnologías On2"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - Archivo de vídeo TrueMotion",
  "description":"Obtenga información sobre el formato de archivo VP9 y las API que pueden crear y abrir archivos VP9",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## ¿Qué es un archivo VP9?

Google ha desarrollado el códec VP9 como un estándar de codificación de video de código abierto y libre de regalías como sucesor de VP8. Originalmente fue diseñado para comprimir el contenido ultra HD en YouTube porque expande y mejora la eficiencia de codificación de su predecesor. Si hablamos de los códecs VPX originales, provienen de On2 Technologies, que fue asimilado por Google en 2010. Google luego abrió el código del códec. Ambos formatos, VP8 y VP9, están disponibles bajo una licencia BSD gratuita que permite a los operadores organizar competencias de codificación o decodificación tanto en software exclusivo como en software de código abierto sin revelar su código fuente.

## Características técnicas de VP9

* VP9 proporciona una resolución máxima de 8192x4352 a hasta 120 fps y múltiples espacios de color, con Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 y sRGB
* La gama completa de casos de uso web y móvil, desde compresión de baja tasa de bits hasta ultra-HD de alta calidad, con soporte adicional para codificación de 10/12 bits y HDR, son totalmente compatibles con este formato.
* Puede disminuir las tasas de bits de video hasta en un 50% en comparación con otros
* Está preparado para transmisión adaptativa y es utilizado por YouTube y otros proveedores de video web conocidos.
* Los dispositivos Chrome, Opera, Edge, Firefox y Android, así como millones de televisores inteligentes, admiten la decodificación de este códec.
* Las resoluciones de video superiores a 1080p se modifican a través de VP9 y permiten la compresión sin pérdidas
* Diferentes espacios de color como Rec. 601, Rec. 709, rec. 2020, SMPTE-170, SMPTE-240 y sRGB son compatibles con VP9
* El video HDR que usa Hybrid Log-Gamma y Perceptual Quantizer también puede ser compatible con VP9


## Breve historia

* El desarrollo del códec de video VP9 comenzó en 2011 y su decodificador se agregó al navegador web Chromium en diciembre de 2012
* Su primera versión del navegador web Google Chrome se lanzó en febrero de 2013 y lanzó la decodificación en ese momento
* Google lanzó Chrome 29.0.1547 con soporte final VP9 en agosto de 2013
* En octubre de 2013, se agregó un decodificador VP9 instintivo a FFmpeg
* Mozilla agregó el sustento VP9 a Firefox en diciembre de 2013 en la versión 2 que luego se lanzó el 18 de marzo de 2014
 

## Trabajo de VP9

Por lo general, el video 4K aumenta la calidad de la imagen al hacer que píxeles específicos sean más pequeños, el códec VP9 y HEVC los hacen más grandes para reducir la tasa de bits y el tamaño del archivo. Si bien esto puede parecer contradictorio, el motor de codificación toma los píxeles más grandes y los convierte en una productividad de mejor resolución. El video de origen, que incluye cuadros de video, se codifica o comprime para crear un flujo de bits de video comprimido. Cada cuadro separado se divide primero en bloques de píxeles. Luego, los bloques se analizan en busca de despidos tridimensionales y se evalúan las conexiones secuenciales entre marcos para aprovechar las áreas que no se pueden cambiar. Estos se codifican a través de vectores de movimiento que aseguran las cualidades del bloque dado en el siguiente cuadro. La información residual se codifica utilizando una compresión binaria eficaz.

## Referencias

* [Wikipedia VP9](https://en.wikipedia.org/wiki/VP9)
* [Documentos web de MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Coco](https://www.coconut.co/)

