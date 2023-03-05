{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo CRL - Lista de revocación de certificados",
  "description":"Obtenga más información sobre el formato de archivo CRL y las API que pueden crear y abrir archivos CRL",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## ¿Qué es un archivo CRL?

Un archivo CRL (Lista de revocación de certificados) es una lista negra de certificados digitales X.509 que una autoridad de certificación (CA) revoca antes de la fecha de revocación asignada. Contiene información sobre la emisión y la fecha de revocación que permite a los administradores de seguridad bloquear los certificados digitales afectados. CRL no incluye certificados vencidos ya que su objetivo principal es notificar sobre los certificados no confiables y no válidos.

Las aplicaciones que pueden **abrir archivos CRL** incluyen OpenSSL, Microsoft IIS Server y Citrix NetScaler.

## Formato de archivo CRL: más información

Los archivos CRL contienen información en el estándar X.509 que también define su semántica para compartir información de clave pública. Otra información contenida dentro de un archivo CRL puede incluir el límite de tiempo por el cual se han revocado los certificados, el motivo de la revocación, el número de serie del certificado revocado y la marca de tiempo.


### Razones principales para agregar certificados a CRL

Puede haber varias razones para que se revoque el certificado de su sitio web y se agregue a la CRL. Algunos de ellos podrían ser;

1. La clave privada de su certificado ha sido comprometida
1. Su certificado no es válido o la CA lo emitió incorrectamente
1. Los detalles de la organización asociados con el certificado se modifican y la CA emite un nuevo certificado
1. Cualquier otro motivo ineludible por el que se haya revocado el certificado

## Referencias

* [Instituto Nacional de Estándares y Tecnología (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Grupo de trabajo de ingeniería de Internet (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Lista de revocación de certificados](https://en.wikipedia.org/wiki/Certificate_revocation_list)

