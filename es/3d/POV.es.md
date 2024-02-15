
{
  "date" : "2023-01-05",
  "keywords" : [ "pov file", "pov file format", "what is a pov file", "file", "pov example", "pov file extension","extension", "format" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : "true",
  "description":"Obtenga información sobre el formato de archivo POV y las API que pueden abrir y crear archivos POV.",
  "title" : "POV - Archivo de persistencia de la visión",
  "linktitle" : "POV",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2023-01-05"
}

## ¿Qué es un archivo POV?

Un archivo POV es un archivo de texto sin formato que contiene instrucciones para el software de trazado de rayos POV-Ray. Estas instrucciones están escritas en un lenguaje de programación especial específico de POV-Ray. Especifica la escena que se va a representar, incluidos los objetos 3D, los materiales, la iluminación y otras propiedades que definen la apariencia de la escena. Los archivos POV utilizan un lenguaje de secuencias de comandos especial que es específico de POV-Ray y se puede utilizar para crear escenas 3D complejas y detalladas. La extensión de archivo de un archivo POV suele ser .pov o .povray. Cuando abre un archivo POV en POV-Ray, el software lee las instrucciones del archivo y las utiliza para generar una imagen renderizada de la escena.

Los artistas y diseñadores suelen utilizar los archivos .pov para crear gráficos y animaciones en 3D para una variedad de aplicaciones, incluidas películas, televisión, videojuegos y materiales de marketing.

## Formato de archivo POV

El archivo **.pov** normalmente comienza con una serie de instrucciones **#include**, que se utilizan para incluir bibliotecas de colores, texturas y otros recursos predefinidos que se pueden utilizar en la escena. Luego, el archivo define los objetos, materiales y otras propiedades de la escena utilizando una serie de bloques. Hay muchos otros tipos de objetos, materiales y otras propiedades que puedes especificar en un archivo .pov, y puedes usar bucles y declaraciones condicionales para crear escenas más complejas y detalladas.

## Aplicaciones de software para puntos de vista

El software de trazado de rayos POV-Ray utiliza el formato de archivo .pov, por lo que la aplicación principal para abrir archivos .pov es el propio software POV-Ray. Puede descargar la última versión de POV-Ray desde el sitio web oficial en https://www.povray.org/.

Además de POV-Ray, existen otras aplicaciones que pueden abrir y editar archivos .pov, entre ellas:

- BRL-CAD: un software de modelado 3D de código abierto que puede importar y exportar archivos .pov
- MeshLab: un software de procesamiento de mallas 3D que puede importar y exportar archivos .pov
- Blender: un popular software de gráficos 3D de código abierto que puede importar y exportar archivos .pov

Es posible que existan otras aplicaciones de software que también puedan abrir archivos .pov, por lo que puede intentar usar un visor de archivos o una herramienta de conversión si no puede abrir un archivo .pov con las aplicaciones anteriores.

## Ejemplo de punto de vista

Por ejemplo, aquí hay un archivo .pov de muestra que define una escena con un solo cilindro azul:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

En este ejemplo, el bloque de cámara especifica la posición y orientación de la cámara en la escena, el bloque `light_source` declara una fuente de luz y especifica su posición y color, y el bloque `cylinder` declara un objeto cilindro y especifica sus puntos finales. radio y propiedades del material. Cuando abre este archivo .pov en el software POV-Ray, generará una imagen de un solo cilindro azul.

## Referencias
 * [POV-Ray - Wikipedia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Sitio web de documentación POV-Ray](http://www.povray.org/documentation/)