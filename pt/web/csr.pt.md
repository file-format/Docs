{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo CSR - Formato de arquivo de solicitação de assinatura de certificado",
  "description" :"Saiba mais sobre o que é um arquivo CSR e APIs que podem criar e abrir arquivos CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## O que é um arquivo CSR?

Um arquivo CSR é um arquivo **Solicitação de assinatura de certificado** usado para solicitar o certificado SSL/TLS. Quando você precisa ter seu certificado SSL/TLS, você gera o CSR no mesmo servidor onde ele finalmente será instalado. Este arquivo CSR é compartilhado com a Autoridade de Certificação (CA) para a criação do certificado. Ele contém informações como nome comum, organização, país e, mais importante, a **chave pública** integrada ao seu arquivo de certificado e assinada com a chave privada correspondente.

Os aplicativos que podem **abrir arquivos CSR** incluem OpenSSL e Microsoft IIS.

## Formato de arquivo de solicitação de assinatura de certificado

Um arquivo CSR é criado em um formato PEM Base-64 que pode ser aberto e visualizado em um editor de texto simples, como o Microsoft Notepad. Inclui um cabeçalho **-----BEGIN NEW CERTIFICATE REQUEST-----** no início do arquivo e um rodapé **-----END NEW CERTIFICATE REQUEST-----** em o final do arquivo.

### Como é um arquivo CSR?

Um exemplo simples de um arquivo CSR é o seguinte.

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

## Quais informações estão incluídas em um CSR?

Um arquivo CSR contém as seguintes informações.

1. `Informações sobre a Empresa e o Site` - Inclui informações como Nome Comum, Organização, Unidade Organizacional, Cidade/Localidade, Estado/Condado/Região (S), País e Endereço de E-mail
1. 'Chave Pública' - Está incluída no certificado e é usada para criptografar os dados transmitidos que são descriptografados usando a chave privada correspondente
1. `Informações sobre o tipo e comprimento da chave` - Geralmente é RSA 2048, mas também pode vir em tamanhos maiores, como RSA 4096+

## Referências

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

