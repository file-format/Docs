{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo HDR - O que é um arquivo de imagem HDR?",
  "description":"Saiba mais sobre o formato de arquivo HDR e APIs que podem criar e abrir arquivos HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## O que é um arquivo HDR?

Um arquivo HDR é um formato de arquivo de imagem raster High Dynamic Range (HDR) para armazenar fotos de câmeras digitais. Ele permite que os editores de fotos aprimorem a cor e o brilho das imagens digitais com alcance dinâmico limitado. Essa modificação pode melhorar o brilho nos cantos, resultando em uma imagem quase natural. Os arquivos HDR geralmente são salvos como imagens raster de 32 bits. O Adobe Photoshop pode criar e abrir arquivos HDR.

Os arquivos HDR também são conhecidos como HDRI.

## Formato de arquivo HDR - Mais informações

O formato de arquivo HDR é baseado no formato de arquivo original Radiance Picture (.pic). Os dados de pixel de um arquivo HDR geralmente são armazenados descompactados, mas em alguns casos são compactados usando um sistema de codificação de comprimento de execução simples.

### Estrutura do arquivo HDR

Um arquivo de imagem HDR consiste nas três seções a seguir:

* **Cabeçalho:** Um arquivo HDR é identificado pelos primeiros bytes no arquivo de imagem, ou seja, "#?RADIANCE".
* **String de resolução:** o cabeçalho é seguido por uma única linha de resolução que consiste em 4 valores; um rótulo X e Y, cada um seguido por um valor numérico inteiro. A ordem de X e Y indica rotação. A combinação de X e Y com valores positivos e negativos cobre todas as orientações e rotações da imagem possíveis.
* **Dados de pixel:** os dados de pixel de um arquivo HDR são descompactados ou compactados usando uma codificação de comprimento de execução padrão.

## APIs HDR/HDRI de código aberto

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Biblioteca de cabeçalho único super rápido de plataforma cruzada [C++](/pt/programming/cpp/) para obter o tamanho e o formato da imagem sem carregar/decodificar.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Biblioteca Rust para obter tamanho e formato de imagem sem carregar/decodificar. Suporta [.avif](/pt/image/avif/), [.bmp](/pt/image/bmp/), [.cur](/pt/image/cur/), [.dds](/pt/image/dds/), [. gif](/pt/image/gif/), hdr (pic), [heic (heif)](/pt/image/heic/), [.icns](/pt/image/icns/), [.ico](/pt/image/ico/), [.jp2](/pt/image/jp2/), [jpeg (jpg)](/pt/image/jpeg/), [jpx](/pt/image/jpx/), ktx, [png](/pt/image/png/), [psd](/pt/image/psd/), qoi, tga, tiff (tif) e webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - implementação Java do HdrHistogram.

## Referências

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo)

