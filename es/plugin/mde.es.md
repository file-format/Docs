{
  "date" : "2023-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo MDE: ¿Qué es un archivo MDE y cómo abrirlo?",
  "description":"Obtenga más información sobre el formato de archivo MDE y las API que pueden crear y abrir archivos MDE.",
  "linktitle" : "MDE",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-es-mde"
    }
  },
  "lastmod" : "2023-12-03"
}

¿Qué es un archivo MDE?

Un archivo .MDE es una versión compilada de una base de datos de Access (.mdb o .accdb). Cuando compila una base de datos de Access en un archivo .MDE, ya no se puede editar con las herramientas de diseño estándar de Access. El objetivo principal de crear un archivo .MDE es distribuir una aplicación de base de datos sin exponer el código fuente original.

## Formato de archivo MDE

Un archivo MDE se crea compilando el código VBA, formularios, informes y otros objetos. Esto da como resultado la creación del formato de archivo binario MDE. El archivo .MDE resultante se puede distribuir a los usuarios que pueden ejecutar la aplicación pero no pueden modificar el diseño ni ver el código original. El archivo MDE es en realidad la versión compilada de un [archivo .MDA](/database/mda/). La distribución de archivos .MDE puede ayudar a proteger la propiedad intelectual al evitar que los usuarios accedan o modifiquen el código fuente. También puede mejorar el rendimiento a medida que el código se compila y optimiza.

## Referencias

* [Especificaciones de acceso](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [La guía no oficial de MDB](http://jabakobob.net/mdb/)
