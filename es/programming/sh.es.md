{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Archivo de secuencia de comandos Bash Shell",
  "description":"Obtenga información sobre el formato de archivo SH y las API que pueden crear y abrir archivos SH",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## ¿Qué es un archivo SH?

Un archivo con la extensión .sh es un archivo de comandos de lenguaje de secuencias de comandos que contiene un programa de computadora para ser ejecutado por el shell de Unix. Puede contener una serie de comandos que se ejecutan secuencialmente para realizar operaciones como procesamiento de archivos, ejecución de programas y otras tareas similares. Estos se ejecutan desde la interfaz de línea de comandos por el usuario o por lotes para realizar múltiples operaciones al mismo tiempo. Los archivos de script se pueden abrir en editores de texto como Notepad, Notepad ++, Vim, Apple Terminal y otras aplicaciones similares en Windows, MacOS y Linux OS.

## Formato de archivo SH

Los archivos SH se escriben en texto sin formato siguiendo la sintaxis definida. Estos archivos de script admiten:

* `Comentarios`: los comentarios comienzan con un # y el shell los ignora.
* `Accesos directos`: se pueden usar para cambiar el nombre de un comando para una ejecución breve y sencilla.
* `Trabajos por lotes`: se pueden ejecutar automáticamente varios comandos que, de lo contrario, se tendrían que introducir manualmente. Esto elimina la necesidad de esperar a que un usuario active cada etapa de la secuencia.
* 'Generalización': al usar bucles simples, se logra mucha más generalización para operaciones como la conversión de imágenes de un fromat a otro.

## Ejemplo de archivo SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## ¿Cómo ejecutar el archivo SH?
Los archivos SH generalmente se ejecutan en Linux, incluso en Windows, debe conectarse con un terminal Linux usando software como Putty para ejecutar los archivos sh. Los siguientes son los pasos para ejecutar un archivo SH en una terminal Linux.

1. Abra la terminal de Linux y vaya al directorio donde se encuentra el archivo SH.
2. Al usar el comando `chmod`, configure el permiso de ejecución en su secuencia de comandos (si aún no lo ha configurado).
3. Ejecute el script usando uno de los siguientes
1. `./nombre de archivo.sh`
2. `sh nombre de archivo.sh`
3. `nombre-guión-bash-aquí.sh`

## Referencias

* [Bashscripting para principiantes](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

