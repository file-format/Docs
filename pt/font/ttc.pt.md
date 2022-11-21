{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - Formato de arquivo de coleção TrueType",
  "description":"Um arquivo TrueType Collection (TTC) combina várias fontes em um único arquivo. A Apple e a Microsoft usaram TTF nos sistemas operacionais Mac e Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## O que é um arquivo TTC?
O TTC é abreviado como TrueType Collection é uma extensão do formato True Type. Um arquivo TTC pode combinar vários arquivos de fonte nele. Esses arquivos são úteis para combinar várias fontes que compartilham muitos glifos em comum. Antes do Windows 2000, os arquivos TTC eram usados nas versões chinesa, japonesa e coreana do Windows, mas posteriormente o suporte estava disponível para todas as regiões.


## A estrutura do arquivo de coleção de fontes
Um arquivo TTC consiste em uma tabela de cabeçalho TTC, diretórios de tabela e várias tabelas OpenType. O cabeçalho TTC deve ser encontrado no início do arquivo. Deve existir um diretório de tabela completo para cada fonte. O formato TableDirectory deve ser semelhante ao existente em um arquivo que não seja de coleção. As contagens de tabela em todos os diretórios em um arquivo TTC são calculadas a partir do início de um arquivo TTC.
As tabelas em um arquivo TTC são referenciadas por meio do diretório de tabelas de suas respectivas fontes. Algumas das tabelas OpenType devem aparecer várias vezes, uma vez para cada fonte adicionada no TTC. Considerando que as outras tabelas podem ser compartilhadas por várias fontes no arquivo TTC.

### Cabeçalho TTC
Duas versões da tabela TTC Header estão disponíveis até o momento:
- A versão 1.0 é usada para arquivos TTC sem assinatura digital.
- A versão 2.0 pode ser usada para arquivos TTC com ou sem assinatura digital.
Aqui estão as tabelas de cabeçalho TTC de ambas as versões:

**Cabeçalho TTC Versão 1.0:**

|Tipo|Nome|Descrição|
---|---|---|
|TAG|ttcTag|String de ID de coleção de fontes: 'ttcf' (usado para fontes com contornos CFF ou CFF2, bem como contornos TrueType)|
|uint16|majorVersion|Versão principal do cabeçalho TTC, = 1.|
|uint16|minorVersion|Versão secundária do cabeçalho TTC, = 0.|
|uint32|numFonts|Número de fontes em TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Matriz de deslocamentos para TableDirectory para cada fonte desde o início do arquivo|

**Cabeçalho TTC Versão 2.0:**

|Tipo|Nome|Descrição|
---|---|---|
|TAG|ttcTag |String do ID da coleção de fontes: 'ttcf'|
|uint16| majorVersion |Versão principal do cabeçalho TTC, = 2.|
|uint16| minorVersion |Versão secundária do cabeçalho TTC, = 0.|
|uint32| numFonts |Número de fontes em TTC|
|Deslocamento32| tableDirectoryOffsets[numFonts] |Matriz de deslocamentos para TableDirectory para cada fonte desde o início do arquivo|
|uint32| dsigTag |Tag indicando que existe uma tabela DSIG, 0x44534947 ('DSIG') (null se não houver assinatura)|
|uint32| dsigLength |O comprimento (em bytes) da tabela DSIG (nulo se não houver assinatura)|
|uint32| dsigOffset |O deslocamento (em bytes) da tabela DSIG desde o início do arquivo TTC (nulo se não houver assinatura)|

## Referências
* [O arquivo de fonte OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

