{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","archivo", "formato", "tipo de archivo", "extensión","¿qué es un archivo ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo ASE y las API que pueden abrir y crear archivos ASE",
  "title" :"ASE: archivo de exportación de escenas ASCII de Autodesk",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## ¿Qué es un archivo ASE?

Un archivo con una extensión .ase es un formato de archivo de exportación de escena ASCII de Autodesk que es una representación ASCII de una escena, que contiene información 2D o 3D mientras se exportan datos de escena usando Autodesk. Autodesk proporciona opciones para incluir componentes de escena al exportar datos de escena. Puede incluir la definición de malla junto con información de vértices y caras, descripción del material, datos de animación de transformación para los objetos, definición de malla completa de cada n cuadros, datos de animación para cámaras y luces y configuración de juntas IK.

## Formato de archivo ASE: más información

Los archivos ASE son archivos de texto almacenados en formato ASCII que se pueden abrir en cualquier editor de texto. Un archivo ASE puede contener los siguientes tipos de información proporcionada por Autodesk.

### Opciones de salida

* `Definición de malla`: exporta la definición de cada malla, incluida la información de vértices y caras para objetos geométricos. Además, al activar esto, se habilitan los elementos en el cuadro de grupo Opciones de malla, que se describe a continuación.
* `Materiales` - Incluye la descripción del material. Si un material no está asignado a un objeto, se exporta su color de estructura alámbrica. Se incluyen todos los niveles de un árbol de materiales, por lo que esto puede generar mucho texto.
* `Transformar claves de animación`: incluye los datos de transformación de animación para los objetos. Si el objeto es una cámara de destino o un foco, esto incluirá datos de animación de destino.
* `Malla animada`: exporta una definición de malla completa de cada n fotogramas. La frecuencia se especifica mediante el control giratorio de salida del controlador, que se describe a continuación. Cada bloque contiene la misma información especificada en el cuadro de grupo Opciones de malla, que se describe a continuación. Activar esto puede resultar en un archivo enorme, incluso para escenas pequeñas.
* `Configuración de cámara/luz animada`: exporta los datos de animación para cámaras y luces, como el color, la intensidad, la atenuación, el sesgo del mapa, etc. Emite un bloque cada n fotogramas, según lo especificado por el control giratorio de salida del controlador.
* `Articulaciones cinemáticas inversas`: exporta la configuración de las articulaciones IK en la rama Jerarquía.

### Tipos de objetos

Los elementos aquí le permiten especificar qué categoría de objeto desea incluir en la salida. Puede incluir objetos geométricos, formas, cámaras, luces y objetos auxiliares.

* Geométrica
* Formas
* Cámaras
* Luces
* Ayudantes

### Opciones de malla

* `Mesh Normals` - Exporta las caras y los vértices normales. La normal de la cara se enumera primero, seguida de las normales de los tres vértices que soportan la cara. Activar esto da como resultado un archivo mucho más grande.
* `Coordenadas de mapeo`: exporta una lista de vértices y caras de mapeo, de acuerdo con las estructuras TVert y TVFace descritas en el kit de desarrollo de software de 3ds Max. Si un objeto usa el mapeo de rostros, se exporta una lista de mapas de rostros que contiene las coordenadas UVW para cada rostro.
* `Colores de vértice` - Exporta colores de vértice.

### Salida del controlador

* `Usar claves` - Exporta valores clave. Si el controlador no usa teclas, entonces se usa el método Force Sample. En el caso de los controladores de transformación, la opción Use Keys solo funciona si todos los controladores de transformación son Linear/TCB o Bezier. Si una de las pistas de transformación usa un tipo diferente de controlador, entonces el método Force Sample se usa para todas las pistas de transformación.
* `Muestras forzadas` - Muestra los valores del controlador en función de la frecuencia especificada en Cuadros por controlador de muestra.

## Referencias

* [Autodesk - Exportación a ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

