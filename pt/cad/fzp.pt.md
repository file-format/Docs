{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo FZP e APIs que podem criar e abrir arquivos FZP.",
  "title" :"Formato de arquivo FZP - Fritzing XML Part Description File",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## O que é um arquivo FZP?

Um arquivo FZP é um arquivo XML criado por [Fritzing](https://fritzing.org/) aplicativo de prototipagem e design de circuito eletrônico. Ele contém informações sobre as propriedades, conectores e barramentos da peça no formato de arquivo [XML](/pt/web/xml/). Os arquivos FPZ não podem ser usados independentemente no Fritzing. Em vez disso, eles são importados como parte do arquivo FZPZ.

## Formato de arquivo FZP - Mais informações

Os arquivos FZP são arquivos XML que contêm informações sobre as propriedades, conectores e barramentos da peça. Além destes, os arquivos FZP também contêm informações sobre o título, descrição, autor e data de publicação do arquivo FZP. Quando um arquivo de peça Fritzing é exportado, o aplicativo Fritzing cria um arquivo compactado [FZPZ](/pt/compression/fzpz/) que contém um arquivo FZP e quatro arquivos [SVG](/pt/page-description-language/svg/).

As [especificações de formato de arquivo FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) estão disponíveis no Github por Fritzing.

## Exemplo de estrutura de arquivo FZP

Um arquivo FZP típico tem a seguinte estrutura XML.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Referências

* [Especificações de formato de arquivo FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Novas peças com extensão fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

