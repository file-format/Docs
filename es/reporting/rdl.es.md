{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Archivo de idioma de definición de informe",
  "keywords" :[ "rdl", "lenguaje de definición de informe", "XmlTextWriter", "XSD", "elemento RDL"],
  "description":"Obtenga más información sobre el formato de archivo RDL, que es una representación XML de una definición de informe de SQL Server Reporting Services",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## ¿Qué es un archivo RDL? ##

El RDL (Lenguaje de definición de informes) es un punto de referencia establecido por Microsoft para definir informes. Un archivo RDL consta de uno o varios elementos RDL. Mientras que un elemento RDL consta de su tipo de datos y cardinalidad. Un elemento puede ser simple o complejo. El elemento simple no tiene elementos secundarios ni atributos, mientras que un elemento complejo tiene elementos secundarios y atributos opcionales.

## Definición de esquema XML RDL
Un archivo de definición de esquema XML (XSD) valida el archivo RDL. El esquema define las reglas sobre dónde pueden aparecer elementos RDL en un archivo .rdl. Un elemento RDL puede ser simple o complejo. Un elemento simple no tiene elementos ni atributos secundarios y un elemento complejo tiene elementos secundarios y, opcionalmente, atributos.

## Creando RDL
Dado que RDL es de naturaleza abierta y extensible, se pueden crear muchas aplicaciones y herramientas que generan archivos RDL basados en su esquema XML. Una de las formas más sencillas de crear RDL desde una aplicación es usar las clases de Microsoft .NET Framework del espacio de nombres **System.Xml** y el espacio de nombres System.Linq. En particular, la clase **XmlTextWriter** se puede usar para escribir RDL. Puede generar una definición de informe completa de principio a fin en cualquier aplicación de .NET Framework usando **XmlTextWriter**. Los desarrolladores también pueden agregar elementos de informes personalizados con propiedades personalizadas para ampliar el RDL.

## Tipos de RDL
La siguiente tabla enumera los tipos y atributos utilizados en los elementos RDL.

|Tipo|Descripción|
---|---|
|Binario |Una propiedad con un valor binario codificado en base 64.|
|Booleano| Una propiedad con verdadero o falso como el valor del objeto. A menos que se especifique lo contrario, el valor de un objeto booleano opcional omitido es False.|
|Fecha |Una propiedad con una fecha completamente especificada o un valor de fechahora especificado en el formato de fecha ISO8601: AAAA-MM-DD[THH:MM[:SS[.S]]].|
|Enumeración |Una propiedad con un valor de texto de cadena que debe ser uno de una lista de valores designados.|
|Flotante |Una propiedad con un valor flotante. Se utiliza un punto (.) como separador decimal opcional.|
|Entero |Una propiedad con un valor entero (int32).|
|Idioma |Una propiedad con un valor de texto que contiene un código de idioma y cultura, como "en-us" para inglés estadounidense. El valor debe ser un idioma específico o un idioma neutral para el cual se define un idioma predeterminado en Microsoft .NET Framework.|
|Nombre |Una propiedad con un valor de texto de cadena. Los nombres deben ser únicos dentro del espacio de nombres del elemento. Si no se especifica, el espacio de nombres de un elemento es el objeto contenedor más interno que tiene un nombre.|
|NormalizedString |Una propiedad con un valor de texto de cadena que se ha normalizado.|
|Tamaño |Un elemento de tamaño debe contener un número (con un carácter de punto utilizado como separador decimal opcional). El número debe ir seguido de un designador para una unidad de longitud CSS como cm, mm, in, pt o pc. Un espacio entre el número y el designador es opcional. Para obtener más información sobre los designadores de tamaño, consulte Referencia de unidades y valores CSS. En lenguaje RDL, el valor máximo para Tamaño es 160 pulgadas. El tamaño mínimo es 0 pulgadas.|
|Cadena |Una propiedad con un valor de texto de cadena.|
|UnsignedInt |Una propiedad con un valor entero sin signo (uint32).|
|Variante |Una propiedad con cualquier tipo XML simple.|

## Tipos de datos RDL
En RDL, la enumeración de tipo de datos define el tipo de datos de un atributo, expresión o parámetro. La siguiente tabla muestra cómo los tipos de datos CLR se corresponden con los tipos de datos RDL.

|Tipo(s) CLR |Tipo de datos correspondiente|
---|---|
|Booleano| Booleano|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Entero|
|Simple, Doble |Flotante|
|Cadena, Char, GUID, intervalo de tiempo |Cadena|


## Referencias ##

- [Lenguaje de definición de informe (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Lenguaje de definición de informes (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

