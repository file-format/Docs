{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "arquivo", "extensão", "formato", "o que é formato de arquivo mod", "música", "formato de arquivo mod", "mod vs MP3", "especificação de formato de arquivo mod"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aprenda sobre o formato de arquivo MOD e APIs que podem criar, converter e abrir arquivos MOD.",
  "title" :"MOD - Arquivo de Módulo de Música",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## O que é um arquivo MOD?
Um arquivo com extensão .mod é um arquivo de módulo de música criado usando o formato de módulo de música padrão, que é baseado no **formato de módulo Amiga** desenvolvido por Karsten Obarski e lançado com o software **Ultimate Soundtracker** para o Commodore Sistema Amiga. Semelhante a um arquivo [MIDI](/pt/audio/mid/), ele consiste em padrões de notas e amostras de som, representando diferentes instrumentos que são reproduzidos de acordo com as notas. Os arquivos MOD são particularmente usados em videogames como música de fundo e na subcultura de arte de computador **demoscene**.

## Formato de arquivo MOD

O MOD é um formato de arquivo de computador cuja função básica é representar música, e foi o primeiro formato de arquivo do módulo. Os arquivos MOD usam a extensão de arquivo .mod, exceto no **Amiga**, que lê o cabeçalho de um arquivo para determinar o tipo de arquivo, portanto, não depende de extensões de nome de arquivo. Um arquivo MOD consiste em um conjunto de vários instrumentos na forma de amostras, vários padrões especificando como e quando as amostras devem ser tocadas e uma lista de quais padrões tocar em que ordem.

### Especificações de formato de arquivo MOD

Um padrão de arquivo MOD é, na verdade, projetado em uma interface de usuário de sequenciador como uma tabela com uma coluna por canal, portanto, esta tabela tem quatro colunas (uma para cada canal de hardware Amiga. Cada coluna tem 64 linhas).

Uma célula na tabela pode fazer com que uma das seguintes ações ocorra no canal de sua coluna quando o tempo de sua linha for atingido:

- Inicie um instrumento tocando uma nova nota neste canal em um determinado volume, possivelmente com um efeito especial aplicado nele
- Altere o volume ou efeito especial aplicado à nota atual
- Mudança de fluxo padrão; pular para uma posição específica de música ou padrão ou fazer um loop dentro de um padrão
- Fazer nada; qualquer nota existente neste canal continuará a tocar

Um instrumento é uma única amostra juntamente com uma especificação opcional de qual parte da amostra pode ser repetida para manter uma nota sólida.

### Cronometragem
O intervalo de tempo mínimo foi de 0,02 segundos no arquivo MOD original, ou um intervalo de "vertical blanking" (VSync), porque o software original usava o tempo VSync do monitor rodando a 50 Hz (para PAL) ou 60 Hz (para NTSC) para cronometragem.

## Referências

* [MOD (formato de arquivo) - Por Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

