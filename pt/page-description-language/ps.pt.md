{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PS",
  "description":"Saiba mais sobre o formato de arquivo PS e APIs que podem criar e abrir arquivos PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo .PS? ##

PostScript (PS) é uma linguagem de descrição de página de uso geral usada no negócio de editoração eletrônica e eletrônica. O foco principal do PostScript (PS) é facilitar o design gráfico bidimensional. A maioria das linguagens requer um estágio de compilação distinto antes da execução do código, enquanto o formato Post Script (PS) suporta uma interpretação direta em tempo de execução. Sua versão inicial define as formas gráficas, diferentes aparências de texto e imagens modeladas em páginas impressas ou páginas exibidas, seguindo as regras do modelo de imagem da Adobe. Um programa de PS é capaz de intercomunicar uma descrição de documento entre um sistema de composição e impressão mantendo o dispositivo independente e de alto nível. Além disso, este programa também é capaz de controlar a aparência de texto e gráficos em uma tela.

A descrição da página PostScript está disponível para ser renderizada, exibida na impressora e em outro dispositivo de saída com a ajuda do interpretador PostScript do dispositivo. Como os comandos para imprimir caracteres, formas gráficas e imagens são executados pelo interpretador, para aquele dispositivo específico, a descrição PostScript de alto nível é convertida no formato de dados raster de baixo nível. Geralmente, diferentes aplicativos como ilustradores, sistemas de composição de documentos e desenho assistido por computador (CAD) são automatizados para gerar descrições de página PostScript. Geralmente os programadores precisam escrever programas PostScript no momento da criação de novos aplicativos. No entanto, um programador pode aproveitar os recursos da linguagem PostScript que não são acessíveis em nenhum aplicativo escrevendo um programa PS para essa situação especial.

## Breve história ##

O conceito da linguagem PostScript foi introduzido pela primeira vez por John Warnock. Em 1966 ele estava trabalhando em um projeto do porto de Nova York. Ele estava tentando desenvolver um interpretador para um grande gráfico tridimensional para o banco de dados daquele projeto. Para processar esses gráficos, John Warnock concebeu a linguagem Design System. Enquanto isso, a Xerox PARC procurava um meio padrão de definir imagens de página para sua primeira impressora a laser. Embora Bob Sproull e William Newman em 1975-76 tenham desenvolvido o formato Press (formato de dados) para acionar impressoras a laser, ainda era necessária uma linguagem para maior flexibilidade. Em 1978, Warnock juntou-se a Martin Newell na Xerox PARC e reescreveu a linguagem interpretativa, JaM, que mais tarde foi ampliada e estendida para a linguagem Interpress. Warnock fundou a Adobe Systems em dezembro de 1982 com Chuck Geschke, Doug Brotz, Ed Taft e Bill Paxton. Eles começaram a trabalhar em uma linguagem mais simples chamada PostScript semelhante ao Interpress, que foi lançada comercialmente em 1984. Steve Jobs da Apple os visitou e os aconselhou a adaptar o PostScript para acionar impressoras a laser.

Em março de 1985, a primeira impressora com um interpretador PostScript embutido foi a LaserWriter da Apple, que revolucionou a editoração eletrônica (DTP). A solidez técnica e ampla disponibilidade fizeram do PostScript, uma linguagem de escolha para editoração eletrônica e eletrônica. Durante 1990, um intérprete para a linguagem PostScript era uma parte essencial das impressoras a laser.

## Principais características ##

Os recursos da linguagem PostScript para lidar com gráficos interativos e descrição de página possuem os seguintes recursos:

**Formas:** de natureza arbitrária, podem incluir linhas retas, curvas, quadrados e curvas cúbicas que podem ser autotransversais e desconectadas (em seções e furos).

**Operadores de pintura:** permitem o contorno da forma de qualquer espessura, cor, preenchimento ou permitem que a forma seja desenhada como um recorte para permitir o recorte de qualquer outro gráfico.

**Cores:** têm a diversidade como escala de cinza, RGB, CMYK e CIE. Tipos especiais de cores são modelados como recursos diferentes: cores exatas, mapeamento de cores, até mesmo sombreamento e padrões repetidos.

**Texto:** totalmente integrado com gráficos. Além disso, o modelo de imagem adobe permite que os caracteres de texto sejam exibidos como formas gráficas que podem ser operadas por qualquer operador gráfico normal.

**Imagens amostradas**: extraídas de fontes originais (fotografias digitalizadas) ou podem ser produzidas sinteticamente. A linguagem PostScript oferece diversos meios para regenerar imagens em qualquer resolução e de acordo com diferentes modelos de cores em um dispositivo de saída.

Uma linguagem de programação de uso geral pode tirar vantagem dos recursos gráficos da linguagem PostScript incorporando Ps em sua estrutura. Os tipos de dados primitivos, como números, caracteres, arrays e strings; primitivas de controle, como loops, procedimentos e condicionais; e alguns recursos não convencionais, como dicionários, são especificados no idioma. Esses recursos facilitam aos programadores escrever comandos para invocar operações de nível superior. Essas operações de alto nível atendem às necessidades de aplicações complexas. Tal prática é mais compacta e eficiente do que usar um conjunto fixo de operações básicas.

Programas escritos em PostScript podem ser produzidos, comunicados e interpretados na forma de texto fonte ASCII. Todo o idioma pode ser definido na forma de caracteres imprimíveis e espaço em branco. Essa representação permite que os programadores criem, manipulem e compreendam a linguagem facilmente. Além disso, o armazenamento e a transmissão de arquivos entre diversos computadores e sistemas operacionais mantiveram-se convenientes por meio da independência da máquina.

Formas codificadas em binário da linguagem são possíveis, quando o programa é garantido para um caminho de comunicação totalmente transparente para o interpretador PostScript. A estrita coesão da representação ASCII de programas PS é recomendada pela Adobe para troca de documentos ou armazenamento de arquivos.

## Versões ##

PS(.ps) é a extensão de arquivo para um documento PostScript. Os Arquivos Nacionais do Reino Unido categorizam cinco versões cronológicas do arquivo PostScript, definidas na versão DSC: versões 1.0, 2.0, 2.1, 3.0, 3.1. Cada versão define importantes comentários de estruturação. Arquivo PostScript Encapsulado (EPS) é um subtipo especial de arquivo PostScript que emprega a linguagem para especificar um gráfico retangular. O PostScript Language Reference Manual descreve um EPS como "Um arquivo PostScript encapsulado (EPS) é um programa PostScript que descreve no máximo uma única página em um formulário que pode ser importado por outros aplicativos para incorporar em um documento que o contém". Um arquivo de documento PostScript pode encapsular um arquivo EPS nele. Um uso adicional de PostScript é mencionado como Display PostScript (DPS). O DPS gera gráficos na tela por meio de um mecanismo gráfico que faz uso de linguagem e modelo de imagem PostScript.

## Referências ##

* [Família de formatos PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

