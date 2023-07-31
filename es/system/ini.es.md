{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "extensión", "archivo", "formato", "sistema", "Iniciación", "extensión de directorio", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Formato de archivo de inicio",
  "description":"Obtenga información sobre el formato de archivo INI y las API que pueden crear y abrir archivos INI",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## ¿Qué es un archivo INI? ##

Un archivo INI es un documento de configuración de mensajes para programas informáticos que contiene claves públicas para características y secciones que organizan los atributos en un marco y una gramática. Estos documentos de configuración de formato de archivo del sistema obtienen su nombre de la extensión de directorio INI del sistema operativo MS-DOS, que significa iniciación. Popularizó esta forma de configuración de software. Muchos programas en otras aplicaciones de software usan varias adiciones de nombre de archivo, como CONF y [CFG](/es/system/cfg/), aunque el formato ha establecido un estándar no oficial en muchas situaciones de configuración.

## Breve historia de los archivos INI##

Inicialmente, la principal técnica de configuración de programas de Windows era un formato de archivo de texto que constaba de líneas de texto con un par crucial por línea, divididas en secciones. Los controladores de dispositivos, los tipos de letra y los lanzadores de inicio se almacenaron en este formato. Las configuraciones individuales también se almacenaban comúnmente en archivos INI por aplicaciones.
Hasta Windows 3.1x, el formato era compatible con plataformas Microsoft Windows de 16 bits. A partir de Windows 95, Microsoft comenzó a animar a los desarrolladores a utilizar el Registro de Windows en lugar de los archivos INI para la configuración.

## Archivo INI - Especificaciones de formato de archivo

### Claves/Propiedades ###

La clave/propiedad es el elemento más básico de un archivo INI. Un símbolo de igual (=) separa el nombre y el valor de cada clave. A la izquierda del signo igual es donde se muestra el nombre. El símbolo igual y el punto y coma son letras discretas en el sistema de Windows, por lo que no se pueden usar en la clave. Se puede utilizar cualquier carácter en el valor.

```
name=value
```

### Secciones ###

El comentario de la sección aparece entre corchetes ([]) en su propia línea. Después de la definición de la sección, todas las claves están vinculadas a esa sección. Las secciones terminan en la siguiente designación de sección o al final del documento; no hay un separador específico de "final de sección". Las secciones no se pueden apilar; solo se pueden nombrar una vez y no es necesario vincularlos.

```
[section]
a=a
b=b
```

### Cambio de funciones ###

El formato de archivo INI no tiene una definición aceptada globalmente. Muchas aplicaciones informáticas incluyen funciones adicionales a las ya mencionadas. La lista a continuación incluye algunas características comunes que pueden o no estar incluidas en cualquier programa individual.

* Comentarios
* Personajes de escape
* Nombres duplicados


## Ejemplo INI ##

El archivo INI de muestra tiene el siguiente aspecto:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Referencia ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

