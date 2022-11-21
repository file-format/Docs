{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo KEY e APIs que podem criar e abrir arquivos KEY.",
  "title" :"Formato de arquivo KEY - Arquivo de chave privada de email com privacidade aprimorada",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## O que é um arquivo KEY?

Um arquivo KEY é a parte privada de um mecanismo de segurança que é salvo no disco no formato de arquivo Privacy-Enhanced Mal (PEM). Ele é usado para descriptografar as informações trocadas entre um navegador da Web e o servidor da Web que atende às solicitações de navegação. Um arquivo KEY contém strings codificadas que são inúteis para o olho humano, mas são a essência da troca de informações de criptografia/descriptografia como parte do certificado SSL em servidores da web. Os arquivos KEY são gerados automaticamente e instalados no cliente.

Você pode abrir arquivos **KEY** com qualquer editor de texto, como Microsoft Notepad (Windows), Apple TextEdit (Mac) ou GitHub Atom (plataforma cruzada). Os arquivos KEY são semelhantes aos formatos de arquivo [CRT](/pt/web/crt/) e [CER](/pt/web/cer/).

## Formato de arquivo KEY - Mais informações

Os arquivos KEY são armazenados no disco como arquivos de texto simples, mas são strings codificadas que não são fáceis de ler. Praticamente, os usuários não entendem as strings quando abertas em um editor de texto. O certificado de chave privada é confidencial e não deve ser compartilhado com ninguém. O processo completo de proteção da troca de informações pela Internet envolve:

* **Chave Pública** - usada para criptografar as informações do usuário para troca de dados entre o navegador e os servidores da web
* **Chave Privada** - usada para descriptografar as informações recebidas pelo servidor web

Os certificados SSL, também conhecidos como certificados X.509, são exclusivos para cada site. KEY arquivos usando a seguinte sintaxe:

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

### Exemplo de arquivo CHAVE

A seguir está um exemplo de arquivo de chave privada.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Referências

* [Chaves públicas, chaves privadas e certificados](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

