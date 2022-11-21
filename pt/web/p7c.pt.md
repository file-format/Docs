{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - Arquivo de Certificado PKCS 7",
  "description":"Saiba mais sobre o formato de arquivo P7C e APIs que podem criar e abrir arquivos P7C.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo P7C?

Um arquivo P7C, como outros arquivos de certificado de segurança, é um certificado digital usado para autenticar a identidade na rede. Os aplicativos que usam certificados autenticam a identidade usando a chave pública incluída nesses arquivos de certificado. A criptografia de chave pública, ou criptografia assimétrica, usa um par de chaves, uma delas é a chave pública e a outra é conhecida como chave privada. A chave privada é mantida segura para uma segurança efetiva, enquanto a chave pública pode ser compartilhada com outras pessoas. Outros formatos comuns de arquivo de certificado incluem [CRT](/pt/web/crt/), DER e PEM.

## Formato de arquivo P7C - Mais informações

Os arquivos P7C são salvos em disco como arquivos binários e incluem as informações de chave pública geradas usando algoritmos criptográficos baseados em problemas matemáticos. Eles podem ser abertos em qualquer editor de texto, mas seu conteúdo não está em formato legível por humanos. Alguns dos aplicativos que podem abrir arquivos P7C incluem Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft Certificate Manager e Microsoft Windows Contacts.

### Exemplo de formato de arquivo P7C

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referências ##

* [Criptografia de chave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Como criar um arquivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

