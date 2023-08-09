{
  "date" : "2021-09-08",
  "keywords" :[ "arquivo mgx", "formato de arquivo mgx", "o que é um arquivo mgx", "arquivo", "exemplo mgx", "extensão de arquivo mgx", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo MGX do Age of Empires 2 Expansion Replay e APIs que podem criar e abrir arquivos MGX.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## O que é um arquivo MGX?

Um arquivo com extensão .mgx é um arquivo gravado para o jogo Age of Empires II: The Conquerors que pode ser reproduzido dentro do programa Age of Empires II. Ele contém a gravação completa da campanha jogada pelo usuário. Ele pode ser carregado e reproduzido no programa Age of Empires II. Uma vez repetido, o jogo mostra todos os eventos e cenários que o usuário planejou para a campanha e jogou.

## Formato de arquivo MGX - Mais informações

O formato de arquivo interno do arquivo MGX foi elaborado e disponibilizado como informações parcialmente validadas em [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format). As especificações descrevem os detalhes nas seções a seguir.

### Definições de estrutura

Acredita-se que as definições de estrutura do formato de arquivo GPX sejam baseadas nas [declarações BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) que fornecem uma maneira de ler e gravar dados binários estruturados. Isso permite que o programador especifique o formato dos dados binários que são lidos e gravados por BinData.

### Mensagens MGX

A mensagem MGX é baseada em dois tipos de mensagens.

* GAMESTART - especifica os comandos de início do jogo e não é validado até o momento
* CHAT - descreve as mensagens de chat no jogo. Tanto os jogadores quanto o próprio jogo (Gaia) podem emitir mensagens no jogo.

### AÇÕES DE JOGO

Existem várias [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) que foram recuperadas e cujos detalhes estão disponíveis.

## Referências

* [Age of Empires 2: The Conquerors — Especificação de formato de arquivo de savegame](https://github.com/stefan-kolb/aoc-mgx-format)

