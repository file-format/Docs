{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Diseño de página de informe",
  "keywords" :[ "rpl", "Diseño de página de informe", "XSD", "SQL Server", "informes"],
  "description":"Obtenga más información sobre el formato de transmisión RPL, que es un formato binario interno utilizado por Microsoft SQL Server Reporting Services cuando se comunica con los controles de visualización",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## ¿Qué es un archivo RPL? ##

El formato de flujo RPL (Diseño de página de informe) es un formato binario interno utilizado por MS SQL Server Reporting Services cuando se pone en contacto con los controles del visor para reducir parte del trabajo de representación del servidor al control del visor del cliente. Los desarrolladores pueden crear diseñadores de informes personalizados mediante el uso de RPL, que generará RPL, así como procesadores de informes personalizados que procesan y muestran el archivo RPL para mostrar informes.

## Estructuras RPL

Una secuencia RPL incluye estructura de secuencia, estructura de informe, propiedades de informe y enumeraciones. Cada estructura incluye lo siguiente:

- Una definición de la estructura.

- La gramática de la Forma de Backus-Naur Aumentada (ABNF) para la estructura.

- Un diagrama de bits de la estructura.

- Definiciones de todos los campos contenidos dentro de la estructura.

Aquí están las breves notas sobre algunas de las estructuras RPL:

### Estructura de flujo
La estructura de flujo consta de una serie de registros. Un registro contiene cero o más campos estructurados que contienen el diseño del informe.

#### Corriente RPL
El flujo RPL debe tener solo un registro de informe y el flujo debe ser una serie de registros binarios que mantengan la jerarquía del informe.

#### Registro
El registro es un bloque de construcción básico que se utiliza para mantener la información sobre un informe. Un registro consta de una secuencia de bytes de longitud variable. Un registro consta de dos componentes:
- Un tipo de registro
- Los datos de registro que son específicos de ese tipo de registro.
El tipo de registro es un byte que define qué tipo de información especifica el registro y cómo se ordena y estructura la estructura de los datos del registro relacionados con el registro. El valor del registro depende del tipo de datos que es particular a ese registro.

#### Estructuras de tipos de datos simples

La siguiente tabla define los tipos de datos en un flujo RPL.

|Descripción| formato|
---|---|
|Char|Representa un valor numérico (ordinal) de 16 bits (2 bytes).|
|Byte|Representa un entero sin signo de 8 bits (1 byte).|
|Int16|Representa un entero con signo de 16 bits (2 bytes).|
|Único|Representa un valor de punto flotante de precisión simple de 32 bits (4 bytes).|
|Decimal|Representa un tipo de datos de 128 bits (16 bytes).|
|DateTime|Representa una codificación de 64 bits (8 bytes) de un valor de fecha y hora.|
|Int64|Representa un entero con signo de 64 bits (8 bytes).|
|Int32|Representa un entero con signo de 32 bits (4 bytes).|
|Flotante|Representa un valor de punto flotante de precisión simple de 32 bits (4 bytes).|
|Booleano|Representa un valor de tipo booleano lógico de 8 bits (1 byte). Los valores válidos son verdadero (1) y falso (0).|
|Largo|Representa un entero con signo de 64 bits (8 bytes).|
|String|Todos los valores de cadena dentro del protocolo DEBEN ser UNICODE UTF-16. De forma predeterminada, todos los valores de cadena comienzan con un número entero que define la longitud de la cadena. Los valores de cadena se representan en el protocolo como una matriz de bytes; el número de bytes DEBE ser igual al número de caracteres en la Cadena multiplicado por dos.|

### Estructuras de informes
Las estructuras del informe incluyen las definiciones y los tamaños de sus estructuras y elementos relevantes.

La siguiente lista especifica las estructuras del informe:

- Reporte
- Versión
- Propiedades del informe
- Elemento de matriz compensada
- Contenido de página
- Página
- Propiedades de la página
- Diseño de página
- Sección
- Sección sencilla
- Sección Mixta
- Propiedades de la sección
- Elemento de área del cuerpo
- Elemento de encabezado de página
- Elemento de pie de página
- Elemento del cuerpo
- Propiedades del elemento
- Propiedades de elementos compartidos
- Usar propiedades de elementos compartidos
- InlineSharedElementProperties
- Propiedades del elemento no compartido
- Estilo
- Propiedades de estilo compartido
- Propiedades de estilo no compartido
- Información de acción
- AcciónInfoContenido
- Acción
- ActionImageMapAreas
- Información de acción con mapas
- Datos de imagen dinámica
- ImageConsolidationOffsets
- Reportar articulo
- Línea
- Imagen
- Propiedades de datos de imagen
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- Propiedades de datos de imagen no compartida
- Datos de imagen
- ImageMapAreas
- ImageMapArea
- Cuadro
- Panel de indicadores
- Mapa
- Rectángulo
- Subinforme
- Cuadro de texto enriquecido
- Contenido del párrafo
- Ejecutar texto
- Párrafo
- RichTextBoxStructure
- Tablix
- Contenido de Tablix
- Estructura Tablix
- TablixMedidas
- Anchos de columnas
- Información de columna
- Alturas de fila
- FilaInfo
- Tablix Fila
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Mediciones
- Medida
- ReportElementEnd

### Propiedades
A continuación se muestra la lista de propiedades que se pueden utilizar en un flujo RPL:

- IDENTIFICACIÓN
- Número de columnas
- Espaciado de columnas
- Nombre único
- Nombre
- Etiqueta
- Marcador
- Información sobre herramientas
- ToggleItem
- Descripción
- Ubicación
- ConsumeContainerWhiteSpace (RPL 10.6)
- Idioma
- Tiempo de ejecución
- Autor
- Autorefrescar
- Reportar nombre
- Altura de la página
- Ancho de página
- Margen superior
- Margen Izquierdo
- Margen Derecho
- Margen inferior
- Columnas
- Nombre de página (RPL 10.6)
- Inclinación
- Puede crecer
- CanShrink
- Valor
- Estado de alternancia
- Puede Ordenar
- Ordenar Estado
- Fórmula
- EsToggleParent
- Código de tipo
- Valor original
- Es simple
- Compensación de contenido
- Nombre de la corriente
- Dimensionamiento
- LinkToChild
- ImprimirEnPrimeraPágina
- Imprimir entre secciones (RPL 10.4)
- FormattedValueExpressionBased
- Procesado con error
- ImagenMIMETipo
- Nombre de la imágen
- Ancho
- Altura
- Resolucion horizontal
- Resolución vertical
- Formato sin formato
- Hipervínculo
- MarcadorEnlace
- ID de obtención de detalles
- URL de obtención de detalles
- Color del borde
- BorderColorLeft
- BordeColorDerecho
- BordeColorSuperior
- BordeColorInferior
- Estilo de borde
- Estilo de borde izquierdo
- Estilo de borde derecho
- Estilo de borde superior
- Estilo de borde inferior
- Ancho del borde
- Ancho del borde izquierdo
- Ancho del borde derecho
-AnchoBordeSuperior
- Ancho del borde inferior
- Relleno a la izquierda
- Relleno Derecho
- Acolchado superior
- Fondo acolchado
- Estilo de fuente
- Familia tipográfica
- Tamaño de fuente
- Peso de la fuente
- Formato
- Decoración de texto
- Texto alineado
- VerticalAlign
- Color
- Altura de la línea
- Dirección
- Modo de escritura
-UnicodeBiDi
- Imagen de fondo
- Color de fondo
- FondoRepetir
- NumeralLanguage
- NumeralVariant
- Calendario
- Filas de encabezado de columna
- FilaEncabezadoColumnas
- ColsBeforeRowHeader
- DiseñoDirección
- DefiniciónRuta
- Nivel
- Índice de celda de miembro
- Desplazamiento de elemento de celda
- ColSpan
- Intervalo de filas
- Índice de definición
- Índice de columna
- índice de fila
- Etiqueta de grupo
- RecursiveToggleLevel
- Estilo de lista
- Nivel de lista
- Número de párrafo
- Sangría derecha
- sangría izquierda
- Sangría colgante
- EspacioAntes
- EspacioDespués
- Primera linea
- Margen
- ContenidoArriba
- Contenido a la izquierda
- Ancho de contenido
- Altura del contenido
- Estado
- CellItemState
-MiembroDefState

### Enumeraciones
La siguiente lista muestra las enumeraciones que se pueden usar en la secuencia RPL:

- Opciones de clasificación
- Tallas
- Tipo de forma
- Formato de imagen sin formato
- Estilos de fuente
- Pesos de fuente
- Decoraciones de texto
- Alineaciones de texto
- Alineaciones verticales
- Direcciones
- Modos de escritura
- UnicodeBiDiTipos
- Calendarios
- Estilos de borde
- Tipos de repetición de fondo
- Estilos de lista
- Estilos de marcado
- Código de tipo
- valores de estado
- TablixMemberStateValues
- TablixMemberDefStateValues
- Tamaño RPL





## Referencias ##

- [Formato de flujo binario de diseño de página de informe (RPL)] (https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

