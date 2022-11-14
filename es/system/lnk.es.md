{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "extensión", "archivo", "formato", "sistema", "archivo LNK", "enlace", "archivos LNK", "documentos LNK", "aplicación", "programas" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Formato de archivo de enlace",
  "description":"Obtenga información sobre el formato de archivo LNK y las API que pueden crear y abrir archivos LNK",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## ¿Qué es un archivo LNK? ##

Un archivo LNK, análogo a una identidad en el sistema Mac, es una alternativa de Windows o "enlace" que sirve como conexión a una carpeta o programa de documento de imagen original. Contiene el tipo, la posición y el nombre de archivo del destino del acceso directo, así como la aplicación que abre el documento de destino y una tecla de acceso directo adicional.

En Windows, dirija un archivo, carpeta o programa ejecutable y seleccione Crear acceso directo. La ubicación del formato de archivo y el directorio "Comienzo" son dos características básicas de los archivos LNK. El formato de archivo de los archivos LNK está enmascarado y una flecha curva indica que son accesos directos.

## Formato de archivo LNK ##

Los formatos de archivo LNK generalmente tienen el mismo ícono que sus archivos de destino, pero con la adición de una pequeña flecha curvada para mostrar que el archivo apunta a una ubicación diferente. Cuando se hace doble clic en el acceso directo, se comporta como si el usuario hubiera hecho doble clic en el archivo real.

Los archivos LNK que contienen accesos directos a aplicaciones pueden tener propiedades que afectan la forma en que se ejecuta el programa. Para cambiar los atributos, haga clic con el botón derecho en el archivo de acceso directo y elija **Propiedades**, luego cambie el campo Destino.

En lugar de ser extensiones de archivo, los archivos LNK son extensiones del Explorador de Windows. Como extensión de terminal, los documentos .lnk solo se pueden usar en el Explorador de Windows para sustituir un archivo, y tienen otros propósitos en el Explorador de Windows además de servir como acceso directo a un documento local. Estos archivos también comienzan con la letra "L".

Si bien los accesos directos se vinculan a archivos y directorios específicos cuando se crean, pueden volverse inoperables si el destino se cambia a una ubicación diferente. Explorer comenzará a reparar una carpeta de acceso directo que apunta a un objetivo muerto cuando se abre.


## Especificación técnica ##

Solo cuando la configuración de visualización de carpetas "Ocultar extensiones para tipos de archivos reconocidos" no está marcada, Windows no muestra la extensión de documento .lnk para accesos directos de documentos. Si bien no se recomienda, puede habilitar la visualización de la extensión del archivo eliminando la propiedad "NeverShowExt" del elemento de registro de Windows del archivo HKEY_CLASSES_ROOT\lnk.

Para hacerlo, siga estos pasos:

* Abra el "Editor de registro" ingresando "Regedit" en el campo de búsqueda de la barra de tareas y eligiendo el programa
* En la aplicación, vaya a la ubicación Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Haga una copia de seguridad del elemento haciendo clic con el botón derecho y seleccionando Exportar
* Seleccione y elimine el atributo "NeverShowExt"
* Se debe reiniciar Windows


## Referencia ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
