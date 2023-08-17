{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Formato de archivo", "CAD", "Abrir", "Crear" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo DWG y las API que pueden crear y abrir archivos DWG",
  "title" :"Formato de archivo DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DWG?

Los archivos con extensión DWG representan archivos binarios propietarios que se utilizan para contener datos de diseño 2D y 3D. Al igual que DXF, que son archivos ASCII, DWG representa el formato de archivo binario para dibujos CAD (diseño asistido por computadora). Contiene imágenes vectoriales y metadatos para la representación de contenidos de archivos CAD. Hay visores gratuitos disponibles para ver archivos DWG en el sistema operativo Windows, como el DWG TrueView gratuito de Autodesk. También hay otras aplicaciones de terceros que admiten el acceso a archivos DWG. Los archivos DWG contienen información creada por el usuario e incluyen:

* Diseños
* Datos geométricos
* Mapas y fotos

Este formato es ampliamente utilizado por arquitectos, ingenieros y diseñadores para diversos propósitos de diseño.

## Breve historia ##

El formato de archivo DWG ha evolucionado con el tiempo desde su introducción formal en 1982. A continuación se ofrece una breve descripción general de los eventos pasados desde la perspectiva de la historia.

**1982:** Autodesk obtuvo la licencia del formato de archivo DWG, desarrollado por Mike Riddle en 1970, como base para AutoCAD.

**1998:** Con el lanzamiento de AutoCAD R14.01, Autodesk agregó la verificación de archivos a través de una función llamada DWGCHECK que incrustó una suma de verificación cifrada y un código de producto, llamado WaterMark por Autodesk, en los archivos DWG creados por el programa.

**2006:** Autodesk modificó AutoCAD 2007 para incluir "tecnología TrustedDWG" para incrustar la cadena de texto "Autodesk DWG. Este archivo es un DWG de confianza guardado por última vez por una aplicación de Autodesk o una aplicación con licencia de Autodesk" en los archivos DWG. El propósito de esto fue ayudar a los usuarios del software de Autodesk a garantizar que estos archivos fueron creados por una aplicación de Autodesk o RealDWG, lo que definitivamente debería ayudar a reducir el riesgo de incompatibilidades.

## Estructura de archivo ##

DWG ha sido uno de los formatos de archivo más utilizados por una variedad de aplicaciones y tiene una estructura de archivos robusta. Dado que DWG es un formato de archivo binario, no es legible por humanos como el formato de archivo simple ASCII [DXF](/es/cad/dxf/). Los archivos DWG generalmente incluyen información sobre las coordenadas de la imagen y los metadatos asociados con ella. Las [especificaciones](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) completas del formato de archivo DWG están disponibles para su descarga a través de OpenDesign. La estructura de archivos del formato de archivo DWG se resume a continuación.

**Encabezado**: el encabezado del archivo consta de variables de encabezado DWG e información sobre la verificación de redundancia cíclica (CRC) que se utiliza para la detección de errores. Cada subsección es un vector especializado donde se utilizan diferentes longitudes de bits para representar diferentes etiquetas. Por ejemplo, los primeros 6 bits de la variable de encabezado DWG representan la cadena de versión.

**Definiciones de clases:** Un archivo DWG puede contener numerosas clases según el propósito específico del archivo .dwg. Información como el tamaño de los metadatos de clase del área de datos de clase, el número de clase y la suma de verificación, entre otros.

**Plantilla**: Esto es opcional y para las versiones R15 y R15, esta sección se encuentra debajo de la sección Espacio libre de objetos.

**Relleno**: los metadatos tienen un sufijo y un postfijo con un número específico de bytes que hace que las versiones anteriores del software AutoCAD sean compatibles con el nuevo formato de archivo DWG.

**Datos de imagen**: los metadatos de esta sección dependen del tipo de .dwg específico. Para usuarios de R14 y R15, esta sección es opcional.

**Datos de objeto**: Los datos de objeto consisten en una lista completa de entidades de tabla, entradas de diccionario, etc. correspondientes a la lista de objetos existente.

**Mapa de objetos**: La ubicación de cada objeto en el archivo se especifica en esta sección del archivo. La mayoría de los metadatos de esta sección son identificadores de archivos que desempeñan un papel en la identificación y la reproducción del objeto.

**Espacio libre de objetos**: esta sección es opcional para todos los usuarios

**Segundo encabezado**: un duplicado de la sección del encabezado del archivo hacia el final del archivo DWG

## Referencias ##

* [Especificaciones de formato de archivo DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Especificación de archivo DWG](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - Por Wikipedia](https://en.wikipedia.org/wiki/.dwg)

