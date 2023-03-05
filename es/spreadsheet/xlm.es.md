{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "archivo", "extensión", "formato de archivo", "Archivo de macros de Microsoft Excel", "Hoja de cálculo" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Su guía de formato de archivo para saber qué es un archivo de macros XLM y las API que pueden crear y abrir archivos XLM",
  "title" :"¿Qué es un archivo XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## ¿Qué es un archivo XLM?

XLM, para Excel Macro, es un tipo de archivo de hoja de cálculo que se utiliza para almacenar macros. Desde el punto de vista de la aplicación, una macro es un conjunto de instrucciones que se utilizan para automatizar procesos. Se utiliza una macro para registrar los pasos que se realizan repetidamente para el formato de archivo [XLS](/es/spreadsheet/xls/) y facilita la realización de las acciones ejecutando la macro nuevamente. Las macros se programan con Visual Basic para Aplicaciones (VBA) de Microsoft desde el Libro de trabajo de Excel usando el Editor de Visual Basic y se pueden ejecutar/depurar directamente desde allí.

## Breve historia ##

Microsoft Excel admitió la programación de macros desde su primer lanzamiento público. Las características de las macros se mantuvieron iguales a través de versiones posteriores de Excel con extensión según las nuevas características. XLM era el lenguaje de macros predeterminado para Excel hasta Excel 4.0. Excel 5.0 grababa macros en VBA de forma predeterminada, pero con la versión 5.0 XLM todavía se permitía la grabación como opción. Después de la versión 5.0, esa opción se suspendió. Todas las versiones de Excel, incluido Excel 2010, pueden ejecutar una macro XLM, aunque Microsoft desaconseja su uso.

## Grabar una Macro en XLM ##

Excel proporciona pasos fáciles de usar para grabar una macro. Requiere tener herramientas de desarrollador instaladas para poder trabajar con macros. Una vez que la grabación de una macro está en proceso, registra cada acción del usuario para reproducirla más adelante. La grabación de macros en realidad involucra todos los pasos que un usuario realiza después de que comienza la grabación. Por lo tanto, si pone el contenido de una celda en negrita, cursiva y establece su justificación de texto después de que se haya iniciado la grabación de una macro, todos estos comandos se grabarán. A cada macro grabada también se le puede asignar un atajo para una reproducción rápida más adelante. La grabación de macros genera código VBA en forma de macro que se puede editar con el Editor de Visual Basic (VBE).

## Modelo de objetos de Excel ##

Las macros usan rutinas VBA en su parte posterior y siguen el [Modelo de objetos de Excel](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) para este propósito. Este modelo identifica los objetos de una hoja de cálculo para la interacción con la hoja de cálculo a través de barras de herramientas de comandos definidas por el usuario, barras de comandos o cuadros de mensajes. Por ejemplo, el acceso a las propiedades del libro de trabajo se otorga con el objeto Libro de trabajo. De manera similar, hay un objeto Hoja de trabajo en el modelo para trabajar con las hojas de trabajo del libro de trabajo mediante programación.

## Macros y Seguridad ##

VBA permite el acceso a todas las áreas de aplicación, así como al sistema de archivos, y también puede ser peligroso. Esto genera inquietudes cuando se comparte el libro de trabajo con alguien que puede ejecutar el archivo en su extremo. Es decir, Microsoft Excel advierte sobre la apertura de dicho archivo. Las macros se pueden certificar con una firma digital para que otros usuarios verifiquen que son confiables. Por lo tanto, las macros se pueden habilitar después de la verificación de su fuente.

## Referencias ##

* [[MS-XLS] - Estructura de formato de archivo binario de Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programación de macros](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

