{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo MASTER - Formato de archivo de página maestra ASP.NET",
  "description" :"Obtenga más información sobre el formato de archivo MASTER y las API para crear y abrir archivos MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## ¿Qué es un archivo MAESTRO?

Un archivo MASTER es un archivo de plantilla de página web maestra creado con ASP.NET. Se utiliza como punto de partida para crear varias páginas que tienen el mismo diseño y configuración que el archivo MASTER. El archivo MASTER de plantilla incluye configuraciones para encabezado, menús de navegación, pie de página, fuente e información de estilo. El uso de un archivo MASTER ayuda a crear varias páginas web rápidamente.

Puede abrir un archivo MASTER usando Microsoft Visual Studio 2022 y superior.

## Formato de archivo MASTER - Más información

Un archivo MASTER se crea y guarda en formato de archivo HTML y es similar a cualquier otro archivo de página web. Está dividido en secciones editables y no editables. Las secciones editables son las que se pueden modificar para satisfacer los requisitos del usuario. Las secciones no editables aparecen atenuadas cuando el archivo MASTER se abre en Microsoft Visual Studio.

Las páginas maestras constan de dos partes, es decir, la propia página maestra y una o más páginas de contenido.

### Página principal

La página maestra tiene extensión .master y está realizada en ASP.NET. Tiene un diseño predefinido que consta de texto estático, etiquetas HTML y controles del lado del servidor. En páginas .aspx normales, se utiliza la directiva @ Page. En el caso de archivos .master, esto se reemplaza por la directiva @ Master.

### Páginas de contenido

Una página de contenido representa el contenido de los controles de marcador de posición de la página maestra. Estas son páginas .aspx que en realidad son el código subyacente de la página maestra. Las páginas de contenido se vinculan mediante la directiva @ Page al incluir un atributo MasterPageFile que apunta a la página maestra que se utilizará como se muestra a continuación.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referencias

* [Descripción general de las páginas maestras de ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

