{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "arquivo", "extensão", "formato", "E-Book", "Livro digital" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo EPUB e APIs que podem criar e abrir arquivos EPUB.",
  "title" :"O que é um arquivo EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## O que é um arquivo EPUB?

Arquivos com extensão .epub são um formato de arquivo de e-book que fornece um formato de publicação digital padrão para editores e consumidores. O formato tem sido tão comum até agora que é suportado por muitos e-readers e aplicativos de software. Por exemplo, no Mac OS, o software **Books** pré-instalado oferece suporte para abrir esses arquivos. Além disso, há muitos softwares compatíveis disponíveis para smartphones, tablets e computadores. Os padrões de arquivo EPUB são mantidos pelo [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). A versão EPUB 3 também é endossada pelo Book Industry Study Group (BISG), uma associação líder no comércio de livros para melhores práticas padronizadas, pesquisas, informações e eventos, para embalagem de conteúdo.

## Breve História do Formato de Arquivo EPUB

* **Outubro de 2007** - EPUB 2.0 foi aprovado
* **Setembro de 2010** - A atualização de manutenção foi lançada
* **Outubro de 2011** - As especificações do EPUB 3.0 entraram em vigor
* **Junho de 2014** - Pequena atualização de manutenção foi lançada para substituir a versão 3.0
* **Janeiro de 2017** - EPUB 3.1 entrou em vigor

## Formato de arquivo EPUB

O formato de arquivo EPUB é um arquivo que pode ser renomeado para a extensão [ZIP](/pt/compression/zip/) e seu conteúdo pode ser visualizado extraindo o arquivo com qualquer extrator de arquivo. É um formato aberto baseado em XML e consiste em arquivos HTML, imagens, folhas de estilo CSS e outros elementos. Também pode ser convertido para PDF, Mobi e vários outros formatos de arquivo por meio de vários aplicativos de software e APIs.

{{< figure src="../epub.png" alt="Formato de arquivo EPUB" >}}

**EPUB E-Book aberto com o aplicativo Mac OS Books**

O formato de arquivo EPUB é baseado em três padrões abertos.

### Estrutura Pública Aberta (OPS) ###

Um arquivo EPUB 2.0 usa XHTML 1.1 para construir o conteúdo de uma publicação. Em essência, isso significa que um arquivo EPUB consiste em uma ou mais páginas da web. Mesmo que você possa incluir todo o conteúdo de um livro ou jornal em uma única página, é melhor que esse arquivo não exceda 300K, tanto por questões de desempenho quanto de compatibilidade. Assim como nas páginas da Web comuns, o estilo e o layout são definidos usando folhas de estilo em cascata (CSS). Em arquivos EPUB, um subconjunto (série limitada de comandos) de CSS2 precisa ser usado. Muitos dos novos recursos do CSS3, como caixas arredondadas ou sombras projetadas, ainda não estão disponíveis. Para compatibilidade com versões anteriores, um criador também pode usar DTBook em vez de XHTML para codificar o conteúdo.

### Formato de embalagem aberta (OPF) ###

Esta parte das especificações lida com informações estruturais como metadados (quem é o autor e o editor, qual é o título,...), o manifesto (uma lista de todos os arquivos dentro de um arquivo epub) e o índice. Esses dados são todos incorporados usando XML.

### Formato de Contêiner Aberto (OCF) ###

Como as descrições acima devem ter deixado claro, um documento EPUB consiste em uma série de arquivos. As especificações do OCF definem como todos esses arquivos acabam sendo empacotados em um único arquivo de contêiner. A compactação ZIP é usada para isso.

## Formatos de arquivo de imagem suportados ##

O formato de arquivo EPUB suporta os seguintes formatos de arquivo de imagem.

* [GIF](/pt/image/gif/)
* [JPG](/pt/image/jpeg/)
* [PNG](/pt/image/png/)
* [SVG](/pt/page-description-language/svg/)

## Referências ##

* [EPUB - Por Wikipedia](https://en.wikipedia.org/wiki/EPUB)

