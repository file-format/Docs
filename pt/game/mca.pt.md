{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Saiba mais sobre o formato de arquivo MCA e as APIs que podem criar e abrir arquivos MCA.",
  "title": "MCA - Formato de arquivo da região da bigorna do Minecraft",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-pta"
}
},
  "lastmod": "2022-12-13"
}

## O que é um arquivo .MCA?

O formato de arquivo da região Minecraft Anvil é um formato de armazenamento de dados usado para armazenar pedaços de terreno de um mundo Minecraft no popular videogame **Minecraft**. O mundo do Minecraft consiste em regiões, onde cada região é dividida em pedaços. O formato de arquivo MCA permite o armazenamento eficiente de grandes quantidades de dados do jogo, como a localização de blocos e entidades em uma determinada parte do mundo do jogo. Os arquivos MCA precisam ser combinados com outros arquivos MCA para gerar um mundo inteiro.

Além de armazenar dados do jogo, o formato de arquivo da região Anvil também inclui suporte para vários outros tipos de dados, como dados e metadados do jogador. Isto permite o armazenamento eficiente de todas as informações necessárias para recriar completamente uma parte específica do mundo do jogo, incluindo a localização de blocos, entidades e outros objetos do jogo.

## Formato de arquivo MCA – Mais informações

O formato de arquivo da região Anvil é uma variante do formato NBT (Named Binary Tag), que é uma estrutura hierárquica semelhante a uma árvore para armazenar dados em um arquivo binário. Isto permite o armazenamento eficiente de estruturas de dados complexas em um formato compacto e de fácil leitura.

### Pedaços no arquivo MCA

No Minecraft, um pedaço é uma área de bloco de 16x16x16 do mundo do jogo que é carregada na memória e renderizada na tela do jogador. O formato de arquivo da região Anvil armazena todos os dados de um determinado pedaço em um único arquivo, que pode ser carregado rapidamente na memória quando necessário. Isso permite armazenamento eficiente e acesso rápido aos dados do jogo, o que é importante para garantir uma experiência de jogo tranquila e contínua.

### Tamanho pequeno do arquivo MCA

Um dos principais recursos do formato de arquivo da região Anvil é o uso de compactação. Isto permite o armazenamento eficiente de grandes quantidades de dados, sem sacrificar a qualidade dos dados ou a velocidade com que podem ser acessados. Isso é feito usando uma variedade de técnicas, como compactação gzip e compactação de dados em pedaços.

O formato de arquivo compactado dos arquivos MCA o torna uma parte importante do sistema de armazenamento e gerenciamento de dados do jogo. Seu uso eficiente de compactação e suporte para vários tipos de dados permite armazenamento eficiente e acesso rápido aos dados do jogo, garantindo uma experiência de jogo tranquila e contínua para os jogadores.

## Estrutura de formato de arquivo MCA

A estrutura interna do formato de arquivo dos arquivos MCA consiste em:
 * Cabeçalho e um
 * Carga útil

### Cabeçalho MCA

O cabeçalho de um arquivo de região MCA começa com um cabeçalho de 8 KB que é dividido em duas tabelas de 4 KB. A primeira tabela contém os deslocamentos dos pedaços no próprio arquivo de região, enquanto a segunda tabela fornece carimbos de data/hora para as últimas atualizações desses pedaços.

### Carga útil do MCA

A carga útil do MCA consiste em blocos, onde cada bloco de dados começa com um campo (big-endian) de comprimento de quatro bytes. Este campo indica o comprimento exato dos dados restantes do bloco em bytes. Os dados do último pedaço são preenchidos para ter um comprimento múltiplo de 4096B. Arquivos onde o último pedaço não é preenchido não são aceitos pelo Minecraft.

## Como abrir arquivos MCA

Você pode abrir e editar arquivos MCA usando o programa MCEdit, que é um editor gratuito e de código aberto para Minecraft. Você pode [download MCEdit](https://www.mcedit.net/) no site oficial e usá-lo para abrir e visualizar o conteúdo do seu arquivo de região Anvil.

Depois de instalar o MCEdit, você pode abrir o arquivo da região Anvil seguindo estas etapas:

 1. Inicie o MCEdit e clique no botão Abrir” no canto superior esquerdo da janela.

 1. Na caixa de diálogo Open World, navegue até o local do arquivo da região Anvil e selecione-o.

 1. Clique no botão Abrir” para abrir o arquivo no MCEdit.

 1. MCEdit irá carregar o arquivo e exibir seu conteúdo na janela principal. Você pode então usar as ferramentas e recursos do MCEdit para visualizar, editar e extrair dados do arquivo da região Anvil.

## Referências

* [Editor Mundial para Minecraft](https://www.mcedit.net/)

* [Sobre o Minecraft](https://www.minecraft.net/)

* [Formato de arquivo de região](https://minecraft.fandom.com/wiki/Region_file_format)


