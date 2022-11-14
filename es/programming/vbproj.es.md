{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "archivo", "extensión", "formato de archivo", "Archivo de proyecto VB", "Guía de programación" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Obtenga más información sobre el formato de archivo VBPROJ y las API que pueden crear y abrir archivos VBPROJ",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo VBPROJ?

Un archivo con la extensión .vbproj es un archivo de proyecto de Microsoft Visual Basic que utiliza el motor MSBuild de Microsoft para crear los proyectos dentro de una solución de Visual Studio. Es similar al archivo [CSPROJ](/es/programming/csproj/) para proyectos .NET escritos en [C#](/es/programming/cs/). El motor de MSBuild lee la información contenida en diferentes grupos de los archivos VBPROJ y genera el archivo de salida. Un archivo VBPROJ puede contener información relacionada con identificadores globales, clases y propiedades que definen el proyecto. Los archivos VBPROJ se pueden abrir y editar con Microsoft Visual Studio y cualquier editor de texto común, como el Bloc de notas en los sistemas operativos Windows y MacOS.

## Formato de archivo VBPROJ - Más información

Los archivos VBPROJ son archivos de texto escritos en formato de archivo [XML](/es/web/xml/) basado en el [Esquema XML de MSBuild](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild- proyecto-archivo-esquema-referencia?view=vs-2019). Un archivo VBPROJ contiene información en forma de etiquetas XML que definen información relacionada con ese grupo particular de configuraciones. Se recomienda encarecidamente abrir y editar estos archivos de configuración en Microsoft Visual Studio IDE.

### Elementos VBPROJ

Los elementos constituyentes de un archivo de configuración de VB se muestran en la siguiente imagen.

{{< figure src="../vbproj.png" alt="Formato de archivo VBPROJ" >}}

La siguiente tabla da una breve descripción de estos elementos.

|Elemento|Descripción|
---|---|
|Proyecto| Elemento raíz de cada archivo de proyecto y puede incluir atributos para especificar los puntos de entrada para el proceso de compilación además de identificar el esquema XML para el archivo de proyecto |
|Propiedades y Condiciones| Las propiedades consisten en pares clave-valor y se definen dentro de un elemento PropertyGroup. El nombre del elemento de propiedad representa la clave de la propiedad y el contenido del elemento define el valor de la propiedad.|
|Elementos y grupos de elementos|Los elementos de un archivo de proyecto son entradas para el proceso de creación, como archivos de código de archivos, archivos de configuración, archivos de comandos y otros necesarios como parte del proceso de creación. Los artículos están y deben estar definidos dentro de un elemento ItemGroup.|
|Objetivos y tareas| Un elemento Task representa una instrucción (o tarea) de compilación individual. MSBuild incluye una multitud de tareas predefinidas como Copiar, CSC, VBC, Exec. Las tareas siempre deben estar contenidas en un elemento `Objetivo`, que es un conjunto de una o más tareas que se ejecutan secuencialmente, y un archivo de proyecto puede contener varios objetivos.|

## Referencias

* [Comprender el archivo del proyecto](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elementos del esquema de MSBuild](https://docs.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

