{
  "date" : "2020-01-10",
  "keywords" :[ "arquivo dib", "formato de arquivo dib", "o que é um arquivo dib", "arquivo", "exemplo dib", "extensão de arquivo dib","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Saiba mais sobre o formato de arquivo DIB e APIs que podem criar e abrir arquivos DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## O que é um arquivo DIB?

Um bitmap independente de dispositivo (DIB) é um arquivo de imagem raster que é semelhante em estrutura aos arquivos bitmap padrão ([BMP]()/image/bmp/)). Ele contém uma tabela de cores que descreve o mapeamento de cores RGB para os valores de pixel. Isso permite que o DIB represente a imagem em qualquer dispositivo. Ele pode ser aberto com quase todos os aplicativos que podem abrir um arquivo BMP padrão no Windows e no macOS. DIB são arquivos binários e têm um formato de arquivo complexo semelhante ao BMP. As imagens DIB são independentes dos recursos de saída dos dispositivos de renderização em termos de profundidade de cor e pixel por polegada.

## Especificações de formato de arquivo DIB ##
Um DIB contém as seguintes informações de cor e dimensão:

* O formato de cor do dispositivo no qual a imagem retangular foi criada.
* A resolução do dispositivo no qual a imagem retangular foi criada.
* A paleta do dispositivo no qual a imagem foi criada.
* Uma matriz de bits que mapeia trigêmeos vermelho, verde, azul ( RGB ) para pixels na imagem retangular.
* Um identificador de compactação de dados que indica o esquema de compactação de dados (se houver) usado para reduzir o tamanho da matriz de bits.

### Formato do bloco de dados DIB ###

DIB vem no contexto de bloco de memória em comparação com arquivos .DIB armazenados em disco. O bloco de memória é composto por uma estrutura que está de acordo com as especificações da API do Windows para DIBs. O DIB real consiste em:
* Um cabeçalho
* Paleta de cores
* Dados de pixel

Praticamente, trabalhar com dados de paleta, cabeçalho e imagem é feito como se fossem três blocos separados de memória. Um identificador para este bloco comum de memória é atribuído usando GlobalAlloc e é conhecido como HDIB, que é usado para extrair e trabalhar com o cabeçalho, tabela de cores e dados de pixel.

### Estruturas ###
As informações contidas em um DIB são representadas por diferentes estruturas. Esses incluem:

BITMAPInfo - Define as informações de dimensão e cor para um DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Consiste em um BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
seguido por duas ou mais estruturas RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bits de dados ###
|Bits|Descrição|
---|---|
|Formato de 1 bit (monocromático)|Os bitmaps monocromáticos consistem em duas cores (preto e branco). Devido a esse número limitado de cores, esses bitmaps ocupam menos espaço no disco. O bitBitCount retorna true ou false para representação de ambas as cores. A maioria dos aplicativos ignora a paleta completamente se bitBitCount==1.
|Formato de 4 bits (VGA ou 16 cores)|Cada byte de dados de imagem representa dois pixels e bitBitCount==4. Esses bits representam a cor do pixel em ordem decrescente.
|Formato de 8 bits (256 cores)|Este formato de 8 bits pode representar um máximo de 256 cores. Cada byte na matriz de dados de bitmap da imagem representa um único pixel. O valor desse byte é o número da entrada da paleta de cores a ser usada das 256 entradas representadas por bmciColors.
|Formato de 24 bits (TrueColor)|Esses bitmaps podem ter no máximo 2^24 cores (biBitCount == 24). Cada sequência de três bytes na matriz de dados de bitmap representa as intensidades relativas dos três matizes primários de um pixel. Os matizes são descritos como valores que variam de 0 a 255 e são armazenados nos três bytes na ordem Azul, Verde e Vermelho. Essa é uma distinção importante, porque a maioria das referências a cores no Windows usa a ordem oposta: vermelho/verde/azul, então pense em "BGR" ao trabalhar com imagens TrueColor em vez de "RGB". Uma paleta de cores pode ser especificada para acelerar o processo de desenho para Windows, nesse caso biClrUsed não será 0. Mas, como você pode ver, não é necessário, pois os próprios dados de pixel contêm as informações de cor.
|Formato de 32 bits|Imagens de 32 bits têm no máximo 2^24 cores (biBitCount == 24).

## Referências ##
* [Bitmaps independentes de dispositivo - pela Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

