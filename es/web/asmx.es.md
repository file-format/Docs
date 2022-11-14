{
  "date" : "2019-10-11",
  "keywords" :[ "asmx","archivo asmx", "formato de archivo asmx", "tipo de archivo asmx", "archivo", "tipo", "qué es un archivo asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - Archivo de servicio web ASP.NET",
  "description" :"Obtenga información sobre qué es un archivo ASMX y las API que pueden crear y abrir archivos ASMX",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## ¿Qué es un archivo ASMX?

Un archivo con extensiones .asmx es un archivo de servicio web ASP.NET que proporciona comunicación entre dos objetos a través de Internet mediante el Protocolo simple de acceso a objetos (SOAP). Se implementa como un servicio en el servidor web basado en Windows para procesar la solicitud entrante y devolver la respuesta. A diferencia de los archivos [ASPX](/es/web/aspx/) que contienen el código para la visualización de páginas web ASP.NET, los archivos ASMX se ejecutan en el servidor en segundo plano y realizan diferentes tareas, como conectarse a la base de datos, recuperar datos y devolverlos en un formato en el que se hizo la solicitud. Estos se utilizan específicamente para servicios web XML.

## Formato de archivo ASMX

Los archivos ASMX están en formato de texto sin formato y se pueden abrir o editar en aplicaciones como Microsoft Visual Studio o editores de texto. Es un formato de archivo propietario de Microsoft y tiene una sintaxis bien definida para la creación de servicios web. Una respuesta de un archivo ASMX en forma de SOAP XML tiene los siguientes elementos.

* `Sobre` - Un elemento raíz que identifica el documento XML como un mensaje SOAP.
* `Header`: un elemento opcional que contiene información específica de la aplicación, como datos de autenticación. Si el elemento Header está presente, debe ser el primer elemento secundario del elemento Envelope.
* `Cuerpo`: contiene el mensaje SOAP destinado al destinatario.
* `Fault` - Un elemento opcional que se usa para indicar mensajes de error. Si el elemento Fault está presente, debe ser un elemento secundario del elemento Body.

Los archivos ASMX se pueden escribir en lenguajes .NET como [C#](/es/programming/cs/), [Visual Basic](/es/programming/vb/) o JScript.

## ¿En qué se diferencia ASMX de ASPX y ASCX?

Los archivos ASMX son diferentes a los archivos ASPX y ASCX.

* Los archivos ASPX, Active Server Pages son archivos de programación que se generan utilizando el marco Microsoft ASP.NET que se ejecuta en servidores web. Estos se representan en el navegador web del cliente cuando el usuario solicita acceder a dicha página.
* ASCX, Active Server User Control, define controles de usuario que se utilizan para definir controles reutilizables en páginas web ASP.NET o en todo el sitio web.

## Referencias

* [Consumo del servicio ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Control de usuario de ASCX] (http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

