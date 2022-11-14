{
  "date" : "2021-08-10",
  "keywords" :[ "archivo .ova", "formato de archivo", "qué es un archivo .ova", "archivo", "extensión de archivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre qué es un formato de archivo .ova y las API que pueden crear y abrir archivos ova",
  "title" :"Formato de archivo OVA - Abrir archivo de dispositivo virtual",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## ¿Qué es un archivo OVA?

Un archivo OVA (Open Virtual Appliance) es un directorio OVF guardado como archivo con el formato de archivo .tar. Es un archivo de paquete de dispositivo virtual que contiene archivos para la distribución de software que se ejecuta en una máquina virtual. Un paquete OVA contiene un archivo descriptor [.ovf](/es/disc-and-media/ovf/), archivos de certificado, un archivo [.mf](/es/programming/mf/) opcional junto con otros archivos relacionados. Los archivos OVA tienen un tipo de medio como application/ovf.

## Formato de archivo OVA

Como se mencionó, un archivo OVA es un archivo de almacenamiento que se crea utilizando el directorio OVF en formato de archivo TAR. El archivo en sí se guarda como un archivo binario. La mayoría de las plataformas de virtualización, como VMware, Microsoft, Oracle y Citrix, pueden instalar dispositivos virtuales desde un archivo OVF que es un archivo descriptor que contiene los detalles de la imagen que se cargará en la máquina virtual.

## Ventajas de un archivo OVA

* Los archivos OVA están comprimidos, lo que permite descargas más rápidas.
* El cliente de vSphere valida un archivo OVA antes de importarlo y se asegura de que sea compatible con el servidor de destino deseado. Si el dispositivo no es compatible con el host seleccionado, no se puede importar y aparece un mensaje de error.
* OVA puede encapsular aplicaciones de varios niveles y más de una máquina virtual.

## Referencias

* [Plantillas y formatos de archivo OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Especificaciones del formato de archivo OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

