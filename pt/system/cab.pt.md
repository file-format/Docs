{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "extensão", "arquivo", "formato", "sistema", "Arquivo de gabinete do Windows", "Microsoft", "Instalador", "Configuração", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Arquivo de Gabinete do Windows",
  "description":"Saiba mais sobre o formato de arquivo CAB e as APIs que podem criar e abrir arquivos CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo CAB? ##

Um arquivo com extensão .cab pertence a um arquivo de gabinete do Windows que pertence à categoria de arquivos do sistema. É um arquivo salvo no formato de arquivo morto nas versões do Microsoft Windows que suportam algoritmos de dados compactados, como [LZX](/pt/compression/lzx/), Quantum e [ZIP](/pt/compression/zip/ ). O arquivo é de uso vital quando um usuário ou desenvolvedor deseja conter e compartilhar dados e arquivos de instalação de software. Os recursos de compactação de dados sem perdas e a certificação digital incluída nesses arquivos tornam este arquivo perfeito para armazenar e compartilhar esses arquivos. Ele suporta diferentes instaladores da Microsoft, como Device Installer, SetUp API e AdvPak.

## Breve história ##

O arquivo CAB é um tipo de arquivo de compactação de dados desenvolvido pela Microsoft. Foi inicialmente chamado de "Diamond", mas depois ficou popularmente conhecido como arquivo CAB, abreviação da palavra "Cabinet"

## Especificação Técnica ##

Um arquivo CAB geralmente pode conter no máximo 65.535 pastas, que podem, por sua vez, conter no máximo 65.536 arquivos cada. O mecanismo de armazenamento de arquivos CAB é eficiente em termos de tempo e espaço, pois salva cada pasta como um bloco compactado em vez de compactar e armazenar cada arquivo separadamente. Pastas vazias não podem ser armazenadas em pastas de arquivo CAB. O arquivo CAB foi desenvolvido pela Microsoft e é usado em vários instaladores, como o InstallShield com um formato ligeiramente diferente. Os arquivos CAB são comumente conectados a programas de extração automática. Os arquivos Microsoft CAB são facilmente reconhecíveis devido ao seu marcador exclusivo que ajuda a identificar o formato. O marcador exclusivo para todos os arquivos Microsoft CAB é um prefixo de quatro palavras, MSCF. Vendo esse código, um usuário pode distinguir facilmente um arquivo Microsoft CAB de outros arquivos e usá-lo adequadamente em compressores ou versões. Os arquivos podem ser compactados com mais dados de instalações de software, ou os dados atuais podem ser descompactados usando o software correto.


## Exemplo de CAB ##

O exemplo a seguir ilustra a relação entre arquivos e pastas em uma estrutura de arquivos CAB:

{{< figure src="../cab.png" alt="Formato de arquivo CAB" >}}

## Referência ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
