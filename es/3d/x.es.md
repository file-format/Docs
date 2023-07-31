{
  "date" : "2020-01-11",
  "keywords" :[ "archivo x", "formato de archivo x", "qué es un archivo x", "archivo", "ejemplo x", "extensión de archivo x","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - Formato de archivo DirectX 2.0",
  "description":"Obtenga información sobre el formato de archivo DirectX X y las API que pueden abrir y crear archivos DirectX X",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## ¿Qué es un archivo X?

Un archivo con extensión .x hace referencia a [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) formato de archivo heredado de gráficos 3D que se introdujo con Microsoft DirectX 2.0. Se utilizó para la representación de gráficos 3D en juegos y especifica las estructuras para mallas, texturas, animaciones y objetos definidos por el usuario. Ha quedado obsoleto desde 2014 porque el formato de archivo Autodesk FBX funciona mejor como un formato más moderno. X está basado en plantillas y está libre de cualquier conocimiento de uso.

Puede abrir archivos DirectX X usando Microsoft DirectX y editores de texto comunes.

## Formato de archivo X

La [referencia del archivo X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) contiene información de referencia para los elementos API que se utilizan para trabajar con archivos DirectX .x. El formato proporciona primitivas de datos de bajo nivel que otras aplicaciones utilizan para definir primitivas de nivel superior a través de plantillas de datos. DirectX 6.0 introdujo interfaces y métodos que permiten leer y escribir en archivos .x. DirectX 3.0 introdujo una versión binaria de este formato de archivo.

La [referencia de formato de archivo X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) definida por DirectX 9 contiene información de referencia para .x archivos en binario, así como codificaciones de texto.

### Codificación binaria

El [formato binario](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) define el formato DirectX X como una representación tokenizada del formato de texto. Estos tokens pueden ser independientes para dar una estructura gramatical o pueden ser tokens que contienen registros y proporcionan los datos necesarios.

#### Encabezado

El encabezado binario se puede leer y escribir usando las siguientes definiciones.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Codificacion de texto

Los archivos DirectX .x no dependen de la forma en que se usa el archivo y no son específicos de ninguna aplicación. Este enfoque basado en plantillas permite que cualquier aplicación cliente utilice el formato de archivo .x.


#### Encabezado

El encabezado de longitud variable es obligatorio y debe estar al principio del flujo de datos. El encabezado contiene los siguientes datos.

|Tipo |Subtipo |Tamaño |Contenido |Contenido Significado|
---|---|---|---|---|
|Número Mágico (requerido)| | 4 bytes |xof |
|Número de versión (obligatorio) |Número principal |2 bytes |03 |Versión principal 3|
| |Número menor |2 bytes |02 |Versión menor 2|
|Tipo de formato (obligatorio)| |4 bytes |"txt" |Archivo de texto|
| | | |"papelera"| Archivo binario|
| | | |"zip"| Archivo de texto comprimido MSZip|
| | | |"bzip"| Archivo binario comprimido MSZip|
|Tamaño flotante (obligatorio)| |4 bytes| 0064| flotantes de 64 bits |
| | | |0032 |flotantes de 32 bits|


## Referencias

* [Archivos X heredados](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [Referencia de formato de archivo de DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

