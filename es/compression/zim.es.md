{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ZIM - Archivo de archivo OpenZIM",
  "description":"Obtenga información sobre el formato de archivo ZIM y las API que pueden crear y abrir archivos ZIM",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## ¿Qué es un archivo ZIM? ##

Los archivos con la extensión .zim son archivos creados para almacenar contenido Wiki sin conexión. Se considera el formato de archivo abierto más adecuado para almacenar Wikipedia en un USB. Almacena contenidos del sitio en un formato compacto. Su nombre proviene de "Zeno IMproved", que era el formato de archivo anterior de Zeno. ZIM es mantenido por el proyecto [openZIM ](https://openzim.org/) patrocinado por Wikimedia CH y respaldado por la Fundación Wikimedia. Los archivos ZIM se pueden abrir con aplicaciones como Kiwix y ZIMReader. El proyecto OpenZIM ha alojado la implementación del formato de archivo ZIM en [Github](https://github.com/openzim) para la contribución de la comunidad OpenSource.

## Especificaciones del formato de archivo ZIM

El formato de archivo ZIM se desarrolló sobre [formato de archivo Zeno](https://openzim.org/wiki/Zeno_file_format) y no es compatible con versiones anteriores. Las especificaciones de formato del formato de archivo ZIM están [disponibles en línea](https://openzim.org/wiki/ZIM_file_format) de openZIM para referencia del desarrollador. OpenZIM ha proporcionado una implementación de código abierto de C++, [LibZim](https://openzim.org/wiki/Zimlib), para leer y escribir archivos ZIM.

El formato de archivo ZIM usa compresión LZMA2 para hacer que el contenido sea compacto.

{{< figure src="../ZIM_File_Format.jpeg" alt="Formato de archivo ZIM" >}}


### Encabezado ZIM

Un archivo ZIM comienza con un encabezado que está en el desplazamiento 0. Todos los componentes se basan en little-endian y todos los enteros son enteros sin signo, es decir, uint_16, uint_32, uint_64.

|Nombre de campo |Tipo| Desplazamiento| Longitud| Descripción|
---|---|---|---|---|
|númeromágico| entero| 0| 4| Número mágico para reconocer el formato del archivo, debe ser 72173914 (0x44D495A)|
|versiónprincipal| entero| 4| 2| Versión principal del formato de archivo ZIM (5 o 6)|
|versión menor| entero| 6| 2| Versión secundaria del formato de archivo ZIM |
|uuid| entero| 8| 16| identificación única de este archivo zim |
|número de artículos| entero| 24| 4| número total de artículos|
|recuento de clústeres| entero| 28| 4| número total de conglomerados|
|urlPtrPos| entero| 32| 8| posición de la lista de punteros de directorio ordenada por URL |
|títuloPtrPos| entero| 40| 8| posición de la lista de punteros de directorio ordenada por Título|
|clusterPtrPos| entero| 48| 8| posición de la lista de punteros de clúster |
|mimeListPos| entero| 56| 8| posición de la lista de tipos MIME (también tamaño del encabezado) |
|páginaprincipal| entero| 64| 4| página principal o 0xffffffff si no hay página principal |
|diseñoPágina| entero| 68| 4| página de diseño o 0xffffffffff si no hay página de diseño |
|sumadecomprobaciónPos| entero| 72| 8| puntero a la suma de comprobación md5 de este archivo sin la suma de comprobación en sí. Esto apunta siempre 16 bytes antes del final del archivo.|

## Referencias ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

