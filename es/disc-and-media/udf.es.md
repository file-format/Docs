{
  "date" : "2021-08-17",
  "keywords" :[ "archivo udf", "formato de archivo udf", "qué es un archivo udf", "archivo", "ejemplo de udf", "extensión de archivo udf","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo UDF y las API que pueden crear y abrir archivos UDF",
  "title" :"UDF - Archivo de formato de disco universal",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## ¿Qué es un archivo UDF?
El archivo con extensión .udf es un formato de imagen de disco que normalmente se usa para guardar archivos en medios ópticos; se puede usar para grabar DVD, CD y otros medios ópticos; almacena una colección de archivos utilizando la estructura de directorios especificada en el estándar UDF; permite eliminar y modificar archivos en el disco de destino incluso después de haberlos escrito. La Asociación de tecnología de almacenamiento óptico estableció el sistema de archivos UDF como un estándar para formar un sistema de archivos común para todos los medios ópticos, como los medios ópticos regrabables y los medios de solo lectura.

## formato de archivo UDF
El formato de archivo UDF es un sistema de archivos abierto e independiente del proveedor para el almacenamiento de datos informáticos para una amplia gama de medios. Se ha utilizado comúnmente para DVD y formatos de disco óptico más nuevos. Por lo general, el software domina un sistema de archivos UDF en un proceso por lotes y lo escribe en medios ópticos en un solo paso. Sin embargo, cuando escribe paquetes en medios regrabables, el UDF permite que se creen, eliminen y cambien archivos en el disco de forma similar a como lo haría un sistema de archivos de uso general en medios extraíbles como unidades flash o disquetes.
### Especificaciones de UDF
El estándar UDF define las siguientes tres variaciones del sistema de archivos:

- **Compilación simple**: este es el formato original admitido en todas las revisiones de UDF. Se introdujo en la primera versión del estándar, este formato se puede usar en cualquier tipo de disco que permita el acceso aleatorio de lectura o escritura, como DVD+RW, discos duros y medios DVD-RAM.
- **Creación de IVA**: se usa específicamente para escribir en medios de una sola escritura. El VAT es una estructura adicional en el disco que permite la escritura de paquetes; es decir, reasignar bloques físicos cuando se modifican o eliminan archivos u otros datos en el disco. Para medios de una sola escritura, todo el disco está virtualizado, lo que hace que la naturaleza de una sola escritura sea transparente para el usuario; el disco se puede tratar de la misma manera que se trataría un disco regrabable.
- **Compilación reservada (RW)**: se usa específicamente para escribir en medios regrabables. Agrega una tabla de repuesto adicional para administrar las fallas que eventualmente ocurrirán en partes del disco que se han reescrito varias veces. Esta tabla guarda el seguimiento de los sectores desgastados y los reasigna a los que funcionan. La gestión de defectos de UDF no se aplica a los sistemas que ya implementan otra forma de gestión de defectos, como Mount Rainier (MRW) para discos ópticos o un controlador de disco para una unidad de disco duro.
 




## Referencias


* [Formato de imágenes de Windows - por Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


