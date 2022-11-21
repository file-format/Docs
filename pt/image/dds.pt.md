{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo DDS - arquivo de imagem de superfície DirectDraw",
  "description":"Saiba mais sobre o formato de arquivo DDS e APIs que podem criar e abrir arquivos DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## O que é um arquivo DDS?

Um arquivo DDS é um arquivo de imagem raster que utiliza o formato de contêiner DirectDraw Surface (DDS). Ele armazena texturas descompactadas e compactadas (DXTn) e implementa diferentes tipos para armazenar diferentes tipos de dados. Ele também suporta vários tipos diferentes de dados, como texturas de camada única, texturas com mipmaps, mapas de cubo, mapas de volume e matrizes de textura. Isso permite que os arquivos DDS armazenem modelos de unidades de textura de videogame, além de fotos digitais e planos de fundo da área de trabalho do Windows. O formato de arquivo DDS foi desenvolvido pela Microsoft para ser usado com o DirectX SDK.

## Formato de arquivo DDS

Os arquivos DDS são salvos como arquivos binários e podem ser usados com o DirectX SDK. Ele utiliza o poder do DirectX para desenvolver aplicativos de renderização em tempo real, como jogos 3D.

### Layout do arquivo DDS

O [layout do arquivo DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) foi documentado pela Microsoft em detalhes. Um arquivo DDS binário contém as seguintes informações.

* Um DWORD (número mágico) contendo o valor do código de quatro caracteres 'DDS' (0x20534444).
* Uma descrição dos dados no arquivo.

O DDS_HEADER descreve os dados e o DDS_PIXELFORMAT descreve o formato do pixel. Ambos substituem as estruturas obsoletas DDSURFACEDESC2, DDSCAPS2 e DDPIXELFORMAT DirectDraw 7.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

O [guia de programação do formato de arquivo DDS](https://docs.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) elabora ainda mais os detalhes técnicos desse formato de arquivo.

## Referências

* [DDS - Por Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [Manual de referência técnica do formato de arquivo ZSoft PCX](http://qzx.com/pc-gpe/pcx.txt)

