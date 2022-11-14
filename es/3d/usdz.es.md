{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "archivo usdz", "formato de archivo usdz", "formato de archivo", "3d","descarga de archivo usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Formato ZIP de descripción de escena universal",
  "description":"Obtenga información sobre el formato de archivo USDZ y las API que pueden abrir y crear archivos USDZ",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## ¿Qué es un archivo USDZ?

Un archivo con .usdz es un archivo ZIP sin comprimir y sin cifrar para el formato de archivo [USD](/es/3d/usd/) (Descripción de escena universal) que contiene y representa archivos de otros formatos (como texturas y animaciones) integrados en el archivo y los ejecuta directamente con el tiempo de ejecución de USD sin necesidad de desempaquetar. Los archivos USDZ son paquetes cuyo diseño se basa en la nueva abstracción de nivel Ar de un paquete. Usdz se registró con IANA y tiene un nombre de tipo de medio de modelo y un nombre de subtipo de vnd.usd+zip y sus detalles se pueden encontrar en [página de registro de IANA] (https://www.iana.org/assignments/media- tipos/modelo/vnd.usdz+zip).

## Formato de archivo USDZ

Los archivos USDZ se basan en el formato de archivo ZIP que archiva archivos individuales en su contenedor. Esto permite que el extremo del receptor simplemente descomprima el contenido y use los archivos de descripción de escena USD normales para trabajar e inspeccionar. Casi todos los sistemas operativos brindan soporte integrado para los formatos de archivo ZIP y elegir este formato de archivo en lugar de cualquier método personalizado facilita que los archivos USDZ sean útiles como un protocolo de transporte simple.

### Restricciones ZIP

El formato de archivo USDZ utiliza el formato de archivo ZIP sin ninguna "compresión" ni "cifrado". Esto fue diseñado para cumplir con dos requisitos:

* Para un paquete ya cargado en la memoria o como un solo archivo en el disco, la API está disponible en USD para acceder a los datos contenidos en la imagen
* No debería haber necesidad de extraer archivos al disco o asignar más almacenamiento en montón

Con USDZ, ambos requisitos se cumplen, ya que la mayoría de los formatos de imagen permiten esquemas de compresión internos, lo que da como resultado un tamaño de archivo compacto.

### Requisitos de diseño

Los paquetes USDZ requieren que el diseño de los archivos dentro del paquete sea que los datos de cada archivo comiencen en un múltiplo de 64 bytes desde el principio del paquete. Sin embargo, el paquete debe comenzar con un archivo [USD](/es/3d/usd/) nativo en caso de que el paquete tenga como destino una referencia simple. En tal caso, este primer archivo USD se denomina Capa predeterminada. Los clientes que deseen entregar "contenido transmisible" también pueden considerar otras restricciones de diseño.

## Descarga de archivos USDZ
Dado que los archivos usdz están empaquetados con otras imágenes de alta calidad y archivos usd, pueden ocupar un mayor espacio de almacenamiento en disco. Aquí puede encontrar un archivo de ejemplo USDZ simple y más pequeño para descargar:

- [Muestra.usdz](../muestra.usdz)

## Referencias

* [Especificaciones de formato de archivo USDZ](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)

