{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "extensión", "archivo", "formato", "sistema", "MemoryDump", "Minidump", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Formato de archivo de volcado de memoria",
  "description":"Obtenga información sobre el formato de archivo DMP y las API que pueden crear y abrir archivos DMP",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## ¿Qué es un archivo DMP? ##

El archivo DMP está asociado principalmente con el formato de archivo MemoryDump o Minidump. Se utiliza en el sistema operativo Microsoft Windows para almacenar datos que se han descargado del espacio de memoria de la computadora. Por lo general, los archivos DMP se crean cuando un archivo falla o se produce un error. A veces, los archivos DMP son muy importantes para los expertos técnicos o los usuarios avanzados de computadoras para solucionar los problemas que enfrenta y resolver cualquier tipo de problema de aplicación. Los archivos DMP se almacenan como un formato propietario en Microsoft que utiliza el sistema operativo para depurar cualquier aplicación instalada en el sistema.


## Especificaciones técnicas del formato de archivo DMP

En Windows, la herramienta del sistema "savedump.exe" genera archivos .dmp que luego pueden ser procesados por varias utilidades de depuración disponibles. Windows almacena el mini volcado (64/128 Kb) en el directorio '%SystemRoot%\Minidump'. Por otro lado, la memoria del kernel y los volcados de memoria completa se almacenan en la raíz del sistema como archivos 'Memory.dmp'. Los archivos de volcado de memoria son archivos relativamente grandes, por lo que pueden ocupar una cantidad suficiente de espacio de almacenamiento. Por lo tanto, se recomienda eliminar los archivos .dmp inútiles que crea que no serán útiles para solucionar problemas.

Puede eliminar archivos .dmp manualmente o utilizando el "asistente de limpieza de disco" predeterminado en su computadora. Los productos de base de datos de Oracle utilizan las extensiones DMP para utilizar los archivos .dmp en los archivos de base de datos de copia de seguridad y recuperación creados y utilizados. Los archivos DMP creados por Oracle son copias de seguridad de la base de datos que se pueden usar para importar o restaurar en una instancia de base de datos en ejecución a través de un servidor de base de datos. En la mayoría de los casos, los archivos .dmp tienen marcas de fecha y hora como nombres de archivo.

### Contenido del archivo DMP

Un archivo de volcado de memoria contiene:

* La declaración de parada y sus parámetros;
* Una lista de controladores cargados;
* El contexto del procesador (PRCB) para los procesos que detuvieron el funcionamiento normal de Windows;
* El contexto del kernel y la información del procesador (EPROCESSES) para los procesos que se han detenido;
* El contexto del kernel y la información del procesador (ETHREAD) para el subproceso que se detuvo;
* La pila de llamadas en modo kernel para el subproceso que finalizó la ejecución del proceso.


## Ejemplo de DMP

El error de detención 0XC0000218 (Registry_File_Failure) crea un archivo DMP de la siguiente manera:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## Referencia ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

