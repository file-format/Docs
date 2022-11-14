{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "Lenguaje de marcado de objetos extensible"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Formato de archivo de flujo de trabajo de Windows",
  "description":"Obtenga información sobre el formato de archivo XOML y las API que pueden crear y abrir archivos XOML",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo XOML?

XOML es el acrónimo de Extensible Object Markup Language y es un formato de serialización para los objetos de flujo de trabajo de Windows Workflow Foundation. Basado en **[XAML](/es/web/xaml/)**, se utiliza principalmente para crear interfaces de usuario en **[XML](/es/web/xml/)** sin formato. Estos se utilizan para declarar el flujo de trabajo para la interfaz de usuario y se compilan junto con el archivo separado que contiene la lógica de implementación. Contiene una estructura basada en árbol que define un nodo de flujo de trabajo raíz, subelementos anidados y segmentos de código incrustados. Cuando se crea un nuevo flujo de trabajo con Visual Studio para .NET, tiene la opción de elegir si debe estar en formato de código o en formato de código separado. En caso de que seleccione el último, el IDE creará dos archivos para usted; uno en formato XOML (que consiste en el diseño y la configuración del flujo de trabajo), y otro en formato [.CS](/es/programming/cs/)/[.VB](/es/programming/vb/) donde reside el código de programación.

