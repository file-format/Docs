{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo FZPZ - Fritzing Part File",
  "description":"Saiba mais sobre o que é um arquivo FZPZ e APIs que podem criar e abrir arquivos FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## O que é um arquivo FZPZ?

Um arquivo FZPZ é um componente/peça usado em um projeto de circuito eletrônico criado com o aplicativo de prototipagem e projeto de circuito **Fritzing**. É um arquivo compactado que contém um arquivo [FZP](/pt/cad/fzp/) e quatro imagens [SVG](/pt/image/svg/) descrevendo a parte geral do Fritzing. A vantagem de usar esses arquivos é que os usuários podem compartilhar seus arquivos FZPZ com cada um do ponto de vista da reutilização. O compartilhamento de peças FZPZ ajuda na integração de peças de circuito para criar designs de PCB maiores de maneira rápida.

## Formato de arquivo FZPZ - Mais informações

Os arquivos FZPZ são salvos em disco como arquivos compactados [ZIP](/pt/compression/zip/). Você pode renomear a extensão de .fzpz para .zip e usar qualquer utilitário de descompactação padrão, como WinZIP, para extrair os arquivos do arquivo.

### Informações da estrutura do arquivo FZPZ

Como mencionado, um arquivo FZPZ é um arquivo que contém vários arquivos para representação de uma peça usada na placa de circuito impresso. O FZPZ contém os seguintes arquivos:

* `Quatro arquivos SVG` - que representam imagens de placa de ensaio, esquema, PCB e ícone da peça
* `Arquivo FZP` - Um arquivo XML que contém informações sobre as propriedades, conectores e barramentos da peça

Os arquivos geralmente são nomeados como segue.

* parte.arquivo.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Referências ##

* [Novas peças com extensão fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

