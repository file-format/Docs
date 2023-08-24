{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "extensión", "formato", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga más información sobre el formato de archivo PML, el lenguaje de marcado de Palm y las API que pueden crear y abrir archivos PML",
  "title" :"PML - Archivo de lenguaje de marcado de Palm",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## ¿Qué es un archivo PML?

Palm Inc introdujo el formato de archivo PML que significa Palm Markup Language File. Su propósito es crear documentos para eReader, que es un dispositivo de lectura de libros electrónicos similar a la tableta. El archivo PML da el diseño a un archivo [PDB](/es/programming/pdb/) (que contiene varios archivos de datos) para mostrar en un dispositivo Palm.

## Detalles técnicos de los archivos PML

La estructura de los archivos PML consta de etiquetas para crear una configuración de libro electrónico, incluidos párrafos, encabezados, sangrías y referencias. También permite las etiquetas de formato como negrita, versalitas y superíndice. Los desarrolladores también pueden agregar imágenes a los libros electrónicos.

### Lenguaje de marcado de Palm
La siguiente tabla especifica los comandos PML:

|Comando|Descripción|
---|---|
| \p | Nueva pagina |
| \ x | Nuevo capitulo; también provoca un nuevo salto de página. Adjunte el título del capítulo (y cualquier código de estilo) con \x y \x |
| \Xn | Nuevo capítulo, sangrado n niveles (n entre 0 y 4 inclusive) en el cuadro de diálogo Capítulo; no provoca un salto de página. Incluya el título del capítulo (y cualquier código de estilo) con \Xn y \Xn |
| \Cn="Título del capítulo" | Inserte "Título del capítulo" en la lista de capítulos, con el nivel n (como \Xn). El texto no se muestra en la página y no fuerza un salto de página. Esto a veces puede ser útil para insertar una marca de capítulo al comienzo de una introducción al capítulo, por ejemplo. |
| \c | Centre este bloque de texto; cierre con \c al principio de la línea |
| \r | Bloque de texto justificado a la derecha; cierre con \r al principio de la línea |
| \i | bloque en cursiva; cerrar con \i |
| \u | Subrayar bloque; cerrar con \u |
| \ o | Bloque de superposición; cerrar con \o |
| \v | Texto invisible; cierre con \v (se puede usar para comentarios) |
| \t | Bloque de sangría. Comience al principio de una línea, cierre con \t al final de una línea |
| \T="50%" | Sangría el porcentaje especificado del ancho de la pantalla, 50% en este caso. Si la posición de dibujo actual ya está más allá de la ubicación de pantalla especificada, esta etiqueta se ignora. |
| \w="50%" | Incruste una regla horizontal de un porcentaje dado de ancho de la pantalla, en este caso 50%. Esta etiqueta provoca un salto de línea antes y después. La regla está centrada. El signo de porcentaje es obligatorio. |
| \n | Cambie a la fuente "normal", que especifica el usuario |
| \s | Cambiar a fuente estándar; cierre con \s para volver a la fuente normal |
| \b | Cambiar a negrita; cierre con \b para volver a la fuente normal (en desuso; use \B en su lugar) |
| \l | Cambiar a fuente grande; cierre con \l para volver a la fuente normal |
| \B | Marca el texto en negrita. A diferencia de la etiqueta \b, \B no cambia la fuente, por lo que puede tener texto grande en negrita. No puede mezclar \b y \B en el mismo archivo PML. |
| \Esp | Marcar texto como superíndice. No se debe mezclar con otros estilos como negrita, cursiva, etc. Encierre el texto en superíndice con \Sp. |
| \Sb | Marcar texto como subíndice. No debe mezclarse con otros estilos como negrita, cursiva, etc. Encierre el texto subíndice con \Sb. |
| \ k | Convierta el texto adjunto en versalitas; cierra con \k. Todos los caracteres encerrados en las etiquetas \k (incluidos los que tienen acentos) se escriben en mayúsculas y se representan en un tamaño de punto más pequeño que un carácter en mayúscula normal. |
| \\ | Representa una sola barra invertida |
| \aXXX | Inserte un carácter que no sea ASCII cuyo código Windows-1252 sea XXX decimal. Consulte la tabla de caracteres PML para obtener más detalles. |
| \UXXXX | Inserte un carácter que no sea ASCII cuyo código Unicode sea XXXX hexadecimal. Consulte la tabla de caracteres de PML extendida para obtener más información. |
| \m="nombre de la imagen.png" | Inserte la imagen nombrada. Consulte la sección sobre Imágenes a continuación. |
| \q="#linkanchor"Algo de texto\q | Haga referencia a un ancla de vínculo que se encuentra en otro lugar del documento. La cadena después de la especificación del ancla y antes del final \q está subrayada o se muestra como un enlace al ver el documento. |
| \Q="anclaje de enlace" | Especifique un ancla de enlace en el documento. |
| \- | Inserte un guión suave. Un guión suave aparece solo si es necesario dividir una palabra en una línea. |
| \Fn="nota al pie1"1\Fn | Vincule el "1" a una nota al pie cuyo nombre sea footnote1, etiquetada al final del documento PML. Consulte la sección sobre notas al pie y barras laterales a continuación. |
| \Sd="barra lateral1"Barra lateral\Sd | Vincule el texto de la "barra lateral" a una barra lateral cuyo nombre sea sidebar1, etiquetada al final del documento PML. Consulte la sección sobre notas al pie y barras laterales a continuación. |
| \ yo | Marcar como elemento de índice de referencia. Encierre el elemento de índice (y cualquier código de estilo) con \I y \I.|
 


## Referencias

* [Palm Markup Language - Por MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Por MobileRead](https://en.wikipedia.org/wiki/E-reader)

