{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo VHDX y las API que pueden crear y abrir archivos VHDX",
  "title" :"Formato de archivo VHDX - ¿Qué es un archivo VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## ¿Qué es un archivo VHDX?

Un archivo VHDX es un archivo de imagen de disco en formato de archivo Virtual Hard Disk v2. Contiene un sistema operativo completo que se puede cargar y usar como cualquier máquina normal para probar software o ejecutar software que requiere un sistema operativo específico. Un VHDX, a pesar de ser una imagen de disco completa, se almacena en un solo archivo. El software de máquina virtual como Parallels Desktop, Windows Virtual Machine y Virtual Box puede cargar y abrir la imagen del disco.

El archivo VHDX se puede convertir a [VHD](/es/disc-and-media/vhd/) con Hyper-V Manager, o a [VDI](/es/disc-and-media/vdi/) con VirtualBox.

## Formato de archivo VHDX - Más información

Los detalles del formato de archivo VHDX están completamente documentados y disponibles en línea como [Especificaciones del formato de archivo VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) en la documentación de Microsoft. Es una extensión del formato VHD e incluye capacidades mejoradas. El formato de archivo VHDX proporciona características adicionales que están disponibles en el disco duro virtual y en las capas de archivo del disco duro virtual. Está más optimizado y brinda mejores resultados para la configuración y las capacidades del hardware de almacenamiento. Los archivos VHDX se pueden abrir

### Compatibilidad con discos duros virtuales en VHDX

Admite tres tipos de discos duros virtuales.

1. **Disco duro virtual fijo**: disco duro virtual con tamaño de datos fijo asignado. El tamaño del disco duro virtual no cambia con la adición o eliminación de datos.

1. **Disco duro virtual dinámico**: disco duro virtual con tamaño de disco dinámico. Su tamaño es en cualquier momento tan grande como los datos reales escritos en él y los metadatos. Su tamaño de archivo aumenta dinámicamente a medida que se agregan o eliminan datos.

1. **Disco duro virtual de diferenciación**: representa el disco duro virtual actual como un conjunto de bloques modificados en comparación con un archivo de disco duro virtual principal.

## Referencias

* [Especificaciones del formato de archivo VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - por Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

