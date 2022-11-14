{
  "date" : "2021-06-30",
  "keywords" :[ "archivo msi", "formato de archivo MSI", "qué es un archivo msi", "archivo", "ejemplo de msi", "extensión de archivo msi","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MSI y las API que pueden crear y abrir archivos MSI",
  "title" :"MSI - Archivo de paquete del instalador de Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## ¿Qué es un archivo MSI?
Un archivo MSI utilizado para instalar y ejecutar programas de Windows; un paquete completo para Microsoft Windows que contiene información de instalación para un programa de software típico, incluidos los archivos esenciales que se instalarán e información sobre la ubicación de la instalación. Los archivos MSI también pueden contener el paquete de actualizaciones de software. Los archivos MSI son similares a [EXE](/es/executable/exe/), pero es posible que EXE en algún momento no incluya la información del instalador y el programa de software puede ejecutarse directamente cuando se ejecuta el archivo EXE.

## formato de archivo MSI
Windows Installer es en realidad una API (interfaz de programación de aplicaciones) y un componente de software de Microsoft Windows que se utiliza para la instalación, eliminación y mantenimiento de un programa de software. La información de instalación y los archivos opcionales se empaquetan como paquetes de instalación y bases de datos relacionales flexibles estructuradas como almacenamientos estructurados COM; conocidos como **archivos MSI**, con la extensión de archivo .msi. Los paquetes con la extensión de archivo **.mst** contienen **Transformation Scripts** de Windows Installer, los archivos con la extensión **.msm** contienen **Merge Modules** y la extensión de archivo **.pcp** se utiliza para **Propiedades de creación de parches**. Windows Installer se vuelve más avanzado después de tener cambios significativos con respecto a sus versiones anteriores, la API de configuración. Un marco GUI y la generación automática de la secuencia de desinstalación son las nuevas características de Windows Installer. Se ha considerado ahora como una alternativa a los marcos de instalación ejecutables independientes.

### Estructura lógica de paquetes MSI
Un paquete designa la instalación de uno o más productos completos y generalmente se identifica mediante un **GUID**. Un producto se compone de uno o varios componentes y se agrupa en varias características. Windows Installer no maneja dependencias entre varios productos simultáneamente. La estructura lógica de los paquetes consta de los siguientes elementos:

- **Productos**: un único programa de trabajo instalado o un conjunto de múltiples programas combinados juntos es un producto. Un producto se identifica mediante un GUID único.
- **Características**: puede contener cualquier cantidad de componentes y otras subcaracterísticas. Los paquetes más pequeños pueden consistir en una sola función.
- **Componentes**: Windows Installer trata el componente como una unidad; puede contener archivos de programa, carpetas, claves de registro, componentes COM y accesos directos.
- **Rutas clave**: una ruta clave es un archivo específico, una fuente de datos ODBC o una clave de registro que el autor del paquete especifica como fundamental para un componente determinado.

## Referencias

* [Instalador de Windows - por Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


