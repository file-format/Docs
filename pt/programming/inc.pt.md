{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extensão de arquivo INC - O que é um arquivo INC?",
  "description":"Saiba mais sobre o formato de arquivo INC Include e APIs que podem criar e abrir arquivos INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## O que é um arquivo INC?

Um arquivo INC é um arquivo de inclusão usado pelo código-fonte do programa de software para referenciar informações de cabeçalhos. É semelhante ao formato de arquivo [.h](/pt/programming/h/) e contém declarações, funções, cabeçalhos ou macros que podem ser reutilizados por arquivos de código-fonte, como C++. Os arquivos INC são usados por uma variedade de linguagens de programação como C, [C++](/pt/programming/cpp/), Pascal, [PHP](/pt/programming/php/) e [Java](/pt/programming/java/). Editores de texto como Microsoft Notepad, Notepad++ e TextEdit podem ser usados para abrir arquivos INC.

## Formato de arquivo INC - Mais informações

Um arquivo INC é salvo como arquivo de texto simples com todas as declarações incluídas de acordo com a sintaxe da declaração. Um arquivo INC também pode fazer referência a outros arquivos INC. Uma vez criado, o arquivo INC torna-se parte do projeto e pode ser referenciado a partir de arquivos de origem, como C++. Ele pode ser referenciado por vários arquivos de origem para evitar qualquer duplicação.

## Conteúdo do arquivo INC

Os arquivos INC podem incluir as seguintes informações.

**`Variables`** - No caso de Programação Orientada a Objetos (OOP), um arquivo de cabeçalho de classe contém definições de todas as variáveis de nível de classe que são acessíveis nos arquivos de código-fonte de implementação

**`Declaração de Métodos`** - Todas as declarações de métodos são incluídas nos arquivos de cabeçalho .h para serem acessíveis em vários arquivos de implementação.

**`Definições de Função Não Inline`** - Arquivos de cabeçalho também podem conter definições de métodos não embutidos.

## Desvantagem de usar o arquivo INC em PHP

PHP são scripts do lado do servidor que são executados no servidor e retornam os resultados para as páginas da Web de chamada. Se um arquivo PHP está referenciando um arquivo INC e o servidor não está configurado para analisar arquivos .inc (o que é muito comum), um usuário pode visualizar o código fonte php no arquivo .inc visitando o diretório URL. Portanto, deve-se ter cuidado ao usar arquivos INC como arquivos de inclusão no PHP.

## Referências

* [Usando INC em PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

