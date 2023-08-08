{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "archivo", "extensión", "formato", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo JT y las API que pueden crear y abrir archivos JT",
  "title" :"JT - Formato de archivo de teselación de Júpiter",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo JT?

**JT** (Jupiter Tessellation) es un formato de datos 3D estandarizado por ISO eficiente, centrado en la industria y flexible desarrollado por Siemens PLM Software. Los dominios de CAD mecánico de la industria aeroespacial, automotriz y de equipos pesados utilizan JT como su formato de visualización 3D más importante.

El formato JT es un gráfico de escena que admite los atributos y nodos que son específicos de CAD. Se utilizan técnicas de compresión sofisticadas para almacenar datos de facetas (triángulos). Este formato está estructurado para admitir atributos visuales, información de productos y fabricación (PMI) y metadatos. Hay un buen soporte para la transmisión asincrónica de contenido. En la industria mecánica pesada, los profesionales utilizan archivos JT en sus soluciones CAD y programas de software de gestión del ciclo de vida del producto (PLM) para examinar la geometría de mercancías complicadas.

Como JT es compatible con casi todos los formatos CAD 3D importantes, su ensamblaje puede manejar una variedad de combinaciones que se conocen como "multi-CAD". Este ensamblaje multi-CAD siempre está bien administrado y actualizado porque la sincronización entre los archivos de descripción de productos CAD nativos con sus archivos JT asociados se realiza automáticamente. Los archivos JT son originalmente livianos, por lo que se consideran adecuados para colaboraciones en Internet. Las empresas colaboran mediante el envío de visualizaciones 3D a través de los medios mucho más fácilmente en comparación con los archivos CAD originales "pesados". Además, los archivos JT garantizan muchas funciones de seguridad que hacen que el intercambio de propiedad intelectual sea más seguro.

## Breve historia del formato de archivo JT

Engineering Animation, Inc. y Hewlett Packard fueron los diseñadores originales de JT, quienes desarrollaron ese formato como el conjunto de herramientas Direct Model. Después de que EAI fuera adquirida por UGS Corp., JT se convirtió en parte de la suite de UGS. A principios de 2007, UGS anunció JT como su formato 3D maestro. En el mismo año, Siemens AG compró UGS y se convirtió en Siemens PLM Software. Siemens utiliza JT como formato común de interoperabilidad y formato de archivo de datos. En 2009, ISO aceptó la especificación JT para su publicación como Especificación disponible públicamente (PAS) de ISO. A mediados de 2010, ProSTEP iViP anunció que a nivel industrial, JT y STEP AP 242 XML se pueden usar juntos para lograr la máxima ventaja en datos escenarios de intercambio. En 2012, JT se declaró oficialmente como formato de visualización 3D estandarizado por ISO (ISO 14306:2012 (ISO JT V1)).

## Formato de archivo JT ##

Todos los objetos en el formato JT se representan a través de un identificador de objeto y las referencias entre objetos se manejan a través del identificador del objeto referenciado. La integridad de estas referencias a objetos se puede mantener a través de punteros que se activan o se activan.

Un archivo JT se organiza como una serie de bloques y el bloque de encabezado es siempre el primer bloque de datos del archivo. Una serie de segmentos de datos y un segmento TOC siguen inmediatamente al bloque de encabezado. El único segmento de datos (6 segmentos LSG) posee un archivo JT compatible con la referencia que siempre existe. TOC Segment contiene la información de ubicación de todos los demás segmentos de datos de ese archivo.

{{< figure src="../JT-1.png" alt="Formato de archivo JT" >}}

### Encabezado del archivo ###

File Header es el primer bloque en la jerarquía de datos del archivo JT. La información de versión y la información de ubicación de TOC se incluyen dentro del encabezado, lo que facilita a los cargadores la lectura de archivos. El contenido del encabezado del archivo se organiza de la siguiente manera.

### Segmento TOC ###

El segmento TOC debe existir dentro de un archivo y contiene información de identificación y ubicación de todos los demás segmentos de datos. La ubicación real del segmento TOC se especifica en el campo Compensación TOC del encabezado del archivo. Cada segmento de datos direccionable individualmente está representado por una entrada TOC en un segmento TOC.

### Segmento de datos

El archivo JT define todos los datos almacenados dentro de un segmento de datos. Algunos segmentos de datos pueden comprimir todos los bytes de información que quedan dentro del segmento. Los segmentos de datos tienen la siguiente estructura:

![alt text](../JT-2.png "JT Data Segment")

La siguiente tabla describe diferentes tipos de segmentos de datos:

|Nombre|Descripción
---|---|
|Segmento LSG|Consta de una colección de objetos vinculados a través de referencias dirigidas para formar LSG (estructura gráfica acíclica dirigida)
|Segmento LOD de forma|contiene los datos que definen las formas geométricas (p. ej., vértices, normales, polígonos, etc.)
|Segmento JT B-Rep|Tener elemento para que los datos representen el límite geométrico preciso para una porción individual en formato JT B-Rep.
|Segmento XT B-Rep|Tener elemento para que los datos representen el límite geométrico preciso para una porción individual en formato de representación de límite
|Segmento de estructura alámbrica|Los datos representan una estructura alámbrica 3D precisa para una porción particular definida por un elemento contenido en este segmento.
|Segmento de metadatos|Permite almacenar metadatos en distintos segmentos direccionables.
|Segmento JT ULP|Con elementos para que los datos representen el límite geométrico semipreciso de una porción individual en formato JT ULP.
|Segmento JT LWPA|Contiene un elemento que define datos analíticos para una parte en particular. LWPA encierra la colección de superficies analíticas en la definición b-rep de la pieza.

## Compresión

Los requisitos de transmisión y almacenamiento de los modelos 3D son más exigentes, por lo que los archivos JT pueden beneficiarse de la compresión. Un modelo de datos JT puede estar compuesto por diferentes archivos que utilizan diferentes técnicas de compresión, pero el proceso de compresión es transparente para el usuario de datos JT.

Hasta ahora, JT Open Toolkit (como estándar) y la compresión avanzada son dos técnicas de compresión utilizadas por los archivos JT. JT Open Toolkit emplea un algoritmo de compresión fácil y sin pérdidas, mientras que la compresión avanzada emplea una técnica de compresión más refinada y específica del dominio que conduce a una compresión de geometría con pérdidas. Las aplicaciones de cliente prefieren la compresión avanzada en lugar de usar la compresión estándar, ya que la compresión avanzada produce índices de compresión bastante altos. La compatibilidad con las aplicaciones de visualización de archivos JT ordinarias se mantiene mediante la provisión de compresión estándar. El formulario de compresión debe ser compatible con la versión del formato de archivo JT, que se puede ver cuando se abre un archivo JT con el editor de texto y se incluye dentro de la información del encabezado ASCII.

## Referencias

* [Referencia de formato de archivo JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (formato de visualización)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)
