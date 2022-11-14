{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "archivo ma", "formato de archivo ma", "formato de archivo", "3d","descarga de archivo ma", "archivo .ma", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MA y las API que pueden abrir y crear archivos MA",
  "title" :"Formato de archivo MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## ¿Qué es un archivo MA?

Un archivo con extensión .ma es un archivo de proyecto 3D creado con la aplicación Autodesk Maya. Contiene una gran lista de comandos textuales para especificar información sobre el archivo. Un archivo **.ma** se puede abrir y editar en cualquier editor de texto para solucionar cualquier problema con los comandos en caso de que un archivo se corrompa. Estos archivos contienen información para definir la escena 3D, como geometría, iluminación, animación y renderizado.

## Formato de archivo MA

Los archivos MA se guardan en el disco en formato de texto ASCII a diferencia de los archivos MB que se guardan en formato de archivo binario en el disco. Una referencia detallada para el formato de archivo MA está disponible en [Documentación de Autodesk Maya] (https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) y se puede consultar para referencia del desarrollador.

### Encabezado del archivo MA

El encabezado del archivo MA comienza con una sección de comentarios que brinda la información de creación del archivo y la fecha de modificación. Los lectores de archivos Maya ignoran este bloque, ya que solo se usa con fines informativos. Sin embargo, un encabezado debe comenzar con los primeros seis caracteres como "//Maya".

El encabezado del archivo ASCII tiene el siguiente aspecto.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Referencias de archivos

La sección de referencias de archivos de un archivo .ma contiene información sobre todos los demás archivos de Maya a los que se hace referencia en este archivo. Cada archivo al que se hace referencia se puede leer usando un solo comando de archivo que está contenido en el mismo archivo. La sintaxis del comando de archivo cuando se usa para hacer referencia es:

```
file -r -rpr prefixString fileName;
```
o

```
file -r -ns nameSpace fileName
```
Aquí hay una cadena de ejemplo.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Este ejemplo muestra que el objeto sol contenido en el archivo `solar` sería accesible en este archivo usando el nombre "solar_sun".

### Requisitos

La sección de requisitos de un archivo .ma consta de una serie de comandos requeridos y brinda información de mayo, como la versión y la información del complemento que se requiere para leer los archivos. Un ejemplo de la sección de requisitos es el siguiente.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


La siguiente sección especifica los requisitos. Este consiste en una serie de comandos require. Esta sección del archivo le dice a Maya qué software se necesita para cargar el archivo correctamente. Específicamente, qué versión de Maya y qué complementos.

## Descarga de archivos MA
Es un poco difícil encontrar y descargar el archivo MA de un modelo 3D. Por lo tanto, puede descargar un archivo MA de muestra desde aquí:

- [Muestra.ma](../muestra.ma)


## Referencias

* [Organización de archivos Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

