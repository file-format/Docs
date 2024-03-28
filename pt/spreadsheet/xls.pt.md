{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "arquivo", "extensão", "formato de arquivo", "Excel", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo XLS e APIs que podem criá-los e abri-los.",
  "title" :"O que é o formato de arquivo XLS? Aprenda com especialistas em formato de arquivo!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## O que é um arquivo XLS?

Arquivos com extensão XLS representam o formato de arquivo binário do Excel. Esses arquivos podem ser criados pelo Microsoft Excel, bem como por outros programas de planilhas semelhantes, como OpenOffice Calc ou Apple Numbers. O arquivo salvo pelo Excel é conhecido como Pasta de Trabalho onde cada pasta de trabalho pode ter uma ou mais planilhas. Os dados são armazenados e exibidos aos usuários em formato de tabela na planilha e podem abranger valores numéricos, dados de texto, fórmulas, conexões de dados externos, imagens e gráficos. Aplicativos como o Microsoft Excel permitem exportar dados da pasta de trabalho para vários formatos diferentes, incluindo [PDF](/pt/pdf/), [CSV](/pt/spreadsheet/csv/), [XLSX](/pt/spreadsheet/xlsx/), [TXT](/pt/word-processing/txt/), [HTML](/pt/web/html/), [XPS](/pt/page-description-language/xps/) e vários outros. O formato de arquivo XLS foi substituído por um formato mais aberto e estruturado, XLSX, com o lançamento do Microsoft Excel 2007. As versões mais recentes ainda oferecem suporte para criação e leitura de arquivos XLS, embora o XLSX seja a primeira opção de uso agora.

## Breve história

XLS foi criado pela Microsoft para uso com o Microsoft Excel e também é conhecido como Binary Interchange File Format (BIFF). Este tipo de arquivo foi introduzido pela primeira vez tornando-o parte do Excel para Windows em 1987. As especificações do formato de arquivo XLS foram divulgadas pela primeira vez em junho de 2008 como Revisão 1. Depois disso, as especificações foram continuamente atualizadas e a última revisão disponível é a partir de agosto de 2018 que está marcado como Revisão 8.0. Um breve histórico de diferentes versões do formato de arquivo XLS é o seguinte:

* Versão 7.0 (lançada com o Office 95): Esta versão do Excel foi a mais robusta e rápida entre todas as versões e as reescritas de fluxo interno foram atualizadas para 32 bits.
* Versão 8 (lançada com o Office 97): O VBA foi introduzido como uma linguagem padrão e os rótulos de linguagem natural removidos foram incorporados nesta versão pela primeira vez. Ele também introduziu um assistente de escritório de clipe de papel pela primeira vez.
* Versão 9 (lançado com o Office 2000): Houve apenas pequenas alterações na versão 9, onde o assistente de escritório com clipe de papel podia armazenar simultaneamente vários objetos que não eram possíveis anteriormente.
* Versão 10 (Lançada com o Office XP): Esta versão não continha nenhuma melhoria perceptível.
* Versão 11 (lançada com o office 2003): Grande atualização na versão 11, excel 2003 foi a introdução de novas tabelas.

## Especificações de formato de arquivo XLS ##

Os dados são organizados em um arquivo XLS como fluxos binários na forma de um arquivo composto, conforme descrito em [MS-CFB]. Os dados são armazenados no arquivo composto usando armazenamentos, fluxos e subfluxos que contêm informações sobre o conteúdo e a estrutura de uma pasta de trabalho, incluindo dados da pasta de trabalho, como definições de planilha. Cada fluxo ou subfluxo contém uma série de registros binários. Cada registro binário contém zero ou mais campos estruturados que contêm os dados da pasta de trabalho. Esta seção fornece uma breve visão geral da estrutura de arquivos XLS, mas para especificações detalhadas de formatos de arquivos, deve-se consultar as [Especificações de formação de arquivos XLS](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) da Microsoft.

#### Transmissão e Subtransmissão ####

Uma pasta de trabalho é representada pelo fluxo da pasta de trabalho. Cada planilha em uma pasta de trabalho é representada por Substreams. Além disso, possui Subfluxo de planilha de gráfico, Subfluxo de planilha de macro ou Subfluxo de planilha de diálogo que segue o Subfluxo global. Cada fluxo binário ou subfluxo que contém dados da pasta de trabalho DEVE ser escrito como uma série de registros binários.

#### Registro ####

As informações sobre recursos em uma pasta de trabalho são armazenadas como um registro que é uma sequência de bytes de comprimento variável. Um registro binário consiste nos três componentes a seguir:

**Tipo de registro:** o tipo de registro é um inteiro sem sinal de dois bytes que especifica que tipo de informação é especificada pelo registro e como a estrutura dos dados de registro específicos a esse registro é ordenada e estruturada. Os valores do tipo de registro DEVEM ser um valor da Enumeração de Registro (seção 2.3) ou o registro DEVE fazer uso da futura arquitetura de registro (seção 2.1.6).

**Tamanho do registro**: o tamanho do registro é um inteiro sem sinal de dois bytes que especifica a contagem de bytes que especifica o tamanho total dos dados do registro. O tamanho do registro DEVE ser maior ou igual a 0 e DEVE ser menor ou igual a 8224.

**Dados de registro:** o componente de dados de registro contém campos que correspondem a um tipo de registro específico e abrangem o restante do registro. A ordem e a estrutura dos campos para um determinado tipo de registro são especificadas na seção correspondente para esse tipo de registro. O tamanho do componente de dados de registro DEVE ser igual ao tamanho do registro. Os campos no componente de dados de registro podem conter valores simples, matrizes de valores, estruturas de vários campos, matrizes de campos e matrizes de estruturas.

#### Tabela de células ####

As células são os blocos fundamentais de uma pasta de trabalho que armazenam o conteúdo da pasta de trabalho, como texto, fórmulas e dados numéricos. As células mantêm o registro dos dados armazenados por meio de uma estrutura de dados chamada Tabela de Células. A própria tabela de células é armazenada na sequência de registros que obedecem às regras da CELLTABLE definidas no documento de especificações. Consiste em uma série de blocos de linhas onde as linhas são organizadas em blocos de linhas. Cada bloco de linha contém linhas da primeira linha contendo dados até a última linha contendo dados.

A formatação de dados ou linha é salva em um registro de linha para cada bloco de linha. Cada célula que contém dados ou formatação de célula individual é representada por um registro. A formatação associada a uma célula pode ser derivada de formatação de célula individual, formatação de linha, formatação de coluna ou formato de célula padrão. A ordem de precedência para formatação é a formatação de célula individual com a precedência mais alta, seguida pela formatação de linha e, em seguida, formatação de coluna e, em seguida, o formato de célula padrão. As células que não contêm dados e não contêm formatação individual não são salvas.

#### Fórmulas ####

Uma fórmula é uma sequência de valores, referências de células, nomes, funções ou operadores em uma célula que juntos produzem um novo valor. As fórmulas são armazenadas em uma representação tokenizada conhecida como "expressões analisadas". Uma expressão analisada é convertida em uma fórmula textual em tempo de execução para exibição e edição do usuário. As fórmulas de célula são especificadas pelo registro Fórmula. As fórmulas de matriz são especificadas pelo registro de matriz. As fórmulas compartilhadas são especificadas pelo registro ShrFmla.

#### Gráficos ####

A folha de gráfico especifica um gráfico, um gráfico que exibe dados ou os relacionamentos entre conjuntos de dados em um formato visual e um cache de dados do gráfico, uma cópia local dos dados usados nos dados do gráfico está ausente ou se links para as fontes de dados estão quebradas. O gráfico especifica grupos de um ou dois eixos, um conjunto de eixos em que os dados do gráfico são plotados e o conjunto de séries, linhas de tendência e barra de erro especificadas no gráfico. Cada grupo de eixos especifica de um a quatro grupos de gráficos que especificam o tipo de visualização usado para exibir os dados. Cada série, linha de tendência e barra de erro especifica um grupo de gráficos ao qual está associada.

#### Metadados ####

Metadados são dados adicionais associados a uma determinada célula ou seu conteúdo. Os metadados são registrados no BIFF8 apenas para fins de extensibilidade futura.

#### Tabelas Dinâmicas ####

Uma tabela dinâmica é um mecanismo para resumir dados de origem para obter uma visão geral da distribuição desses dados. Em uma tabela dinâmica, as colunas aplicáveis dos dados de origem se tornam campos que podem ser usados para resumir dados. Quando os dados de origem da Tabela Dinâmica são dados de origem OLAP, as hierarquias OLAP e algumas outras entidades OLAP tornam-se campos na Tabela Dinâmica.
Uma Tabela Dinâmica tem duas partes principais, um PivotCache e uma exibição de Tabela Dinâmica. Pode haver várias exibições de tabela dinâmica com base em um único PivotCache não OLAP.

#### Estilos ####

Esta visão geral descreve como as informações de formatação e proteção para células em uma planilha (1) são especificadas. A formatação da célula é composta por vários conjuntos de propriedades:

* Propriedades da fonte (negrito, itálico, cor da fonte, tamanho da fonte, etc…)
* Propriedades de preenchimento (cor de primeiro plano, cor de fundo, padrão, gradiente, etc…)
* Propriedades de alinhamento (esquerda, centro, alinhamento à direita, etc…)
* Propriedades da borda (esquerda, direita, superior, inferior, grossa ou fina, cor, etc…)
* Propriedades de formatação de números (data, hora, número de casas decimais, etc…)
* Propriedades de proteção (bloqueado, oculto, etc…)

Essas propriedades, como um todo, descrevem como uma determinada célula é exibida e impressa.

## Referências ##

* [[MS-XLS] - Estrutura de formato de arquivo binário do Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Formato de arquivo binário de arquivo composto](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

