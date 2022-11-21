{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo de linguagem de marcação de dispositivo portátil",
  "description":"Saiba mais sobre o formato de arquivo HDML e APIs que podem criar e abrir arquivos HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## O que é um arquivo HDML?

Um arquivo com extensão .hdml (Handheld Device Markup Language) é uma linguagem de marcação para criar páginas da Web para dispositivos eletrônicos portáteis, como computadores portáteis, smartphones e dispositivos de exibição de informações. O HDML é considerado uma extensão da linguagem [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). O HDML é semelhante ao HTML, mas para dispositivos sem fio e portáteis que possuem telas pequenas, como PDA, telefones celulares e assim por diante. Foi substituído por WML para o qual atuou como uma influência importante.

## Formato de arquivo HDML - Mais informações

HDML é uma linguagem de marcação para dispositivos portáteis que se baseia em tags de marcação semelhantes ao HTML. O HDML foi submetido ao W3C para padronização, mas nunca se tornou um padrão. No entanto, suas especificações de formato de arquivo estão disponíveis no [site W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) para referência. A [sintaxe para linguagem HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) está disponível para referência do desenvolvedor e pode ser usada para desenvolvimento de aplicativos de amostra.

## Elementos HDML

A seguir está uma lista de elementos que fornecem ambiente de tempo de execução para HDML e são referidos como o agente do usuário.

|Elemento|Descrição|
---|---|
|Cartões|Este é o bloco de construção fundamental do HDML, e exibe e permite que o usuário interaja com cartões de informação. |
|Decks|Cartões HDML são agrupados em decks. Um deck HDML é semelhante a uma página HTML, pois é identificado por URL [RFC1738] e é a unidade de conteúdo solicitada de um servidor e armazenada em cache pelo agente do usuário.|
|Ações|As ações podem ser do tipo PREV, SOFT1-SOFT8 e HELP. Eles são abstratos e têm suporte na interface do usuário de uma maneira específica do agente do usuário.|
|Atividades|Uma atividade é como um grupo de cartas relacionadas que executam uma função lógica. Estes podem abranger um ou mais decks. A navegação HDML e o modelo de estado são estruturados em torno de atividades.|
|Navegação baseada em histórico|O agente do usuário mantém um histórico dos cartões exibidos ao usuário. Cada cartão acessado é adicionado ao histórico do cartão. O agente do usuário permite que o usuário navegue facilmente de volta ao cartão anterior no histórico.|

## Referências

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Especificações HDML - Escolas W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

