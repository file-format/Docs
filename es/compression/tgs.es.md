{
  "date" : "2019-10-11",
  "keywords" :[ "archivo tgs", "formato de archivo tgs", "qué es un archivo tgs", "archivo", "ejemplo de tgs", "extensión de archivo tgs","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Formato de archivo de etiqueta animada de Telegram",
  "description":"Obtenga información sobre el formato de archivo TGS y las API que pueden crear y abrir archivos TGS",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## ¿Qué es un archivo TGS?

Un archivo con la extensión .tgs es un archivo de etiqueta animada que introdujo el servicio de mensajería multiplataforma, [Telegram](https://core.telegram.org/stickers#animated-stickers). Los usuarios de aplicaciones de mensajería utilizan pegatinas animadas para enviar contenido más mejorado y animado en los mensajes, a diferencia de los gráficos estáticos que son imágenes fijas. Telegram utilizó inicialmente el formato de archivo [WEBP](/es/image/webp/) para pegatinas de imágenes fijas. El formato de archivo TGS puede almacenar datos de animación en resoluciones más altas y un tamaño de archivo más pequeño en comparación con las pegatinas WEBP estáticas. Los archivos TGS se pueden abrir con aplicaciones como Telegram, 7-zip, Apple Archive Utility y Corel WinZip.

## Formato de archivo TGS

Telegram introdujo el formato de archivo TGS en julio de 2019 basado en la biblioteca Lottie. Un archivo TGS consta de texto [JSON](/es/web/json/) que se exporta desde una animación en Adobe After Effects. El texto JSON exportado se comprime con la compresión gzip, que reduce el tamaño del archivo. La información JSON sobre el archivo de texto se almacena en un archivo de texto que se convierte en la base de las altas tasas de compresión.

### Especificaciones de las pegatinas TGS

El formato de archivo TGS impone ciertas limitaciones en la creación de pegatinas animadas TGS. Un archivo animado TGS:

* El tamaño de la etiqueta/lienzo debe ser de 512х512 píxeles.
* Los objetos adhesivos no deben salir del lienzo.
* La duración de la animación no debe exceder los 3 segundos.
* Todas las animaciones deben estar en bucle.
* El tamaño de la etiqueta no debe exceder los 64 KB después de renderizar en Bodymovin.
* Todas las animaciones deben ejecutarse a 60 fotogramas por segundo.

### Ejemplo de texto TGS JSON

Una etiqueta animada de muestra, cuando se descomprime, contiene el siguiente contenido de texto JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Referencias ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

