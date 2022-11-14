{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","qué es un archivo cd","cómo abrir un archivo cd", "extensión", "archivo", "archivo cd","formato de archivo cd", "extensión de archivo cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Archivo de diagrama de clases de Visual Studio",
  "description":"Obtenga información sobre el formato de archivo de CD y las API que pueden crear y abrir archivos de CD",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## ¿Qué es un archivo de CD?

Un archivo con extensión .cd es un archivo de diagrama de clase de Visual Studio que proporciona información sobre la estructura y la relación entre todas las clases en la solución actual. Una solución de Visual Studio (representada por [.sln](/es/programming/sln/)) puede contener uno o más proyectos, cada uno con varias clases diferentes. El archivo de diagrama de clase se puede generar haciendo clic derecho en el proyecto y seleccionando la opción de diagrama de clase.

## Formato de archivo de diagrama de clase (.cd): más información

Un archivo de diagrama de clases se guarda en un formato de archivo XML estándar que representa las clases en un proyecto como nodos XML. Si Visual Studio no está disponible, estos archivos de diagrama de clase se pueden abrir en cualquier programa de aplicación que admita la apertura de archivos XML.

### Cómo agregar diagramas de clase al proyecto de Visual Studio

En Visual Studio, abra la Solución/Proyecto para el que desea agregar el diagrama de clases. Luego, haga clic con el botón derecho en el nodo del proyecto y luego elija Agregar > Nuevo elemento. O bien, presione Ctrl+Mayús+A.

* Se abre el cuadro de diálogo Agregar nuevo elemento.

* Expanda Elementos comunes > General y luego seleccione Diagrama de clase de la lista de plantillas. Para proyectos de Visual C++, busque en la categoría Utilidad para encontrar la plantilla Diagrama de clase.

### Exportación de diagramas de clase (CD) a imágenes

Visual Studio permite convertir/exportar diagramas de clase a imágenes como [PNG](/es/image/png/), [JPEG](/es/image/jpeg/) y [BMP](/es/image/bmp/). Estos archivos de diagramas de clase exportados se pueden utilizar para la documentación y el mantenimiento de registros del paquete de datos técnicos (TDP). Para convertir un diagrama de clases en una imagen, se pueden utilizar los siguientes pasos desde Microsoft Visual Studio.

1. Abra su archivo de diagrama de clase (.cd).
1. En el menú Diagrama de clase o el menú contextual de la superficie del diagrama, seleccione Exportar diagrama como imagen.
1. Seleccione un diagrama.
1. Seleccione el formato que desee.
1. Elija Exportar para finalizar la exportación.

## Referencias

* [Clases de diseño en Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

