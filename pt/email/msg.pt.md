{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Formato de e-mail do Microsoft Outlook",
  "description":"Saiba mais sobre o formato de arquivo MSG e APIs que podem criar e abrir arquivos MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo MSG?

MSG é um formato de arquivo usado pelo [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) e pelo Exchange para armazenar mensagens de email , contato, compromisso ou outras tarefas. Essas mensagens podem conter um ou mais campos de e-mail, com o remetente, destinatário, assunto, data e corpo da mensagem, ou informações de contato, detalhes do compromisso e uma ou mais especificações de tarefas. As propriedades que constituem o objeto Message, inclusive, também fazem parte do arquivo MSG. O arquivo MSG possui cabeçalhos, corpo da mensagem principal e hiperlinks como texto ASCII simples. Os arquivos MSG também são adequados para os programas que precisam do MAPI (Messaging Applications Programming Interface) da Microsoft.

## Estrutura do arquivo MSG

O formato CFB_3 é a base do arquivo MSG. O paradigma é baseado nos conceitos de storages e streams, bem próximos de diretórios e arquivos. Portanto, uma grande diferença no primeiro é a hierarquia inteira, empacotada em um arquivo distinto, chamado de arquivo composto. Os objetos constituem os arquivos de mensagens e consistem em uma única propriedade ou suas coleções. Essa capacidade facilita que os aplicativos armazenem dados complexos e estruturados em um único arquivo. Esse formato também especifica vários armazenamentos, cada armazenamento representa o objeto Message como um componente principal. Esses armazenamentos contêm vários fluxos que representam uma propriedade desse componente. Aninhamento de armazenamento também é possível.

## Propriedades Mapi

No nível superior do arquivo .msg, os armazenamentos contêm fluxos que armazenam propriedades neles. As propriedades podem ser classificadas da seguinte forma:

* Propriedades de comprimento fixo
* Propriedades de comprimento variável
* Propriedades de vários valores

Independentemente da categoria, uma propriedade é identificada ou nomeada. No entanto, informações de mapeamento adequadas são necessárias para propriedades nomeadas conforme especificado pelo armazenamento de mapeamento.

## Armazenamentos

Os armazenamentos constituem os principais componentes do objeto Message. O formato de arquivo MSG indica os seguintes armazenamentos:

## Estrutura de nível superior

O objeto Message representa todo o nível superior do formato de arquivo MSG. Dependendo do tipo, propriedades, número de destinatários e objetos de anexo, um objeto de mensagem pode ter diferentes armazenamentos de fluxo em seu arquivo .MSG correspondente.

### Relacionamento com outras estruturas

O formato de arquivo Msg tem as seguintes relações com outras estruturas:

* A base de .msg é o formato de arquivo binário de arquivo composto.
* As propriedades usadas pelo Message and Attachment Object Protocol são usadas por este formato.

## Cenários para evitar formatos MSG

O objeto de mensagem pode ser compartilhado entre clientes ou armazenamentos de mensagens que usam o sistema de arquivos .msg. Existem algumas circunstâncias em que o armazenamento de um objeto Message no formato de arquivo .msg não seria apropriado. Por exemplo:

* No caso de manter um grande arquivo independente, é melhor usar um formato completo no qual as visualizações possam ser renderizadas com mais precisão.
* Se o receptor for desconhecido, é possível que o formato não seja suportado pelo receptor e que seja privado ou irrelevante.

## Exemplo de arquivo MSG

Para ter uma ideia de como um arquivo MSG se parece, você pode baixar um [exemplo de arquivo MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) e abrir no seu computador para visualizar seu conteúdo.

## Referências

* [[MS-OXMSG]: Formato de arquivo MSG do Outlook](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

