{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "extensión", "archivo", "formato", "sistema", "Biblioteca de enlace dinámico", "configuración", "programas", "computadora", "aplicación" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Biblioteca de enlaces dinámicos",
  "description":"Obtenga información sobre el formato de archivo DLL y las API que pueden crear y abrir archivos DLL",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## ¿Qué es un archivo DLL? ##

Un archivo DLL o biblioteca de vínculos dinámicos es un tipo de archivo ejecutable. Es uno de los archivos de extensión más comúnmente encontrados en su dispositivo y generalmente se almacena en la carpeta System32 en su Windows. El archivo de extensión DLL fue desarrollado por Microsoft y es popularmente utilizado por ellos. Tiene una calificación de usuario de alta popularidad. La DLL funciona como un estante que contiene los *controladores/procedimientos/funciones/propiedades* que el servidor de Windows diseña y aplica para un programa/aplicación. Un solo archivo DLL también se puede compartir entre varios programas de Windows. Estos archivos de extensión son vitales para el buen funcionamiento de los programas de Windows en su dispositivo, ya que son responsables de habilitar y ejecutar varias funciones en el programa, como escribir y leer archivos, conectarse con otros dispositivos que son externos a su configuración.
Sin embargo, estos archivos solo se pueden abrir en un dispositivo compatible con cualquier versión de Windows (Windows 7/Windows 10/etc.) y, por lo tanto, no se pueden abrir directamente en un dispositivo compatible con Mac OS. (Si desea abrir un archivo DLL en Mac OS, varias aplicaciones externas pueden ayudarlo a abrirlo).


## Formato de archivo DLL ##

El archivo DLL fue desarrollado por Microsoft y tiene la extensión ".dll" que representa el tipo. Ha sido una parte integral del servidor Windows 1.0 y más allá. Es un tipo de archivo binario y es compatible con todas las versiones de Microsoft Windows. Este tipo de archivo se creó como un medio para crear un sistema de biblioteca compartida dentro de los programas de Windows, para permitir ediciones o cambios separados e independientes en las bibliotecas de programas sin necesidad de volver a vincular los programas.


## Ejemplo de DLL ##

El código de ejemplo para un punto de entrada de DLL se puede encontrar a continuación:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Referencia ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
