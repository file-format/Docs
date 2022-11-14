{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extensión", "archivo", "formato", "web", "certificado", "idioma" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Formato de archivo de certificado",
  "description":"Obtenga información sobre el formato de archivo CER y las API que pueden crear y abrir archivos CER",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## ¿Qué es un archivo CER? ##

Un archivo con extensión .cer es responsable de almacenar cierta información sobre el certificado del propietario y la clave pública específica. Este formato de archivos no puede almacenar las claves privadas y tiene la capacidad de almacenar solo un certificado que es x509. Las autoridades de certificación específicamente seguras son las que pertenecen a HTTPS, un protocolo confiable y seguro para navegar
El CER es un certificado de su servidor. Por lo general, lo recibe la autoridad de certificación del dominio. CER se considera mayormente lo mismo que [CRT](/es/web/crt/), aunque ambos tienen el mismo formato de certificado SSL pero tienen extensiones de nombre de archivo diferentes.
Estos se pueden usar en sistemas operativos simplemente abriendo un navegador y verificando la seguridad del navegador o sitio web que se está utilizando.

## Breve historia ##

En 1995, Thawte se convirtió en la primera autoridad de certificación para resolver el problema de los certificados SSL públicos (enlace de socket seguro) fuera de los EE. UU. Después de eso, hay una serie de autoridades de este tipo que se fundaron entre 1995 y 2020.

## Formato de archivo CER ##

Estos archivos pueden ser simplemente
* El PKC S#7 incluye codificación Base64 ASCII
* Sus extensiones de archivo son p7b o p7cZ
* Para contenido binario, el certificado sería DER o pkcs12/pfx.
Hay muchos tipos de archivos de certificado con algunas especificaciones únicas:
* .pem, cuando una organización usthawteificate encadenar este formato es bien conocido para crear certificados
* .arm, cuando se requiera el método para extraer una certificación asiste autofirmado, el formato especificado para tal fin es .arm. Se representa en codificación ASCII base-64.
* .der, consta de datos binarios. Esto significa que solo se puede utilizar para un único certificado.
* .pfx (PKC512), Consiste en una clave privada correspondiente a un certificado emitido por CA o un certificado autofirmado. Este formato es bien conocido por la conversión de una implementación SSL a otra.


