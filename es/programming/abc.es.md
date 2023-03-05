
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - Archivo de código de bytes de ActionScript",
  "description":"Aprenda qué es el formato de archivo ABC con ejemplos y API que pueden crear y abrir archivos ABC",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## ¿Qué es un archivo ABC?

Un archivo con la extensión .abc es un archivo de código de bytes de ActionScript creado por el compilador de Flash como resultado de la compilación de los archivos de script de ActionScript. El código de bytes contenido en el archivo ABC lo ejecuta la máquina virtual ActionScript (AVM y AVM2). El código de bytes se compone de datos constantes, instrucciones del conjunto de instrucciones AVM2 y varios tipos de metadatos. Cuando se carga un archivo ABC en AVM o AVM2, se somete a verificación. Si no se ajusta a la descripción general de AVM2, se rechaza. Los archivos ABC se pueden abrir en Adobe Flash Player, que se suspendió hace mucho tiempo.

## Formato de archivo ABC - Más información

Los archivos ABC se guardan en un disco en formato de archivo binario que pueden leer las máquinas virtuales AVM o AVM2. Su estructura de archivo interna representa un bloque de código ejecutable con todos sus datos constantes, descriptores de tipo, código y metadatos.

## Estructura del archivo ABC

La estructura del archivo ABC es como se muestra a continuación.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Campos del archivo ABC

|Nombre de campo|Descripción|
---|---|
|versión_secundaria, versión_principal|Los valores de versión_principal y versión_secundaria son los números de versión principal y secundaria del formato abcFile.|
|constant_pool|Constant_pool es una estructura de longitud variable compuesta por números enteros, dobles, cadenas, espacios de nombres, conjuntos de espacios de nombres y nombres múltiples.|
|method_count, método|El valor demethod_count es el número de entradas en la matriz de métodos. Cada entrada en la matriz de métodos es una estructura method_info de longitud variable.|
|metadata_count, metadata|El valor de metadata_count es el número de entradas en la matriz de metadatos. Cada entrada de metadatos es una metadata_infostructure que asigna un nombre a un conjunto de valores de cadena. |
|class_count, instancia, clase|El valor de class_count es el número de entradas en las matrices de instancia y clase. |
|script_count, script|El valor de script_count es el número de entradas en la matriz de secuencias de comandos. Cada entrada de script es una estructura script_info que define las características de un solo script en este archivo. |
|method_body_count, method_body|El valor de method_body_count es el número de entradas en la matriz method_body. Cada method_bodyentry consiste en una estructura method_body_info de longitud variable que contiene las instrucciones para un método o función individual.|

## Referencias

* [ABC robusto (código de bytes de ActionScript) [Des] ensamblador - Github](https://github.com/CyberShadow/RABCDAsm)

