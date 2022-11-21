{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - Arquivo de caixa de correio de e-mail",
  "description":"Saiba mais sobre o formato de arquivo MBOX e APIs que podem criar e abrir arquivos MBOX.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo MBOX?

O formato de arquivo MBox é um termo genérico que representa um contêiner para coleta de mensagens de correio eletrônico. As mensagens são armazenadas dentro do contêiner junto com seus anexos. As mensagens de uma pasta inteira são salvas em um único arquivo de banco de dados e as novas mensagens são anexadas ao final do arquivo. Numerosos aplicativos e API fornecem suporte para o formato de arquivo MBox, como Apple Mail e Mozilla Thunderbird.

## Formato de arquivo MBOX ##

O formato de arquivo MBox permaneceu não padronizado por muito tempo até 2005, quando o aplicativo/mbox foi padronizado como [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Mensagens, no formato RFC 2822 , são concatenados dentro do formato de arquivo MBox um após o outro. Cada mensagem começa com uma linha separadora que identifica o remetente da mensagem e também identifica a data e hora em que a mensagem foi recebida pelo destinatário final (o sistema de último salto no caminho de transferência ou o sistema que serve como correio). Cada mensagem é normalmente terminada por uma linha vazia. O final do banco de dados geralmente é reconhecido pela ausência de quaisquer dados adicionais ou pela presença de um marcador de final de arquivo explícito.

## Lendo uma mensagem do arquivo MBox ##

Um leitor varre um arquivo mbox procurando por linhas From_. Qualquer linha From_ marca o início de uma mensagem. O leitor não deve tentar tirar vantagem do fato de que cada linha From_ (após o início do arquivo) é uma linha em branco. Uma vez que o leitor encontra uma mensagem, ele extrai um remetente de envelope (possivelmente corrompido) e a data de entrega da linha From_. Em seguida, ele lê até a próxima linha From_ ou final do arquivo, o que ocorrer primeiro. Ele retira a linha em branco final e exclui a citação de linhas >From_ e >>From_ linhas e assim por diante. O resultado é uma mensagem RFC 822.

## Considerações de codificação ##

O conteúdo de um arquivo MBox pode ficar irreversivelmente misturado quando um e-mail recebido contém um arquivo Mbox como anexo e é salvo em outro arquivo Mbox. Para evitar isso, os sistemas de mensagens devem codificar um banco de dados mbox com codificação de transferência não transparente (como BASE64 ou Quoted-Printable) sempre que tal objeto for transferido por meio de protocolos de mensagens. Os implementadores também devem estar preparados para codificar dados mbox localmente se dados não compatíveis forem recebidos.

## Referências ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)

