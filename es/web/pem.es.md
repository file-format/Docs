{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo PEM: formato de archivo de certificado de correo con privacidad mejorada",
  "description":"Obtenga información sobre el formato de archivo PEM y las API que pueden crear y abrir archivos PEM",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## ¿Qué es un archivo PEM?

Un archivo PEM es un archivo de certificado de seguridad que se utiliza para establecer un canal de comunicación seguro entre un servidor web y un navegador. Está codificado en Base64 y puede contener una clave privada, un certificado de servidor y/o una combinación de otros certificados. Los archivos PEM son similares a los archivos de certificado .der en términos de uso, pero se almacenan como texto codificado en Base64 en lugar de datos binarios. Otros formatos de archivo de certificado similares incluyen archivos [.cer](/es/web/cer/) y [.crt](/es/web/crt/).

Las aplicaciones que pueden **abrir archivos PEM** incluyen editores de texto como Microsoft Notepad y Apple TextEdit.

## Formato de archivo PEM

PEM es un formato de archivo contenedor que define la estructura y el tipo de codificación del archivo utilizado para almacenar los datos. Los archivos PEM se almacenan en el disco como formato de archivo codificado en Base64 que no es legible por humanos. El estándar define que un archivo PEM comienza con:

```
-----BEGIN <type>-----
```
y termina con:
```
-----END <type>-----
```

Todo el resto del contenido dentro de estos está codificado en base64 (letras mayúsculas y minúsculas, dígitos, + y /). Un solo archivo PEM puede comprender varios bloques que pueden ser utilizados por otros programas. Si un archivo PEM contiene varios certificados, cada certificado se separa en bloques individuales de la siguiente manera:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Ejemplo de archivo PEM

Un archivo PEM con bloque de CERTIFICADO generalmente tiene el siguiente aspecto:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Un archivo PEM con RSA comienza de la siguiente manera.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referencias ##

* [Criptografía de clave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [¿Cómo crear un archivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

