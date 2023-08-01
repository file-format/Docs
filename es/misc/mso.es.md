{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Archivo de referencia de macros de Microsoft Office",
  "description":"Obtenga información sobre el archivo MSO y las API que pueden crear y abrir archivos MSO",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## ¿Qué es un archivo MSO?

Un archivo MSO es un formato de archivo contenedor de datos que se crea cuando se envía un mensaje HTML mediante Microsoft Outlook. Esto sucede principalmente con las aplicaciones de Microsoft Office 2000. En la mayoría de los casos, el mensaje de correo electrónico se adjunta con el nombre de archivo **Oledata.mso**. El destinatario del correo electrónico, cuando abre dicho correo electrónico, puede ver el archivo correctamente incluso si no tiene instalado el mismo software. Los archivos MSO hacen referencia al [Formato de archivo de documento compuesto de Microsoft (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Formato de archivo MSO de Microsoft

Los archivos MSO se guardan en formato de archivo de documento compuesto de Microsoft (MCDF), que también se conoce como vinculación e incrustación de objetos (OLE) o formato de archivo binario de implementación de archivo compuesto de almacenamiento estructurado del modelo de objetos componentes (COM).

### Estructura de formato de archivo MSO

La estructura de formato de archivo interno del formato de archivo MSO está bien definida en las [Estructuras](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) de la documentación del MCDF. La tabla de asignación de archivos (FAT) administra la asignación de sectores y las cadenas de sectores. Contiene una matriz de números de sector de 32 bits. Cada índice de la matriz representa un número de sector, mientras que su valor representa el siguiente sector de la cadena o un valor especial.

## Referencias

* [Almacenamiento estructurado COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Formato de archivo de documento compuesto de Microsoft (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

