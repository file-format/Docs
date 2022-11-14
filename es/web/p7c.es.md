{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Archivo de certificado PKCS 7",
  "description":"Obtenga información sobre el formato de archivo P7C y las API que pueden crear y abrir archivos P7C",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo P7C?

Un archivo P7C, como otros archivos de certificados de seguridad, es un certificado digital que se utiliza para autenticar la identidad en la red. Las aplicaciones que utilizan certificados autentican la identidad mediante la clave pública incluida en estos archivos de certificado. La criptografía de clave pública, o criptografía asimétrica, utiliza un par de claves de las cuales una es la clave pública y la otra se conoce como clave privada. La clave privada se mantiene segura para una seguridad efectiva, mientras que la clave pública se puede compartir con otros. Otros formatos de archivo de certificado comunes incluyen [CRT](/es/web/crt/), DER y PEM.

## Formato de archivo P7C - Más información

Los archivos P7C se guardan en el disco como archivos binarios e incluyen la información de clave pública generada mediante algoritmos criptográficos basados en problemas matemáticos. Estos se pueden abrir en cualquier editor de texto, pero su contenido no está en forma legible por humanos. Algunas de las aplicaciones que pueden abrir archivos P7C incluyen Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager y Microsoft Windows Contacts.

### Ejemplo de formato de archivo P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencias ##

* [Criptografía de clave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [¿Cómo crear un archivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

