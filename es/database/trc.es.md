{
  "date" : "2021-08-24",
  "keywords" :[ "archivo trc", "formato de archivo trc", "qué es un archivo trc", "archivo", "ejemplo trc", "extensión de archivo trc","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo TRC y las API que pueden crear y abrir archivos TRC",
  "title" :"TRC: archivo de seguimiento de SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## ¿Qué es un archivo TRC?
Un archivo con extensión .trc contiene los resultados del seguimiento de la actividad de una base de datos del servidor Miscrosoft SQL. Estos archivos son creados por un software SQL Server Profiler; generalmente empaquetado con el software Microsoft SQL Server. Los administradores de la base de datos pueden analizar una secuencia de declaraciones de la base de datos y pueden revisar el registro de seguimiento si se sospecha algún tipo de error o advertencia. Estos archivos generalmente se encuentran en la carpeta LOG típica de MSSQL dentro del directorio Archivos de programa en un sistema operativo Windows.

## formato de archivo TRC
SQL Server Profiler utiliza el formato de archivo TRC para generar automáticamente un nuevo seguimiento de las declaraciones ejecutadas recientemente por el servidor MS SQL. SQL Server Profiler usa la plantilla predeterminada para cualquier seguimiento nuevo. Sin embargo, el software incluye varias plantillas predefinidas para monitorear ciertos tipos de eventos. Además, SQL Server Profiler se puede utilizar para crear plantillas que definen las clases de eventos y las columnas de datos que se incluirán en los seguimientos.

### Plantillas predefinidas
Aquí está la lista de algunas plantillas predefinidas incluidas en SQL Server Profiler:
- **SP_Counts**: captura el comportamiento de ejecución del procedimiento almacenado a lo largo del tiempo.
- **Estándar**: Punto de partida genérico para la creación de una traza.
- **TSQL**: captura todas las declaraciones de Transact-SQL que los clientes envían a SQL Server y la hora de emisión.
- **TSQL_Duration**: captura todas las declaraciones de Transact-SQL enviadas a SQL Server por los clientes, su tiempo de ejecución y las agrupa por duración.
- **TSQL_Grouped**: se usa para investigar consultas de un cliente o usuario en particular.
- **TSQL_Locks**: se utiliza para solucionar problemas de puntos muertos, tiempo de espera de bloqueo y eventos de escalada de bloqueo.
- **TSQL_Replay**: se utiliza para realizar ajustes iterativos, como pruebas comparativas.
- **TSQL_SPs**: se utiliza para analizar los pasos de los componentes de los procedimientos almacenados.
- **Ajuste**: se usa para generar resultados de seguimiento que el Asistente para la optimización del motor de base de datos puede usar como carga de trabajo para optimizar las bases de datos.
### Correlacionar un seguimiento con los datos del registro de rendimiento de Windows
SQL Server Profiler se puede usar para abrir un registro de rendimiento de Microsoft Windows, elegir los contadores para correlacionar con un seguimiento y mostrar los contadores de rendimiento seleccionados junto con el seguimiento en la GUI de MS SQL Server Profiler. Para indicar los datos de registro de rendimiento que se correlacionan con el evento de seguimiento seleccionado, una barra roja vertical en el panel de la ventana de datos del Monitor del sistema de SQL Server Profiler.


## Referencias ##

* [Perfilador de SQL Server](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

