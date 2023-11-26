{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Formato de archivo Lidar LASer",
  "description":"Obtenga más información sobre el formato de archivo LAS y las API que pueden crear y abrir archivos LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## ¿Qué es un archivo LAS?

El formato de archivo LAS (Lidar LASer) es un formato de archivo binario diseñado específicamente para almacenar datos de nubes de puntos LIDAR. Fue desarrollado y mantenido por la Sociedad Estadounidense de Fotogrametría y Teledetección (ASPRS) como un formato estandarizado para el intercambio e interoperabilidad de datos LIDAR.

Los archivos LAS almacenan información detallada sobre puntos LIDAR individuales, incluidas sus coordenadas 3D (x, y, z), valores de intensidad, códigos de clasificación y atributos adicionales. El formato admite datos LIDAR de forma de onda completa y de retorno discreto, lo que permite el almacenamiento de múltiples retornos por pulso láser.

## Formato de archivo LAS

La estructura de un archivo LAS consta de tres secciones principales: el encabezado del archivo, los registros de longitud variable (VLR) y los registros de datos de puntos.

1. Encabezado del archivo: el encabezado del archivo contiene información esencial sobre el archivo LAS, como la versión del formato de datos, el formato de datos de puntos, el número de puntos, las coordenadas del cuadro delimitador, el sistema de referencia de coordenadas (CRS) y otros metadatos. Proporciona un resumen de los datos LIDAR contenidos en el archivo.

2. Registros de longitud variable (VLR): los VLR son opcionales y pueden almacenar metadatos adicionales e información personalizada sobre los datos lidar. Los VLR permiten flexibilidad a la hora de ampliar el formato para adaptarse a los requisitos específicos del usuario. Los ejemplos de VLR incluyen información sobre el sistema de sensores, parámetros de procesamiento de datos o esquemas de clasificación.

3. Registros de datos de puntos: Los registros de datos de puntos almacenan las mediciones LIDAR reales. Cada registro de datos de puntos representa un único punto LIDAR y contiene atributos como coordenadas x, y, z, valores de intensidad, códigos de clasificación (p. ej., suelo, vegetación, edificios) y otros atributos definidos por el usuario. Los registros de puntos también pueden almacenar marcas de tiempo, recuentos de retorno y ángulos de escaneo.

Los archivos LAS admiten diferentes formatos de datos (0 a 10) para adaptarse a varios tipos de datos LIDAR y el nivel de información necesario. Por ejemplo, el formato 0 representa un formato de puntos simple con información básica, mientras que los formatos 1 a 3 proporcionan datos más completos que incluyen información de forma de onda para cada retorno.

Los archivos LAS son ampliamente compatibles con el software y las herramientas de procesamiento LIDAR, lo que los convierte en un formato estándar para el intercambio y análisis de datos LIDAR. Además, los archivos LAS se pueden comprimir utilizando técnicas de compresión sin pérdidas para reducir el tamaño del archivo y al mismo tiempo preservar la fidelidad de los datos originales. La versión comprimida de los archivos LAS a menudo se conoce como LAZ, y ofrece capacidades eficientes de almacenamiento y transferencia de datos.

## Referencias

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
