{
  "date" : "2019-10-11",
  "keywords" :[ "crt","arquivo crt", "formato de arquivo crt", "tipo de arquivo crt", "arquivo", "tipo", "o que é um arquivo crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Formato de arquivo de certificado de segurança",
  "description":"Saiba mais sobre o formato de arquivo CRT e APIs que podem criar e abrir arquivos CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo CRT?

Um arquivo com extensão .crt é um arquivo de certificado de segurança usado por sites seguros para estabelecer conexões seguras do servidor da Web para um navegador. Sites seguros possibilitam transferências de dados seguras, logins, transações com cartão de pagamento e fornecem navegação protegida no site. Se você abrir um site seguro, verá um ícone de "cadeado" na barra de endereço. Se você clicar nele, poderá visualizar os detalhes do certificado instalado. Empresas internacionais como Verisign e Thawte distribuem esses certificados SSL.

## Formato de arquivo CRT

Os arquivos CRT estão no formato ASCII e podem ser abertos em qualquer editor de texto para visualizar o conteúdo do arquivo de certificado. Segue o padrão de certificação X.509 que define a estrutura do certificado. Ele define os campos de dados que devem ser incluídos no certificado SSL. O CRT pertence ao formato PEM de certificados que são arquivos codificados em Base64 ASCII.

### Estrutura do arquivo PEM

Um arquivo PEM pode ter vários certificados. Nesse caso, cada certificado no arquivo PEM segue a seguinte estrutura.

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

### Exemplo de formato de arquivo CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referências ##

* [Chaves públicas, chaves privadas e certificados](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

