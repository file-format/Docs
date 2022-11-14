{
  "date" : "2021-08-13",
  "keywords" :[ "archivo sdi", "formato de archivo sdi", "qué es un archivo sdi", "archivo", "ejemplo sdi", "extensión de archivo sdi","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo SDI y las API que pueden crear y abrir archivos SDI",
  "title" :"SDI - Archivo de imagen de implementación del sistema de Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## ¿Qué es un archivo SDI?
El archivo con la extensión .sdi contiene un blob de carga, un blob de arranque y un blob de parte; comúnmente utilizado por Windows Embedded Studio para crear discos RAM o discos de arranque para cargar e instalar Windows. SDI se abrevia para Imagen de implementación del sistema. Windows Embedded Studio es un programa utilizado para crear imágenes de disco para Windows. En realidad, este programa contiene el programa Administrador de archivos SDI y una herramienta de línea de comandos llamada **sdimgr.exe**, ambos se pueden usar para distribuir, crear y editar imágenes SDI.

## formato de archivo SDI
El formato de archivo SDI se usa ampliamente para habilitar el uso de un disco virtual para iniciar un sistema. Algunas versiones de Microsoft Windows permiten el **arranque de RAM**, lo cual es importante para cargar un archivo SDI en la memoria y luego arrancar desde allí. El formato de archivo SDI también se habilita para el arranque en red mediante el PXE (entorno de ejecución previo al arranque). También se está utilizando para la creación de imágenes del disco duro.
### Secciones de archivos SDI
El archivo SDI en sí se puede subdividir en las siguientes secciones:
- **Boot BLOB**: contiene el programa de arranque real, STARTROM.COM. Este es un análogo al sector de arranque de un disco duro.
- **Cargar BLOB**: normalmente contiene NTLDR y lo inicia el BLOB de arranque.
- **Parte BLOB**: contiene el tiempo de ejecución de arranque real; también incluye los archivos boot.ini y ntdetect.com que deben estar ubicados dentro del directorio raíz del tiempo de ejecución.
- **Disk BLOB**: esta es una imagen HDD plana que comienza con un MBR. Se utiliza para crear imágenes del disco duro en lugar de arrancar. Además, solo se pueden montar discos BLOB con las utilidades de Microsoft.


## Referencias

* [Imagen de implementación del sistema - por Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


