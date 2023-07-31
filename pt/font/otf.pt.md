{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo otf", "formato de arquivo otf", "o que é um arquivo otf", "arquivo", "exemplo otf", "extensão de arquivo otf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Formato de arquivo de fonte TrueType",
  "description":"Saiba mais sobre o formato de arquivo OTF e APIs que podem criar e abrir arquivos OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## O que é um arquivo OTF?

Um arquivo com extensão .otf refere-se ao formato de fonte OpenType. O formato de fonte OTF é mais escalável e estende os recursos existentes dos formatos [TTF](/pt/font/ttf/) para tipografia digital. Desenvolvido pela Microsoft e pela Adobe, o OTF combina os recursos dos formatos de fonte PostScript e TrueType. Isso torna o formato OTF para acomodar sistemas de escrita majoritários e é por isso que é usado de maneira uniforme nas principais plataformas de computador. O formato de fonte OpenType é suportado pelo Mac OS X e Windows 2000 e posterior.

## Breve história

O requisito de fontes OpenType originou-se como um requisito para um formato de fonte mais expressivo que pudesse lidar com tipografia fina. Além disso, visava atender aos requisitos de comportamento complexo de muitos dos sistemas de escrita do mundo. A Microsoft tentou licenciar a tecnologia de tipografia avançada da Apple, conhecida como GX Typography, no início dos anos 90. Isso não deu certo e, como resultado, a Microsoft começou a aprimorar sua própria tecnologia de fonte TrueType em 1994. As modificações também incluíram a introdução de um formato de fonte mais adequado que também atende aos recursos dos formatos de fonte Type 1 (PostScript) da Adobe.

A Adobe, em 1996, juntou-se à Microsoft em seus esforços para substituir o TrueType da Apple e seus próprios formatos de fonte Type 1. Isso resultou na combinação de ambos os formatos de fonte subjacentes para superar as limitações e adicionar novas extensões. Essa nova tecnologia foi introduzida no mesmo ano com o nome **OpenType**.

## Especificações de formato de arquivo OTF

As especificações OTF estão disponíveis publicamente pela Microsoft e podem ser consultadas da perspectiva do desenvolvedor. Como o TTF, ele usa a mesma estrutura de contêiner 'sfnt' e é compatível com as especificações TrueType. Os dados dentro de um arquivo de fonte OpenType são usados para diferentes propósitos, como calcular o layout do texto, definir glifos como contornos TrueType ou Compact Font Format (CFF), fornecer bitmaps monocromáticos ou coloridos ou documentos SVG como descrições de glifos alternativos e informações de metadados.

### Tipos de dados OTF
Os arquivos OTF usam os seguintes tipos de dados, todos em Big Endian.

|Tipo de dados| Descrição|
---|---|
|uint8| inteiro sem sinal de 8 bits.|
|int8| inteiro com sinal de 8 bits.|
|uint16| inteiro sem sinal de 16 bits.|
|int16| inteiro com sinal de 16 bits.|
|uint24| inteiro sem sinal de 24 bits.|
|uint32| inteiro sem sinal de 32 bits.|
|int32| inteiro com sinal de 32 bits.|
|Corrigido| Número de ponto fixo assinado de 32 bits (16.16)|
|FWORD| int16 que descreve uma quantidade em unidades de design de fonte.|
|UFWORD| uint16 que descreve uma quantidade em unidades de design de fonte.|
|F2DOT14| Número fixo assinado de 16 bits com os 14 bits baixos de fração (2,14).|
|LONGDATETIME| Data e hora representadas em segundos desde a meia-noite de 1º de janeiro de 1904, UTC. O valor é representado como um inteiro de 64 bits com sinal.|
|Etiqueta| Matriz de quatro uint8s (comprimento = 32 bits) usada para identificar uma tabela, eixo de variação de design, script, sistema de linguagem, recurso ou linha de base|
|Deslocamento16| Deslocamento curto para uma tabela, igual a uint16, deslocamento NULL = 0x0000|
|Deslocamento32| Deslocamento longo para uma tabela, igual a uint32, deslocamento NULL = 0x00000000|
|Versão16Ponto16| Valor de 32 bits compactado com números de versão principal e secundária. (Consulte Números de versão da tabela.)|

### Diretório de tabelas OTF

Um arquivo OTF começa com um diretório de tabela. Esse diretório é a coleção de nível superior das tabelas no arquivo de fonte. Dependendo do número de fontes em um arquivo, o diretório da tabela pode estar localizado em um local diferente no arquivo. Por exemplo, caso o arquivo de fonte tenha apenas uma fonte, o diretório da tabela inicia no byte 0 do arquivo. No caso de várias coleções de fontes OpenType,
o início do diretório da tabela é indicado no TTCheader.

|Tipo |Nome |Descrição|
---|---|---|
|uint32 |sfntVersão| 0x00010000 ou 0x4F54544F ('OTTO')|
|uint16| numTables |Número de tabelas.|
|uint16| searchRange |Potência máxima de 2 menor ou igual a numTables, vezes 16 ((2\**floor(log2(numTables)))) * 16, onde “**” é um operador de exponenciação).|
|uint16 |entrySelector Log2 da potência máxima de 2 menor ou igual a numTables (log2(searchRange/16), que é igual a floor(log2(numTables))).|
|uint16 |rangeShift |numTables vezes 16, menos searchRange ((numTables * 16) - searchRange).|
|tabelaRegistro| tableRecords[numTables] |Matriz de registros de tabela—uma para cada tabela de nível superior na fonte|


### Registro de tabela

Para cada tabela de nível superior na fonte, há um registro de tabela que consiste nos seguintes campos.

|Tipo| Nome| Descrição|
---|---|---|
|Etiqueta| tabelaTag| Identificador de tabela.|
|uint32| soma de verificação| Soma de verificação para esta tabela.|
|Deslocamento32| deslocamento| Deslocamento do início do arquivo de fonte.|
|uint32| comprimento Comprimento desta tabela.|

Cada tabela no arquivo de fonte OpenType é representada por nomes conhecidos como tags de tabela. É obrigatório que todos os registros na matriz sejam classificados em ordem crescente por tag.

## Referências
* [Especificações de fonte OpenType da Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Visão geral do TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

