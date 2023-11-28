{
"fecha": "2023-07-18",
   "keywords":[
"PAR",
"Archivo PAR",
"cómo abrir un archivo par",
"archivo",
"Extensión de archivo PAR",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo PAR - Archivo de índice Parchive",
   "description":"Obtenga más información sobre el formato PAR y las API que pueden crear y abrir archivos PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent" : "compression"
}
},
"último mod": "2023-07-18"
}

## ¿Qué es un archivo PAR?

Dentro de los archivos Parchive (PAR), un archivo .par hace referencia a un archivo de índice que contiene un grupo de volúmenes de paridad o bloques de paridad. Este archivo de índice se utiliza con fines de detección y recuperación de errores cuando uno o más archivos del archivo se pierden o dañan.

Un archivo Parchive normalmente consta tanto de los archivos de datos originales como de los volúmenes de paridad correspondientes. Los volúmenes de paridad se crean utilizando algoritmos de corrección de errores de Reed-Solomon. Estos volúmenes de paridad contienen información redundante que se puede utilizar para recuperar los archivos de datos originales.

El archivo .par, también conocido como conjunto de volúmenes de paridad, contiene información sobre la estructura y ubicación de los volúmenes de paridad dentro del archivo. Sirve como índice o mapa para el proceso de recuperación. Al utilizar el archivo .par, el software PAR especializado puede determinar qué volúmenes de paridad se necesitan y cómo deben usarse para reconstruir los archivos faltantes o dañados.

Cuando uno o más archivos dentro del archivo Parchive se vuelven inaccesibles o están dañados, el archivo .par se puede utilizar junto con los volúmenes de paridad disponibles para recuperar los datos perdidos. El software PAR lee el archivo .par, identifica los archivos faltantes o dañados y utiliza los volúmenes de paridad para reconstruirlos.

## ¿Cómo abrir un archivo PAR?

Para abrir y utilizar archivos .par, necesitará un software PAR especializado. A continuación se muestran algunas opciones de software populares que pueden manejar archivos .par:

- **QuickPar:** QuickPar es un software PAR ampliamente utilizado para Windows. Le permite crear, verificar y reparar archivos PAR. Puede abrir un archivo .par en QuickPar para verificar su integridad o usarlo para reparar archivos dañados o faltantes en un archivo Parchive.

- **MultiPar:** MultiPar es otro software PAR popular disponible para Windows. Admite formatos de archivo PAR y PAR2 y proporciona funciones avanzadas para crear, verificar y reparar archivos. MultiPar puede abrir archivos .par y realizar operaciones de detección y recuperación de errores según los volúmenes de paridad proporcionados.

- **MacPAR deLuxe:** MacPAR deLuxe es un software PAR diseñado específicamente para macOS. Admite formatos de archivo PAR y PAR2 y proporciona una funcionalidad similar a QuickPar y MultiPar. MacPAR deLuxe puede abrir archivos .par y ayudar a verificar archivos y recuperar archivos dañados o faltantes.

## Formato de archivo PAR - Más información

El formato de archivo PAR, comúnmente conocido como Parchive, es un formato de archivo específico que se utiliza para crear datos de paridad y realizar detección y recuperación de errores en archivos comprimidos. El formato de archivo PAR normalmente consta de tres tipos: PAR, PAR2 y PAR3.

- **PAR:** El formato de archivo PAR original, también conocido como PAR1, fue desarrollado por el proyecto Parchive. Incluye datos de paridad generados a partir de los archivos de datos originales. Los archivos PAR proporcionan un nivel básico de detección y recuperación de errores, pero tienen limitaciones en términos de capacidades de corrección de errores.

- **PAR2:** PAR2 es una versión mejorada del formato de archivo PAR. Ofrece capacidades de corrección de errores más avanzadas y funciones de recuperación mejoradas. Los archivos PAR2 se utilizan normalmente para crear datos de paridad que pueden recuperar archivos perdidos o dañados dentro de un archivo. Los archivos PAR2 brindan una mejor protección contra la corrupción de datos y se usan ampliamente para fines de archivado de archivos.

- **PAR3:** PAR3 es la última versión del formato de archivo PAR y proporciona mejoras adicionales en la corrección y recuperación de errores. Ofrece niveles aún más altos de redundancia y capacidades de corrección de errores en comparación con PAR2. Los archivos PAR3 están diseñados para proporcionar opciones de protección y recuperación más sólidas para los datos almacenados en archivos.

Los formatos de archivo PAR2 y PAR3 son ampliamente compatibles con el software PAR y ofrecen la capacidad de verificar la integridad de los archivos dentro de un archivo y recuperar datos perdidos o dañados. Los archivos PAR y PAR2 todavía se usan comúnmente, mientras que los archivos PAR3 están ganando adopción gradualmente debido a sus capacidades mejoradas de corrección de errores.

## Referencias
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

