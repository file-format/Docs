{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Obtenga información sobre el formato de archivo SLN y las API que pueden crear y abrir archivos SLN",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es el archivo SLN?
Un archivo con extensión .SLN representa un archivo de **solución de Visual Studio** que guarda información sobre la organización de proyectos en un archivo de solución. El contenido de dicho archivo de solución está escrito en texto sin formato dentro del archivo y se puede observar/editar abriendo el archivo en cualquier editor de texto. La información contenida en un archivo de solución permanece persistente y se usa para cargar la información asociada con la solución, como [proyectos](/es/programación/csproj/) y cualquier otra información requerida. Los archivos de proyecto a los que hace referencia el archivo de solución contienen información adicional para permitir que el entorno complete la jerarquía con los elementos de ese proyecto. No se almacenan datos en el archivo .sln, aunque la información del proyecto se puede escribir en el archivo .sln si es necesario.

## **Historial de versiones de SLN** ##

La versión del formato de la solución ha evolucionado con cada solución de Microsoft Visual Studio con el paso del tiempo. Los detalles sobre estos son los siguientes.


|Versión de Visual Studio|Versión de formato de solución
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Contenido de un archivo de solución** ###

Un archivo de solución consta de varias secciones que el entorno lee para cargar el proyecto. El contenido de un archivo .sln de muestra se muestra a continuación.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Declaración de proyecto** ###

Un archivo de solución puede contener más de una declaración de proyectos y también de diferentes tipos de proyectos. Por ejemplo, un solo archivo de solución puede contener un proyecto CSharp y VB.NET. Estos tipos se distinguen en una solución mediante el [GUID de tipo de proyecto](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). La declaración del proyecto anterior se puede generalizar de la siguiente manera para una comprensión clara.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID es único para diferentes tipos de proyectos y el lector de soluciones lo utiliza para identificar el tipo de proyecto. En este caso, F184B08F-C81C-45F6-A57F-5ABD9991F28F muestra que es un proyecto de VB.NET.

`GUID del proyecto:` El GUID único del proyecto que lo diferencia de otros proyectos en la solución. El identificador único de un proyecto en la solución hace posible que otros proyectos en la solución accedan a él.

Según la información contenida en la sección del proyecto del archivo .sln, el entorno carga cada archivo de proyecto. El proyecto en sí es responsable de llenar la jerarquía del proyecto y cargar cualquier proyecto anidado. Todos los cambios realizados en la solución se guardan en el archivo de la solución al guardar o cerrar el proyecto.

## Solución de Visual Studio VS proyecto

**Proyecto:** Lógicamente, cuando comienza a crear una aplicación o software con Visual Studio, inicia un nuevo proyecto. Un proyecto contiene todos los archivos necesarios, como código fuente, íconos, imágenes, archivos de datos y más, que se compilarán en una aplicación ejecutable, un sitio web o una biblioteca.

**Solución:** Una solución contiene uno o más proyectos. Entonces, la solución es como un contenedor para proyectos de Visual Studio. Lógicamente, podemos decir que alguien quiere obtener una solución completa para su negocio que incluya un sitio web, una aplicación de escritorio, un servicio tranquilo y una aplicación móvil.

### **Referencias** ###

* [Archivo de solución: por MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID de tipo de proyecto](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

