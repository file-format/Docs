{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo DTSX y las API que pueden crear y abrir archivos DTSX",
  "title" :"Formato de archivo DTSX - Archivo de configuración DTS de SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## ¿Qué es un archivo DTSX?

Un archivo con la extensión. Esto incluye las transformaciones y cualquier paso de procesamiento opcional que pueda ser necesario durante la transferencia de datos entre los puntos de origen y destino. SQL Server Integration Services (SSIS), un componente de Microsoft SQL Server, utiliza los archivos DTSX para identificar los pasos para el procesamiento de datos entre servidores de bases de datos. Los archivos DTSX se pueden abrir con Microsoft SQL Server 2019.

## Formato de archivo DTSX

El movimiento de datos entre servidores de bases de datos requiere reglas y pasos de procesamiento para garantizar la integridad de los datos durante esta operación. SSIS asegura que todas estas actividades, para mover y conformar datos de diferentes fuentes en una empresa, se lleven a cabo convenientemente. Ahí es donde entra DTSX que define las estructuras que utilizará SSIS para establecer los pasos donde se pueden procesar los datos a medida que sigue estos pasos.

El flujo de datos descrito por DTSX es como se muestra en la siguiente imagen.

{{< figure src="../DataFlowDTSX.png" alt="Flujo de datos DTSX" >}}

DTSX está basado en [XML](/es/web/xml/) y está documentado en [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd). La refactorización mejorada de DTSX XML es DTSX 2.0 que incluye nuevos atributos para las estructuras, el reemplazo de propiedades con nombre como atributos XML principales, especifica valores predeterminados para la mayoría de los valores de atributos y la ubicación de elementos repetidos dentro de un elemento principal. Las estructuras DTSX se describen utilizando estos [esquemas XML](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc) y el formato estructural es XML de texto claro.

## Referencias

* [Formato DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Formato DTSX 2 - Por Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

