{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "formato de arquivo", "o que é um arquivo pak", "arquivo", "exemplo de pacote", "Arquivo de pacote de videogame","extensão"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o arquivo .pak e APIs que podem criar e abrir arquivos PAK.",
  "title" :"Formato de arquivo PAK - Arquivo de pacote de videogame",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## O que é um arquivo PAK?

Um arquivo PAK é um arquivo de pacote criado por diferentes videogames para arquivar dados de jogos. Essencialmente, é um formato de arquivo de jogo. Isso pode incluir vários elementos do jogo, como gráficos, texturas, sons, objetos, além de outros dados do jogo. O arquivo é salvo principalmente como arquivo .zip e pode ser extraído com software de descompactação popular, como WinZip e WinRAR. Exemplos de videogames usando arquivos PAK incluem Quake, Hexen, Crysis e Half-Life.

## Formato de arquivo PAK - Mais informações

Na maioria dos casos, os arquivos PAK são salvos em [formato de arquivo ZIP](/pt/compression/zip/). Mas aplicativos diferentes podem usar formatos de arquivo diferentes para armazenar esses arquivos.


## Como abrir arquivos PAK?

Você pode abrir arquivos PAK com aplicativos como [PakExplorer](https://www.quaketerminus.com/tools.shtml) e [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- -----------------------**

## Formato de arquivo PAK - Arquivo de objeto Simutrans

Um arquivo com extensão .pak é um formato de arquivo de jogo de simulação de transporte [Simutrans](https://www.simutrans.com/en/). Ele contém objetos usados na simulação, como gráficos feitos pelo usuário e conteúdo de dados. Ele pode ter vários objetos diferentes, como veículos de jogo, prédios, terrenos, etc. Os arquivos PAK são gerados usando o MakeObject, um utilitário que compila arquivos .dat e imagens .png para criar esses objetos de simulação. Simutrans permite que os jogadores executem um sistema de transporte de sucesso construindo e gerenciando sistemas de transporte de passageiros, correio e mercadorias por terra

## Como criar arquivos PAK?

O Simutrans listou exemplos de exemplo para criar arquivos PAK no sistema operacional Windows e Linux.

### SO Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/SO

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Referências

* [Simutrans](https://en.wikipedia.org/wiki/Simutrans)