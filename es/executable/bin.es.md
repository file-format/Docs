{
"fecha": "2023-07-20",
   "keywords":[
"PAPELERA",
"Archivo BIN",
"archivo",
"Extensión de archivo BIN",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo BIN: archivo ejecutable Unix",
   "description":"Obtenga más información sobre el formato BIN y las API que pueden crear y abrir archivos BIN.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent" : "executable"
}
},
"último mod": "2023-07-20"
}

## ¿Qué es un archivo BIN?

Un archivo BIN es un archivo ejecutable en sistemas operativos basados en Unix, como Linux o FreeBSD. Contiene un programa compilado compuesto de código binario derivado del código fuente, lo que lo hace compatible con la arquitectura del sistema subyacente. Los archivos BIN ejecutables de Unix se pueden comparar con los archivos .EXE de Windows y los archivos .APP de macOS en términos de su función como formatos ejecutables.

En el ámbito del desarrollo de software para sistemas Unix, los desarrolladores suelen utilizar archivos BIN para empaquetar y distribuir programas. Ofrecen un medio conveniente para entregar software a los usuarios, permitiendo una fácil instalación y ejecución. Además de los archivos BIN, existen otros tipos de ejecutables de Unix, incluidos [.ELF](/es/executable/elf/), .X86, [.RUN](/es/executable/run/) y .X86_64, cada uno de ellos adaptado a hardware o Requisitos del sistema.

Cuando se trata de la estructura interna de un archivo BIN, consta de datos codificados que el sistema operativo Unix utiliza para identificar, leer y ejecutar el programa adjunto. El sistema se basa en firmas o encabezados de archivos específicos para reconocer el archivo BIN como un ejecutable, seguido de la interpretación y ejecución de las instrucciones binarias contenidas en él.

Los archivos BIN a menudo vienen con un archivo **INSTALL.TXT** adjunto, que proporciona instrucciones detalladas sobre cómo instalar y configurar correctamente el programa. Esta documentación garantiza que los usuarios puedan navegar con éxito por el proceso de instalación y comenzar a utilizar el software sin complicaciones.

## ¿Cómo abrir el archivo BIN?

Los archivos BIN no están diseñados para abrirse y verse directamente. Sin embargo, puedes ejecutar los programas o extraer los datos que contienen. Para acceder al contenido de un archivo BIN, siga estos pasos en la línea de comando, asumiendo que el nombre del archivo BIN es "sample.bin":

1. **Asegurar permisos ejecutables:**

Antes de ejecutar el archivo BIN, asegúrese de que tenga los permisos necesarios para ejecutarse como ejecutable. Utilice el comando:

```
$ chmod +x sample.bin
```

Este comando otorga privilegios ejecutables al archivo.

2. **Ejecute el archivo BIN:**

Después de configurar los permisos ejecutables, puede ejecutar el archivo BIN ingresando el siguiente comando:

```
$ ./sample.bin
```

**Advertencia**

_Tenga cuidado al manipular archivos BIN descargados o enviados por correo electrónico, ya que los ciberdelincuentes pueden utilizarlos para distribuir malware. Ejecute únicamente archivos BIN de fuentes confiables para mitigar el riesgo de ataques ejecutables maliciosos._

## Otros archivos BIN

Aquí hay otros tipos de archivos que usan la extensión de archivo **.bin**.

- [BIN - Archivo codificado MacBinary](/es/compression/bin/)
- [BIN - Archivo de imagen de disco binario](/es/disc-and-media/bin/)
- [BIN - Archivo de políticas de TI de BlackBerry](/es/settings/bin/)
- [BIN - ROM del juego Sega Genesis](/es/juego/bin/)
- [BIN - Imagen del BIOS de PSX PlayStation](/es/game/bin-pcsx/)

## Referencias

* [Cómo ejecutar archivos binarios en Linux](https://linuxhint.com/execute-binary-files-in-linux/)


