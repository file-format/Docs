{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier CSR - Format de fichier de demande de signature de certificat",
  "description" :"Découvrez ce qu'est un fichier CSR et les API qui peuvent créer et ouvrir des fichiers CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Qu'est-ce qu'un dossier RSE ?

Un fichier CSR est un fichier **Certificate Signing Request** utilisé pour demander un certificat SSL/TLS. Lorsque vous avez besoin de votre certificat SSL/TLS, vous générez le CSR sur le même serveur où il sera finalement installé. Ce fichier CSR est partagé avec l'autorité de certification (CA) pour la création du certificat. Il contient des informations telles que le nom commun, l'organisation, le pays et, plus important encore, la **clé publique** intégrée dans votre fichier de certificat et signée avec la clé privée correspondante.

Les applications qui peuvent **ouvrir les fichiers CSR** incluent OpenSSL et Microsoft IIS.

## Format de fichier de demande de signature de certificat

Un fichier CSR est créé dans un format PEM Base-64 qui peut être ouvert et visualisé dans un simple éditeur de texte tel que Microsoft Notepad. Il comprend un en-tête **-----BEGIN NEW CERTIFICATE REQUEST-----** au début du fichier et un pied de page **-----END NEW CERTIFICATE REQUEST-----** à la fin du dossier.

### À quoi ressemble un fichier CSR ?

Un exemple simple de fichier CSR est le suivant.

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

## Quelles informations sont incluses dans un CSR ?

Un fichier CSR contient les informations suivantes.

1. "Informations sur l'entreprise et le site Web" - Comprend des informations telles que le nom commun, l'organisation, l'unité organisationnelle, la ville/localité, l'état/comté/région (S), le pays et l'adresse e-mail
1. `Clé publique` - Elle est incluse dans le certificat et est utilisée pour chiffrer les données transmises qui sont déchiffrées à l'aide de la clé privée correspondante
1. "Informations sur le type et la longueur de la clé" - Il s'agit généralement de RSA 2048, mais peut également être disponible dans des tailles plus grandes telles que RSA 4096+

## Références

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

