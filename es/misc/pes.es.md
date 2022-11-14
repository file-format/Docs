{
  "date" : "2021-07-29",
  "keywords" :[ "archivo pes", "formato de archivo pes", "qué es un archivo pes", "archivo", "ejemplo pes", "extensión de archivo pes","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PES - Formato de bordado Brother PE",
  "description":"Obtenga información sobre el formato de archivo PES y las API que pueden crear y abrir archivos PES",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## ¿Qué es un archivo de bordado PES?

El archivo de bordado PES es un archivo de diseño que contiene instrucciones para las máquinas de coser/bordar. Fue desarrollado por Brother Industries para sus máquinas de bordar, pero luego se formalizó como un formato de archivo general. Los archivos PES son utilizados por las máquinas de coser para leer instrucciones para coser patrones en tela. Estos archivos tienen dos propósitos; en primer lugar, proporciona información de diseño para la aplicación PE-Design desarrollada por Brother Industries y, en segundo lugar, proporciona el nombre del diseño, los colores y los códigos de la máquina de bordar, como "detener", "saltar" y "recortar".

## Formato de archivo PES - Más información

Un archivo PES se guarda en un disco en formato de archivo binario. Contiene múltiples secciones que tienen información de costura almacenada usando un método predefinido. El formato de archivo PES es el siguiente.

* Datos de la versión: brinda información de la versión y puede ser cualquier valor `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Valor de búsqueda de PEC: un entero little-endian de 4 bytes que sigue inmediatamente a los datos de la versión y representa el valor de búsqueda para la sección de PEC que contiene detalles de diseño Información
* Sección PSE: contiene información de diseño relevante para el diseño PE de Brother y puede haber otras aplicaciones de costura
* Sección PCE: puede estar en cualquier lugar del archivo PSE pero referenciado por el valor de búsqueda de PEC.

## Tipo de máquinas de coser que utilizan archivos PES

Los archivos PES son creados principalmente por el software PE-Design que se utiliza con las máquinas de coser Brother. Algunas otras máquinas que pueden admitir archivos PES incluyen las máquinas de bordar domésticas Babylock y Bernina.

## ¿Cómo convertir archivos PSE?

La aplicación de software PE-Design puede [convertir archivo PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) a otros formatos como .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd o .xxx. Se puede hacer usando la aplicación PE-Design abriendo el archivo y seleccionando el formato de Conversión.

## Referencias

* [Diseño de PE - Manual de instrucciones](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

