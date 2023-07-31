{
  "date" : "2019-10-11",
  "keywords" :[ "archivo emf", "formato de archivo emf", "qué es un archivo emf", "archivo", "ejemplo emf", "extensión de archivo emf","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - Formato de metarchivo mejorado",
  "description":"Obtenga información sobre el formato de archivo EMF y las API que pueden crear y abrir archivos EMF",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo EMF?

**Formato de metarchivo mejorado (EMF)** almacena imágenes gráficas independientemente del dispositivo. Los metarchivos de EMF se componen de registros de longitud variable en orden cronológico que pueden representar la imagen almacenada después de analizarla en cualquier dispositivo de salida. Estos registros de longitud variable pueden ser definiciones de objetos encerrados, comandos para dibujar y propiedades gráficas críticas para representar la imagen con precisión. Cuando un dispositivo abre un metarchivo EMF utilizando su propio entorno de gráficos, las proporciones, las dimensiones, los colores y otras propiedades gráficas de la imagen original siguen siendo las mismas independientemente de la plataforma del dispositivo de apertura.

## Breve historia ##

En 1990, Microsoft diseñó un formato de archivo de imagen Windows Metfile ([WMF](/es/image/wmf/)) para Microsoft Windows. Los metarchivos de Windows tienen un formato de 16 bits que puede contener algunos componentes de mapa de bits. WMF puede consistir en gráficos vectoriales y está diseñado para que sea portátil entre diferentes aplicaciones. En 1993, Win32/GDI anunció el metarchivo mejorado (EMF), una versión más nueva con mayor flexibilidad y escalabilidad. EMF también se utiliza como comando de lenguaje gráfico para ejecutar los controladores de impresora. Microsoft ahora recomienda el formato de metarchivo mejorado (EMF) sobre el formato de Windows (WMF). Cuando se introdujo Windows XP, se lanzó la versión Enhanced Metafile Format Plus (EMF+). Esta versión más nueva encuentra su camino al serializar las llamadas a la API de GDI+, así como las llamadas de registros WMF/EMF a GDI. Existe una versión comprimida gzip de EMF conocida como EMZ.

## Formato de metarchivo EMF ##

Los siguientes son los elementos esenciales del formato de metarchivo mejorado:

* Un EMR_HEADER (versión, tamaño, resolución de la imagen en el momento de la creación)
* Una tabla para objetos GDI
* Una paleta reservada (opcional)
* Registros de metarchivos organizados en estructura de matriz (configuración de propiedades, objetos definidos, comandos de dibujo)
* Registro EMR_EOF (último registro en el metarchivo EMF)

## Versiones CEM ##
* **Original**: La versión original especifica el registro necesario para conservar la imagen original y mantener su dispositivo independiente. Además, admite el registro que contiene objetos gráficos y comandos para dibujar.
* **Versión 1**: la segunda versión de EMF mejoró la flexibilidad y la independencia del dispositivo al agregar el registro para el formato de píxel y la disposición para usar el comando OpenGL.
* **Versión 2**: la tercera versión mejoró la precisión al agregar el sistema métrico para medir las distancias de la superficie del dispositivo, dejando el registro más escalable.

## Registros de metarchivo mejorados ##

Los registros del metarchivo se organizan en forma de matriz. Estos registros tienen estructura ENHMETARECORD y longitud variable. ENHMETARECORD especifica datos que definen funciones GDI para crear una imagen utilizando un formato de metarchivo mejorado. La estructura **ENHMETAHEADER** es siempre el primer registro en este formato. Este encabezado EMF contiene la siguiente información.

Cada registro de metarchivo mejorado tiene dos miembros de EMR (proporciona la estructura base) al principio. El primer miembro reconoce la función GDI (los parámetros se usan en el registro) que determina el tipo de registro y se conoce como iType. El otro miembro nSize define el tamaño de cada registro. Parámetros restantes (si los hay) y datos adicionales dispuestos inmediatamente debajo de nSize. Inmediatamente después del encabezado se puede presentar una descripción de texto opcional. El nombre de la imagen y el autor se registra en esa descripción de texto. La paleta cuya presencia es una opción especifica los colores utilizados en la creación de metarchivos mejorados. Los otros registros utilizados para especificar la función GDI que es esencial en la creación de imágenes.

Al menos un registro EMF debe estar presente en cada metarchivo. La información transversal de un registro a otro depende de los registros EMF, por lo que estos registros deben organizarse de forma adyacente. En cualquier registro dado en el metarchivo, excepto EOF_record, la longitud de ese registro en particular se define para pasar al siguiente registro.

## Creación mejorada de metarchivos ##

La función **CreateEnhMetaFile** se utiliza para crear un metarchivo mejorado. Los argumentos de esta función se utilizan para las dimensiones y el almacenamiento de la imagen en el disco/memoria. Además, esta función requiere la dimensión del dispositivo en el que apareció primero la imagen (dispositivo de referencia) y el contexto del dispositivo de referencia (DC). Por lo tanto, los argumentos para manejar este DC deben proporcionarse al llamar a la función **CreateEnhMetaFile**. La sintaxis de la función es la siguiente:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** manejar a un dispositivo de referencia.

**lptoFilename:** Un puntero al nombre del archivo.

**lprc:** El puntero a la estructura ovalada especifica las dimensiones de la imagen en mm.

**lpDesc:** un puntero a una cadena para el título de la imagen y el nombre de la aplicación que creó la imagen.

## Operaciones de metarchivo mejoradas ##

Los siguientes son trabajos que se pueden realizar utilizando el identificador de un metarchivo mejorado.

* Visualización y edición de la imagen almacenada.
* Producir copias mejoradas de metarchivos.
* Recuperar la copia de un encabezado EMF, descripción opcional y versión binaria de un metarchivo mejorado
* Recapitular los colores en la paleta.

## Objetos gráficos ##

En las operaciones de dibujo y pintura, los objetos gráficos se pueden crear mediante registros de creación de objetos y se pueden guardar para su uso posterior. Un registro `EMR_SELECTOBJECT` puede recuperar estos objetos gráficos utilizando el contexto del dispositivo de reproducción. Los bolígrafos, las paletas, los pinceles, los espacios de color, las fuentes y los objetos de stock son algunos tipos de objetos reutilizables.

## Ordenación de bytes ##

El formato little-endian se utiliza para almacenar datos en registros de metarchivos.

## Versión ##

El formato de archivo EMF se ha revisado dos veces. Las versiones modificadas son la original, la extensión 1 y la extensión 2. Las versiones extendidas tienen provisión para registros OpenGL y un descriptor opcional para el formato de píxel interno. Se agrega una función de medición en mililitros para las dimensiones mostradas.

## Referencias ##

* [Metarchivos de formato mejorado | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Especificación y formato de metarchivo mejorado](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

