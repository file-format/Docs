{
  "date" : "2021-08-10",
  "keywords" :[ "archivo .ovf", "formato de archivo", "qué es un archivo .ovf", "archivo", "extensión de archivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Obtenga información sobre qué es un formato de archivo .ovf y las API que pueden crear y abrir archivos OVF",
  "title" :"Formato de archivo OVF - Abrir archivo de virtualización",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## ¿Qué es un archivo OVF?

Un archivo OVF es un archivo de texto que contiene información sobre el empaquetado y la distribución de un software que se ejecuta en una máquina virtual. Está formateado según las [Especificaciones estándar de virtualización abierta](https://www.dmtf.org/standards/ovf) que describen todos los requisitos (como seguridad, portabilidad, eficiencia y capacidad de ampliación) para ejecutar aplicaciones en máquinas virtuales. La Organización Internacional de Normalización (ISO) ha adoptado OVF como norma ISO 17203.

## Breve historia del formato de archivo OVF

El formato de archivo OVF fue introducido por DMTF (Distributed Management Task Force) que crea estándares abiertos de capacidad de administración. Es independiente de cualquier hipervisor particular o arquitectura de conjunto de instrucciones. El paquete OVF contiene uno o más sistemas virtuales, cada uno de los cuales se puede implementar en una máquina virtual.

## Formato de archivo OVF - Más información

Un paquete OVF consta de varios archivos ubicados en un solo directorio. Entre estos, contiene exactamente un archivo descriptor OVF (con extensión .ovf) que se almacena en formato de archivo [XML](/es/web/xml/). Describe la información de la máquina virtual empaquetada y la información de metadatos sobre el paquete OVF, como:

* nombre
* Requisitos de hardware
* referencias a los otros archivos en el paquete OVF, y
* descripciones legibles por humanos

Otros archivos que se pueden encontrar en un paquete OVF incluyen una o más imágenes de disco y, opcionalmente, archivos de certificado y otros archivos auxiliares.

## Referencias

* [Formato de virtualización abierto - DMTF](https://www.dmtf.org/standards/ovf)
* [Especificaciones del formato de archivo OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

