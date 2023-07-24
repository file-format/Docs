{
  "date" : "2019-11-25",
  "keywords" :[ "arquivo jpm", "formato de arquivo jpm", "o que é um arquivo jpm", "arquivo", "exemplo jpm", "extensão de arquivo jpm","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - Formato de arquivo composto JPEG 2000",
  "description":"Saiba mais sobre o formato de arquivo JPM e APIs que podem criar e abrir arquivos JPM.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## O que é um arquivo JPM?

JPM refere-se ao sistema de codificação de imagem JPEG 2000 Parte 6, que é usado para geração de imagens de documentos. Ele é baseado no Mixed Raster Content Standard (ISO/IEC 16485) e contém imagens estáticas em camadas que usam JPEG 2000 e outras codificações. Além de suas próprias especificações, o formato de arquivo JPM herda recursos de seu pai, ou seja, o formato de arquivo [jp2](/pt/image/jp2/).

## Formato de arquivo JPM

O formato de arquivo JPM é definido por [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) -- a imagem JPEG 2000 sistema de codificação -- Parte 6: Formato de arquivo de imagem composto. Uma imagem composta pode conter imagens digitalizadas, imagens sintéticas ou ambas, exigindo uma combinação de métodos de compactação de tom contínuo e de dois níveis. O formato de arquivo JPM define um modelo de composição que descreve o método de combinação de várias imagens para gerar uma imagem composta usando o modelo de imagem MRC (Mixed Raster Content) de várias camadas, definido em ITU-T T.44 | ISO/IEC 16485.

### Especificações JPM
O padrão de formato de arquivo JPM o especifica como um contêiner binário para representar uma imagem composta pela qual várias imagens podem ser combinadas em uma única imagem. Ele define o mecanismo para agrupar várias imagens em uma hierarquia de objetos de layout, páginas e coleções de páginas para armazenar JPEG 2000 e outros formatos de dados de imagem compactados. O formato inclui o mecanismo de incorporação de metadados (muitas vezes referido como metadados estruturais em projetos de bibliotecas digitais).

## Referências

* [ITU-T Rec. T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

