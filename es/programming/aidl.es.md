{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo AIDL - Archivo de idioma de definición de interfaz de Android",
  "description":"Aprenda qué es el formato de archivo AIDL con ejemplos y API que pueden crear y abrir archivos AIDL",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ¿Qué es un archivo AIDL?

Un archivo AIDL (Lenguaje de definición de interfaz de Android) permite a los desarrolladores de Android establecer comunicación entre diferentes aplicaciones. Según la interfaz de programación, tanto el cliente como el servicio acuerdan comunicarse mediante la comunicación entre procesos (IPC). El archivo AIDL contiene código fuente [Java](/es/programming/java/) para definir estas interfaces y contratos para la comunicación entre aplicaciones.

Puede abrir archivos AIDL con Google Android Studio o cualquier editor de texto como Microsoft Notepad y Notepad++.

## Formato de archivo AIDL - Más información

AIDL son archivos de texto que contienen las interfaces para la comunicación entre aplicaciones. El sistema operativo Android no permite que un proceso acceda a la memoria de otro proceso. Esto lleva a los procesos a dividir sus objetos en primitivos para comprender el sistema operativo subyacente y establecer el proceso de estructuras de comunicación para el desarrollador.

### ¿Qué tipos de datos admite AIDL?

AIDL admite los siguientes tipos de datos de forma predeterminada.

* Todos los tipos primitivos en el lenguaje de programación Java (como int, long, char, boolean, etc.)
* Cuerda
* Secuencia de caracteres
* Lista
* Mapa

## Ejemplo de archivo AIDL

A continuación se muestra un archivo AIDL de ejemplo.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Referencias

* [Lenguaje de definición de interfaz de Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

