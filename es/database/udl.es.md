{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extensión", "archivo udl", "formato de archivo udl", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "qué es un archivo udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo UDL y las API que pueden crear y abrir archivos UDL",
  "title" :"UDL - Archivo de enlace de datos universal de Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## ¿Qué es un archivo UDL?
El archivo con extensión .udl se llama archivo Microsoft Universal Data Link; especificar atributos de conexión; utilizado por las aplicaciones de Windows para establecer una conexión con la base de datos. El archivo UDL contiene la cadena de conexión para un origen de datos OLE DB; con nombre de usuario y contraseña y propiedades esenciales de la cadena de conexión. Para evitar especificar directamente las propiedades a mano en una cadena de conexión, se puede usar un cuadro de diálogo Propiedades de vínculo de datos para guardar la información de conexión en un archivo .udl como alternativa.

## Formato de archivo UDL
Básicamente, un archivo UDL (Universal Data Link) es un archivo de texto simple que consta de una cadena de conexión de base de datos con atributos o propiedades particulares. Una vez que se crea el archivo UDL, se puede probar con SQL Server Management Studio para verificar la conectividad.

### Propiedades de la cadena de conexión
Las siguientes propiedades se pueden establecer en un UDL para garantizar la conectividad adecuada:

- **Nombre del servidor**: ubicación del servidor donde se encuentra la base de datos a la que desea acceder.
- **Opciones de autenticación**
- **Autenticación de Windows**: Autenticación a SQL Server usando las credenciales de la cuenta de Windows del usuario actualmente conectado.
- **Autenticación de SQL Server**: Autenticación usando ID de inicio de sesión y contraseña.
- **Active Directory - Integrado**: Autenticación integrada con una identidad de Azure Active Directory; también se puede utilizar para la autenticación de Windows en SQL Server.
- **Active Directory - Contraseña**: ID de usuario y autenticación de contraseña con una identidad de Azure Active Directory.
- **Active Directory - Universal con compatibilidad con MFA**: autenticación interactiva con una identidad de Azure Active Directory.
- **Active Directory - Entidad de servicio**: Autenticación con una entidad de servicio de Azure Active Directory.
- **SPN del servidor**: si utiliza una conexión de confianza, puede especificar un nombre principal de servicio (SPN) para el servidor.
- **Nombre de usuario**: escriba el ID de usuario que se usará para la autenticación cuando inicie sesión en la fuente de datos.
- **Contraseña**: escriba la contraseña que se usará para la autenticación cuando inicie sesión en la fuente de datos.
- **Contraseña en blanco**: cuando está marcada, permite que el proveedor especificado use una contraseña en blanco en la cadena de conexión.
- **Permitir guardar contraseña**: Permite guardar la contraseña con la cadena de conexión.
- **Utilice un cifrado fuerte para los datos**: los datos que pasan a través de la conexión se cifrarán.
- **Certificado de servidor de confianza**: Se validará el certificado del servidor.
- **Base de datos**: Nombre de la base de datos a la que desea acceder.
- **Adjuntar un archivo de base de datos como nombre de base de datos**: especifica el nombre del archivo principal para una base de datos adjunta.

## Referencias ##

* [Componentes de acceso a datos de Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Configuración de enlace de datos universal (UDL)](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

