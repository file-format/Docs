{
  "date" : "2019-10-11",
  "keywords" :[ "archivo vrml", "formato de archivo vrml", "qué es un archivo vrml", "archivo", "ejemplo de vrml", "extensión de archivo vrml","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo VRML",
  "description":"Obtenga más información sobre el formato de archivo VRML y las API que pueden abrir y crear archivos VRML",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo VRML?
El lenguaje de modelado de realidad virtual (VRML) es un formato de archivo para la representación de objetos del mundo [3D](/es/3d/) interactivos en la World Wide Web (www). Encuentra su uso en la creación de representaciones tridimensionales de escenas complejas, como ilustraciones, definición y presentaciones de realidad virtual. El formato ha sido reemplazado por [X3D](/es/3d/x3d/). Muchas aplicaciones de modelado 3D pueden guardar objetos y escenas en formato VRML.

## Formato de archivo VRML

VRML es un formato de archivo de texto que especifica información como los vértices y los bordes de un polígono 3D junto con información como el color de la superficie, las texturas mapeadas UV, el brillo, la transparencia, etc. Tiene la capacidad de representar objetos estáticos y animados además de tener hipervínculos a otros medios como sonido, películas e imágenes. Esto permite abrir elementos con hipervínculos cuando el usuario hace clic en estos objetos.

Los archivos TVRML en la terminología común se denominan "mundos" y tienen la extensión .wrl. La naturaleza textual de estos archivos permite reducir el tamaño del archivo utilizando formatos de compresión como gzip, haciéndolos más favorables para la transferencia rápida a través de Internet. Las especificaciones de formato de archivo para [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) actúan como referencia del desarrollador para crear aplicaciones compatibles para leer/escribir estos archivos.

## Criterio de diseño ##

El objetivo y el diseño de VRML giran en torno a los siguientes requisitos.

* **Autoridad**: permite desarrollar generadores y editores de aplicaciones e importar datos de otros formatos industriales
* **Integridad**: proporciona toda la información necesaria para la implementación y aborda un conjunto completo de funciones para una amplia aceptación en la industria
* ** Componibilidad **: la capacidad de usar elementos de VRML en combinación y, por lo tanto, permitir la reutilización.
* **Extensibilidad**: la capacidad de agregar nuevos elementos.
* **Implementación** -Capaz de implementación en una amplia gama de sistemas.
* **Potencial multiusuario**: no debe impedir la implementación de entornos multiusuario.
* **Ortogonalidad**: los elementos de VRML deben ser independientes entre sí, o cualquier dependencia debe estar estructurada y bien definida.
* **Rendimiento**: los elementos deben diseñarse con énfasis en el rendimiento interactivo en una variedad de plataformas informáticas.
* **Escalabilidad**: los elementos de VRML deben diseñarse para composiciones infinitamente grandes.
* **Práctica estándar**: solo se deben estandarizar aquellos elementos que reflejan la práctica existente, que son necesarios para respaldar la práctica existente o que son necesarios para respaldar los estándares propuestos.
* **Bien estructurado**: un elemento debe tener una interfaz bien definida y un propósito incondicional simplemente establecido. Deben evitarse los elementos polivalentes y los efectos secundarios.

## Referencias ##

* [VRML - Por Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [Especificaciones de formato de archivo VRML v 2.0] (http://gun.teipir.gr/VRML-amgem/spec/index.html)

