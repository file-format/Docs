{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Arquivo de modelo de email do Microsoft Outlook",
  "description":"Saiba mais sobre o formato de arquivo OFT e APIs que podem criar e abrir arquivos OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo OFT?

Arquivos com extensão .oft são arquivos de modelo criados usando o Microsoft Outlook. O layout pré-formatado definido para modelos de mensagem é usado para enviar e-mails com informações comuns para economizar tempo. Esses arquivos podem ser gerados criando um novo e-mail, adicionando as informações necessárias e usando a lista suspensa Salvar como modelo do Office (.oft) do Microsoft Outlook. Os usuários podem abrir os arquivos OFT clicando duas vezes nele e ele será aberto no aplicativo associado nesse sistema específico.

## Estrutura de arquivos OFT ##

O formato de arquivo .OFT usa o formato de arquivo [MSG](/pt/email/msg/) em sua base. A única diferença é que os arquivos OFT têm CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) como classe de armazenamento (WriteClassStg), enquanto os arquivos MSG usam CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

O formato CFB_3 é a base do arquivo MSG. O paradigma é baseado nos conceitos de storages e streams, bem próximos de diretórios e arquivos. Portanto, uma grande diferença no primeiro é a hierarquia inteira, empacotada em um arquivo distinto, chamado de arquivo composto. Os objetos constituem os arquivos de mensagens e consistem em uma única propriedade ou suas coleções. Essa capacidade facilita que os aplicativos armazenem dados complexos e estruturados em um único arquivo. Esse formato também especifica vários armazenamentos, cada armazenamento representa o objeto Message como um componente principal. Esses armazenamentos contêm vários fluxos que representam uma propriedade desse componente. Aninhamento de armazenamento também é possível.

### Propriedades OFT

No nível superior do arquivo .msg, os armazenamentos contêm fluxos que armazenam propriedades neles. As propriedades podem ser classificadas da seguinte forma:

* Propriedades de comprimento fixo
* Propriedades de comprimento variável
* Propriedades de vários valores

Independentemente da categoria, uma propriedade é identificada ou nomeada. No entanto, informações de mapeamento adequadas são necessárias para propriedades nomeadas conforme especificado pelo armazenamento de mapeamento.

### Armazenamentos OFT

Os armazenamentos constituem os principais componentes do objeto Message. O formato de arquivo MSG indica os seguintes armazenamentos:

### Estrutura de nível superior

O objeto Message representa todo o nível superior do formato de arquivo Msg. Dependendo do tipo, propriedades, número de destinatários e objetos de anexo, um objeto de mensagem pode ter diferentes armazenamentos de fluxo em seu arquivo .MSG correspondente.

#### Relacionamento com outras estruturas

O formato de arquivo MSG/OFT tem as seguintes relações com outras estruturas:

* A base de .msg é o formato de arquivo binário de arquivo composto.
* As propriedades usadas pelo Message and Attachment Object Protocol são usadas por este formato.

## Referências

* [[MS-OXMSG]: Formato de arquivo MSG do Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

