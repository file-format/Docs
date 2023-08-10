{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Paquete de aplicación de nivel de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo DACPAC y las API que pueden crear y abrir archivos DACPAC",
  "title" :"DACPAC - Paquete de aplicación de nivel de datos",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## ¿Qué es un archivo DACPAC?

Un archivo con la extensión .dacpac (siglas de Data Tier AppliCation Package) es un archivo de base de datos, creado con la aplicación de nivel de datos de Microsoft SQL Server, que contiene el modelo de base de datos para la representación de los objetos de la base de datos. Como contiene el modelo completo de la base de datos, se utiliza para restaurar una base de datos a partir de los detalles disponibles en el modelo. Los archivos DACPAC generalmente se entregan a los equipos de implementación para su instalación en las instalaciones del cliente para restaurar la base de datos. Estos se pueden abrir con
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Formato de archivo DACPAC - Más información

Los archivos del paquete de datos DACPAC son en realidad archivos ZIP comprimidos que contienen varios archivos [XML](/es/web/xml/) que contienen información sobre el modelo de la base de datos, como tablas y vistas, que se utilizan para restaurar una base de datos. Para ver el contenido de los archivos DACPAC, cambie el nombre de los archivos de .dacpac a [.zip](/es/compression/zip/) y extraiga el archivo zip con cualquier utilidad de descompresión.

Los siguientes son algunos archivos que se encuentran dentro de un archivo DACPAC.

* [Tipos_de_contenido].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origen.xml

* modelo.xml

Cabe señalar que DACPAC no contiene DATOS ni otros objetos a nivel de servidor. El archivo puede contener todos los tipos de objetos que pueden mantenerse en el proyecto SSDT.

## Referencias

* [Aplicaciones de nivel de datos - Beneficios](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Implementación de una aplicación de nivel de datos - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [¿Cómo crear un archivo DACPAC?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

