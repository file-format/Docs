{
  "date" : "2020-08-20",
  "keywords" :[ "archivo fon", "formato de archivo fon", "qué es un archivo fon", "archivo", "ejemplo de fon", "extensión de archivo fon","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Archivo de biblioteca de fuentes",
  "description":"Obtenga información sobre el formato de archivo FON y las API que pueden crear y abrir archivos FON",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## ¿Qué es un archivo FON?

Un archivo con la extensión .fon es una biblioteca de fuentes de Microsoft Windows 3.x que en realidad es un archivo ejecutable pero cuyo nombre se cambió a .fon. Es una colección de archivos [.fnt](/es/font/fnt/) en sí mismo y las aplicaciones hacen referencia a él al acceder a la fuente del sistema. Es por eso que actúa como un archivo de recursos. Se puede abrir en el sistema operativo Windows usando la aplicación Microsoft Windows Font View.

## Formato de archivo FON

Un archivo FON contiene recursos de fuente y tiene formato de archivo Resource (.res). El formato de archivo .res especifica el encabezado del archivo, así como las especificaciones de la sección de datos. Un .fnt también es un archivo de datos de recursos que se incluye con un archivo de recursos. Los archivos FON tienen formato de archivo binario y tienen el tipo MIME application/octet-stream.

Los recursos de fuentes, a diferencia de otro tipo de recursos, no se agregan a los recursos de una aplicación. En su lugar, se agregan a los archivos EXE y se les cambia el nombre a archivos .fon, lo que da como resultado archivos de biblioteca en lugar de aplicaciones. Varias fuentes individuales constituyen componentes de un grupo de fuentes donde cada grupo sigue una estructura de grupo de recursos. Los recursos de fuentes utilizan estas estructuras de grupos de recursos. El encabezado del grupo tiene toda la información necesaria para acceder a una fuente específica del grupo. Un recurso de componente de fuente tiene el siguiente formato.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/es/font/fnt/) file)
```
Un único archivo de recursos .rc puede tener declaraciones de recursos mixtos. Los grupos de fuentes pueden estar en cualquier parte del archivo de recursos y no es necesario que estén juntos. Es obligatorio para los programas que crean archivos .RES agregar la entrada manual de FONTDIR. A continuación se muestra la estructura del encabezado del grupo.

```
[Encabezado de recurso normal (tipo = 7)]

PALABRA NúmeroDeFuentes; // Número total en archivo .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fuenteOrdinal;
struct FontDirEntry {
WORD dfVersión;
DWORD dfTamaño;
char dfCopyright[60];
PALABRA dfTipo;
PALABRA dfPuntos;
PALABRA dfVertRes;
PALABRA dfHorizRes;
PALABRA dfAscenso;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfcursiva;
BYTE dfSubrayado;
BYTE dfStrikeOut;
PALABRA dfPeso;
BYTE dfCharSet;
PALABRA dfPixWidth;
PALABRA dfPixHeight;
BYTE dfPitchAndFamily;
PALABRA dfAvgWidth;
PALABRA dfMaxWidth;
BYTE dfFirstChar;
BYTE dfÚltimoCarácter;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfAnchoBytes;
DWORD dfDispositivo;
DWORD dfCara;
DWORD dfReservado;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

