{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo AHK y las API que pueden crear y abrir archivos AHK",
  "title" :"Formato de archivo AHK: archivo de secuencia de comandos AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## ¿Qué es un archivo AHK?

Un archivo AHK es un archivo de secuencia de comandos generado con la aplicación de software AutoHotkey que se utiliza para la automatización de tareas en Microsoft Windows. Contiene instrucciones para la automatización de tareas mediante teclas de método abreviado que se pueden utilizar para realizar acciones instantáneas. El archivo es ejecutado por AutoHotkey y todas las acciones se realizan secuencialmente. Los archivos AHK son lo suficientemente potentes como para realizar tareas complejas utilizando las teclas de acceso rápido definidas mediante las teclas de acceso rápido. Los archivos AHK se pueden abrir con editores de texto como Microsoft Notepad y Notepad++.

## Formato de archivo AHK

Los archivos AHK se guardan en el disco como archivos de texto sin formato y contienen líneas de código que AutoHotkey puede ejecutar. AutoHotkey es un lenguaje de secuencias de comandos gratuito y de código abierto que permite a los usuarios crear secuencias de comandos simples o complejas para realizar acciones como completar formularios, hacer clic automáticamente, ejecutar macros, etc. Un archivo AHK como mínimo puede realizar una sola acción y luego salir .

Hay herramientas disponibles que se pueden usar para convertir AHK a archivos [Exe](/es/executable/exe/).

### Ejemplo de AHK

El siguiente ejemplo usa la tecla Win+Z para ejecutar el Bloc de notas de Microsoft o traerlo al frente si ya se está ejecutando.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## ¿Cómo creo un archivo AHK?

Los siguientes pasos se pueden usar para crear un archivo AHK. Estos asumen que AutoHotkey ya está instalado en la máquina.

* Haga clic derecho en su escritorio.
* Busque "Nuevo" en el menú.
* Haga clic en "AutoHotkey Script" dentro del menú "Nuevo".
* Dale al script un nuevo nombre.
* Busque el archivo recién creado en su escritorio y haga clic derecho en él.
* Haga clic en "Editar guión".
* Debería haber aparecido una ventana, probablemente el Bloc de notas.
* Guarda el archivo.

## Referencias

* [AutoHotkey](https://www.autohotkey.com/)
* [Archivo por lotes - por Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

