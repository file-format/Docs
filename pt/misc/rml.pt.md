{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Arquivo de modelo de relatório Elixir",
  "description":"Saiba mais sobre arquivos RML e APIs que podem criar e abrir arquivos RML.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## O que é um arquivo RML?

Um arquivo RML é um arquivo de modelo de relatório com o mecanismo de relatório [Elixir Repertoire](https://elixirtech.com/repertoire-2/). O arquivo de modelo é usado para gerar relatórios com a fonte de dados conectada ao Elixir FileSystem. Os dados são lidos e preenchidos no arquivo de modelo RML e podem ser exportados para vários formatos de arquivo diferentes, como [PDF](/pt/pdf/), [RTF](/pt/word-processing/rtf/) e planilha [XLS] (/pt/planilha/xls/). O mecanismo de relatório Elixir Repertoire pode ser conectado a uma ampla variedade de fontes de dados JDBC.

## Formato de arquivo RML

Os detalhes da estrutura de arquivo interna do formato de arquivo RML não estão disponíveis publicamente. Os arquivos são gerados e salvos internamente pelo aplicativo Elixir Repertoire para gerar relatórios com dados preenchidos das fontes de dados conectadas. O arquivo de modelo RML contém o layout geral e as informações de marcadores do relatório final a ser gerado a partir dos dados.

## Como arquivo de modelo RML?

Para gerar o modelo RML no Elixir Repertoire, as etapas a seguir podem ser seguidas.

1. Conecte uma origem de dados JDBC ao sistema de arquivos.
1. Inicie o Assistente de modelo de relatório
1. Use o software para localizar o arquivo .ds da fonte de dados
1. Escolha o relatório tabular como opção de exportação
1. Selecione os campos a serem incluídos no modelo de relatório
1. Por fim, ao clicar no botão Finish, First report.rml é adicionado ao repositório e aberto para mostrar a aba Layout.

## Referências

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)

