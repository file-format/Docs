{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo STR - Arquivo de objeto de lista de estrutura dBASE - O que é arquivo .str e como abri-lo?",
  "description" : "Aprenda sobre o arquivo de objeto de lista de estrutura STR dBASE e como abri-lo.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-pt",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## O que é um arquivo .STR?

O formato de arquivo STR é comumente associado ao dBASE, um sistema de gerenciamento de banco de dados. No dBASE, um arquivo .str normalmente representa um arquivo de objeto de lista de estruturas. Este arquivo contém a estrutura de uma tabela do banco de dados, incluindo informações sobre os campos (colunas) e suas propriedades.

O arquivo de objeto de lista de estrutura (.str) contém metadados como nomes de campos, tipos de dados, comprimentos de campos e quaisquer outras propriedades associadas a cada campo na tabela do banco de dados. É usado para definir a estrutura da tabela do banco de dados sem conter registros de dados reais.

Programas como dBASE ou outras ferramentas de gerenciamento de banco de dados podem utilizar este arquivo para entender o layout da tabela do banco de dados e realizar operações como consultar, atualizar ou criar novos registros com base nesta estrutura.

Aqui está um exemplo básico do que um arquivo STR pode conter:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Este exemplo descreve uma tabela com quatro campos: ID, Nome, Idade e Data de nascimento, juntamente com seus respectivos tipos e comprimentos de dados.

## Como abrir o arquivo STR?

A principal maneira de abrir arquivos .str é usando o próprio dBASE, principalmente em sistemas operacionais Windows. O dBASE é capaz de ler e interpretar o conteúdo desses arquivos, permitindo aos usuários visualizar e trabalhar com a estrutura do banco de dados.

Como os arquivos .str são essencialmente arquivos de texto simples que contêm informações sobre a estrutura do banco de dados, você também pode abri-los usando um editor de texto. Exemplos de editores de texto incluem Microsoft Notepad no Windows e Apple TextEdit no Mac. Quando aberto em um editor de texto, você poderá ver o conteúdo do arquivo, incluindo nomes de campos, tipos de dados e outras informações estruturais, em um formato legível por humanos.

## Referências
* [dBase](https://en.wikipedia.org/wiki/DBase)


