{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo P7S: mensaje de correo electrónico firmado digitalmente",
  "description":"Obtenga información sobre el formato de archivo P7S y las API que pueden crear y abrir archivos P7S",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## ¿Qué es un archivo P7S?

Un archivo P7S es una firma digital que se recibe con un correo electrónico firmado digitalmente. La presencia de este archivo como archivo adjunto con el correo electrónico verifica que el correo electrónico se envía desde una fuente auténtica. Esto garantiza que el remitente tenga un certificado de firma de correo electrónico instalado en su computadora. Cuando se envía un correo electrónico firmado desde la computadora del usuario, se adjunta el archivo P7S que contiene el nombre del remitente. Los clientes de correo electrónico que admiten correos electrónicos firmados pueden ver la información del remitente.

## Formato de archivo P7S - Más información

Los archivos S/MIME (Extensiones de correo de Internet seguras/multipropósito) P7S contienen la información en formato de texto sin formato que es legible por humanos. Los clientes de correo electrónico como Microsoft Outlook, Apple Mail y Mozilla Thunderbird admiten la lectura de la información firmada digitalmente de un correo electrónico S/MIME. Firmar un correo electrónico verifica la identidad del remitente y le dice al receptor que el mensaje es auténtico. Cuando los correos electrónicos se descargan de clientes de correo electrónico (ya sea como [EML](/es/email/eml/) o [MSG](/es/email/msg/)), estos archivos P7S se encuentran adjuntos a estos correos electrónicos.

Un archivo P7S contiene la siguiente información:

* Fuente de origen del email
* Fecha y hora en que fue enviado,
* Si ha sido modificado durante la transmisión

Esta información se incrusta mediante la tecnología Public-Key Cryptography Standard #7 (PKCS7) para adjuntar digitalmente las firmas cifradas al correo electrónico.

## Referencias ##

* [Herramienta de inicio de sesión de Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

