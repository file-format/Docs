{
  "date" : "2023-01-11",
  "keywords" :["archivo ac", "qué es un archivo aci", "archivo", "cómo abrir un archivo ac", "extensión de archivo ac","extensión"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo AC y las API que pueden crear y abrir archivos ACCDB",
  "title" :"Formato de archivo AC - Archivo de script de autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## ¿Qué es un archivo AC?

El archivo AC es el archivo de script de Autoconf. **Autoconf** es un paquete extensible de macros M4 que produce scripts de shell para configurar automáticamente paquetes de código fuente de software. Estos scripts pueden adaptar los paquetes a muchos tipos de sistemas similares a UNIX sin la intervención manual del usuario. Autoconf crea una secuencia de comandos de configuración para un paquete a partir de un archivo de plantilla que enumera las funciones del sistema operativo que el paquete puede usar, en forma de llamadas de macro M4.

Producir scripts de configuración usando Autoconf requiere GNU M4. Debe instalar GNU M4 (al menos la versión 1.4.6, aunque se recomienda la 1.4.13 o posterior) antes de configurar Autoconf, para que el script de configuración de Autoconf pueda encontrarlo. Los scripts de configuración producidos por Autoconf son autónomos, por lo que sus usuarios no necesitan tener Autoconf (o GNU M4).

## ¿Cómo abrir un archivo AC?

AC significa Configuración automática. Es un script generado por GNU Autoconf que permite que el código fuente del software se adapte a varios sistemas similares a Posix al probar las características necesarias en el paquete. El script se denomina archivo AC.

## Principales componentes de Autotools

Una comprensión de las herramientas automáticas de GNU (`automake`, `autoconf`, etc.) puede ser útil cuando se trabaja con ebuilds:

Autotools es una colección de paquetes relacionados que, cuando se usan juntos, eliminan gran parte de la dificultad que implica la creación de software portátil. Estas herramientas, junto con algunos archivos de entrada proporcionados aguas arriba relativamente simples, se utilizan para crear el sistema de compilación de un paquete.

**Una descripción general básica de cómo encajan los principales componentes de las herramientas automáticas.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

En una configuración sencilla:

- El programa `autoconf` produce un script de configuración desde `configure.in` o `configure.ac`.
- El programa `automake` produce un Makefile.in a partir de un Makefile.am.
- El script `configure` se ejecuta para producir uno o más archivos Makefile a partir de archivos Makefile.in.
- El programa `make` usa el Makefile para compilar el programa.

## Referencias
* [Software de autoconf](https://www.gnu.org/software/autoconf/)
* [Los fundamentos de Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)


