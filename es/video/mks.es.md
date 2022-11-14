{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MKS",
  "keywords" :[ "mks", "video matroska", "formato mkv", "archivo", "formato", "video"],
  "description":"Obtenga más información sobre el formato de archivo MKS para subtítulos creados únicamente por Matroska y las API que pueden crear y abrir archivos MKS",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## ¿Qué es un archivo MKS?

Los archivos MKS se conocen generalmente como archivos Matroska que solo contienen subtítulos. Si bien el Matroska es un contenedor de archivos general, evita guardar la información de formatos específicos. Dado que los subtítulos se utilizan en algunos de los contenedores de audio o video, Matroska está prestando atención para almacenar algunos formatos de subtítulos comunes. Ayuda a Matroska a ser consistente con la tasa de crecimiento. Debe seguir los puntos que se indican a continuación para almacenar los subtítulos en Matroska:

- Los “.mks”. la extensión será utilizada por el archivo Matroska (que contiene solo subtítulos).
- **CodecPrivate** se utiliza para almacenar toda la información relacionada con los códecs que es global para una transmisión completa.
- Elimine las marcas de tiempo de inicio y detención que se utilizan en un formato de almacenamiento nativo de marca de tiempo. En su lugar, utilice la marca de tiempo y la duración de los bloques.
- Puedes usar cualquier cosa con una capa transparente, incluido un video.

## Formatos de subtítulos comunes

Aquí hay algunas notas breves sobre los formatos de subtítulos más comunes almacenados en Matroska:

### Imágenes Subtítulos
El formato de subtítulos VobSub es el primer formato de subtítulos de imágenes que se importa a Matroska. Este formato se genera exportando los subtítulos desde un DVD. Las pistas deben separarse mientras se almacenan en Matroska si el VobSub consta de un conjunto de múltiples flujos.

### Subtítulos SRT
El SRT es el más simple y básico de todos los formatos de subtítulos. Consta de cuatro partes como se indica a continuación:
 



1. Un número que indica la secuencia del subtítulo.
2. Tiempo de aparición y desaparición de los subtítulos en la pantalla.
3. El subtítulo en sí.
4. Una línea en blanco para indicar el comienzo del siguiente subtítulo.
 



### Subtítulos SSA/ASS
Sub Station Alpha (SSA) es un formato de archivo utilizado por el popular editor de subtítulos SubStation Alpha. Los subtítulos de SSA son muy utilizados por fansubbers. Tiene la capacidad de mostrar funciones modernas, por ejemplo, karaoke, posicionamiento, estilo, etc.
 



### Subtítulos WebVTT
El Consorcio World Wide Web (W3C) desarrolló WebVTT, que se abrevia como "Formato de pistas de texto de video web". Este formato se utiliza para marcar recursos de seguimiento de texto externo en relación con el elemento HTML.

### Subtítulos de gráficos de presentación HDMV
El formato de subtítulos de gráficos de presentación HDMV (HDMV PGS) es una serie de mapas de bits y no podemos decirlo en absoluto. En otras palabras, puede decir que es solo una secuencia cronometrada de imágenes gráficas. Para extraer la información, convertir PGS a SRT es un proceso necesario.

### Subtítulos de texto HDMV
El texto HDMV se conoce como el formato de subtítulos de texto que se utiliza en Blu-rays. Matroska solo permite el conjunto de caracteres UTF-8 cuando almacena los subtítulos de TextST.

### Subtítulos de transmisión de video digital (DVB)
El formato de subtítulos DVB se introdujo para regular la transmisión y visualización de subtítulos en varios idiomas en las señales de televisión. Un formato de subtitulado típico también permitiría a cualquier espectador ver transmisiones subtituladas de DVB, sin importar cuál sea el fabricante de los sistemas de transmisión.


## Referencias ##

- [Subtítulos Matroska](https://www.matroska.org/technical/subtitles.html)

