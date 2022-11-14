{
  "date" : "2019-10-11",
  "keywords" :[ "crt","archivo crt", "formato de archivo crt", "tipo de archivo crt", "archivo", "tipo", "qué es un archivo crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Formato de archivo de certificado de seguridad",
  "description":"Obtenga información sobre el formato de archivo CRT y las API que pueden crear y abrir archivos CRT",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo CRT?

Un archivo con la extensión .crt es un archivo de certificado de seguridad que utilizan los sitios web seguros para establecer conexiones seguras desde el servidor web a un navegador. Los sitios web seguros permiten transferencias de datos seguras, inicios de sesión, transacciones con tarjetas de pago y proporcionan una navegación protegida en el sitio. Si abre un sitio web seguro, verá un icono de "candado" en la barra de direcciones. Si hace clic en él, puede ver los detalles del certificado instalado. Empresas internacionales como Verisign y Thawte distribuyen estos certificados SSL.

## Formato de archivo CRT

Los archivos CRT están en formato ASCII y se pueden abrir en cualquier editor de texto para ver el contenido del archivo del certificado. Sigue el estándar de certificación X.509 que define la estructura del certificado. Define los campos de datos que se deben incluir en el certificado SSL. CRT pertenece al formato PEM de certificados que son archivos codificados en Base64 ASCII.

### Estructura del archivo PEM

Un archivo PEM puede tener varios certificados. En tal caso, cada certificado en el archivo PEM sigue la siguiente estructura.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Ejemplo de formato de archivo CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencias ##

* [Claves públicas, claves privadas y certificados](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

