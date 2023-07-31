{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Obtenga información sobre el formato de archivo CSPROJ y las API que pueden crear y abrir archivos CSPROJ",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## ¿Qué es un archivo CSProj?
Los archivos con la extensión CSPROJ representan un archivo de proyecto de C# que contiene la lista de archivos incluidos en un proyecto junto con las referencias a los ensamblados del sistema. Cuando se inicia un nuevo proyecto en Microsoft VIiual Studio, obtiene un archivo .csproj junto con el archivo de la solución principal ([.sln](/es/programming/sln/)). Si hay más de un ensamblaje en un proyecto, también habrá la misma cantidad de archivos de proyecto donde el archivo .sln los une a todos como parte del proyecto. El contenido de este archivo define todos los requisitos necesarios para construir el proyecto, como el contenido que se debe incluir, los requisitos de la plataforma, la información de versiones, la configuración del servidor web o del servidor de base de datos y las tareas que se deben realizar. El contenido de un archivo de proyecto se organiza en formato de archivo XML y se puede abrir en cualquier editor de texto para editarlo y verlo. También ofrece una vista lógica de los archivos del proyecto para una organización adecuada.

## Formato de archivo CSPROJ #

Los desarrolladores pueden crear archivos de proyecto por sí mismos y respetar el [esquema XML de MSBuild](https://msdn.microsoft.com/library/5dy88c2e.aspx). La estructura abierta y transparente de los archivos de proyecto permite a los desarrolladores de aplicaciones imponer un control sofisticado y detallado sobre cómo se construyen e implementan los proyectos. Los contenidos de un archivo de proyecto de este tipo tienen una relación muy clara entre sí. La siguiente figura muestra los elementos clave y la relación entre estos para un archivo de proyecto de este tipo.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Las siguientes secciones elaboran los elementos de formato de archivo para un archivo de proyecto.

### Elemento del proyecto ###

El elemento [Proyecto](https://msdn.microsoft.com/library/bcxfsh87.aspx) es el elemento raíz de cada archivo de proyecto. Identifica el esquema XML para el archivo del proyecto y puede incluir atributos para especificar los puntos de entrada para el proceso de construcción.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Propiedades y Condiciones

Las propiedades representan la información necesaria requerida para construir un proyecto. Dichas propiedades se definen dentro de un elemento [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Estas propiedades constan de pares clave-valor donde el nombre del elemento de propiedad define la clave de la propiedad y el contenido del elemento define el valor de la propiedad. Por ejemplo, podría definir propiedades denominadas ServerName y ConnectionString para almacenar un nombre de servidor estático y una cadena de conexión.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Las condiciones se pueden especificar a través de elementos para especificar los criterios para evaluar el elemento. Esto se especifica mediante la palabra Condición al definir la propiedad como se muestra a continuación:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Cuando MSBuild procesa esta definición de propiedad, primero comprueba si hay disponible un valor de propiedad **$(OutputRoot)**. Si el valor de la propiedad está en blanco, en otras palabras, el usuario no proporcionó un valor para esta propiedad, la condición se evalúa como **verdadera** y el valor de la propiedad se establece en **..\Publish\Out.**

### Artículos y grupos de artículos

Un archivo de proyecto define entradas para el proceso de compilación que en realidad son diferentes tipos de archivos. En la nomenclatura de MSBuild, estas entradas se representan mediante elementos Item y se definen dentro de un elemento [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Al igual que los elementos **Property**, puede nombrar un elemento **Item** como desee. Sin embargo, debe especificar un atributo **Incluir** para identificar el archivo o comodín que representa el elemento.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Objetivos y tareas

Un elemento [Tarea](https://msdn.microsoft.com/library/77f2hx1s.aspx) representa una instrucción (o tarea) de compilación individual. MSBuild incluye una multitud de tareas predefinidas. Por ejemplo:

* La tarea **Copiar** copia archivos a una nueva ubicación.
* La tarea **Csc** invoca el compilador de Visual C#.
* La tarea **Vbc** invoca el compilador de Visual Basic.
* La tarea **Exec** ejecuta un programa específico.
* La tarea **Mensaje** escribe un mensaje en un registrador.

Las tareas siempre deben estar contenidas dentro de los elementos [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Un elemento **Objetivo** es un conjunto de una o más tareas que se ejecutan secuencialmente, y un archivo de proyecto puede contener varios objetivos.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referencias

* [Comprender el archivo del proyecto - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- expediente)

