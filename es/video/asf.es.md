{
  "date" : "2021-02-15",
  "keywords" :[ "archivo asf", "formato de archivo asf", "qué es un archivo asf", "archivo", "ejemplo de asf", "extensión de archivo asf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Formato de archivo de sistemas avanzados",
  "description":"Obtenga información sobre el formato de archivo ASF y las API que pueden crear y abrir archivos ASF",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## ¿Qué es un archivo ASF?

Un archivo con extensión .asf es un formato de archivo multimedia para almacenar y reproducir flujos de medios digitales a través de la red. Es un formato de archivo contenedor que puede tener contenido de video y audio para transmitir en línea. Rara vez encontrará archivos ASF, y es más probable que encuentre archivos de Windows Media Audio ([WMA](/es/audio/wma/)) y Windows Media Video ([WMV](/es/video/wmv/)) que especifican archivos ASF tener contenido codificado con los códecs respectivos. Los archivos de medios de Windows se pueden crear y leer con el SDK de formato de Windows Media.

## Formato de archivo ASF

Un archivo ASF puede comprender múltiples flujos independientes o dependientes. Esto puede incluir múltiples flujos de audio para audio multicanal o múltiples flujos de video de tasa de bits. Las múltiples tasas de bits hacen que las secuencias sean adecuadas para la transmisión en diferentes anchos de banda. Además, las transmisiones en un archivo ASF pueden estar en formato comprimido o sin comprimir. La mejor compresión se logra con los códecs de la serie 9 de audio y video de Microsoft Windows Media. Las especificaciones completas del formato de archivo ASF están disponibles en [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Estructura de archivos de nivel superior ASF

Los archivos ASF contienen lógicamente tres tipos de objetos de nivel superior:

* `Objeto de encabezado`: obligatorio y debe colocarse al principio de cada archivo ASF
* `Objeto de datos`: obligatorio y debe seguir al objeto de encabezado
* `Objeto(s) de índice` - opcional, pero útil para proporcionar acceso aleatorio basado en el tiempo a los archivos ASF

La siguiente imagen muestra la estructura de archivos de nivel superior de los archivos ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Objeto de encabezado de nivel superior ASF

El objeto Header proporciona una secuencia de bytes bien conocida al principio de los archivos ASF y, opcionalmente, puede contener metadatos como información bibliográfica. Contiene toda la información necesaria para interpretar correctamente la información dentro del objeto de datos. El objeto de encabezado puede incluir varios objetos estándar que incluyen, entre otros:

* Objeto de propiedades de archivo: contiene atributos de archivo globales.
* Objeto de propiedades de flujo: define un flujo de medios digitales y sus características.
* Objeto de extensión de encabezado: permite agregar funciones adicionales a un archivo ASF manteniendo la compatibilidad con versiones anteriores.
* Objeto de Descripción del Contenido - Contiene información bibliográfica.
* Objeto de comando de script: contiene comandos que se pueden ejecutar en la línea de tiempo de reproducción.
* Objeto de marcador: proporciona puntos de salto con nombre dentro de un archivo.

El objeto de encabezado se representa utilizando la siguiente estructura:

|Nombre de campo |Tipo de campo |Tamaño (bits)|
---|---|---|
|Id. de objeto| GUID| 128|
|Tamaño del objeto| QPALABRA| 64|
|Número de objetos de encabezado| PALABRA D | 32|
|Reservado1| BYTE| 8|
|Reservado2| BYTE| 8|

#### Objeto de datos de nivel superior ASF

Todos los datos de medios digitales para un archivo ASF están contenidos en el objeto de datos y se almacenan en forma de paquetes de datos ASF. Cada paquete de datos tiene una longitud fija y contiene datos para uno o más flujos de medios digitales.

#### Objetos de índice de nivel superior ASF

Los objetos de índice de nivel superior de ASF tienen los dos tipos siguientes:

* `Objeto de índice simple`: contiene un índice basado en el tiempo de los datos de video en un archivo ASF. El intervalo de tiempo entre las entradas del índice es constante y se almacena en el objeto de índice simple.
* `Objeto de índice`: hace referencia al objeto de índice, el objeto de índice de objetos multimedia y el objeto de índice de código de tiempo, cuyos formatos son similares. Al igual que el objeto de índice simple, el objeto de índice indexa por tiempo con un intervalo de tiempo fijo, pero no se limita a transmisiones de video.

## Referencias

* [Formato de archivo ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Formato de archivo QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

