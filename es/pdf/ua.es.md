{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PDF/UA",
  "description":"Obtenga más información sobre el formato de archivo PDF/UA y las API que pueden crear y abrir archivos PDF/UA",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# ¿Qué es un archivo PDF/UA? #

PDF/UA se publicó como [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) en agosto de 2012 y es, con mucho, la primera definición completa de un conjunto de requisitos para documentos PDF de acceso universal. El término "accesible universalmente" se refiere al entendimiento de que la información contenida en un documento [PDF](/es/pdf/) debe ser accesible por igual e independientemente para todos en general y para las personas con discapacidades en particular. La introducción del estándar PDF/UA puede considerarse un paso importante en la creación de herramientas y aplicaciones para crear y leer contenido PDF.

## Requisitos de formato de archivo ##

El PDF/UA tiene algunos requisitos definidos en su base que actúan como la esencia de este estándar. Básicamente, se basan en el etiquetado de archivos PDF, lo que significa que todos los documentos PDF/UA deben etiquetarse correctamente. También requiere que las etiquetas sean semánticamente apropiadas y en orden lógico. Esto garantiza que el documento final creado con la especificación PDF/UA sea más confiable y accesible. Esto puede hacer que los autores de PDF se pregunten si necesitan saber todo acerca de todos esos requisitos. Afortunadamente, no es así, ya que las herramientas de conformidad de PDF/UA asumen la responsabilidad de agregar y preservar la accesibilidad del PDF.

Los requisitos de formato de archivo para PDF/UA son los siguientes.

* El contenido se clasifica en una de dos formas: contenido significativo y artefactos, como elementos de página decorativos. Todo el contenido significativo debe etiquetarse e integrarse en el árbol de estructura de todas las etiquetas dentro de un documento. Los artefactos, por otro lado, solo necesitan ser marcados como tales.
* El contenido significativo debe marcarse con etiquetas y, junto con las otras etiquetas del documento, crear una estructura de árbol completa.
* El contenido significativo debe marcarse con las etiquetas semánticas apropiadas.
* El árbol de estructura creado por las etiquetas del documento debe reflejar el orden lógico de lectura del documento.
* Solo se pueden usar las etiquetas estándar definidas en PDF 1.7; si se utilizan otras etiquetas, una entrada de asignación de roles debe registrar qué etiqueta estándar representa cada una.
* La información no se puede transmitir utilizando únicamente medios visuales (por ejemplo, contraste, color o posición en la página).
* No se permite ningún contenido parpadeante, parpadeante o parpadeante, ya sea como efectos controlados por JavaScript o como parte de cualquier video incrustado en el PDF.
* Debe proporcionarse un título de documento y el documento debe configurarse de modo que el título (en lugar del nombre del archivo) aparezca en el título de la ventana.
* Se debe anotar el idioma de todo el contenido, y los cambios de idioma se deben marcar explícitamente como tales.

## Conformidad con PDF/UA ##

El estándar PDF/UA define especificaciones para contenido, lectores y tecnología de asistencia. Estos tres aspectos están vinculados entre sí en función del contenido del documento. Los requisitos de conformidad para cada uno de estos son los que se mencionan a continuación.

## Archivos conformes ##

Los archivos que cumplen con el estándar PDF/UA deben contener funciones válidas según las [especificaciones de PDF 1.7] (http://www.adobe.com/go/pdfreference). Sin embargo, las funciones que están prohibidas específicamente por PDF/UA deben excluirse.

## Lectores conformes ##

Un lector conforme debe obedecer las reglas deletreadas por las especificaciones de PDF 1.7. Específicamente, debe soportar:

* todas las etiquetas, atributos y valores clave especificados para la accesibilidad. También debe tener la capacidad de procesar y representar firmas digitales, anotaciones y contenido opcional.
* procesar y representar firmas digitales, anotaciones y contenido opcional
* navegar el documento por una variedad de medios

## Tecnología de asistencia conforme ##

Una tecnología de asistencia conforme está destinada a soportar las características de PDF/UA. Estos incluyen, por ejemplo, características del contenido y del lector, y deben permitir la navegación por etiquetas de página, estructura del documento o esquema. También debería permitir al usuario anular el zoom de navegación predeterminado.

## Referencias ##

* [PDF/UA - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA en pocas palabras](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

