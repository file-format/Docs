{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - Arquivo de certificado PKCS 7",
  "description":"Saiba mais sobre o formato de arquivo P7C e APIs que podem criar e abrir arquivos P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo P7B?

Um arquivo P7B é um arquivo de certificado de segurança que contém um certificado digital seguro para autenticar uma pessoa ou um dispositivo. Semelhante a um arquivo de certificado [.cer](/pt/web/cer/), um arquivo P7B pode ser instalado usando a opção "Instalar certificado" clicando com o botão direito do mouse no arquivo. O P7B usa uma opção de formatação diferente do formato de arquivo CER. Ele contém um ou mais arquivos de certificado digital X.509 que usam a codificação base64 (ASCII). Os arquivos P7B são recebidos como um arquivo [ZIP](/pt/compression/zip/) ou recebidos da Autoridade de Certificação.

## Formato de arquivo P7B

Os arquivos P7B são armazenados como arquivos ASCII simples que podem ser abertos em qualquer editor de texto. Ele contém a chave pública que é uma string codificada que não tem sentido do ponto de vista da legibilidade.

### Exemplo de formato de arquivo P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referências ##

* [Criptografia de chave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Como criar um arquivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

