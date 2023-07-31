{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo ADE y las API que pueden crear y abrir archivos ADE",
  "title" :"ADE - Acceder al archivo de extensión del proyecto",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## ¿Qué es un archivo ADE?

Un archivo con extensión .ade es un archivo de proyecto de Microsoft Access que contiene la salida compilada de la información contenida en el archivo de proyecto de Microsoft Access ADP. La información del archivo de proyecto de Access, distinta de Visual Basic para Aplicaciones (VBA), está disponible en formato compilado en archivos ADE. Los datos se almacenan en formato comprimido en estos archivos para reducir el tamaño del archivo y mejorar el rendimiento en Access. Dado que ADE es la salida compilada del archivo del proyecto de Access, cualquier código fuente de VBA que sea parte del proyecto permanece protegido al no permitir que forme parte de la salida. Los archivos ADE se pueden abrir en Microsoft Access 365.

## Formato de archivo ADE - Más información

ADE son archivos de base de datos de acceso compilados que se almacenan en el disco como archivos binarios. La estructura de archivo interna de estos archivos no se conoce.

Los archivos ADE pueden crear problemas al abrirlos según la versión de Microsoft Access que se haya utilizado para crear estos archivos. Las bases de datos de Access que usan la versión de 64 bits de Microsoft Access 2010 y que están compiladas como archivos MDE, [ACCDE](/es/database/accde/) o ADE deben volver a compilarse en Microsoft Access 2021 Service Pack 1 (SP1) para funcione correctamente con Access 2010 SP1. Este problema se produce porque Access 2010 SP1 usa una versión más reciente del archivo VBE7.dll (versión 7.00.1619).

## Referencias

* [Problema con archivos ADE de Access](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Qué formatos de archivo de acceso usar](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

