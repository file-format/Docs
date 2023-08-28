{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "arquivo", "extensão", "formato de arquivo", "Excel", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo OTS e APIs que podem criar e abrir arquivos OTS.",
  "title" :"OTS - Formato de arquivo de modelo de planilha OpenDocument",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## O que é um arquivo OTS?

Um arquivo com extensão .ots é um arquivo de modelo de planilha OpenDocument que é criado com o software de aplicativo Calc incluído no Apache OpenOffice. O software aplicativo Calc é semelhante ao Excel disponível no Microsoft Office. O formato de arquivo OTS é usado para criar modelos que contêm configurações predefinidas relacionadas a estilos, fonte, dados, layout de planilha e formatação. Os arquivos OTF têm `mime-type application/vnd.oasis.opendocument.spreadsheet-template`. Esses arquivos de modelo podem ser usados como ponto de partida para gerar e salvar arquivos de dados reais que são salvos em [formato de arquivo ODS](/pt/spreadsheet/ods/). Os arquivos OTS podem ser usados com aplicativos como OpenOffice e LibreOffice.

## Formato de arquivo OTS

Os arquivos OTS são salvos no formato de arquivo baseado em XML OpenDocument do OASIS que compreende uma coleção de vários subdocumentos com um pacote como um arquivo [ZIP](/pt/compression/zip/). Cada arquivo zip armazena parte do documento completo e cada subdocumento armazena um aspecto particular do documento. Por exemplo, um subdocumento contém as informações de estilo e outro subdocumento contém o conteúdo do documento. Um documento ODF típico tem os seguintes componentes:

### Conteúdo OTS.xml

O arquivo content.xml contém o conteúdo real do documento. No entanto, isso não inclui dados binários, como imagens.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml do formato de arquivo OTS

O arquivo styles.xml contém informações de estilo e é muito usado para formatação e layout. Os tipos de estilos incluem:

* Estilos de parágrafo
* Estilos de página
* Estilos de personagens
* Estilos de moldura
* Listar estilos

### Meta.xml

O arquivo meta.xml contém informações sobre os metadados do arquivo, como autor, data da última modificação etc.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Configurações.xml

O arquivo `settings.xml` inclui configurações de nível de documento, como fator de zoom e posição do cursor.

## Referências ##

* [Especificação OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Por Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

