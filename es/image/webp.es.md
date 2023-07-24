{
  "date" : "2019-10-11",
  "keywords" :[ "archivo webp", "formato de archivo webp", "qué es un archivo webp", "archivo", "ejemplo de webp", "extensión de archivo webp","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP: formato de archivo de imagen rasterizado de Google",
  "description":"Obtenga información sobre el formato de archivo WEBP y las API que pueden crear y abrir archivos WEBP",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo WEBP?

WebP, presentado por Google, es un formato de archivo de imagen web rasterizado moderno que se basa en la compresión sin pérdida y con pérdida. Proporciona la misma calidad de imagen mientras reduce considerablemente el tamaño de la imagen. Dado que la mayoría de las páginas web utilizan imágenes como representación efectiva de los datos, el uso de imágenes WebP en las páginas web da como resultado una carga más rápida de las páginas web. Según Google, las imágenes sin pérdida de WebP son un 26 % más pequeñas en comparación con [PNG](/es/image/png/), mientras que las imágenes con pérdida de WebP son un 25-34 % más pequeñas que las imágenes [JPEG](/es/image/jpeg/) comparables. Las imágenes se comparan según el índice de similitud estructural (SSIM) entre WebP y otros formatos de archivo de imagen. WebP es un proyecto hermano del formato contenedor multimedia [WebM](https://en.wikipedia.org/wiki/WebM).

## Descripción general de las características de WebP ##

Las imágenes WebP utilizan el proceso de compresión basado en la predicción de píxeles de los bloques circundantes, lo que da como resultado que los píxeles se utilicen varias veces en un solo archivo. Admite imágenes animadas y se espera que admita más funciones en el futuro. Google ha puesto a disposición el código fuente [en línea](https://developers.google.com/speed/webp/download) de su codificador y decodificador para que se utilice cuando sea necesario. La imagen WebP proporciona soporte para:

* **Compresión con pérdida:** La compresión con pérdida se basa en la codificación de fotogramas clave [VP8](https://en.wikipedia.org/wiki/VP8). VP8 es un formato de compresión de video creado por On2 Technologies como sucesor de los formatos VP6 y VP7.
* **Compresión sin pérdidas:** El formato de compresión sin pérdidas es desarrollado por el equipo de WebP.
* **Transparencia:** el canal alfa de 8 bits es útil para imágenes gráficas. El canal alfa se puede usar junto con RGB con pérdida, una función que actualmente no está disponible con ningún otro formato.
* **Animación:** Admite imágenes animadas en color real.
* **Metadatos:** Puede tener metadatos EXIF y XMP (utilizados por cámaras, por ejemplo).
* **Perfil de color:** Puede tener un perfil ICC integrado.

La compresión WebP con pérdida usa codificación predictiva para codificar una imagen, el mismo método que usa el códec de video VP8 para comprimir fotogramas clave en videos. La codificación predictiva utiliza los valores de los bloques de píxeles vecinos para predecir los valores de un bloque y, a continuación, codifica solo la diferencia.

La compresión WebP sin pérdida utiliza fragmentos de imágenes ya vistos para reconstruir exactamente nuevos píxeles. También puede usar una paleta local si no se encuentra ninguna coincidencia interesante.

## Formato de archivo ##

El formato de archivo WebP se basa en el formato de documento RIFF (formato de archivo de intercambio de recursos). El contenedor WebP brinda soporte para funciones superiores a las que contienen solo una imagen codificada como un cuadro clave VP8. El elemento básico de un archivo RIFF es un fragmento que consta de:


|Campo|Descripción
---|---|
|Chunk FourCC: 32 bits|Código ASCII de cuatro caracteres utilizado para la identificación de fragmentos
|Tamaño del fragmento: 32 bits (uint32)|El tamaño del fragmento sin incluir este campo, el identificador del fragmento o el relleno
|Carga útil de fragmento: Bytes de tamaño de fragmento|La carga útil de datos. Si Chunk Size es impar, se agrega un solo byte de relleno ~-~- que debería ser 0 ~-~-
|ChunkHeader ('ABCD')|Se utiliza para describir el encabezado FourCC y Chunk Size de fragmentos individuales, donde 'ABCD' es el FourCC del fragmento. El tamaño de este elemento es de 8 bytes.

### Encabezado WebP ###

Un encabezado de archivo WebP es el siguiente:

* Encabezado RIFF: 32 bits que representan los caracteres ASCII 'R' 'I' 'F' 'F'
* Tamaño del archivo: 32 bits (uint32) que representan el tamaño del archivo en bytes a partir del desplazamiento 8. El valor máximo de este campo es 2^32 menos 10 bytes y, por lo tanto, el tamaño del archivo completo es como máximo 4 GiB menos 2 bytes. .
* 'WEBP': 32 bits que representan los caracteres ASCII 'W' 'E' 'B' 'P'

### Formato de archivo con pérdida ###

Las imágenes WebP utilizan el formato de archivo con pérdida si la imagen se basa en la codificación con pérdida y no requiere funciones avanzadas o ampliadas, como transparencia, animación, alfa, etc. Las imágenes con pérdida son más pequeñas y también son compatibles con las aplicaciones más antiguas.

El archivo WebP, en este caso, consta de:

* Encabezado de archivo WebP de 12 bytes
* Trozo VP8

La [Guía de formato y decodificación de datos VP8](https://tools.ietf.org/html/rfc6386) ilustra las especificaciones del formato de flujo de bits VP8.

### Formato de archivo sin pérdidas ###

Este diseño se utiliza cuando la imagen se basa en una codificación sin pérdidas y no se necesitan las funciones avanzadas proporcionadas por el formato externo. Sin embargo, es posible que las aplicaciones más antiguas no puedan leer dichos archivos.

El archivo WebP, en este caso, consta de:

* Encabezado de archivo WebP de 12 bytes
* Trozo VP8L

## Referencias ##

* [Referencia del desarrollador WebP - Por Google](https://developers.google.com/speed/webp/)
* [Formato de archivo WebP - Por Wikipedia](https://en.wikipedia.org/wiki/WebP)

