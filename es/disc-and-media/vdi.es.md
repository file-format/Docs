{
  "date" : "2021-08-11",
  "keywords" :[ "archivo vdi", "formato de archivo vdi", "qué es un archivo vdi", "archivo", "ejemplo de vdi", "extensión de archivo vdi","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo VDI y las API que pueden crear y abrir archivos VDI",
  "title" :"VDI - Archivo de imagen de disco virtual de VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## ¿Qué es un archivo VDI?
Un archivo con extensión .vdi es una imagen de disco virtual; específico del programa de virtualización de escritorio de código abierto de Oracle llamado VirtualBox. Los archivos VDI se utilizan para iniciar la máquina virtual VirtualBox. Las máquinas virtuales permiten a los usuarios ejecutar sistemas operativos o programas adicionales en una sola computadora. Por lo tanto, el beneficio de los archivos VDI es que los usuarios pueden guardar estos archivos de imagen de disco en su disco duro y ejecutarlos usando emuladores cuando lo necesiten.

## formato de archivo VDI
La imagen de disco virtual (VDI) es el formato de archivo de disco principal para una VM de Oracle de código abierto y desarrollada activamente conocida como VirtualBox, que es un producto de virtualización de clase empresarial. El formato de archivo VDI está diseñado para crear una imagen de disco portátil que se puede ejecutar fácilmente con otros programas de virtualización. Admite almacenamiento de tamaño fijo y asignado dinámicamente. Le permite expandir un archivo de imagen después de que se haya creado, incluso si ya contiene datos.

### Virtualización de disco
El sistema emula discos duros en formato de imagen de disco VDI. Una máquina virtual VirtualBox puede usar discos anteriores creados en Microsoft Virtual PC o VMware, así como su propio formato nativo. VirtualBox también es capaz de conectarse a objetivos iSCSI y particionar sin procesar en el host, ya sea como discos duros virtuales. VirtualBox emula IDE (controladores PIIX4 e ICH6), SATA (controlador ICH8M), controladores SAS a los que se pueden conectar discos duros y SCSI.

El soporte está disponible para Open Virtualization Format (OVF) desde la versión 2.2.0 de VirtualBox. Tanto los dispositivos físicos conectados al host como las imágenes ISO se pueden montar como unidades de CD o DVD.
De forma predeterminada, VirtualBox admite gráficos a través de una tarjeta gráfica virtual personalizada compatible con VESA.

### Soporte de virtualización para Ethernet
VirtualBox virtualiza las siguientes tarjetas de interfaz de red para un adaptador de red Ethernet:
-AMD PCnet PCI II (Am79C970A)
-AMD PCnet-Fast III (Am79C973)
- Escritorio Intel Pro/1000 MT (82540EM)
- Servidor Intel Pro/1000 MT (82545EM)
- Servidor Intel Pro/1000 T (82543GC)
- Adaptador de red paravirtualizado (virtio-net)

Las tarjetas de red emuladas permiten que los sistemas operativos invitados se ejecuten sin necesidad de buscar e instalar controladores para hardware de red, ya que están disponibles como parte del sistema operativo invitado. Un adaptador de red paravirtualizado especial mejora el rendimiento de la red al reducir la necesidad de coincidir con una interfaz de hardware específica. Por lo tanto, requiere un soporte especial del controlador en el invitado.


## Referencias

* [VirtualBox - por Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


