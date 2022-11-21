{
  "date" : "2021-10-20",
  "keywords" :[ "arquivo sfar", "formato de arquivo sfar", "o que é um arquivo sfar", "arquivo", "exemplo sfar", "Extensão de arquivo Mass Effect 3 DLC", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo SFAR do Mass Effect 3 e as APIs que podem criar e abrir arquivos SFAR.",
  "title" :"SFAR - Arquivo DLC Mass Effect 3",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## O que é um arquivo SFAR?

Um arquivo com extensão .sfar é um arquivo de dados do jogo usado pelo Mass Effect 3 para armazenar seu DLC (conteúdo para download) em um arquivo proprietário e compactado. Mass Effect 3 é um jogo criado pela Electronic Arts, uma importante empresa de desenvolvimento de jogos. O conteúdo do DLC armazenado em um arquivo SFAR é usado para estender o jogo com conteúdo e recursos adicionais.

## Formato de arquivo SFAR - Mais informações

Os arquivos SFAR são armazenados/salvos como arquivos compactados em formato de arquivo binário. Eles usam algoritmos de compactação LZX e LZMA para compactar o conteúdo. Os arquivos SFAR podem ser abertos usando o DLC Editor que acompanha o ME3 Explorer. Além do SFAR, o DLC Editor pode extrair outros arquivos do jogo, como [PCC](/pt/game/pcc/).

## Especificações de formato de arquivo SFAR

Um arquivo SFAR é dividido nas quatro partes principais a seguir.

### Cabeçalho SFAR

O cabeçalho SFF contém informações sobre os vários pedaços que compõem o arquivo.

### Tabela de arquivos SFAR

A Tabela de Arquivos SFAR contém uma lista de entradas de arquivo em que cada entrada tem 30 bytes.

### Tabela de tamanho de bloco

O Block-Size contém várias entradas, onde cada entrada tem 2 byes de comprimento. Este valor especifica o tamanho do bloco correspondente a uma entrada na tabela de arquivos.

### Blocos

Blocos de blocos em um arquivo SFAR contêm os dados dentro do arquivo SFAR.

## Referências

* [Formato de arquivo DLC SFAR - Pesquisa](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

