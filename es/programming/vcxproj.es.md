{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "archivo", "extensión", "formato de archivo", "Proyecto Visual C++", "Guía de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PROJVCX",
  "description":"Obtenga más información sobre el formato de archivo VCXPROJ y las API que pueden crear y abrir archivos VCXPROJ",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo VCXPROJ?

Un archivo con la extensión .vcxproj es un archivo de proyecto de Microsoft Visual C++ que almacena la información del proyecto [C++](/es/programming/cpp/). Contiene información que utiliza el sistema de proyectos MSBuild para compilar y crear el resultado final. VCXPROJ de proyectos de Visual C++ es el mismo que el de [CSPROJ](/es/programming/csproj/) para proyectos .NET. Los archivos VCXPROJ no contienen ningún código, pero se refieren a todas las clases, objetivos y propiedades definidas para el proyecto para construir el proyecto. Estos se pueden abrir en editores de texto sin formato o, preferiblemente, en Microsoft Visual Studio IDE.


## Formato de archivo VCXPROJ - Más información

Los archivos VCXPROJ son archivos de texto que se crean en formato de archivo [XML](/es/web/xml/). Estos se pueden abrir en cualquier editor de texto, pero se recomienda encarecidamente utilizar Microsoft Visual Studio IDE para abrir y editar estos archivos. Estos no fueron diseñados para la edición manual. Los errores pueden hacer que el IDE se bloquee o se comporte de forma inesperada.

El contenido de un archivo VCXPROJ de muestra es el siguiente.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Elementos del archivo VCXPROJ

Un archivo VCXPROJ típico contiene una serie de elementos, como se puede ver en el ejemplo XML anterior. La [estructura VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) de Microsoft explica cada elemento del archivo en detalle y se puede consultar desde la perspectiva del desarrollador.

#### Elemento del proyecto

Este es el nodo raíz del archivo VCXPROJ. MSBuild usa este elemento para leer la versión de compilación y el destino predeterminado para la compilación.

#### Elemento de grupo de elementos de configuraciones de proyecto

Contiene la información de configuración del proyecto que puede incluir el método de compilación (depuración o lanzamiento), compilación de 32 o 64 bits, opciones de optimización y otros. El IDE utiliza la información de este grupo para cargar el proyecto.

#### Elementos de configuración del proyecto

Los elementos de ProjectConfiguration en un archivo VCXPROJ contienen información sobre la compilación y la plataforma para la que se carga el proyecto. Su nombre debe seguir el formato `$(Configuración)|$(Plataforma)`.

#### Elemento de grupo de propiedades globales

Esta sección contiene configuraciones que brindan información para el nivel del proyecto, como:

* ProjectGuid
* Espacio de nombres raíz
* Tipo de aplicación o Revisión del tipo de aplicación


## Referencias

* [Estructura VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Archivos de proyecto de C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

