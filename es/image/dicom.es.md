{
  "date" : "2019-10-11",
  "keywords" :[ "archivo dicom", "formato de archivo dicom", "qué es un archivo dicom", "archivo", "ejemplo dicom", "extensión de archivo dicom","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Formato de archivo de comunicaciones e imágenes digitales",
  "description":"Obtenga información sobre el formato de archivo DICOM y las API que pueden crear y abrir archivos DICOM",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo DICOM?

DICOM es el acrónimo de Digital Imaging and Communications in Medicine y pertenece al campo de la informática médica. DICOM se utiliza para la integración de dispositivos de imágenes médicas como impresoras, servidores, escáneres, etc. de varios proveedores y también contiene datos de identificación de cada paciente para que sean únicos. Los archivos DICOM se pueden compartir entre dos partes si son capaces de recibir datos de imagen en formato DICOM. La parte de comunicación de DICOM es un protocolo de capa de aplicación y utiliza TCP/IP para comunicarse entre entidades. Las versiones compatibles con los servicios web son 1.0, 1.1, 2 o posteriores.

## Historia ##

DICOM fue desarrollado conjuntamente por el Colegio Americano de Radiología (ACR) y la Asociación Nacional de Fabricantes Eléctricos (NEMA) para el intercambio y la visualización de imágenes médicas como resonancias magnéticas, tomografías computarizadas e imágenes de ultrasonido. Inicialmente, era difícil decodificar las imágenes que producían las máquinas. Por lo tanto, ACR y NEMA juntos formaron un equipo en 1983 que lanzó su primer estándar, ACR/NEMA 300 en 1985. La segunda versión se lanzó en 1988 y fue más popular entre los proveedores, pero pronto se dio cuenta de que la segunda versión también necesita mejoras. La tercera versión del estándar se lanzó en 1993 como "DICOM". 3.0 sigue siendo la última versión, pero se ha actualizado continuamente desde 1993.

## Formato de archivo DICOM ##

DICOM es la combinación de definición de formato de archivo y un protocolo de comunicaciones de red. DICOM utiliza la extensión .DCM. .DCM existe en dos formatos diferentes, es decir, formato 1.x y formato 2.x. DCM Format 1.x también está disponible en dos versiones normal y extendida. Los protocolos HTTP y HTTPS se utilizan para los servicios web de DICOM.

### Encabezado del archivo ###

El encabezado del archivo contiene un preámbulo de archivo de 128 bytes y un prefijo DICOM de 4 bytes.

**Preámbulo # 128 Bytes**|**Prefijo # 4 Bytes “D, I, C, M**

**Preámbulo** se utiliza para acceder a las imágenes y otros datos en el archivo DICOM, lo que proporciona compatibilidad con los formatos de archivo de imagen más utilizados.

**Prefijo** contiene la cadena "DICM" en mayúsculas.

### Conjunto de datos ###

Cada archivo debe contener un único conjunto de datos que represente la instancia de SOP y la clase de SOP con el IOD relacionado. El conjunto de datos es la representación de la información del mundo real. El conjunto de datos contiene elementos de datos y los elementos de datos contienen valores de los atributos de ese objeto. La estructura de los atributos se especifica en los IOD. Un objeto de datos DICOM consta de una serie de atributos, incluidos elementos como nombre, ID, etc., y también un atributo especial que contiene los datos de píxeles de la imagen.

### Elementos de datos ###

El elemento de datos consta de la etiqueta del elemento de datos, la longitud del valor y el valor del elemento de datos. Hay 5 tipos de elementos de datos, a saber, elementos de datos requeridos de tipo 1, elementos de datos condicionales de tipo 1C, elementos de datos requeridos de tipo 2, elementos de datos condicionales de tipo 2C y elementos de datos opcionales de tipo 3. Los tres tipos básicos de estructuras de elementos de datos son los siguientes.

**Elemento de datos con un VR explícito**

|Número de grupo|Número de elemento|Representación de valor|Reservado|Longitud de valor|Campo de valor
---|---|---|---|---|---|
|2 bytes|2 bytes|2 bytes|2 bytes # 0x00, 0x00|4 bytes|"Bytes de longitud de valor"

**Elemento de datos con un VR explícito**

|Número de grupo|Número de elemento|Representación de valor|Longitud de valor|Campo de valor
---|---|---|---|---|
|2 bytes|2 bytes|2 bytes|2 bytes|"Bytes de longitud de valor"

**Elemento de datos con una VR implícita**


|Número de grupo|Número de elemento|Longitud de valor|Campo de valor
---|---|---|---|
|2 bytes|2 bytes|4 bytes|"Bytes de longitud de valor"

1. **Etiqueta de elemento de datos**: un número entero ordenado que representa el número de grupo y el número de elemento
1. **Representación de valor VR**: VR es una cadena de caracteres que representa la VR del elemento de datos.
1. **Longitud del valor**: es el entero sin signo que representa la longitud explícita del campo de valor.
1. **Campo de valor**: Describe los valores de los elementos de datos.

## Transferir sintaxis ##

La sintaxis de transferencia es un conjunto de reglas de codificación para representar sin ambigüedades más sintaxis abstractas. Con la ayuda de la sintaxis de transferencia, las entidades comunicantes negocian las técnicas de codificación comunes que soportan.

## SOP ##

La unión de IOD y DIMSE define una Clase SOP. La definición de Clase SOP contiene las reglas y la semántica que pueden restringir el uso de los servicios en el Grupo de Servicio DIMSE o los Atributos del IOD. Ejemplos de Elementos de Servicio son Almacenar, Obtener, Buscar, Mover, etc. Ejemplos de Objetos son imágenes CT, imágenes MR, pero también incluyen listas de programación, colas de impresión, etc.

## Servicios ##

DICOM proporciona varios servicios, en su mayoría relacionados con la comunicación de datos. Cada uno de ellos se describe brevemente a continuación:


**Tienda:** El servicio DICOM Store envía imágenes u otros objetos a un sistema de archivo y comunicación de imágenes (PACS) o servidor.


**Compromiso de almacenamiento:** El servicio de compromiso de almacenamiento se utiliza para confirmar que una imagen se ha almacenado permanentemente en un dispositivo en cualquier tipo de medio.


**Consulta/recuperación:** Este servicio permite que una estación de trabajo encuentre las listas de imágenes u otros objetos y luego los recupere de PACS.


**Lista de trabajo de modalidad:** El servicio de lista de trabajo de modalidad brinda una lista de procedimientos de imágenes que se han programado para realizar mediante un dispositivo de adquisición de imágenes.


**Imprimir:** Este servicio envía imágenes a la impresora.

## Números de puerto sobre IP ##

DICOM utiliza los siguientes puertos TCP y UDP:

1. 104
1. 2761
1. 2762
1. 11112

## Referencias ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

