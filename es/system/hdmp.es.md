{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo HDMP - Formato de archivo de volcado de montón de Windows",
  "description":"Obtenga información sobre el formato de archivo HDMP y las API que pueden crear y abrir archivos HDMP",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## ¿Qué es un archivo HDMP?

El archivo HDMP es un volcado de memoria sin comprimir cuando una aplicación o programa falla debido a un error. Solo lo crea Windows XP/Vista y contiene un volcado del estado de la aplicación cuando se bloqueó. Al no estar comprimidos, los archivos HDMP ocupan más espacio en el disco en comparación con los archivos Minidump [MDMP](/es/system/mdmp/) que se comprimen para generar informes.

Las aplicaciones que se pueden usar para **abrir** o analizar archivos HDMP incluyen Microsoft Visual Studio con herramientas de depuración para Windows.

## Formato de archivo HDMP

Los archivos HDMP se almacenan en el disco como archivos binarios y no brindan ningún beneficio si se abren sin las aplicaciones apropiadas. Estos contienen datos relevantes del sistema registrados cuando ocurrió el error.

### Diferencia entre los formatos de archivo HDMP y MDMP

HDMP son archivos de volcado de memoria sin comprimir. Por el contrario, MDMP son archivos de mini volcado que se comprimen para reducir el tamaño del archivo y se envían a Microsoft para informar el problema.

## Referencia ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

