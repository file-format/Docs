{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC: lenguaje de definición de informes del lado del cliente",
  "keywords" :[ "rdlc", "lenguaje de definición de informe", "formato mkv", "XSD", "lenguaje de definición de informe del lado del cliente"],
  "description":"Obtenga más información sobre el formato de archivo RDLC, que es una representación XML de una definición de informe de SQL Server Reporting Services",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## ¿Qué es un archivo RDLC? ##

El RDLC significa Report Definition Language Client side. En realidad, es una extensión del archivo de informe creado mediante el uso de la tecnología de informes de Microsoft. La versión de SQL Server 2005 del Diseñador de informes se utiliza para crear estos archivos. El control **ReportViewer** en el lado del cliente puede ejecutar directamente los informes RDLC.

## Archivos RDL VS RDLC
|Archivos .rdl |Archivos .rdlc|
---|---|
|Los archivos RDL los crea la versión SQL Server 2005 del Diseñador de informes|Los archivos RDLC los crea la versión Visual Studio 2005 del Diseñador de informes|
|Se usa en SQL Server Reporting Services|Se usa en Visual Studio|
|Es un reporte remoto|Es un reporte local|
|Se necesita una instancia de Reporting Services para ejecutarlo|No se necesita una instancia de Reporting Services|

## Creación de archivos de definición de informe de cliente (.rdlc)
El control ReportViewer se usa para ejecutar archivos de definición de informe de cliente (.rdlc) usando la capacidad de procesamiento integrada del control. Los informes de clientes que ejecuta en el modo de procesamiento local se pueden crear fácilmente en su proyecto de aplicación. Los siguientes son los enfoques para crear el informe:

- Utilice el **Asistente de informes** para crear una nueva definición de informe de cliente (.rdlc).

- Cree un nuevo archivo de definición de informe de cliente (.rdlc) mediante Visual Studio.

- Generar una definición de informe mediante programación.


Solo puede obtener una vista previa de un informe ejecutándolo en un control **ReportViewer**. Tenga en cuenta que puede abrir y editar la definición del informe en cualquier momento y luego compilar o implementar la aplicación para verificar los resultados.

## Referencias ##

- [Creación de archivos de definición de informe de cliente (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

