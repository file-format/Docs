{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo MK3D",
  "keywords" :[ "mk3d", "video matroska", "formato mkv", "3d estereoscópico", "StereoMode", "video", "archivo", "formato" ],
  "description":"Obtenga más información sobre el formato de archivo MK3D para videos 3D estereoscópicos creados por Matroska y las API que pueden crear y abrir archivos MK3D",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## ¿Qué es un archivo MK3D? ##

Los archivos MK3D pertenecen a la familia de formatos de video Matroska. Estos archivos son en realidad **videos estereoscópicos en 3D** creados con el formato Matroska 3D. El contenedor de archivos MKV utiliza el valor de un campo StereoMode para definir el tipo de material de video 3D estereoscópico. También está disponible un valor StereoMode para mostrar los videos 3D estéreo antiguos separando los colores cian y rojo (AnaGlyph)

## Detalles técnicos ##
Los videos 3D se pueden comprimir de las siguientes dos maneras:

- Pista separada para cada ojo.
- Combine cada seguimiento ocular en una sola pista.

El contenedor de archivos MKV es compatible con ambos.

Para los videos de una sola pista que son más fáciles con el material 3D dentro de ellos, debe configurar el campo **StereoMode** que decide si los planos se ensamblan en la pista mono o izquierda derecha combinada. Puede utilizar uno de los siguientes valores de campo StereoMode:

|Valor | Descripción |
|---|---|
|0| mono|
|1| uno al lado del otro (el ojo izquierdo es el primero) |
|2| arriba-abajo (el ojo derecho es el primero)|
|3| arriba-abajo (el ojo izquierdo es el primero)|
|4| tablero de ajedrez (la derecha es la primera) |
|5| tablero de ajedrez (la izquierda es la primera) |
|6| fila intercalada (la derecha es la primera)|
|7| fila intercalada (la izquierda es la primera) |
|8| columna intercalada (la derecha es la primera)|
|9| columna intercalada (la izquierda es la primera) |
|10| anaglifo (cian/rojo)|
|11| uno al lado del otro (el ojo derecho es el primero) |
|12| anaglifo (verde/magenta)|
|13| ambos ojos entrelazados en un bloque (el ojo izquierdo es el primero) (modo secuencial de campo) |
|14| ambos ojos entrelazados en un bloque (el ojo derecho es el primero) (modo secuencial de campo) |

Para las pistas múltiples, el contenedor MKV debe decidir la funcionalidad de cada pista por separado. **TrackOperation** con **TrackCombinePlanes** se utilizan para hacer el trabajo.


## Referencias ##

- [Notas de especificaciones de Matroska] (https://www.matroska.org/technical/notes.html)
- [Soporte de contenedor de archivos MKV para video 3D estéreo y archivos MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- archivos/)

