{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo P7S - Mensagem de e-mail assinada digitalmente",
  "description":"Saiba mais sobre o formato de arquivo P7S e APIs que podem criar e abrir arquivos P7S.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## O que é um arquivo P7S?

Um arquivo P7S é uma assinatura digital recebida com um e-mail assinado digitalmente. A presença deste arquivo como um anexo com o e-mail verifica se o e-mail é enviado de uma fonte autêntica. Isso garante que o remetente tenha um certificado de assinatura de email instalado em seu computador. Quando um e-mail assinado desse tipo é enviado do computador do usuário, o arquivo P7S é anexado a ele contendo o nome do remetente. Os clientes de e-mail que oferecem suporte a e-mails assinados podem ver as informações do remetente.

## Formato de arquivo P7S - Mais informações

S/MIME (Secure/Multipurpose Internet Mail Extensions) Os arquivos P7S contêm as informações em formato de texto simples que pode ser lido por humanos. Clientes de e-mail como Microsoft Outlook, Apple Mail e Mozilla Thunderbird suportam a leitura de informações assinadas digitalmente de um e-mail S/MIME. Assinar um e-mail verifica a identidade do remetente e informa ao destinatário que a mensagem é autêntica. Quando os e-mails são baixados de clientes de e-mail (como [EML](/pt/email/eml/) ou [MSG](/pt/email/msg/)), esses arquivos P7S são encontrados anexados a esses e-mails.

Um arquivo P7S contém as seguintes informações:

*Fonte de origem do e-mail
* Data e hora em que foi enviado,
* Se foi modificado durante a transmissão

Essas informações são incorporadas usando a tecnologia Public-Key Cryptography Standard #7 (PKCS7) para anexar digitalmente as assinaturas criptografadas ao e-mail.

## Referências ##

* [Ferramenta de assinatura da Microsoft](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

