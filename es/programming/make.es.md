{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Crear archivo: archivo de secuencia de comandos Makefile de Xcode",
  "description":"Obtenga más información sobre el formato XCode MakeFile y las API que pueden crear y abrir archivos MakeFile",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## ¿Qué es un archivo MAKE?

Un archivo MAKE es un archivo de script XCode que organiza la compilación de código. Se utiliza para compilar y vincular programas de múltiples archivos de código fuente. Esta ayuda decide qué partes de una aplicación grande deben volver a compilarse cuando la aplicación necesita actualizarse. Haga que los archivos usen una serie de instrucciones para ejecutarse según los archivos que hayan cambiado.

## Ejemplo de formato de archivo MAKE

El siguiente contenido se ejecuta usando la utilidad Make y las salidas son las siguientes.

```
hello:
	echo "hello world"
```
**Hacer salida**

```
$ make
echo "hello world"
hello world
```

## Referencias
* [XCode y Make - Foros de Apple](https://developer.apple.com/forums/thread/657458)
* [Guía de Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

