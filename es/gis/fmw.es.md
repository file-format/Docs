{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo FMW - Formato de archivo de banco de trabajo FME",
  "description":"Obtenga información sobre el formato de archivo FMW y las API que pueden crear y abrir archivos FMW",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## ¿Qué es un archivo FMW?

Un archivo FMW es un archivo de proyecto creado con el software FME Workbench (viene como parte de la suite FME Desktop) que se utiliza para la transformación de datos espaciales. Contiene configuraciones definidas por el usuario que se utilizan para la manipulación de datos espaciales, como conjuntos de datos de entrada, propiedades de traducción, proyecciones y configuraciones de salida. La configuración de manipulación de datos espaciales se almacena como un diseño visual y es fácil de editar y guardar nuevamente.

Puede abrir archivos FMW usando [Safe Software FME Desktop] (https://www.safe.com/fme/fme-desktop/).

## Formato de archivo FMW - Más información

Los archivos FMW se almacenan en el disco como archivos binarios y solo se pueden leer con el software FME Desktop. El software también puede leer datos de varios formatos de bases de datos relacionales y también es compatible con una variedad de formatos de datos.

### Datos breves de FMW

|Hecho|Valor|
---|---|
|Lector/Escritor|Lector|
|Nivel de licencia|Base|
|Dependencias|Ninguna|
|Tipo de conjunto de datos|Archivo|
|Tipo de función|Fijo|
|Extensiones de archivo típicas|.fmw|
|Soporte de traducción automática|Sí|
|Atributos definidos por el usuario|No|
|Soporte del sistema de coordenadas|No|
|Compatibilidad con colores genéricos|No|
|Índice espacial|No|
|Esquema requerido|No|
|Soporte de transacciones|No|
|Atributo de tipo de geometría|Ninguno|
|Soporte de codificación|No|

### Soporte de geometría FMW

|Geometría|¿Compatible?|
---|---|
|agregado|no|
|círculos|no|
|arco circular|no|
|polígono de dona|no|
|arco elíptico|no|
|puntos suspensivos|no|
|línea|no|
|ninguno|sí|
|punto|no|
|polígono|no|
|raster|no|
|sólido|no|
|superficie|no|
|texto|no|
|valores z|no|


## Referencias

* [Software seguro FME Desktop](https://www.safe.com/fme/fme-desktop/)
* [Datos breves de FMW](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)

