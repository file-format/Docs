{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PCX - arquivo de imagem bitmap Paintbrush",
  "description":"Saiba mais sobre o formato de arquivo PCX e APIs que podem criar e abrir arquivos PCX.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## O que é um arquivo PCX?

Um arquivo PCX, arquivo Picture Exchange, é um formato de arquivo de imagem raster que foi usado como formato de arquivo nativo para o aplicativo PC Paintbrush. Foi desenvolvido pela ZSoft Corporation, EUA para plataformas DOS e Windows e foi adotado como o principal formato de arquivo de imagem antes da chegada de [BMP](/pt/image/bmp/), [JPEG](/pt/image/jpeg/) e [ PNG](/pt/image/png/) formatos de arquivo. Os arquivos PCX são menores em tamanho, pois são compactados usando a codificação RLE. Ele é usado no arquivo [DCX](/pt/image/dcx/) de várias páginas que é usado principalmente para criar arquivos de fax digital.

## Formato de arquivo PCX

Os arquivos PCX são salvos em disco no formato de arquivo binário. A estrutura de formato de arquivo interno segue a ordenação de bytes little endian e possui as três seções a seguir:

**`PCX Header`** - Um PCX Header tem 128 bytes. Ele contém um identificador, um número de versão, dimensões da imagem, 16 cores de paleta, número de planos de cores e profundidade de bits de cada plano e um valor para o método de compactação.

O cabeçalho PCX é mostrado abaixo com referência da Enciclopédia de formatos de arquivos gráficos (2ª ed.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Image Data`** - Os dados da imagem PCX seguem logo após o cabeçalho. Os dados da imagem podem ser compactados dependendo da configuração de campo no cabeçalho. O armazenamento de dados no arquivo PCX depende do número de planos de cores especificados. Os dados da imagem são organizados em linhas. No caso de vários planos, estes são armazenados por plano dentro de linha em arranjo sequencial de dados em vermelho, verde e azul. Este padrão é repetido para cada linha no plano.

## Referências

* [PCX - Pela Wikipedia](https://en.wikipedia.org/wiki/PCX)

