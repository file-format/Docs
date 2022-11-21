{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo ttf", "formato de arquivo ttf", "o que é um arquivo ttf", "arquivo", "exemplo ttf", "extensão de arquivo ttf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Formato de arquivo de fonte TrueType",
  "description":"As fontes TrueType (TTF) são baseadas em especificações de tecnologia de fonte digital inicialmente projetadas pela Apple, Inc. Tanto a Apple quanto a Microsoft usaram TTF nos sistemas operacionais Mac e Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## O que é um arquivo TTF?

Um arquivo com extensão .ttf representa arquivos de fonte com base na tecnologia de fonte de especificações TrueType. Ele foi inicialmente projetado e lançado pela Apple Computer, Inc para Mac OS e mais tarde foi adotado pela Microsoft para Windows OS. As fontes TrueType fornecem exibição da mais alta qualidade em telas de computador e impressoras sem qualquer dependência de resolução. Todos os aplicativos modernos que usam fontes podem trabalhar com arquivos TTF. Os arquivos de fonte TTF estão disponíveis gratuitamente na Internet e também podem ser convertidos para outros formatos de arquivo de fonte, como OTF e WOFF.

## Breve história

Projetado pela Apply Computer, Inc na década de 1980 para MacOS, o formato de fonte TTF visava resolver algumas limitações técnicas do formato Type 1 da Adobe. A Apple incluiu suporte para fontes TrueType no Mac em 1991. O objetivo do design por trás das fontes TTF era eficiência no armazenamento e processamento e extensibilidade. Com base nessa extensibilidade, as fontes existentes podem ser convertidas para o formato TrueType.

A Microsoft usou pela primeira vez as fontes TrueType no Windows 3.1 em abril de 1992, depois que a Apple concordou em licenciar TrueType para a Microsoft. Melhorou o mecanismo de rasterização e melhorou sua eficiência e desempenho.

## Especificações de formato de arquivo True Type

Um arquivo de fonte TrueType é um arquivo binário que consiste em uma sequência de tabelas concatenadas. Cada tabela é uma sequência de palavras e tem um nome conhecido como 'Tag'. Cada tag é do tipo de dados uint32 e consiste em quatro caracteres. A primeira tabela no arquivo é o diretório de fontes que dá acesso a outras tabelas no arquivo de fontes. Os dados da fonte estão contidos em outras tabelas seguidas da tabela do diretório de fontes. Como cada tabela é acessível por sua tag, as tabelas podem aparecer em qualquer ordem no arquivo.

As tabelas necessárias e seus nomes de tags são mostrados na tabela a seguir.

|**Etiqueta**|**Tabela**|
---|---|
|'cmap'| mapeamento de caracteres para glifos|
|'glif'| dados de glifo|
|'cabeça'| cabeçalho da fonte|
|'hea'| cabeçalho horizontal|
|'hmtx'| métricas horizontais|
|'localização'| índice para localização|
|'maxp'| perfil máximo|
|'nome'| nomeação|
|'postar'| PostScript|

### Tipos de dados
As fontes TrueType usam o número inteiro padrão e os tipos de dados adicionais, conforme listado na tabela a seguir.

|**Tipo de dados** | **Descrição** |
---|---|
|shortFrac| fração assinada de 16 bits|
|Corrigido| Número de ponto fixo assinado de 16,16 bits|
|FWord| Inteiro com sinal de 16 bits que descreve uma quantidade em FUnits, a menor distância mensurável no espaço em.|
|uFWord| Inteiro sem sinal de 16 bits que descreve uma quantidade em FUnits, a menor distância mensurável no espaço em.|
|F2Ponto14| Número fixo assinado de 16 bits com os 14 bits baixos representando fração.|
|longDateTime| O formato interno longo de uma data em segundos desde 12:00 meia-noite de 1º de janeiro de 1904. Ele é representado como um inteiro de 64 bits assinado.|

### Diretório de fontes

A primeira tabela na fonte TrueType é o diretório de fontes que fornece acesso às informações necessárias para acessar dados em outras tabelas. Consiste ainda em:

* `Subtabela de deslocamento` - mantém registro das tabelas na fonte e fornece informações de deslocamento para acessar cada tabela no diretório
* `Table Directory` - Contém entradas para cada tabela na fonte

#### Subtabela de deslocamento
A subtabela de deslocamento é mostrada abaixo.

|**Tipo**|**Nome**|**Descrição**|
---|---|---|
|uint32| tipo de escala | Uma tag para indicar o scaler OFA a ser usado para rasterizar essa fonte; consulte a nota sobre o tipo de escalonador abaixo para obter mais informações.|
|uint16| numTabelas| número de mesas|
|uint16| searchRange| (potência máxima de 2 <= numTables)*16|
|uint16| seletor de entrada| log2(potência máxima de 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Diretório de tabelas
O diretório da tabela vem logo após a subtabela de deslocamento. Sua estrutura é conforme a tabela a seguir.

|**Tipo**|**Nome**|**Descrição**|
---|---|---|
|uint32| etiqueta| identificador de 4 bytes|
|uint32| checkSum| soma de verificação para esta tabela|
|uint32| deslocamento| deslocamento do início de sfnt|
|uint32| comprimento| comprimento desta tabela em bytes (comprimento real não preenchido)|

Cada tabela em um arquivo de fonte deve ter sua própria entrada de diretório de tabela. As entradas em uma tabela devem ser classificadas em ordem crescente por tag.


## Referências
* [Manual de referência de fonte TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Visão geral do TrueType](https://docs.microsoft.com/en-us/typography/truetype/)

