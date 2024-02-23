{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Aprenda sobre o formato de arquivo MCR e APIs que podem criar e abrir arquivos MCR.",
  "title": "MCR - formato de arquivo de região do Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-ptr"
}
},
  "lastmod": "2022-12-14"
}

## O que é um arquivo .MCR?

O formato de arquivo Minecraft MCR é um formato de dados usado pelo Minecraft para armazenar pedaços de terreno de um mundo Minecraft. É baseado no formato NBT (Named Binary Tag), que foi desenvolvido pelos desenvolvedores do popular mecanismo de jogo de código aberto Minecraft Forge. O tipo de arquivo MCR foi introduzido no início e posteriormente substituído pelo [MCA file format](/game/mca/).

## Formato de arquivo MCR

O formato de arquivo MCR é estruturado como uma série de tags binárias nomeadas, cada uma contendo um tipo específico de dados. A tag de nível superior é a tag Level”, que contém todos os dados de um único nível de jogo. Dentro da tag Level, existem diversas outras tags nomeadas que armazenam diferentes tipos de dados, como a tag Data, que armazena informações sobre o mundo do jogo, e as tags Entities e TileEntities, que armazenam dados sobre o mundo do jogo. objetos de jogo e entidades de peças no mundo, respectivamente.

## O que há dentro do formato de arquivo MCR?

No formato de arquivo Minecraft MCR, uma região é uma área de blocos de 32x32 do mundo do jogo. O formato MCR divide o mundo do jogo em regiões para gerenciar os dados de forma mais eficiente e permitir carregamento e salvamento mais rápido dos níveis do jogo. Cada região é armazenada em um arquivo separado e o formato de arquivo MCR usa um sistema de coordenadas para identificar a posição de cada região no mundo do jogo. As coordenadas de uma região são determinadas pelas coordenadas do bloco no canto inferior esquerdo da região. Por exemplo, uma região com coordenadas (-1,0) estaria localizada uma região à esquerda e zero regiões abaixo da origem do mundo do jogo.

## Especificações de formato de arquivo MCR

As especificações do formato de arquivo MCR estão disponíveis publicamente. As especificações do formato NBT, no qual o formato MCR se baseia, estão disponíveis no site do Minecraft Forge. Além disso, o [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) também possui informações detalhadas sobre o formato de arquivo MCR, incluindo sua estrutura e os vários tipos de dados que ele suporta.

### Dados compactados em arquivos MCR

O formato de arquivo Minecraft MCR oferece suporte à compactação. O formato de arquivo MCR é baseado no [NBT format](https://minecraft.fandom.com/wiki/NBT_format) que permite que os dados sejam armazenados em um formato compactado. Isso ajuda a reduzir o tamanho dos arquivos MCR e torná-los mais eficientes para transferência e armazenamento. Este é um recurso importante do formato de arquivo MCR, pois permite que os jogadores compartilhem grandes dados de terreno do Minecraft World com outras pessoas.

## Referências

* [Editor Mundial para Minecraft](https://www.mcedit.net/)

* [Sobre o Minecraft](https://www.minecraft.net/)

* [Formato de arquivo de região](https://minecraft.fandom.com/wiki/Region_file_format)

* [Formato NBT](https://minecraft.fandom.com/wiki/NBT_format)


