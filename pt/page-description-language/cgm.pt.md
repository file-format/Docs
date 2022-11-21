{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Metarquivo de Gráficos de Computador", "Arquivo", "Extensão", "Formato de Arquivo", "Gráficos Vetoriais", "Descritor de Metaarquivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo CGM",
  "description":"Saiba mais sobre o formato de arquivo CGM e APIs que podem criar e abrir arquivos CGM.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo CGM? ##

O Computer Graphics Metafile (CGM) é um formato de metarquivo de padrão internacional gratuito e independente de plataforma para armazenar e trocar gráficos vetoriais (2D), gráficos raster e texto. O CGM usa uma abordagem orientada a objetos e muitas provisões de funções para produção de imagens. O CGM usa essas características orientadas a objetos para remodelar elementos gráficos para renderizar uma imagem. Um metarquivo contém informações necessárias que definem outros arquivos. No CGM, um arquivo fonte baseado em texto contém todos os elementos gráficos que podem ser compilados posteriormente em um arquivo binário. Basicamente, o CGM é uma forma de facilitar o intercâmbio de dados gráficos 2D, independente de qualquer plataforma ou dispositivo em particular.

O formato CGM fornece diferentes elementos para executar funções e significar objetos para ajustar primitivas geométricas e informações gráficas. Embora o CGM tenha sido substituído por outros formatos para exibir artes gráficas em páginas da Web, pois não é bem suportado por páginas da Web, ainda é muito popular entre aplicações industriais, aeronáuticas e outras técnicas. Embora o World Wide Web Consortium tenha desenvolvido o WebCGM, uma abordagem alternativa para o uso do CGM na Web. A implementação principal do CGM foi uma ilustração da sequência de operações básicas do Graphical Kernel System (GKS). Não foi muito adotado em designs profissionais, mas foi amplamente suplantado por outros formatos, como DXF e SVG.

## História ##

O CGM tornou-se um padrão internacional em 1987 (ISO 8632-1987) e também foi adotado como padrão nacional no Reino Unido pelo BSI e nos EUA pelo ANSI. Após uma série de emendas em 1991, uma norma revisada da CGM foi lançada em 1992 (ISO 8632:1992). Em 2001, o World Wide Web Consortium desenvolveu o WebCGM com capacidade aprimorada para ser usado com as páginas da web. Em 2007, a segunda versão do WebCGM foi lançada e a terceira versão foi lançada em 2010 com recursos aprimorados.

## Formato de arquivo CGM ##

Os metarquivos gráficos de computador são basicamente bancos de dados para informações gráficas e fornecem os meios para a captura, armazenamento e transmissão de dados gráficos. Conseqüentemente, deve haver um componente gráfico do sistema para criar o banco de dados simultaneamente com a execução de uma aplicação em formato de metarquivo. Na maioria dos casos, este componente é o gerador de Metafile. Paralelamente, há a necessidade de outro componente que possa buscar, interpretar e renderizar dados gráficos em um metarquivo. Essa necessidade é atendida pela presença de um interpretador de metarquivo. A figura a seguir representa o ambiente de trabalho do metarquivo gráfico.

A relação do CGM com outros componentes de um sistema gráfico típico é ilustrada na figura acima. Também é evidente na figura que a funcionalidade do metarquivo não depende da saída final do dispositivo.

Geralmente, há duas categorias de metarquivo: **captura de seção** e **captura de imagem**. A principal funcionalidade do metarquivo de captura de imagem é a captura de várias definições de imagem independentes de dispositivo. Enquanto os meta-arquivos de captura de sessão usam a interface do sistema para capturar o diálogo de saída em um sistema gráfico. O CGM pertence à categoria de meta-arquivos de captura de imagem estática. O CGM fornece um arranjo bem organizado de componentes com uma estrutura de dois níveis.

1. Descritor de metarquivo
1. Um conjunto de imagens logicamente independentes

Cada imagem é uma coleção de descritores de imagem e um corpo de imagem incluindo uma definição de imagem. descritor de metarquivo define informações descritivas que se aplicam igualmente a todas as imagens desse metarquivo. Essas informações ajudam o intérprete a analisar corretamente um metarquivo e reconhecer os recursos necessários para a renderização correta de uma imagem. Embora o descritor de imagem também inclua as informações descritivas, ele só pode reconhecer a imagem na qual o descritor reside. Nesse formato de arquivo, cada definição de imagem é independente e logicamente soberana. Eles são independentes de todas as outras definições de imagem em um arquivo. Logo após a interpretação do meta-descritor, as imagens podem ser acessadas e interpretadas aleatoriamente. A mudança no estado das fotos anteriores não afeta seus sucessores. Esta independência de imagem é outra característica proeminente do CGM.CGM consiste em um espaço de coordenadas que são coordenadas cartesianas 2D chamadas de coordenadas do dispositivo virtual e podem ser representadas através de número ou precisão representando o alcance e granularidade. O CGM especifica tanto a seleção direta de cores quanto a seleção baseada em índice. No primeiro, o especificador de cores consiste em um triplo RGB, enquanto, posteriormente, o especificador de cores indica um índice em uma tabela de cores.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
