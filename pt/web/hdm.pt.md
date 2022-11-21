{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo HDM - Arquivo de linguagem de marcação de dispositivo portátil",
  "description":"Saiba mais sobre o formato de arquivo HDM e APIs que podem criar e abrir arquivos HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## O que é um arquivo HDM?

Um arquivo HDM é um arquivo de página da Web de linguagem de marcação que é criado no Handheld Device Markup Language (HDML). Ele contém tags de marcação semelhantes à linguagem [HTML](/pt/web/html/), mas foi projetada para dispositivos eletrônicos portáteis, como smartphones e PDAs. As [especificações de formato de arquivo HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) foram enviadas ao W3C para padronização, mas não puderam se tornar um padrão. O HDM é baseado nas especificações de formato de arquivo [HDML](/pt/web/hdml/) disponíveis no site W3.

## Formato de arquivo HDM - Mais informações

O arquivo HDM consiste em tags de marcação que são renderizadas para um site projetado visualmente em dispositivos portáteis. Os arquivos HDM são copiados para dispositivos usando o protocolo HDTP (Handheld Device Transport Protocol) em vez do protocolo HTTP que é usado para páginas HTML.

## Elementos de arquivo HDML

A seguir está uma lista de elementos que fornecem ambiente de tempo de execução para HDML e são referidos como o agente do usuário.

|Elemento|Descrição|
---|---|
|Cartões|Este é o bloco de construção fundamental do HDML, e exibe e permite que o usuário interaja com cartões de informação. |
|Decks|Cartões HDML são agrupados em decks. Um deck HDML é semelhante a uma página HTML, pois é identificado por URL [RFC1738] e é a unidade de conteúdo solicitada de um servidor e armazenada em cache pelo agente do usuário.|
|Ações|As ações podem ser do tipo PREV, SOFT1-SOFT8 e HELP. Eles são abstratos e têm suporte na interface do usuário de uma maneira específica do agente do usuário.|
|Atividades|Uma atividade é como um grupo de cartas relacionadas que executam uma função lógica. Estes podem abranger um ou mais decks. A navegação HDML e o modelo de estado são estruturados em torno de atividades.|
|Navegação baseada em histórico|O agente do usuário mantém um histórico dos cartões exibidos ao usuário. Cada cartão acessado é adicionado ao histórico do cartão. O agente de usuário permite que o usuário navegue facilmente de volta ao cartão anterior no histórico.|

## Referências

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Especificações HDML - Escolas W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

