{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo HDR - Formato de arquivo de cabeçalho ESRI BIL",
  "description":"O que é um arquivo HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## O que é um arquivo .HDR?

Um arquivo HDR é um arquivo de cabeçalho GIS que contém informações de cabeçalho para um arquivo Banda intercalada por linha (.BIL). Ele descreve os dados da imagem e tem o mesmo nome do arquivo de imagem. Um arquivo HDR é composto por um conjunto de entradas, cada uma das quais descreve um atributo específico da imagem. O arquivo HDR descreve o layout e a formatação do arquivo BIL para tradução para coordenadas do mundo real em combinação com um arquivo de georreferenciamento separado.

## Formato de arquivo HDR

Os arquivos HDR são salvos no formato de arquivo de texto ASCII. Ele contém um conjunto de entradas onde cada entrada descreve um atributo específico da imagem. Cada arquivo HDR tem o seguinte formato:

```
<keyword> <value>
```

`<keyword> ` - Indica o atributo específico que está sendo definido
`<value> ` - É o valor para o qual o atributo está sendo definido

Não há limitação na ordem das entradas no cabeçalho. No entanto, cada entrada deve estar em uma linha separada da linha para cumprir o método de análise usado pelos leitores HDR.

## Resumo das palavras-chave usadas no arquivo HDR

|Palavra-chave |Valor aceitável |Padrão|
---|---|---|
|nrows |qualquer número inteiro > 0| nenhum
|ncols |qualquer número inteiro > 0| nenhum
|nbands |qualquer número inteiro > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|ordem de bytes| I = Intel;M = Motorola |igual à máquina host|
|disposição| bil, bip, bsq| conta|
|pular bytes| qualquer número inteiro ≥ 0| 0
|ulxmap |qualquer número real| 0|
|ulymap |qualquer número real |nrows - 1|
|xdim |qualquer número real| 1
|ydim |qualquer número real| 1
|bandrowbytes |qualquer número inteiro > 0| menor inteiro ≥ (ncols x nbits) / 8|
|totalrowbytes |qualquer número inteiro > 0| para bil: nbands x bandrowbytes;para bip: menor inteiro ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |qualquer número inteiro ≥ 0| 0|

## Referências

* [Formato de arquivo HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

