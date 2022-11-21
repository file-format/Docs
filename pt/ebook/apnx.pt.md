{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Amazon Page Number Index", "extensão", "arquivo", "formato", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo do Amazon APNX e as APIs que podem criar e abrir arquivos APNX.",
  "title" :"APNX - Índice de número de página da Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## O que é um arquivo APNX? ##

O arquivo Amazon Page Number Index que usa a extensão .apnx é um tipo de arquivo eBook; usado pelo Amazon Kindle. Esses arquivos são conhecidos como arquivos de paginação usados por dispositivos Kindle. Portanto, os arquivos APNX normalmente são criados para marcar as páginas dos eBooks Kindle. O recurso de paginação foi iniciado em dispositivos Amazon Kindle desde seu firmware 3.1. Ele examina o arquivo APNX em busca de índices de página e o mapeia com os números de página no livro impresso original. Esses arquivos são salvos em dispositivos Kindle junto com os arquivos do Amazon eBooks. Você não pode abrir ou editar os arquivos APNX.

## Especificações de formato de arquivo APNX ##

### Disposição

|bytes| conteúdo| comentários|
---|---|---|
|4 |00010001 | Identificador de formato. Valor de 65537 little-endian.|
|4 |início do próximo | O deslocamento após a localização final do primeiro cabeçalho. Inicia uma nova sequência de informações de cabeçalho|
|4 |comprimento| Comprimento do primeiro cabeçalho|
|N |primeiro cabeçalho | String contendo cabeçalho de conteúdo. Ele inicia a próxima sequência|
|2 |desconhecido | Sempre 1|
|2 |comprimento | Comprimento do segundo cabeçalho|
|2 |contagem de páginas | Número total de bytes após o segundo cabeçalho que representam páginas. Esse total inclui bytes que são ignorados pelo pageMap.|
|2 |desconhecido | Sempre 32|
|N |segundo cabeçalho | String contendo o cabeçalho de mapeamento de página|
|4*N |preenchimento | O primeiro número fornecido no cabeçalho de mapeamento de página indica o número de 0 bytes.|
|4*N |lista de páginas ||

### Cabeçalho de conteúdo

O cabeçalho de conteúdo consiste em uma string entre {} contendo pares de chave e valor:

|conteúdo| comentários|
---|---|
|contentGuid| Guia.|
|asin | Identificador da Amazon para a versão Kindle do livro.|
|cdeType | MOBI cdeType. Deve ser sempre EBOK para ebooks.|
|fileRevisionId | Revisão deste arquivo.|

#### Exemplo
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Cabeçalho de mapeamento de página
O cabeçalho de mapeamento de página consiste em uma string entre {} contendo pares de chave e valor.

|conteúdo | comentários|
---|---|
|asin | O ISBN 10 para o livro em papel a que correspondem as páginas|
|páginaMapa| Tupla de três valores. Parece: "(N,N,N)\
1) Número de bytes após o cabeçalho que inicia a sequência de numeração da página\
2) desconhecido\
3) desconhecido\|
#### Exemplo
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Lista de páginas

A lista de páginas é uma sequência de deslocamentos no HTML bruto. Cada
value é o início de uma nova página. Cada entrada é um big endian de 4 bytes
int.



## Referências

* [formato de arquivo Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - por MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

