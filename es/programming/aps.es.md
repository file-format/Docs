{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Archivo de recursos de Visual C++",
  "description":"Obtenga información sobre el formato de archivo APS con el ejemplo de APS y las API que pueden crear y abrir archivos APS",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## ¿Qué es un formato de archivo APS?
Un archivo APS es creado por Visual C++, una aplicación de desarrollo de software de Microsoft. Guarda la representación binaria de un recurso incorporado con el proyecto y permite que la aplicación cargue recursos más rápidamente. Puede encontrar fácilmente estos archivos con la extensión de archivo .aps. De hecho, los editores de recursos no leen directamente los archivos resource.h, por eso el compilador de recursos los compila en archivos .aps que consumen los editores de recursos.

## formato de archivo APS
El formato de archivo APS es solo un paso de compilación y solo almacena datos simbólicos. La información no simbólica, como los comentarios, se descarta durante el proceso de compilación. Por ejemplo, cuando guarda, el editor de recursos sobrescribe el archivo de script de recursos y el archivo resource.h. Cualquier cambio en los propios recursos permanece incorporado en el archivo de script de recursos, pero los comentarios siempre se perderán una vez que se sobrescriba el archivo de script de recursos.


## Referencias

* [Archivos de recursos (C++)](https://docs.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


