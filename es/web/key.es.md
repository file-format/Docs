{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo KEY y las API que pueden crear y abrir archivos KEY",
  "title" :"Formato de archivo KEY - Archivo de clave privada de correo con privacidad mejorada",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## ¿Qué es un archivo KEY?

Un archivo KEY es la parte privada de un mecanismo de seguridad que se guarda en un disco en formato de archivo de privacidad mejorada Mal (PEM). Se utiliza para descifrar la información intercambiada entre un navegador web y el servidor web que atiende las solicitudes de navegación. Un archivo KEY contiene cadenas codificadas que son inútiles para el ojo humano, pero son la esencia del intercambio de información de cifrado/descifrado como parte del certificado SSL en los servidores web. Los archivos KEY se generan automáticamente y se instalan en el extremo del cliente.

Puede abrir archivos **CLAVE** con cualquier editor de texto como Microsoft Notepad (Windows), Apple TextEdit (Mac) o GitHub Atom (multiplataforma). Los archivos KEY son similares a los formatos de archivo [CRT](/es/web/crt/) y [CER](/es/web/cer/).

## Formato de archivo KEY - Más información

Los archivos KEY se almacenan en el disco como archivos de texto sin formato, pero son cadenas codificadas que no son fáciles de leer para los humanos. Prácticamente, los usuarios tienen cero comprensión de las cadenas cuando se abren en un editor de texto. El certificado de clave privada es confidencial y no debe compartirse con nadie. El proceso completo de asegurar el intercambio de información a través de Internet implica:

* **Clave pública**: se utiliza para cifrar la información del usuario para el intercambio de datos entre el navegador y los servidores web
* **Clave privada**: se utiliza para descifrar la información tal como la recibe el servidor web

Los certificados SSL, también conocidos como certificados X.509, son únicos para cada sitio web. Archivos KEY usando la siguiente sintaxis:

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

### Ejemplo de archivo CLAVE

A continuación se muestra un ejemplo de archivo de clave privada.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referencias

* [Claves públicas, claves privadas y certificados](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

