{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "archivo", "extensión", "formato", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre los archivos GLTF y las API que pueden crear y abrir archivos GLTF",
  "title" :"GLTF - Formato de archivo de transmisión GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo GLTF?

glTF (formato de transmisión GL) es un formato de archivo 3D que almacena información del modelo 3D en formato JSON. El uso de JSON minimiza tanto el tamaño de los activos 3D como el procesamiento en tiempo de ejecución necesario para desempaquetar y usar esos activos. Fue adoptado para la transmisión y carga eficiente de escenas y modelos 3D por aplicaciones. glTF fue desarrollado por el Grupo de Trabajo de Formatos 3D del Grupo Khronos y sus creadores también lo describen como [JPEG](/es/image/jpeg/) de 3D.

El formato de archivo GLTF define un formato de publicación común extensible para herramientas y servicios de contenido 3D que agiliza los flujos de trabajo de creación y permite el uso interoperable de contenido en toda la industria. La intención detrás de la creación del formato de archivo glTF fue definir un formato de publicación común y extensible para herramientas y servicios de contenido 3D que debería optimizar los flujos de trabajo de creación y permitir el uso interoperable de contenido en toda la industria. Minimiza el procesamiento en tiempo de ejecución de las aplicaciones que utilizan WebGL y otras API.

## Breve historia del archivo GLTF

Las primeras especificaciones para el formato de archivo glTF 1.0 se anunciaron en octubre de 2015. Esto se produjo como una serie de esfuerzos que comenzó en marzo de 2012 por parte de Khronos. El objetivo de estos esfuerzos fue evaluar las oportunidades en torno a la tracción WebGL. Como resultado, la primera demostración del formato glTF, basado en el formato JSON, se presentó en la reunión de WebGl en 2012. El formato fue adoptado por varias empresas de vez en cuando, incluidas Cesium, 3D Tiles, Oculus, Microsoft, Archilogic y otras.

glTF 2.0 se publicó el 5 de junio de 2017 en la Conferencia Web3D 2017. Hay una larga lista de empresas que adoptaron el formato de archivo glTF después de eso.

## Formato de archivo GLTF

Las especificaciones de formato de archivo para glTF 2.0 están disponibles [en línea](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) como referencia y deben consultarse en cualquier implementación relacionada con lectura/escritura para soporte de formato de archivo glTF.

glTF define activos como archivos JSON con datos externos compatibles. Representa modelos 3D con la ayuda de:

* Descripción completa de la escena contenida en un archivo .glTF con formato JSON que incluye información sobre la jerarquía de nodos, materiales, cámaras, así como información de descripción para mallas, animaciones y otras construcciones
* Archivos binarios (.bin) que contienen datos de geometría y animación, y otros datos basados en búfer
* Archivos de imagen ([.jpg](/es/image/jpeg/), [.png](/es/image/png/)) para texturas

Todos los activos externos, como las imágenes, se almacenan en archivos externos a los que se hace referencia a través de URI. Estos URI se almacenan junto con el contenedor GLB o se integran directamente en el JSON mediante URI de datos. Cada glTF válido debe especificar su versión.

glTF ha sido diseñado para lograr archivos de tamaño pequeño, carga rápida, representación completa de escenas en 3D y extensibilidad. Estos objetivos de diseño únicos son las razones principales de la popularidad del formato de archivo glTF en el dominio 3D. Los siguientes son los tipos mime admitidos por el formato de archivo glTF para diferentes tipos de archivos:

* Los archivos .gltf usan model/gltf+json
* Los archivos .bin usan application/octet-stream
* Los archivos de textura usan la imagen oficial/* tipo basado en el formato de imagen específico. Para compatibilidad con los navegadores web modernos, se admiten los siguientes formatos de imagen: image/jpeg, image/png.

### Codificación JSON

glTF impone las siguientes restricciones adicionales en el formato de archivo JSON

Para simplificar la implementación del lado del cliente, glTF tiene restricciones adicionales en el formato y la codificación JSON.

1. JSON debe usar la codificación UTF-8 sin BOM.
1. Todas las cadenas definidas en esta especificación (nombres de propiedades, enumeraciones) usan solo juegos de caracteres ASCII y deben escribirse como texto sin formato, por ejemplo, "búfer" en lugar de `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Los nombres (claves) dentro de los objetos JSON deben ser únicos, es decir, no se permiten claves duplicadas.

### URI

Los búferes y los recursos de imagen se referencian a través de URI. Los siguientes dos tipos de URI deben ser compatibles con los clientes.

**URI de datos:** Los URI de datos son definidos por RFC 2397 y glTF los utiliza para incorporar recursos en JSON.

**Rutas URI relativas:** o path-noscheme como se define en RFC 3986, [Sección 4.2](https://tools.ietf.org/html/rfc3986#section-4.2), sin esquema, autoridad ni parámetros. Los caracteres reservados deben estar codificados en porcentaje, según RFC 3986, [Sección 2.2] (https://tools.ietf.org/html/rfc3986#section-2.2).

## Referencias ##

* [Especificaciones de glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Formato de archivo glTF - Por Wikipedia](https://en.wikipedia.org/wiki/GlTF)

