{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Archivo de intercambio de datos LIDAR comprimido",
  "description":"Obtenga más información sobre el formato de archivo LAZ y las API que pueden crear y abrir archivos LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## ¿Qué es un Archivo LAZ?

El formato de archivo LAZ es una versión comprimida del formato de archivo LAS (Lidar LASer), que está diseñado específicamente para almacenar datos de nubes de puntos LIDAR. Los archivos LAZ conservan los mismos datos y estructura que los archivos LAS, pero emplean técnicas de compresión sin pérdidas para reducir el tamaño del archivo y al mismo tiempo preservar la fidelidad de los datos originales.

## Formato de archivo LAZ - Breve historia

El formato de archivo LAZ se desarrolló para abordar la creciente demanda de almacenamiento y transmisión eficientes de grandes conjuntos de datos LIDAR. Al comprimir archivos LAS, los archivos LAZ reducen significativamente su tamaño, lo que los hace más fáciles de administrar y transferir. La compresión se logra empleando una combinación de diferentes algoritmos, como codificación de entropía y codificación de longitud variable, para representar atributos de puntos lidar en una forma más compacta.

## Formato de archivo LAZ

A pesar de la compresión, los archivos LAZ conservan la capacidad de restaurar completamente los datos LAS originales sin pérdida de información. Esto significa que una vez que se descomprime un archivo LAZ, se puede procesar y analizar de la misma manera que un archivo LAS sin comprimir. El proceso de compresión y descompresión generalmente se realiza utilizando software o bibliotecas especializadas que admitan el formato LAZ.

El formato de archivo LAZ mantiene la compatibilidad con los archivos LAS, lo que garantiza la interoperabilidad entre el software LIDAR y las herramientas de procesamiento. Esto significa que las aplicaciones que pueden leer y procesar archivos LAS normalmente pueden manejar archivos LAZ sin ninguna modificación. Además, los archivos LAZ todavía incluyen el encabezado del archivo, registros de longitud variable (VLR) y registros de datos de puntos, preservando la misma estructura que los archivos LAS.

## Ventajas del formato de archivo LAZ

**Tamaño de archivo reducido:** La compresión LAZ reduce significativamente el tamaño de archivo de los conjuntos de datos LIDAR, haciéndolos más manejables y fáciles de almacenar y transferir.

**Integridad de los datos:** La compresión LAZ no tiene pérdidas, lo que significa que los datos descomprimidos son una réplica exacta de los datos LAS originales, lo que garantiza que no haya pérdida de información ni precisión.

**Interoperabilidad:** Los archivos LAZ son compatibles con los archivos LAS, lo que permite una integración perfecta con el software LIDAR y los flujos de trabajo existentes.

**Procesamiento eficiente:** Debido a su tamaño reducido, los archivos LAZ se pueden cargar y procesar más rápidamente, lo que mejora los tiempos generales de procesamiento y análisis.

El formato de archivo LAZ ha sido ampliamente adoptado en la comunidad lidar como estándar para el almacenamiento e intercambio de datos lidar comprimidos. Ofrece un equilibrio entre la compresión de datos eficiente y la integridad de los datos, lo que permite un manejo más sencillo de grandes conjuntos de datos LIDAR manteniendo al mismo tiempo la precisión y la calidad de los datos originales.

## Referencias

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
