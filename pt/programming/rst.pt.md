{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST File Format - reStructuredText File",
  "description":"Saiba mais sobre o formato de arquivo RST e APIs que podem criar e abrir arquivos RST.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## O que é um arquivo RST?

Um arquivo RST é um formato de arquivo de documentação técnica, usado principalmente na comunidade de programação Python. É um arquivo de texto escrito na linguagem de marcação reStructuredText que aplica estilos e formatação a documentos de texto simples para geração de documentação. Os arquivos RST usam os comentários e outras informações no código dos programas Python para criar a documentação técnica do aplicativo. No entanto, eles também podem conter texto que pode ser convertido em páginas da Web simples e [eBooks](/pt/ebook/). Editores de texto como Github Atom, GNU Emacs (plataforma cruzada), Microsoft Notepad (Windows), Apple TextEdit (Mac) e Vim (Linux) podem ser usados para abrir arquivos RST.

## Formato de arquivo RST

Os arquivos RST contêm código escrito na linguagem de marcação reStructuredText. Faz parte do projeto Docutils do Python Doc-SIG (Documentation Special Interest Group) que fornece um conjunto de ferramentas para Python semelhantes ao Javadoc para Java. O analisador para formato de arquivo RST está embutido no Docutils e pode extrair informações de programas Python para formatá-los na documentação do programa.

### Exemplo de RST de texto reestruturado

Vamos dar um exemplo de texto escrito no formato de arquivo RST como segue.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

Quando esse texto é inserido em um processador rST como o Docutils, a saída é a seguinte.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## Referência ##

* [reStructuredText - pela Wikipedia](https://en.wikipedia.org/wiki/ReStructuredText)

