{
  "date" : "2021-06-30",
  "keywords" :[ "archivo exe", "formato de archivo exe", "qué es un archivo exe", "archivo", "ejemplo exe", "extensión de archivo exe","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Un archivo .exe es un archivo ejecutable de Microsoft que se ejecuta en el sistema operativo Windows. Obtenga más información sobre el formato de archivo EXE",
  "title" :"¿Qué es un archivo EXE ejecutable?",
  "linktitle" : "EXE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## ¿Qué es un archivo EXE?

La palabra EXE es la abreviatura de **ejecutable**. Un archivo .exe es un programa que se puede ejecutar en el sistema operativo Microsoft Windows. Los desarrolladores de aplicaciones publican principalmente sus programas para el sistema operativo Windows en formato ejecutable como archivos exe. Es el formato de archivo estándar para ejecutar aplicaciones en Windows. **Setup.exe**, **Install.exe** y **cmd.exe** son algunos nombres comunes y familiares de archivos EXE.

## Formato de archivo EXE

Los compiladores de MS-DOS se introdujeron con los modelos de memoria que tenían la limitación de memoria de 64K. El concepto general es configurar diferentes registros de segmento en la CPU x86 (CS, DS, ES, SS) para apuntar a los mismos o diferentes segmentos, lo que permite varios grados de acceso a la memoria. Algunos modelos de memoria específicos fueron:

- **Pequeño**: todos los accesos a la memoria son de 16 bits (los registros de segmento no cambian). Produce un archivo .COM en lugar de un archivo .EXE.
- **Pequeño**: todos los accesos a la memoria son de 16 bits (los registros de segmento no cambian).
- **Compacto**: las direcciones de datos incluyen tanto el segmento como el desplazamiento, recargando los registros DS o ES en el acceso y permitiendo hasta 1M de datos. Los accesos de código no cambian el registro CS, lo que permite 64K de código.
- **Medio**: Las direcciones de código incluyen la dirección del segmento, recargando CS en el acceso y permitiendo hasta 1M de código. Los accesos a datos no modifican los registros DS y ES, permitiendo 64K de datos.
- **Grande**: Tanto las direcciones de código como las de datos son pares (segmento, desplazamiento), siempre recargando las direcciones de segmento. Todo el espacio de memoria de 1M byte está disponible tanto para código como para datos.
- **Enorme**: Igual que el modelo grande, con aritmética adicional generada por el compilador para permitir el acceso a matrices de más de 64K.

Los desarrolladores tienen que decidir qué modelo se debe seleccionar al crear un archivo exe.

### Formato de archivo EXE portátil

El formato de archivo ejecutable portátil (PE) contiene una serie de encabezados informativos, la siguiente es la lista de encabezados:

- **Encabezado de DOS**: el encabezado de MS-DOS garantiza la compatibilidad con versiones anteriores o el rechazo elegante de nuevos tipos de archivos.
- **Encabezado PE**: en el desplazamiento 60 (0x3C) desde el comienzo del encabezado DOS hay un puntero al encabezado del archivo PE
- **Cabecera COFF**: La cabecera COFF tiene información que es útil para un ejecutable y otra información que es más útil para un archivo objeto.
- **Encabezado opcional de PE**: El encabezado opcional de PE aparece directamente después del encabezado COFF y algunas fuentes incluso muestran los dos encabezados como parte de la misma estructura.
- **Tabla de Sección**: Inmediatamente después del Encabezado Opcional PE encontramos una tabla de sección. La tabla de secciones consta de una matriz de estructuras IMAGE_SECTION_HEADER.
- **Secciones asignables**: puede ahorrar espacio en la memoria al asignar el código de una biblioteca a más de un proceso.

## ¿Puedes ejecutar un archivo EXE en una Mac?

Los archivos exe no se usan como ejecutables en Mac OS. Sin embargo, si desea ejecutar un archivo exe en Mac OS, se pueden utilizar los siguientes métodos.

1. **Wine**: Wine es la solución perfecta para las personas que desean usar sus aplicaciones de PC en sistemas Mac. Es un acrónimo que significa "Wine Is Not A Emulator", que significa. Wine crea el mismo entorno de directorios que usa Microsoft para que pueda ejecutar su aplicación de Windows usándolo.
2. **Máquinas virtuales**: cree una máquina virtual de Windows utilizando Parallel Desktop o VM Virtual Box y ejecute su aplicación dentro de la máquina virtual.
3. **Boot Camp**: la instalación y configuración de Windows Boot Camp en Mac OS le permite ejecutar el sistema operativo Windows en una máquina Mac.

## Referencias

* [.exe- por Wikipewdia](https://en.wikipedia.org/wiki/.exe)
* [Desmontaje x86/Archivos ejecutables de Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)

