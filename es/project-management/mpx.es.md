{
  "date" : "2019-10-11",
  "keywords" :[ "archivo mpx", "formato de archivo mpx", "qué es un archivo mpx", "archivo", "ejemplo mpx", "extensión de archivo mpx","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX: formato de archivo de intercambio de proyectos de Microsoft",
  "description":"Obtenga información sobre el formato de archivo MPX y las API que pueden crear y abrir archivos MPX",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## ¿Qué es un archivo MPX? ##

Un archivo con extensión .mpx es un formato de archivo de Microsoft Exchange. Microsoft Project (MSP) desarrolló un formato de archivo MPX para facilitar el intercambio de información de proyectos entre MSP y otras aplicaciones compatibles con el formato de archivo MPX, incluidas Primavera Project Planner, Sciforma y Timerline Precision Estimating. Con los archivos MPX, puede transferir todo tipo de información de un proyecto a un sistema diferente, como información detallada sobre la asignación de recursos, información del calendario o información del cuadro de diálogo Información del proyecto.

Microsoft Project 4.0 introdujo soporte para crear y leer formatos de archivo MPX que continuaron usándose hasta Microsoft Project 98. Sin embargo, el soporte para crear archivos MPX ha interrumpido el lanzamiento de Microsoft Project 2000, y las versiones hasta Microsoft Project 2010 solo admiten lectura MPX. El formato de archivo MPX no es compatible con versiones posteriores a MSP 2010.

## Formato de archivo MPX ##

En esta sección se proporciona una descripción general de las especificaciones del archivo MPX. Las especificaciones completas se pueden encontrar en esta [Base de conocimientos] (https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) artículo y se puede consultar para obtener más detalles.

### Registros ###

Un registro del archivo MPX consta de información para el proyecto. Hay diferentes tipos de registros donde cada registro tiene su propio orden. Cada tipo de registro se identifica por su número de registro. Para un archivo MPX, es necesario que contenga el tipo de registro Creación de archivos. Otros tipos de registros no son obligatorios. La siguiente tabla muestra todos los tipos de registro, sus números de registro y la cantidad de registros que cada tipo puede contener en el archivo MPX. La inclusión de registros en el archivo MPX debe seguir el orden de la tabla, con comentarios insertados en cualquier lugar.

|Nombre del registro|Número de registro|Número máximo de registros
---|---|---|
|Creación de archivo (requerido)|ninguno|1
|Configuración de moneda|10|1
|Configuración predeterminada|11|1
|Configuración de fecha y hora|12|1
|Definición de calendario base|20|250
|Horas calendario base|25| 7 por registro de definición de calendario base
|Excepción de calendario base|26| 250 por registro de definición de calendario base
|Encabezado del proyecto|30|1
|Definición de tabla de recursos de texto|140|1- (O puede usar el registro Definición de tabla de recursos numéricos)
|Definición de tabla de recursos numéricos|41|1
|Recurso|50|9,999
|Notas de recursos|51| 1 por registro de recurso
|Definición del calendario de recursos|55| 1 por registro de recurso
|Horas del calendario de recursos|56| 7 por calendario de recursos
|Excepción del calendario de recursos| 57|250 por calendario de recursos
|Definición de tabla de tareas de texto|60|1 (O puede usar el registro Definición de tabla de tareas numéricas)
|Definición de tabla de tareas numéricas|61|1
|Tarea|70|9
|Notas de tareas|71| 1 por registro de tarea
|Tarea recurrente|72| 1 por registro de tarea
|Asignación de recursos|75| 100 por registro de tarea
|Campos de grupo de trabajo de asignación|76| 1 por registro de asignación
|Nombres de proyectos|80|500
|Enlaces de cliente DDE y OLE|81|500
|Comentarios|0|ilimitado

### Estructura del archivo ###

Un archivo MPX consta de los registros mencionados anteriormente que se organizan de manera preestablecida dentro del archivo. Los detalles sobre estos tipos de registro se describen a continuación:

**Registro de Creación de Expediente (FCR):** Es un registro obligatorio cuyo propósito es identificar a:

* Formato de archivo (MPX)
* Carácter separador de lista utilizado en el archivo
* Programa y número de versión utilizados para crear el archivo
* Número de versión del formato de archivo MPX utilizado en el archivo
* Página de códigos utilizada para crear el archivo

Este debe ser el primer registro en el archivo. Al exportar desde Microsoft Project, el carácter separador de lista se especifica en el elemento Configuración regional en el Panel de control de Windows. Un registro FCR incluye los siguientes campos:

* MPX seguido inmediatamente por el carácter separador de lista
* Nombre/identificador del programa
* Número de versión del archivo
* Página de códigos (850, 437, MAC, ANSI)

Por ejemplo, el registro puede contener información **MPX, Microsoft Project, 3.0**, que especifica que se utiliza una coma como carácter separador de lista en este archivo MPX. La versión del formato MPX utilizado en el archivo se exporta desde Microsoft Project versión 3.0.

**Configuración de moneda** Este registro, que tiene el número de registro 10, especifica la configuración de las opciones de moneda en el cuadro de diálogo Opciones. Si no se incluye este registro, se utilizan las configuraciones actuales en el cuadro de diálogo Opciones. Los separadores de miles y decimales se especifican en el elemento Configuración regional en el Panel de control de Windows.
Los campos incluidos en este registro son:

* Símbolo de moneda
* Posición del símbolo (0 # después, 1 # antes, 2 # después con un espacio, 3 # antes con un espacio)
* Dígitos de moneda (0,1,2)
* Separador de miles
* Separador decimal

**Ejemplo:** 10,$,1,2,",",.
Este ejemplo especifica que los valores de moneda incluyen un signo de dólar ($) antes de ellos, que se incluyen dos dígitos después del punto decimal, que se usa una coma para separar miles y que se usa un punto como punto decimal. Debido a que el carácter separador de lista se incluye en el campo Separador de miles, el campo está entre comillas.

**Configuración predeterminada:** Este registro, que tiene el número de registro 11, especifica la configuración de las opciones predeterminadas en el cuadro de diálogo Opciones. Si no se especifica una duración, se debe establecer la Unidad de duración predeterminada para realizar los cálculos correctos de la unidad de duración. Si no se incluye este registro, se utilizan las configuraciones actuales en el cuadro de diálogo Opciones.
Los campos incluidos en este registro son:

* Unidades de duración predeterminadas (0 # minutos, 1 # horas, 2 # días, 3 # semanas)
* Tipo de duración predeterminado (0 # no fijo, 1 # fijo)
* Unidades de trabajo predeterminadas (0 # minutos, 1 # horas, 2 # días, 3 # semanas)
* Horas/día predeterminados
* Horas/semana predeterminadas
* Tarifa estándar predeterminada
* Tasa de horas extra predeterminada
* Actualización del estado de la tarea Actualizaciones del estado de los recursos (0 # no, 1 # sí)
* Dividir tareas en curso (0 # no, 1 # sí)

**Configuración de fecha y hora:** Este registro, que tiene el número de registro 12, especifica la configuración para las opciones de fecha y hora en el cuadro de diálogo Opciones y la opción Formato de fecha de texto de barra en el cuadro de diálogo Diseño. Si no se incluye este registro, se utilizan las configuraciones actuales en el cuadro de diálogo Opciones.
\\Los campos incluidos en este registro son:

* Orden de fecha (0 # mes/día/año, 1 # día/mes/año, 2 # año/mes/día)
* Formato de hora (0 # 12 horas, 1 # 24 horas)
* Hora predeterminada (número de minutos después de la medianoche)
* Separador de fechas
* Separador de tiempo
* 0:00 a 11:59 Texto
* 12:00 a 23:59 Texto
* Formato de fecha (0 -14)*
* Formato de fecha de texto de barra (0 -194) *

**Definición de Calendario Base:** Estos registros, teniendo el número de registro 20, definen los calendarios base y sus días laborables y no laborables de la semana. La configuración predeterminada se utiliza si no hay ninguna entrada para un día. La configuración predeterminada es de lunes a viernes para los días laborables y los sábados y domingos para los días no laborables. En este registro, el campo Nombre es obligatorio. Para cada uno de los días, una entrada de 0 indica que el día es un día no laborable y una entrada de 1 indica que el día es un día laborable.
Los campos incluidos en este registro son:

* Nombre
* Domingo
* Lunes
* Martes
* Miércoles
* Jueves
* Viernes
* Sábado

**Horas de calendario base:** Estos registros, que tienen el número de registro 25, especifican las horas de trabajo para los días de la semana si difieren de la configuración predeterminada. El horario de trabajo predeterminado es de 8:00 a. m. a 12:00 p. m. y de 1:00 p. m. a 5:00 p. m. Cada registro de Horas de calendario base hace referencia al registro de Definición de calendario base anterior. Hasta siete de estos registros pueden seguir a cada registro de definición de calendario base.

* Día de la semana (1 - 7, donde 1 # domingo y 7 # sábado)
* Desde el Tiempo 1
* Hasta el Tiempo 1
* Desde el Tiempo 2
* Hasta el Tiempo 2
* Desde el Tiempo 3
* Hasta el Tiempo 3

**Excepción del calendario base:** Estos registros, que tienen el número de registro 26, definen las excepciones a los días y horas especificados en los dos tipos de registro anteriores. Hasta 250 de estos registros pueden seguir a cada registro de definición de calendario base. Estos registros deben enumerarse en orden cronológico. Si una excepción es un día, puede dejar el campo Hasta la fecha vacío. Si no se indica ningún horario, se utilizan los horarios predeterminados de 8:00 a. m. a 12:00 p. m. y de 1:00 p. m. a 5:00 p. m.
Los campos incluidos en este registro son:

* Partir de la fecha
* Hasta la fecha
* Sin trabajo/Trabajando (0 # no trabajando, 1 # trabajando)
* Desde el Tiempo 1
* Hasta el Tiempo 1
* Desde el Tiempo 2
* Hasta el Tiempo 2
* Desde el Tiempo 3
* Hasta el Tiempo 3

**Encabezado del proyecto:** este registro, que tiene un valor de registro de 30, establece campos de proyecto globales, como la fecha de inicio y la fecha de finalización del proyecto. Los campos de este registro corresponden a la información de los cuadros de diálogo Información del proyecto y Estadísticas.
Los campos y pestañas incluidos en este registro son:

* Pestaña de proyecto
* Compañía
* Gerente
* Calendario (Estándar utilizado si no hay entrada)
* Fecha de inicio (se calcula este campo o el campo siguiente para un archivo importado, según la configuración Programar desde)
* Fecha de finalización
* Programar desde (0 # inicio, 1 # fin)
* Fecha actual*
* Comentarios
* Costo
* Costo de referencia
* Costo real
* Trabajar
* Trabajo de referencia
* Trabajo actual
* Trabajar
* Duración*
* Duración de la línea de base*
* Duración real
* Porcentaje completo
* Comienzo de la línea de base
* Finalización de la línea de base
* Comienzo real
* Acabado real
* Variación de inicio
* Variación de acabado
* Tema
* Autor
* Palabras clave

**Definición de tabla de recursos de texto**: este registro enumera los campos de recursos, en orden, que se importan o exportan. Para los archivos importados, los nombres deben coincidir con los nombres de campo utilizados en Microsoft Project. Para los archivos exportados, este registro proviene de la tabla de exportación de recursos. Se debe utilizar este registro o el registro de definición de tabla de recursos numéricos. Al exportar desde Microsoft Project, se incluyen ambos registros.

**Definición de tabla de recursos numéricos:** Usando números en lugar de nombres, este registro enumera los campos de recursos, en orden, que se importan o exportan. Este es un método alternativo para identificar los campos de recursos incluidos en cada registro de recursos y es útil cuando se define un archivo MPX creado por un producto en un idioma extranjero.

**Recurso:** Estos registros contienen la información de cada recurso que se importa o exporta. Cada registro de recurso describe un recurso. Cuando importa información, los campos que se incluyen están definidos por el registro Definición de tabla de recursos de texto o el registro Definición de tabla de recursos numéricos. Cuando exporta información, los campos que se incluyen son los que se enumeran en la tabla de exportación de recursos.

**Notas de recursos:** Estos registros contienen notas sobre el registro de recursos inmediatamente anterior. Para una nueva línea dentro de la nota, se usa el carácter ASCII 127. Si la nota incluye el carácter separador de lista, encierre la nota entre comillas.

**Definición de calendario de recursos:** Estos registros definen los días hábiles para el recurso especificado en el registro de recursos inmediatamente anterior. Para los archivos importados, si no hay una entrada para el campo Nombre del calendario base, se usa Estándar. Ninguna entrada para el día específico indica que el día está establecido en el valor predeterminado (2). Si no hay registros de definición de calendario de recursos, se usa Estándar como calendario base para el recurso, con el uso predeterminado para los días. Para cada uno de los días, una entrada de 0 indica que el día es un día no laborable, 1 indica que el día es un día laborable y 2 especifica que se utiliza el valor predeterminado.

**Horas del calendario de recursos:** Estos registros definen las horas de trabajo del recurso que difieren del calendario base utilizado por el recurso. Estos registros se aplican al registro Definición de calendario de recursos que precede inmediatamente a este registro. Hasta siete de estos registros pueden seguir a cada registro de definición de calendario de recursos.

**Excepción del calendario de recursos:** Estos registros definen las excepciones a los días y horas especificados en los dos tipos de registros anteriores. Hasta 250 de estos registros pueden seguir a cada registro de definición de calendario de recursos. Estos registros deben enumerarse en orden cronológico. Si la excepción es solo un día, puede dejar el campo Hasta la fecha vacío. Si no se indica ningún horario, se utilizan los horarios predeterminados de 8:00 a. m. a 12:00 p. m. y de 1:00 p. m. a 5:00 p. m.

**Definición de tabla de tareas de texto:** Este registro enumera los campos de tareas, en orden, que se importan o exportan. Para los archivos importados, los nombres deben coincidir con los nombres de campo utilizados en Microsoft Project. Si el archivo se está exportando, este registro proviene de la tabla Exportar de la tarea. Al exportar desde Microsoft Project, se incluyen ambos registros. Los campos calculados por Microsoft Project, como Inicio programado y Fin programado, se ignoran si se importan. Si tiene fechas de inicio o finalización de tareas fijas, utilice los campos Tipo de restricción y Fecha de restricción.

**Definición de tabla de tareas numéricas:** Usando números en lugar de nombres, este registro enumera los campos de tareas, en orden, que se importan o exportan. Este es un método alternativo para identificar los campos de tareas incluidos en cada registro de tareas y es útil cuando se define un archivo MPX creado por un producto en un idioma extranjero.

**Tarea:** Estos registros contienen la información de cada tarea que se importa o exporta. Cada registro de Tarea describe una tarea. Cuando importa información, los campos que se incluyen están definidos por el registro Definición de tabla de tareas de texto o el registro Definición de tabla de tareas numéricas. Cuando exporta información, los campos que se incluyen son los que se enumeran en la tabla Exportar tarea.

**Notas de la tarea:** Estos registros contienen notas sobre el registro de la tarea inmediatamente anterior. Use el carácter ASCII 127 para indicar una nueva línea dentro de la nota. Si la nota incluye el carácter separador de lista, encierre la nota entre comillas.

**Asignación de recursos**: estos registros enumeran información sobre los recursos asignados a la tarea que se definió en el registro de tareas anterior. Si está fusionando archivos y desea conservar la información de asignación de recursos, debe incluir la información en el archivo MPX. Si fusiona, se eliminarán todas las asignaciones existentes en las tareas fusionadas. Si está fusionando archivos en función de los ID únicos, los recursos se asignan utilizando los ID únicos de recursos en lugar de los ID.

**Campos de grupo de trabajo de asignación de recursos:** Estos registros enumeran la información que se almacena con cada asignación para las funciones de grupo de trabajo de Microsoft Project 4.0 y 4.1. Si utiliza las funciones del grupo de trabajo, debe incluir este registro para asegurarse de que no se pierda ninguna información.

**Nombres de proyectos:** Estos registros enumeran todos los nombres de enlaces DDE almacenados en el proyecto.

**Enlaces de cliente DDE y OLE:** Estos registros enumeran los enlaces DDE en el proyecto.

**Comentarios:** Estos registros se pueden usar para agregar comentarios al archivo y pueden aparecer en cualquier posición del archivo. Cada registro de comentarios debe comenzar con un "0".

## Problemas para abrir un archivo MPX ##

Aquí está la lista de algunos problemas comunes que pueden surgir y causar un mal funcionamiento del formato MPX:

* Ausencia de software de soporte
* Archivo dañado
* Archivo infectado por virus
* Sin derecho de acceso en el sistema para abrir los archivos
* Unidad obsoleta en su sistema
* Se renombra la extensión del archivo

## Referencias ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

