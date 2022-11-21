{
  "date" : "2021-12-09",
  "keywords" :[ "aro", "arquivo.aro", "formato de arquivo aro", "um tipo de arquivo", "arquivo", "tipo", "o que é um arquivo .aro" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARO File Format - SteelArrow Web Application File",
  "description" :"Saiba mais sobre o que é um arquivo ARO e APIs que podem criar e abrir arquivos ARO.",
  "linktitle" : "ARO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## O que é um arquivo ARO?

Um arquivo ARO é um arquivo de página da Web do lado do servidor que é gerado com o SteelArrow Web Application. Ele contém tags e scripts [HTML](/pt/web/html/) e SteelArrow. Eles são executados no servidor para gerar uma página de resposta completa antes de enviá-los ao navegador do usuário. Os arquivos ARO contêm quase 95% do conteúdo HTML, enquanto o restante consiste em código SteelArrow. Para que os arquivos ARO funcionem para você, o servidor SteelArrow Web Applications deve ser instalado e executado na máquina do servidor web.

## Formato de arquivo ARO

Os arquivos ARO são escritos em arquivo de linguagem de marcação HTML com código JavaScript incorporado e applets Java. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) são os blocos de construção básicos para o desenvolvimento de páginas da web. Embora eles não alterem a exibição da página, eles são usados para preencher a página com dados. Além disso, eles também podem ser usados para controlar a saída com instruções condicionais.

### Exemplo de Tag ARO

o<SAOUTPUT> A tag ARO permite que os desenvolvedores produzam valores de dados em qualquer lugar dentro de um script. Por exemplo, pode ser usado para obter a saída da tabela PARAM com<SAOUTPUT VALUE=PARAM[]> que pode ser exibido dentro do HTML<BODY> marcação.

## Referências

* [tags SteelArrow](http://www.steelarrow.com/docs/basics.aro)

