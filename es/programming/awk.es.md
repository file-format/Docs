{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo AWK - Archivo de secuencia de comandos AWK",
  "description":"Obtenga información sobre el formato de archivo AWK y las API que pueden crear y abrir archivos AWK",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## ¿Qué es un archivo AWK?

Un archivo AWK es un archivo de script creado para la aplicación de procesamiento de texto **AWK** que viene con los sistemas operativos Unix y Linux. Contiene instrucciones lógicas para realizar acciones en el texto o el contenido de un archivo, como hacer coincidir, reemplazar e imprimir texto. Esto ayuda a generar informes y texto formateado desde el archivo de entrada. La utilidad awk generalmente se encuentra en /usr/bin/awk en la mayoría de las distribuciones de Linux/Unix.

## ¿Cómo crear un script AWK?

Un archivo AWK se puede crear o abrir en cualquier editor de texto en el sistema operativo Linux/Unix. Se puede crear un nuevo archivo de script AWK de la siguiente manera.

```
$ vi script.awk
```

Esto abrirá el archivo AWK en el editor de texto. Ingrese algunas declaraciones en el editor de texto de la siguiente manera.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
La primera línea del contenido de este texto se explica de la siguiente manera.

* \#! – denominado `Shebang`, que especifica un intérprete para las instrucciones en un script
* /usr/bin/awk – es el intérprete
* -f – opción de intérprete, utilizada para leer un archivo de programa

## ¿Cómo ejecutar el script AWK?

Guarde el archivo y haga que el script sea ejecutable emitiendo el siguiente comando:
```
$ chmod +x script.awk
```

El script se puede ejecutar de la siguiente manera.

```
$ ./script.awk
```

que da como resultado el siguiente resultado.

```
Writing my first Awk executable script!
```

## Referencia ##

* [Escribir scripts utilizando el lenguaje de programación Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

