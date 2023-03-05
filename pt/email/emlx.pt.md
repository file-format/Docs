{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Formato de arquivo do Apple Mail",
  "description":"Saiba mais sobre o formato de arquivo EMLX e APIs que podem criar e abrir arquivos EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo EMLX?

O formato de arquivo EMLX é implementado e desenvolvido pela Apple. O aplicativo Apple Mail usa o formato de arquivo EMLX para exportar os e-mails. Também existem outros aplicativos que podem abrir os arquivos EMLX e convertê-los em outros formatos de arquivo.

## Breve História do Formato de Arquivo EMLX

O sistema operacional Mac OS X adotou o programa de e-mail existente, NeXTMail, criado pela NeXT como parte do sistema operacional NeXTSTEP. A Apple depois de adquirir a NeXT elevou seus recursos e tornou-se o agora aplicativo de e-mail Apple Mail a ser usado como cliente de e-mail padrão. Os e-mails exportados via Apple Mail são salvos diretamente como arquivos EMLX. Além disso, é o cliente de e-mail padrão para arquivos EMLX quando alguém os abre clicando duas vezes no Mac OS.

## Formato de arquivo EMLX

Os arquivos EMLx são arquivos simples baseados em texto que podem ser abertos em qualquer editor de texto como o Bloco de Notas. A estrutura do arquivo EMLX consiste em três partes:

* Uma contagem de bytes para a mensagem - Comprimento da própria mensagem, escrita em ASCII em decimal, terminada por 0x0a
* A mensagem em si
* Metadados de mensagem na forma de XML plist

Isso pode ser melhor explicado com a ajuda do seguinte exemplo de e-mail extraído do Apple Mail como EMLX e aberto em um editor de texto.

### Exemplo EMLX

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

Neste exemplo, o 875 mostra o comprimento total da mensagem. Os metadados da mensagem são incluídos no<plist> tags e os sinalizadores são descritos a seguir:

|Campo|Descrição|Valor
---|---|---|
|0|ler|1 << 0
|1|excluído|1 << 1
|2|respondido|1 << 2
|3|criptografado|1 << 3
|4|sinalizado|1 << 4
|5|recente|1 << 5
|6|rascunho|1 << 6
|7|inicial (não é mais usado)|1 << 7
|8|encaminhado|1 << 8
|9|redirecionado|1 << 9
|10-15|contagem de anexos|3F << 10 (6 bits)
|16-22|nível de prioridade|7F << 16 (7 bits)
|23|assinado|1 << 23
|24|é lixo|1 << 24
|25|não é lixo|1 << 25
|26-28|tamanho da fonte delta|7 << 26 (3 bits)
|29|nível de lixo eletrônico registrado|1 << 29
|30|destaque o texto no toc|1 << 30
|31|(não utilizado)|

## Veja também ##

* [EML](/pt/email/eml/)
* [MSG](/pt/email/msg/)

