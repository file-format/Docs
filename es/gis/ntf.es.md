{
  "date" : "2021-07-28",
  "keywords" :[ "archivo ntf", "formato de archivo ntf", "qué es un archivo ntf", "archivo", "ejemplo ntf", "extensión de archivo ntf","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Archivos de formato de transferencia nacional",
  "description":"Obtenga información sobre el formato de archivo NTF y las API que pueden crear y abrir archivos NTF",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## ¿Qué es un archivo NTF?
Los archivos con extensión .ntf se denominan archivos **National Transfer Format (NTF)**; utilizado principalmente por el Ordnance Survey (OS) del Reino Unido; específicamente para la transferencia de datos geoespaciales. Está gestionado por la British Standards Institution. Se ha convertido en el formato de transferencia estándar para los datos digitales de Ordnance Survey. La proyección National Grid del Reino Unido, que es un tipo de Transverse Mercator, contiene toda la información georreferenciada de los archivos NTF.

## formato de archivo NTF
El formato de archivo NTF es propiedad de Ordnance Survey en el Reino Unido; compatible con la biblioteca GDB para la importación. La versión actual del formato de archivo NTF es 2.0. Este formato de archivo se introdujo para abordar una limitación del segmento vectorial **PCIDSK** que tiene solo un campo de atributo por estructura, pero hay una variedad de atributos que se pueden extraer con datos vectoriales. Para moverse, el formato de archivo NTF está constituido por dos segmentos. Cada segmento consta de los mismos vectores, pero con diferentes atributos. El primer segmento de un archivo vectorial NTF contiene los vectores con el número de código de función como atributo. El segundo segmento contiene los vectores con el valor como atributo.

### Sistema de referencia de coordenadas
La biblioteca GDB representa datos ráster y vectoriales con las características de proyección TM apropiadas:

- Longitud de referencia: 49.0
- Latitud de referencia: 2.0
- Este Falso: 400000
- Falsa Norte: -100000
- Escala: 0.9996012717
- Elipsoide: Airy 1830 (E009)
No hay soporte disponible para actualizar o escribir archivos NTF, ni se pueden vincular los archivos DTM.

### Ejemplo de Ogrinfo
El siguiente ejemplo usa **ogrinfo** en un archivo NTF para recuperar números de capa:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referencias

* [Formato de transferencia nacional del Reino Unido (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Mapeo web: ilustrado por Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

