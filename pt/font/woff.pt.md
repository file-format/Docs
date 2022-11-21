{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo woff", "formato de arquivo woff", "o que é um arquivo woff", "arquivo", "exemplo woff", "extensão de arquivo woff", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Formato de arquivo aberto da Web",
  "description":"Um arquivo WOFF é um formato de fonte aberta criado no Web Open Font Format.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## O que é um arquivo WOFF?

Um arquivo com extensão .woff é um arquivo de fonte da Web baseado no Web Open Font Format (WOFF). Ele possui um contêiner compactado específico de formato baseado em tipos de fonte TrueType (.TTF) ou OpenType (.OTT). O WOFF foi introduzido com o objetivo de diferenciar fontes da web de arquivos de fontes usados em aplicativos de desktop. Além disso, o formato visa reduzir a latência da transferência de fontes do servidor para o computador do cliente pela rede. Estão disponíveis várias ferramentas que podem converter arquivos WOFF para TTF e outros formatos de arquivo de fonte.

## **Formato de arquivo WOFF**

O formato de fonte WOFF compacta as tabelas de dados de fonte de estruturas sfnt baseadas em tabela usadas em diferentes tipos de fonte, como TrueType, OpenType e Open Font Format. É como um contêiner para esses tipos de fonte e também tem espaço para incluir os metadados da fonte e os dados de uso privado a serem incluídos no contêiner. Os conversores usam os arquivos sfnt em um arquivo formatado em WOFF e os agentes do usuário restauram o arquivo codificado para uso com o documento da web. Deve-se notar que os dados da fonte restaurada correspondem exatamente ao formato da fonte de entrada em todos os aspectos.

Utilitários de arquivo WOFF geralmente contêm recursos adicionais, como subconjunto de glifos, validação ou adições de recursos de fonte, mas não é necessário. Tanto o criador quanto os agentes de uso devem garantir que a validade dos dados de fonte subjacentes seja preservada.

### Estrutura do arquivo WOFF

A estrutura do arquivo WOFF é semelhante à das fontes sfnt. Ele é baseado em um diretório de tabela que contém os comprimentos e deslocamentos para cada tabela de dados de fonte. Todas as tabelas são seguidas após esta informação inicial. O arquivo contém o banco de dados de fontes que são os mesmos das fontes originais. A ordem das tabelas também é a mesma, mas cada uma pode ser compactada. O diretório de tabela WOFF substitui o diretório de tabela original.

Um arquivo WOFF consiste no seguinte:

* WOFFHeader - Cabeçalho de arquivo com tipo de fonte básica e versão, juntamente com deslocamentos para metadados e blocos de dados privados.
* TableDirectory - Diretório de tabelas de fontes, indicando o tamanho original, tamanho compactado e localização de cada tabela dentro do arquivo WOFF.
* FontTables - As tabelas de dados de fonte da fonte sfnt de entrada, compactadas para reduzir os requisitos de largura de banda.
* ExtendedMetadata - Um bloco opcional de metadados estendidos, representados em formato XML e compactados para armazenamento no arquivo WOFF.
* PrivateData- Um bloco opcional de dados privados para o designer de fontes, fundição ou fornecedor usar.

### Cabeçalho WOFF
O cabeçalho WOFF é composto por uma assinatura de identificação que indica o tipo de dados incluídos no arquivo. O cabeçalho WOFF junto com seus campos é o seguinte.

|Tipo|Nome do Campo|Descrição|
---|---|---|
|UInt32|assinatura |0x774F4646 'wOFF' |
|UInt32| sabor |A "versão sfnt" da fonte de entrada.|
|UInt32| length |Tamanho total do arquivo WOFF.|
|UInt16| numTables |Número de entradas no diretório de tabelas de fontes.|
|UInt16| reservado |Reservado; definido como zero.|
|UInt32| totalSfntSize |Tamanho total necessário para os dados de fonte não compactados, incluindo o cabeçalho sfnt, diretório e tabelas de fontes (incluindo preenchimento).|
|UInt16| majorVersion |Versão principal do arquivo WOFF.|
|UInt16| minorVersion |Versão secundária do arquivo WOFF.|
|UInt32| metaOffset |Deslocamento para bloco de metadados, desde o início do arquivo WOFF.|
|UInt32| metaLength |Comprimento do bloco de metadados compactado.|
|UInt32| metaOrigLength |Tamanho não compactado do bloco de metadados.|
|UInt32| privOffset |Deslocamento para bloco de dados privado, desde o início do arquivo WOFF.|
|UInt32| privLength |Comprimento do bloco de dados privados.|


## **Referências**
* [Formato de arquivo w3 WOFF](https://www.w3.org/TR/WOFF/)

