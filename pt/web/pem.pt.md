{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo PEM - Formato de arquivo de certificado de email com privacidade aprimorada",
  "description":"Saiba mais sobre o formato de arquivo PEM e APIs que podem criar e abrir arquivos PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## O que é um arquivo PEM?

Um arquivo PEM é um arquivo de certificado de segurança usado para estabelecer um canal de comunicação seguro entre um servidor da Web e um navegador. É codificado em Base64 e pode conter uma chave privada, certificado de servidor e/ou uma combinação de outros certificados. Os arquivos PEM são semelhantes aos arquivos de certificado .der em termos de uso, mas são armazenados como texto codificado em Base64 em vez de dados binários. Outros formatos de arquivo de certificado semelhantes incluem arquivos [.cer](/pt/web/cer/) e [.crt](/pt/web/crt/).

Os aplicativos que podem **abrir arquivos PEM** incluem editores de texto, como o Microsoft Notepad e o Apple TextEdit.

## Formato de arquivo PEM

PEM é um formato de arquivo contêiner que define a estrutura e o tipo de codificação do arquivo usado para armazenar os dados. Os arquivos PEM são armazenados no disco como formato de arquivo codificado em Base64 que não é legível por humanos. O padrão define que um arquivo PEM começa com:

```
-----BEGIN <type>-----
```
e termina com:
```
-----END <type>-----
```

Todos os outros conteúdos dentro deles são codificados em base64 (letras maiúsculas e minúsculas, dígitos, + e /). Um único arquivo PEM pode ser composto por vários blocos que podem ser usados por outros programas. Se um arquivo PEM contiver vários certificados, cada certificado será separado por blocos individuais da seguinte forma:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Exemplo de arquivo PEM

Um arquivo PEM com bloco CERTIFICATE geralmente se parece com o seguinte:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Um arquivo PEM com RSA começa como a seguir.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Referências ##

* [Criptografia de chave pública](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Como criar um arquivo P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

