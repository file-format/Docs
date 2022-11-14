{
  "date" : "2022-04-01",
  "keywords" :[ "archivo nkit", "formato de archivo nkit", "qué es un archivo nkit", "archivo", "ejemplo de nkit", "extensión de archivo nkit","extensión", "formato", "pie de página nkit", "archivo formato de nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo NKIT y las API que pueden crear y abrir archivos NKIT",
  "title" :"NKIT - Formato de archivo de imagen de disco",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## ¿Qué es un archivo NKIT?

Un archivo NKIT es una imagen de disco de datos extraídos de juegos de NintendoWii y GameCube. NKIT es para el formato Nintendo Toolkit. El archivo de compresión resultante [ISO](/es/compression/iso/) utiliza los datos principales de estos juegos para ejecutarse con programas emuladores como Dolphin, Swiss y Nintendont. NKit viene en formatos de archivo crudo (iso) y comprimido (gcz) que fueron diseñados teniendo en cuenta la jugabilidad y el tamaño.

## Formato de archivo NKIT

El formato de archivo NKit es un formato sin pérdidas y se usa para reducir y restaurar imágenes de Nintendo Wii y GameCube. Los formatos están disponibles en formato de archivo ISO y GCZ para cada uno de los juegos de GameCube y Wii.

|Sistema |Formato |Hardware compatible |Dolphin compatible |Restaurable 1:1 |Notas|
---|---|---|---|---|---|
|GameCube| nkit.iso| Sí |Sí| Sí |Igual que la iso de GameCube compactada|
|GameCube| nkit.gcz| No| Sí| Sí |GCZ es el propio formato de compresión de búsqueda de bloques de Dolphin|
|Wii| nkit.iso| No Sí| Sí| El formato RVT-H solo se puede reproducir en Dolphin|
|Wii| nkit.gcz| No Sí| Sí| RVT-H en GCZ jugable solo en Dolphin |

### Encabezado NKIT

El encabezado del formato de archivo NKIT es el siguiente.

|Desplazamiento |Longitud |Nombre|
---|---|---|
|0x200 |0x4 |NKit Encabezado 'NKIT'|
|0x204 |0x4 |Versión NKit 'v01'|
|0x208 |0x4 |Imagen fuente original CRC32|
|0x20C |0x4 |NKit CRC: hace que el archivo NKit CRC32 sea igual al CRC de origen en 0x208 (en 0x4 en GCZ)|
|0x210 |0x4 |Longitud de la imagen de origen|
|0x214 |0x4 |Identificación basura forzada (cuando la ID del disco es diferente - rara - solo GameCube)|
|0x218 |0x4 |Wii Actualiza la partición CRC32 si se elimina al convertir|

## Referencias ##

* [Formato de archivo NKIT - por gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

