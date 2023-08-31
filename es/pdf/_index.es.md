{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "fundamentos" ],
  "description":"El formato de documento portátil (PDF) es una representación estándar de documentos independiente del software, el hardware y el sistema operativo. Los estándares de PDF incluyen PDF/A, PDF/E, PDF/UA, PDF/VT y PDF/X",
  "title" :"Formato de archivo PDF - ¿Qué es un archivo PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

El formato de documento portátil (PDF) es un tipo de documento creado por Adobe en la década de 1990. El propósito de este formato de archivo era introducir un estándar para la representación de documentos y otro material de referencia en un formato que es independiente del software de la aplicación, el hardware y el sistema operativo. El formato de archivo PDF tiene la capacidad completa de contener información como texto, imágenes, hipervínculos, campos de formulario, medios enriquecidos, firmas digitales, archivos adjuntos, metadatos, características geoespaciales y objetos 3D que pueden convertirse en parte del documento de origen.

En la mayoría de los casos, los documentos existentes se convierten a PDF en lugar de crear un nuevo PDF desde cero. Pero eso no significa que no haya software para la creación o manipulación de archivos PDF.

**(¿Tiene que compartir algo sobre el formato de archivo PDF? Puede publicar sus hallazgos en la sección [Noticias de formato de archivo PDF](https://news.fileformat.com/t/PDF).)**

## Formato de archivo PDF - Breve historia

Un recorrido rápido por la línea de tiempo sobre la formación del archivo PDF en términos de línea de tiempo es el siguiente:

**1993**: Adobe Systems puso a disposición las especificaciones en PDF de forma gratuita

**2008**: el PDF se lanzó como estándar abierto el 1 de julio de 2008 y la Organización Internacional de Normalización lo publicó como **ISO 32000-1:2008**.

**2008**: Adobe publicó una licencia de patente pública para los derechos libres de regalías del formato ISO 32000-1 para todas las patentes propiedad de Adobe que son necesarias para crear, usar, vender y distribuir implementaciones compatibles con PDF.

La primera versión de PDF designada como PDF 1.0 que luego pasó por revisiones hasta PDF 1.7. PDF 1.7, que se convirtió en ISO 32000-1, incluye algunas tecnologías propietarias no estandarizadas, así como Adobe XML Forms Architecture (XFA) y la extensión de JavaScript para Acrobat. Fue el 28 de julio de 2017 cuando se publicó el PDF 2.0, conocido como ISO 32000-2:2017, que no incluye ninguna tecnología no estandarizada.

## Especificaciones del formato de archivo PDF

Un archivo PDF es un conjunto de bytes que se pueden agrupar en tokens de acuerdo con las reglas de sintaxis definidas por las especificaciones de PDF. Una o más fichas se combinan para formar entidades sintácticas de nivel superior, principalmente objetos, que son los valores de datos básicos a partir de los cuales se construye un documento PDF.

### Estructura de archivos de archivos PDF

El contenido del archivo PDF se organiza en la siguiente secuencia dentro del archivo.

|Encabezado
|Cuerpo
|Tabla de referencias cruzadas
|Tráiler

#### Encabezado del archivo PDF ####

Independientemente de la versión PDF, un archivo PDF comienza con un encabezado que contiene un identificador único para PDF y la versión del formato, como %PDF-1.x, donde x varía de 1 a 7.

#### Cuerpo del archivo ####

El cuerpo de un archivo PDF consta de una secuencia de objetos indirectos que representan el contenido de un documento. Los objetos, como se describe arriba, representan componentes del documento como fuentes, páginas e imágenes de muestra. A partir de PDF 1.5, el cuerpo también puede contener flujos de objetos, cada uno de los cuales contiene una secuencia de objetos indirectos.

#### Tabla de referencias cruzadas ####

La tabla de referencias cruzadas contiene información que permite el acceso aleatorio a objetos indirectos dentro del archivo, de modo que no es necesario leer todo el archivo para ubicar un objeto en particular. La tabla deberá contener una entrada de una línea para cada objeto indirecto, especificando el desplazamiento de bytes de ese objeto dentro del cuerpo del archivo. (A partir de PDF 1.5, parte o toda la información de referencias cruzadas puede estar contenida alternativamente en flujos de referencias cruzadas.

#### Tráiler de archivos ####

El tráiler de un archivo PDF permite que un lector conforme encuentre rápidamente la tabla de referencias cruzadas y ciertos objetos especiales. Los lectores conformes deben leer un archivo PDF desde su extremo. La última línea del archivo contendrá solo el marcador de fin de archivo, %%EOF. Las dos líneas anteriores contendrán, una por línea y en orden, la palabra clave startxref y el byte de desplazamiento en el flujo decodificado desde el comienzo del archivo hasta el comienzo de la palabra clave xref en la última sección de referencia cruzada.

### Objetos PDF ###

Un archivo PDF incluye varios tipos diferentes de objetos que son de los siguientes tipos

* Valores booleanos - que representan condicional verdadero o falso
* Números - valores enteros y reales
* Cadenas: contiene caracteres entre paréntesis
* Nombres: comience con un carácter hacia adelante, por ejemplo, /ASomewhatLangerName da como resultado ASomewhatLangerName
* Matrices: PDF admite matrices unidimensionales. Se pueden construir arreglos de dimensiones más altas usando arreglos como elementos anidados
* Diccionarios - colección de objetos como pares clave-valor. Puede tener cero entradas.
* Flujos: representa una secuencia de bytes que también puede tener una longitud ilimitada
* Objeto nulo: representa un valor nulo

Puede haber otros otros objetos como comentarios que se introducen con el signo % y pueden contener caracteres de 8 bits.

### Objetos indirectos ###

Cualquier objeto en un archivo PDF se puede etiquetar como un objeto indirecto. Los objetos indirectos reciben un identificador de objeto único por el cual otros objetos pueden referirse a él. Las referencias cruzadas a estos se mantienen en una tabla de índice y se marcan con la palabra clave xref que sigue al cuerpo principal y proporciona el desplazamiento de bytes de cada objeto indirecto desde el inicio del archivo.

### Diseños PDF lineales y no lineales ###

Los diseños de PDF se clasifican como lineales y no lineales según las aplicaciones de destino y otros factores.

No lineal: los archivos PDF no lineales utilizan menos espacio en disco en comparación con los archivos PDF lineales. Las páginas PDF del documento residen dispersas en el archivo PDF y es por eso que los archivos no lineales son más lentos en comparación con los archivos lineales.

PDF lineal: dirigido a lectores de PDF en línea, los archivos PDF lineales se construyen de tal manera que se escriben en el disco de forma lineal. Esto no requiere complementos del navegador para que todo el documento se cargue primero antes de mostrarlo.

### Resumen de objetos ###

Como se mencionó, el cuerpo del PDF es una colección de objetos mencionados anteriormente. PDF se basa en gran medida en PostScript sin las funciones de control de los lenguajes de programación como los comandos if y loop. Los comandos emitidos por el código Postscript para generar contenidos gráficos se recopilan y tokenizan además de los archivos, gráficos o fuentes a los que hace referencia el documento. Todos estos contenidos se acumulan en un solo archivo, lo que da como resultado una salida PostScript compuesta.

#### Texto ####

El texto en PDF está representado por elementos de texto que en realidad se muestran con glifos de fuentes. Un glifo es una forma gráfica y está sujeto a todas las manipulaciones gráficas, como la transformación de coordenadas. Debido a la importancia del texto en la mayoría de las descripciones de las páginas, PDF proporciona funciones de alto nivel para describir, seleccionar y representar glifos de manera conveniente y eficiente.

#### Gráficos ####

Los operadores gráficos que se utilizan en los flujos de contenido de PDF describen la apariencia de las páginas que se van a reproducir en un dispositivo de salida de trama. Las instalaciones están destinadas tanto para aplicaciones de impresión como de visualización. Los operadores gráficos forman seis grupos principales:

* Los operadores de estado de gráficos manipulan la estructura de datos llamada estado de gráficos, el marco global dentro del cual se ejecutan los demás operadores de gráficos. El estado de los gráficos incluye la matriz de transformación actual (CTM), que mapea las coordenadas del espacio del usuario utilizadas dentro de un flujo de contenido PDF en las coordenadas del dispositivo de salida. También incluye el color actual, la ruta de recorte actual y muchos otros parámetros que son operandos implícitos de los operadores de pintura.
* Los operadores de construcción de rutas especifican rutas, que definen formas, trayectorias lineales y regiones de varios tipos. Incluyen operadores para comenzar una nueva ruta, agregarle segmentos de línea y curvas y cerrarla.
* Los operadores de pintura de rutas rellenan una ruta con un color, pintan un trazo a lo largo de ella o la utilizan como límite de recorte.
* Otros operadores de pintura pintan ciertos objetos gráficos autodescriptivos. Estos incluyen imágenes de muestra, sombreados definidos geométricamente y flujos de contenido completos que a su vez contienen secuencias de operadores gráficos.
* Los operadores de texto seleccionan y muestran glifos de caracteres de fuentes (descripciones de tipos de letra para representar caracteres de texto). Debido a que PDF trata los glifos como formas gráficas generales, muchos de los operadores de texto podrían agruparse con los operadores de pintura o de estado de gráficos. Sin embargo, las estructuras de datos y los mecanismos para manejar las descripciones de glifos y fuentes son suficientemente especializados.
* Los operadores de contenido marcado asocian información lógica de nivel superior con objetos en el flujo de contenido. Esta información no afecta la apariencia renderizada del contenido; es útil para las aplicaciones que utilizan PDF para el intercambio de documentos.

## Referencias ##

* [Formato de archivo PDF: Estructura básica](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Referencia PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

