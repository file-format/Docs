{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo CSR - Formato de archivo de solicitud de firma de certificado",
  "description" :"Obtenga información sobre qué es un archivo CSR y las API que pueden crear y abrir archivos CSR",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## ¿Qué es un archivo CSR?

Un archivo CSR es un archivo de **Solicitud de firma de certificado** que se utiliza para solicitar un certificado SSL/TLS. Cuando necesites tener tu certificado SSL/TLS, generas el CSR en el mismo servidor donde finalmente se instalará. Este archivo CSR se comparte con la autoridad de certificación (CA) para la creación del certificado. Contiene información como el nombre común, la organización, el país y, lo que es más importante, la **clave pública** que está integrada en su archivo de certificado y está firmada con la clave privada correspondiente.

Las aplicaciones que pueden **abrir archivos CSR** incluyen OpenSSL y Microsoft IIS.

## Formato de archivo de solicitud de firma de certificado

Se crea un archivo CSR en un formato PEM Base-64 que se puede abrir y ver en un editor de texto simple como el Bloc de notas de Microsoft. Incluye un encabezado **-----COMENZAR NUEVA SOLICITUD DE CERTIFICADO-----** al inicio del archivo y un pie de página **-----FINALIZAR NUEVA SOLICITUD DE CERTIFICADO-----** al el final del archivo.

### ¿Cómo se ve un archivo CSR?

Un ejemplo simple de un archivo CSR es el siguiente.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## ¿Qué información se incluye en un CSR?

Un archivo CSR contiene la siguiente información.

1. "Información sobre la empresa y el sitio web": incluye información como nombre común, organización, unidad organizativa, ciudad/localidad, estado/condado/región (S), país y dirección de correo electrónico
1. "Clave pública": se incluye en el certificado y se utiliza para cifrar los datos transmitidos, que se descifran con la clave privada correspondiente.
1. "Información sobre el tipo y la longitud de la clave": generalmente es RSA 2048, pero también puede venir en tamaños más grandes, como RSA 4096+

## Referencias

* [Servidor de aplicaciones conceptuales] (https://github.com/Devronium/ConceptApplicationServer)

