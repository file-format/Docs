{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "arquivo", "extensão", "formato", "formato de vídeo", "O que é um arquivo SWF", "formato de arquivo swf", "reprodutor de arquivo swf","como abrir arquivo swf"] ,
  "title" :"Arquivo SWF - Formato de arquivo de filme Shockwave Flash",
  "description":"Saiba mais sobre o que é um arquivo SWF e APIs que podem criar e mostrar como abrir o arquivo SWF.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo SWF?

Um arquivo SWF é um arquivo de animação criado com o Adobe Flash. Ele pode conter diferentes tipos de elementos, como texto, imagens vetoriais, imagens raster, scripts de ação, objetos como círculos, linhas, quadrados e retângulos para criar a animação. Os arquivos SWF organizam esses itens multimídia em quadros que podem ser reproduzidos em diferentes quadros por segundo (fps). SWF significa Short Web File, mas também é conhecido como Shockwave Format.

Os aplicativos que podiam *abrir arquivos SWF** incluíam o Adobe Flash Player (agora descontinuado) e o Eltima Elmedia Player.

## Formato de arquivo SWF - Mais informações

Os arquivos SWF foram usados para serem armazenados como arquivos binários em disco. O formato de arquivo SWF foi usado para desenvolver animações e jogos que poderiam ser incorporados em sites e reproduzidos de forma independente também. Ele também suportava vídeos e sons que davam aos desenvolvedores muitas opções para criar aplicativos multimídia interativos. Os arquivos SWF podem ser reproduzidos em navegadores da Web que tenham o Adobe Shockwave instalado. O Adobe Flash foi descontinuado em dezembro de 2020 devido a falhas e problemas de segurança.

## Breve História do Formato de Arquivo SWF

O formato de arquivo SWF foi originalmente projetado pela FutureWave Software, para exibir animações com a intenção de rodar em um software player em qualquer sistema com conexões de rede mais lentas, mantendo o tamanho do arquivo pequeno. Em dezembro de 1996, a Macromedia era proprietária do FutureWave e converteu para Macromedia Flash 1.0.

Em 2005, a Macromedia foi adquirida pela Adobe, que anunciou o SWF como parte de seu projeto de código aberto em 2008. Durante o mesmo ano, a Adobe lançou código para mecanismos da Web populares do mundo para permitir o rastreamento e a indexação de arquivos SWF. No entanto, como os arquivos SWF parecem se tornar um formato padrão para publicação de conteúdo Flash na Internet, o SWF foi revisado para significar Small Web Format.

## Estrutura do arquivo SWF

Path é o elemento gráfico básico no SWF, que é uma sequência de segmentos de elementos básicos, variando de linhas simples a curvas de Bezier. Esses elementos simples também ajudam a criar outras primitivas adicionais, como cubos, elipses e até mesmo textos. As primitivas gráficas em SWF possuem similaridade com os elementos gráficos de outros formatos como SVG e MPEG-4 BIFS.

Listas de exibição e reutilização/renomeação de elementos já definidos também são permitidos pelo formato. O formato de fluxo binário do SWF pode ser comparado aos átomos do QuickTime, que são semelhantes em termos de tag, tamanho e carga útil. O formato de fluxo binário permite que os players mais antigos ignorem conteúdos não suportados. Embora as versões originais do SWF fossem limitadas a oferecer gráficos e imagens vetoriais, as novas versões também permitem conteúdo de áudio e vídeo.

Uma nova API 3D de baixo nível do Flash Player chamada “Stage3D” foi introduzida na versão 11. Essa API foi concebida para ser a contrapartida do OpenGL ou Direct3D. Stage3D define cores em uma linguagem de baixo nível chamada Adobe Graphics Assembly Language (AGAL). A seguir estão alguns tipos de dados básicos do formato de arquivo SWF.

### Coordenadas

As coordenadas XY no formato de arquivo SWF são armazenadas como números inteiros e medidas em uma unidade chamada twip. Um twip consiste em 1/20 de um pixel lógico. O pixel lógico e o pixel da tela são os mesmos quando o arquivo é reproduzido sem escala em 100%.

### Tipos inteiros e ordem de bytes

Os tipos inteiros assinados e não assinados de 8, 16, 32 e 64 bits são permitidos no formato de arquivo SWF. A ordem de bytes Little-endian é usada para armazenar valores inteiros. Embora dentro de bytes, a ordem de bits é armazenada em big-endian. Todos os valores inteiros devem ser alinhados por byte. Os inteiros com sinal são representados usando padrões tradicionais de bits de complemento de 2.

### Números de ponto fixo

Dois tipos de números de ponto fixo são suportados pelo formato de arquivo SWF, ou seja, 32 e 16 bits.

### Números de ponto flutuante

SWF 8 e versões posteriores usam três tipos de números de ponto flutuante (FLOAT, FLOAT 16, DOUBLE) que são compatíveis com o padrão IEEE 754 de tipos de ponto flutuante.

### Inteiros codificados

Um tipo de inteiro codificado é suportado pelo SWF 9 e posterior com número variável de bytes.

## Referências

* [formato de arquivo SWF](https://en.wikipedia.org/wiki/Swf)

