{
  "date" : "2020-03-16",
  "keywords" :[ "Archivo IGES", "Formato de archivo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo IGES y las API que pueden crear y abrir archivos IGES",
  "title" :"Formato de archivo IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## ¿Qué es un archivo IGES?

Se utiliza un archivo con extensión .iges para intercambiar información de diseño entre aplicaciones de diseño asistido por computadora (CAD). IGES significa Especificaciones Iniciales de Intercambio de Gráficos. La información intercambiada mediante IGES incluye diagrama de circuito, estructura alámbrica, superficie de forma libre o representaciones de modelado sólido. IGES encuentra sus aplicaciones en dibujos de ingeniería tradicionales, análisis de modelos y funciones de fabricación. El formato puede intercambiar información de diseño 2D o 3D entre programas CAD. Los archivos IGES se pueden abrir con varias aplicaciones CAD como Autodesk y CADSoftTools ABViewer. También hay varias API disponibles para abrir y convertir archivos IGES mediante programación.

## Formato de archivo IGES

Los archivos IGES están en formato de texto ASCII y se pueden abrir en cualquier editor de texto para ver el contenido del archivo. La información textual en un archivo IGES se representa en formato "Hollerith". Un archivo IGES común puede contener miles de líneas para representar la información 2D o 3D que se puede intercambiar según este formato. Un archivo IGES se divide en cinco secciones, indicadas por la letra mayúscula específica en la columna 73. Esas secciones son las secciones "Inicio" (S), "Global" (G), "Entrada de datos" (D), "Datos de parámetros" (P) y "Terminación" (T). Las secciones Entrada de datos y Datos de parámetros se abrevian comúnmente DE y PD, respectivamente.

### Encabezado del archivo IGES

Las secciones Inicio y Global contienen información básica sobre:
* Nombre del archivo y su fuente
* Delimitadores para la sección de datos de parámetros
* Autor del archivo, y otra información general.

Las secciones Inicio y Global del documento de ejemplo en Wikipedia son las siguientes.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Como se puede ver, el campo de inicio contiene descripciones legibles por humanos del archivo, y puede tener caracteres en las columnas 1-72, con la línea que termina con el encabezado de la sección y el número de línea de la sección. Debe haber al menos 1 línea de la sección Inicio. La sección global contiene datos del preprocesador. También debe estar presente en el archivo y terminar con el formato G000000#.

### Sección de entrada de datos (DE) y datos de parámetros (PD)

#### Sección de entrada de datos
Un archivo IGES consta de varias entidades que contienen la información sobre los datos básicos del formato de archivo IGES. Una entidad contiene información sobre diferentes elementos de un formato de datos IGES y se utiliza para dibujar. Las entidades más utilizadas incluyen:
* Arco circular
* Curva compuesta
* Arco cónico
* Plano
* Línea

Estos son solo algunos y hay alrededor de 150 entidades diferentes en IGES. Cada entidad se identifica por un número de tipo como:
* ARCO CIRCULAR (Tipo 100)
* LÍNEA (Tipo 110)

##### Propiedades de la entidad

Cada entidad declarada tiene las siguientes propiedades.

|Nombre de campo|Descripción|
---|---|
|Tipo de entidad |Este es el tipo de entidad que se describe. Por ejemplo, 116 describe una entidad Punto.|
|Puntero PD |Esto proporciona la ubicación de los datos de esta entidad en la sección Datos de parámetros. Esta ubicación es simplemente el número de línea dentro de la sección PD que tiene la primera línea de los datos de esta entidad.|
|Estructura |Cero o puntero a entidad de definición. No aplica para la mayoría de las entidades|
|Patrón de fuente de línea| Entidad de patrón de fuente de número o puntero a línea. El número significa: * 0 Ningún patrón especificado (predeterminado) * 1 Sólido * 2 Discontinuo * 3 Fantasma * 4 Línea central * 5 Punteado|
|Nivel| Especifica los niveles que se asociarán con esta entidad. Permite que la entidad aparezca en más de un nivel |
|Ver| Especifica las opciones de visualización. Estos son: 0 Indica la misma visibilidad y características en todas las vistas. Puntero predeterminado a la entidad de Vista (Tipo 410) desde la que se puede ver Referencia a una entidad de Asociatividad Visible de Vista (Tipo 402, Formulario 3)
|Puntero de matriz de transformación| Hace referencia a una entidad de matriz de transformación (Tipo 124) o es cero por defecto (sin transformación)|
|Asociación de visualización de etiquetas| Hace referencia a una asociatividad de visualización de etiquetas (tipo 402, formulario 5) que define cómo aparece la etiqueta de la entidad.|
|Número de estado| Contiene cuatro secciones de dos números. 1-2: Estado en blanco. 00 para normal o 01 para en blanco. 3-4: Cambio de entidad subordinada: es 00 para independiente, 01 para dependiente físico, 02 para dependiente lógica y 03 para ambos. 5-6: Indicador de uso de entidad: es 00 para geometría, 01 para anotación, 02 para definición, 03 para otro, 04 para lógica, 05 para paramétrica 2D y 06 para geometría de construcción. Finalmente, 7-8 es la jerarquía, donde 00 indica de arriba hacia abajo global (use las características de esta entidad), 01 es diferido global (no use las características de esta entidad) y 02 es propiedad de jerarquía de uso (use Entidad de jerarquía (Tipo 406, Formulario 10)determinar características de agrupación jerárquica).|
|Número de secuencia| Especificado por D#, donde # es el número de línea de esta sección (no desde la parte superior del archivo). Esto también se usa para apuntar a esta entidad de entrada de datos.|
|Tipo de entidad| se especifica dos veces por lista de entidades|
|Número de grosor de línea| Especifica el grosor al mostrar la entidad. El más pequeño es 1, 0 es el valor predeterminado |
|Número de color| Especifica el color de la entidad. Los valores enteros permitidos son: 0 Sin color (predeterminado) 1 Negro 2 Rojo 3 Verde 4 Azul 5 Amarillo 6 Magenta 7 Cian 8 Blanco|
|Número de recuento de líneas de parámetro| Especifica el número de líneas que ocupa esta entidad en la Sección de datos de parámetros |
|Número de formulario| Indica la forma, o la representación de esta entidad. Cambia la forma en que se interpretan los datos del parámetro. El valor predeterminado es 0|
|Campo Reservado| No usado|
|Campo Reservado| No usado|
|Etiqueta de entidad| Identificador especificado por la aplicación: justificado a la derecha |
|Número de subíndice| Calificador numérico para la etiqueta de entidad. Ambos juntos forman un identificador único para la entidad|
|Número de secuencia Ver arriba. |Este será D#+1, ya que cada entidad se especifica en dos líneas.|

#### Sección de datos de parámetros
La sección Entradas de datos es seguida por la sección Datos de parámetros. Enumera los datos para cada entrada respectiva y enumera los parámetros para la entidad en función de los delimitadores especificados en la sección Global (generalmente comas para separar los parámetros y un punto y coma para finalizar la lista).


## Referencias
* [IGES de WikiPedia](https://en.wikipedia.org/wiki/IGES)

