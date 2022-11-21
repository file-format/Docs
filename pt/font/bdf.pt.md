{
  "date" : "2021-02-25",
  "keywords" :[ "arquivo bdf", "formato de arquivo bdf", "o que é um arquivo bdf", "arquivo", "exemplo bdf", "extensão de arquivo bdf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Formato de distribuição de bitmap de glifo",
  "description":"Saiba mais sobre o formato de arquivo BDF e APIs que podem criar e abrir arquivos BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## O que é um arquivo BDF?
Os arquivos BDF são de forma legível e geralmente distribuídos em uma codificação ASCII. O arquivo começa com informações globais relevantes para a fonte completa, seguidas pelas informações e bitmaps para os glifos individuais. Os dados nele são exibidos para a fonte para uma orientação de tamanho único. As métricas a serem usadas em mais de uma direção podem ser compostas em um único arquivo. No arquivo BDF, cada item está contido em uma linha de texto separada no arquivo. Os espaços são usados para separar os itens em uma linha.

## Formato de arquivo BDF
Os shorts BDF para Glyph Bitmap Distribution Format; propriedade da Adobe é um formato de arquivo para salvar fontes do tipo bitmap. O conteúdo assume a forma de um arquivo de texto destinado a ser legível por computador e por humanos. O BDF é particularmente usado em ambientes Unix X Window. Ele foi amplamente substituído pelo formato de fonte PCF, que deveria ser mais eficiente, e pelas fontes OpenType e TrueType.
### Estrutura do arquivo BDF
Um arquivo de fonte BDF consiste em três seções:

- uma seção global que se aplica a todos os glifos em uma fonte.
- uma seção com uma entrada separada para cada glifo.
- a instrução ENDFONT.

## Exemplo
Aqui está um exemplo de fonte contendo um glifo, para ASCII maiúsculo 'A'. Suas declarações globais começam com a linha "STARTFONT" e terminam com a linha "CHARS"
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Referências
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) Specification](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

