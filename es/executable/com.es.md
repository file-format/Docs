{
  "date" : "2021-06-29",
  "keywords" :[ "archivo com", "qué es un archivo com", "archivo", "ejemplo com", "extensión de archivo com", "extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo COM y las API que pueden crear y abrir archivos COM",
  "title" :"COM - Formato de archivo de comando DOS",
  "linktitle" : "COM",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo COM?
Los archivos COM simplemente se utilizan para ejecutar un conjunto de comandos o instrucciones. Un archivo COM consta de un programa ejecutable que se puede ejecutar desde Windows o MS-DOS. Al igual que un archivo EXE, el archivo COM también se guarda en formato binario, pero es diferente al archivo EXE porque no tiene encabezado ni metadatos y también tiene un tamaño máximo de 64 KB aproximadamente. Cuando el archivo COM se ejecuta por primera vez en un sistema de 32 bits, solicita la instalación del componente NT Virtual DOS Machine (NTVDM). El archivo COM se puede ejecutar en la versión de 64 bits de Microsoft Windows con una máquina virtual compatible con el entorno MS-DOS.

## formato de archivo COM
El formato de archivo COM es un formato ejecutable binario utilizado en Microsoft Windows o MS-DOS. Su estructura consiste en solo un conjunto de instrucciones; no tiene encabezado y no contiene metadatos estándar. Almacena todos sus datos y código en un solo segmento y su binario tiene un tamaño máximo de 64 KB. Este formato de archivo no se reubica cuando se intenta volver a ejecutar. Entonces el sistema operativo lo carga en una dirección preestablecida. Además, es posible hacer que un archivo COM se ejecute en ambos sistemas operativos en forma de un **binario pesado**. No hay ninguna compatibilidad real a nivel de instrucción. Las instrucciones en el punto de entrada se seleccionan para que sean iguales en funcionalidad pero diferentes en ambos sistemas operativos y hacen que el programa en ejecución salte a la sección del sistema operativo en uso. Básicamente se trata de dos programas diferentes con el mismo procedimiento en un solo archivo, precedido de código seleccionando el que se va a utilizar.
### Ejemplo de archivo COM
Al ejecutar un archivo COM, las instrucciones se leen desde el primer byte y se siguen consecutivamente hasta encontrar las últimas instrucciones. Aquí hay un ejemplo de código ASM:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## Referencias

* [archivo COM - por Wikipewdia](https://en.wikipedia.org/wiki/COM_file)

