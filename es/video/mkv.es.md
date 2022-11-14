{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MKV",
  "keywords" :[ "mkv", "video matroska", "formato mkv", "cómo reproducir archivos mkv", "video", "archivo", "formato" ],
  "description":"Obtenga información sobre el formato de archivo MKV y las API que pueden crear y abrir archivos MKV",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## ¿Qué es un archivo MKV? ##

MKV (Matroska Video) es un contenedor multimedia similar al formato [MOV](/es/video/mov/) y [AVI](/es/video/avi/), pero admite más de una pista de audio y subtítulos en el mismo archivo. Un archivo MKV es el formato de contenedor multimedia de Matroska que se usa para video. MKV se basa en Extensible Binary Metal Language y admite varios formatos de compresión de video y audio. La principal diferencia entre MKV y otros formatos de video es que MKV es un contenedor y no un códec. Los archivos MKV se guardan con la extensión de archivo .mkv. MKV puede incorporar audio, video y subtítulos en un solo archivo, incluso si esos elementos usan diferentes tipos de codificación. Por ejemplo, podría tener un archivo MKV que contenga video H.264 y MP3 o AAC para audio. MKV también admite descripciones, clasificaciones, carátulas e incluso puntos de capítulo. Hay varias características clave que MKV está preparado para el futuro. Estas características incluyen:

- Soporte para búsqueda rápida.
- Posibilidad de seleccionar diferentes flujos de audio y video.
- Soporte para subtítulos (codificados de forma rígida y codificada por software).
- Soporte para metadatos, capítulos y menús.
- Capacidad para transmitir en línea.
- Capacidad para recuperar archivos erróneos que brindan la capacidad de reproducir archivos dañados.

## Breve historia ##

El archivo MKV se originó en 2002 en Rusia. El desarrollador principal fue Lasse Kärkkäinen, quien trabajó con el fundador de Matroska, Steve Lhomme, y un equipo de programadores. MKV se desarrolló como un proyecto de estándares abiertos, lo que significa que es de código abierto y de uso gratuito. Con el paso del tiempo, el formato se mejoró y se convirtió en la base del formato multimedia WebM en 2010.

## Diseño Matroska ##

Matroska agrega las siguientes restricciones a la especificación EBML.

- El **docType** del **Encabezado EBML** debe ser 'matroska'.
- El **EBMLMaxIDLength** del **EBML Header** debe ser 4.
- La **EBMLMaxSizeLength** del **EBML Header** debe estar entre 1 y 8 (inclusive).

Todos los elementos de nivel superior están codificados en 4 octetos.

- Códigos de idioma: Matroska (versión 1 a 3) usó códigos de idioma que pueden ser la forma bibliográfica ISO-639-2 de 3 letras (como "fre" para francés), o se puede usar un código de país adicional como "fre-ca " para el francés canadiense. A partir de la versión 4 de Matroska, se PUEDE utilizar ISO 639-2 o BCP 47 para los códigos de idioma, aunque se recomienda BCP 47.
- Tipos físicos: estos tienen un significado diferente para los archivos de audio y video. Por ejemplo, ChapterPhysicalEquiv = 60 significa (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) para audio y (DVD / VHS / LASERDISC) para video.
- Estructura del bloque - Encabezado del bloque: el encabezado del bloque contiene información sobre el número de pista, las marcas de tiempo, el tipo de enlace, etc.
- Lacing: Es un mecanismo para ahorrar espacio al almacenar datos que normalmente se usa para pequeños bloques de datos (frames). Hay 3 tipos de cordones:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Estructura de bloque simple: se inspira en la **estructura de bloque**, con la diferencia principal de agregar indicadores de **Fotograma clave** y **Desechable**. Aparte de eso, todo es igual.

## Estructura Matroska ##

Un documento Matroska debe estar compuesto por al menos un **Documento EBML** utilizando el **Tipo de documento Matroska**. Cada **Documento EBML** debe comenzar con un **Encabezado EBML** seguido del **Elemento raíz EBML** que se define como un Segmento. Matroska define varios Elementos de nivel superior que pueden ocurrir dentro del **Segmento**.

EBML utiliza un sistema de elementos para componer un documento EBML. La siguiente es la lista de elementos de nivel superior en el archivo Matroska:

- **Documento EBML**: Wrapper para todo el archivo.
- **Encabezado EBML**: Contiene la información del encabezado para el archivo como DocType.
- **Segmento**: el elemento superior que contiene todos los demás elementos de nivel superior.
- **SeekHead**: Contiene la posición de Segmentos de otros Elementos de Nivel Superior.
- **Info**: Contiene información general sobre el Segmento.
- **Pistas**: un elemento de información de nivel superior con muchas pistas descritas.
- **Capítulos**: Se utiliza para definir menús básicos y particionar datos.
- **Cluster**: El elemento de nivel superior que contiene la estructura de bloque.
- **Cues**: un elemento de nivel superior que contiene todas las entradas locales al segmento que aceleran la búsqueda de acceso.
- **Archivos adjuntos**: contiene archivos adjuntos.
- **Etiquetas**: este elemento contiene metadatos que describen pistas, ediciones, capítulos, archivos adjuntos o el segmento como un todo.

La siguiente tabla muestra la estructura del documento Matroska con la mayoría de los elementos mostrados en una jerarquía:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Encabezado EBML | | | |
| Segmento | Cabeza de búsqueda | Buscar | ID de búsqueda |
| | | | Posición de búsqueda |
| | Información | UID de segmento | |
| | | Nombre de archivo de segmento | |
| | | AnteriorUID | |
| | | PrevNombre de archivo | |
| | | SiguienteUID | |
| | | SiguienteNombre de archivo | |
| | | SegmentoFamilia | |
| | | CapítuloTraducir | |
| | | Escala de marca de tiempo | |
| | | Duración | |
| | | FechaUTC | |
| | | Título | |
| | | Aplicación Muxing | |
| | | aplicación de escritura | |
| | Pistas | Entrada de pista | Número de pista |
| | | | TrackUID |
| | | | Tipo de pista |
| | | | Nombre |
| | | | Idioma |
| | | | ID de códec |
| | | | CódecPrivado |
| | | | Nombre de códec |
| | | | Vídeo | BanderaEntrelazada |
| | | | | Orden de campo |
| | | | | Modo estéreo |
| | | | | Modo Alfa |
| | | | | Ancho de píxel |
| | | | | Altura de píxel |
| | | | | Ancho de visualización |
| | | | | Altura de visualización |
| | | | | Tipo de relación de aspecto |
| | | | | Color |
| | | | sonido | Frecuencia de muestreo |
| | | | | Canales |
| | | | | Profundidad de bits |
| | Capítulos | EdiciónEntrada | EdiciónUID |
| | | | EdiciónBanderaOculta |
| | | | EdiciónBanderaPredeterminado |
| | | | EdiciónBanderaPedido |
| | | | CapítuloÁtomo | Capítulo UID |
| | | | | UID de cadena de capítulo |
| | | | | InicioHoraCapítulo |
| | | | | Fin del tiempo del capítulo |
| | | | | CapítuloBanderaOculto |
| | | | | Visualización del capítulo | cadena de capítulos |
| | | | | | ChapIdioma |
| | Clúster | Marca de tiempo |
| | | Pistas silenciosas |
| | | Posición |
| | | Tamaño anterior |
| | | Bloque simple |
| | | Grupo de bloques |
| | | Bloque cifrado |
| | Señales | Punto de referencia | CueTime |
| | | | CueTrackPosiciones |
| | Archivos adjuntos | Archivo adjunto | Descripción del archivo |
| | | | Nombre de archivo |
| | | | FileMimeType |
| | | | UID de archivo |
| | | | Referencia de archivo |
| | | | ArchivoUsadoHoraInicio |
| | | | FileUsedEndTime |
| | Etiquetas | Etiqueta | Objetivos | Valor de tipo de destino |
| | | | | Tipo de destino |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAdjuntoUID |
| | | | Etiqueta simple | Nombre de etiqueta |
| | | | | Idioma de etiqueta |
| | | | | Etiqueta por defecto |
| | | | | cadena de etiquetas |
| | | | | EtiquetaBinario |
| | | | | Etiqueta simple |


### Uso de códecs ###

Si no desea un nuevo reproductor multimedia y prefiere usar su reproductor existente, deberá instalar algunos códecs (abreviatura de compresión/descompresión). Si bien la descarga de códecs es una opción válida, debe tener cuidado con la fuente ya que estos pueden contener malware.

## Referencias ##

- [Matroska por Wikipedia](https://en.wikipedia.org/wiki/Matroska)

