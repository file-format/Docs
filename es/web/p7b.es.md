{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Archivo de certificado PKCS 7",
  "description":"Obtenga información sobre el formato de archivo P7C y las API que pueden crear y abrir archivos P7C",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo P7B?

Un archivo P7B es un archivo de certificado de seguridad que contiene un certificado digital seguro para autenticar a una persona o un dispositivo. Similar a un archivo de certificado [.cer](/es/web/cer/), un archivo P7B se puede instalar usando la opción "Instalar certificado" haciendo clic con el botón derecho en el archivo. P7B utiliza una opción de formato diferente al formato de archivo CER. Contiene uno o más archivos de certificados digitales X.509 que usan codificación base64 (ASCII). Los archivos P7B se reciben como un archivo [ZIP](/es/compression/zip/) o se reciben de la autoridad de certificación.

## Formato de archivo P7B

Los archivos P7B se almacenan como archivos ASCII simples que se pueden abrir en cualquier editor de texto. Contiene la clave pública que es una cadena codificada que no tiene sentido desde el punto de vista de la legibilidad.

### Ejemplo de formato de archivo P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencias ##

* [Criptografía de clave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [¿Cómo crear un archivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

