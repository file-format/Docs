{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "arquivo", "extensão", "formato de arquivo", "Mathematica", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o que é uma API de arquivo NB que pode criar e abrir arquivos NB.",
  "title" :"NB - Formato de Arquivo de Notebook do Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## O que é um arquivo NB?

Um arquivo com extensão .nb é um formato de arquivo de notebook Wolfram que salva instruções para instruções matemáticas em um arquivo textual. Ele pode conter muitos tipos diferentes de dados, como computação ao vivo, interfaces dinâmicas arbitrárias, entrada tipográfica completa, entrada de imagem, anotação automática de código, uma interface programática completa de alto nível e milhares de funções e opções cuidadosamente organizadas. As instruções textuais são entradas e saídas do Mathematica que são geradas e atualizadas conforme as instruções de entrada são colocadas no arquivo.

## Formato de arquivo Wolfram Notebook NB - Mais informações

Os arquivos do Wolfram Notebook NB são salvos em formato textual simples, que é um formato de arquivo legível por humanos. O conteúdo de um bloco de anotações é organizado em seções como texto simples, onde cada um é representado por grupos de células, semelhante a uma planilha. O intervalo desses grupos é definido por um colchete no final de cada célula. O estilo atribuído a uma célula determina sua função no bloco de anotações, conforme detalhado abaixo.

### Notebooks como linguagem Wolfram

Quando se pretende salvar o Notebook que consiste em instruções matemáticas para execução pelo Wolfram Language Kernal, as células do documento recebem automaticamente o estilo de texto 'Input'. Isso diz ao kernal para considerá-las como instruções que são executadas quando o usuário emite uma combinação de teclas `Shift+Return`. Um Mathematica Notebook é mostrado no exemplo a seguir.

{{< figure src="../Wolfram Notebook.jpeg" alt="Formato de arquivo do notebook Wolfram" >}}

### Cadernos como Documentos

Cadernos do Mathematica podem estar em formato de documento para dar uma visão do que você vê o que é o que você obtém (WYSIWYG). Esses documentos são os mesmos visualizados na tela ou em papel impresso e são interativos. Para isso, o `Text Style` é atribuído à célula para exibir o conteúdo sem executar as instruções pelo Kernel.

## Exportar Notebooks Mathematica

Os Notebooks do Mathematica podem ser exportados para vários formatos de arquivo diferentes, como PDF, gráficos, GIS, compactados e planilhas.

## Referências

* [Noções básicas do Mathematica Notebook](https://reference.wolfram.com/language/guide/NotebookBasics.html)

