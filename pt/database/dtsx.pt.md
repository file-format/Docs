{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DTSX e APIs que podem criar e abrir arquivos DTSX.",
  "title" :"Formato de arquivo DTSX - Arquivo de configurações DTS do SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo DTSX?

Um arquivo com extensão .dtsx (Data Transformation Services Package XML) é um arquivo Data Transformation Services (DTS) usado pelo Microsoft SQL para fazer referência a etapas/regras de migração de dados para transferência de dados de um banco de dados para outro. Isso inclui as transformações e quaisquer etapas de processamento opcionais que possam ser necessárias durante a transferência de dados entre os pontos de origem e destino. O SQL Server Integration Services (SSIS), um componente do Microsoft SQL Server, usa os arquivos DTSX para identificar as etapas de processamento de dados entre servidores de banco de dados. Os arquivos DTSX podem ser abertos com o Microsoft SQL Server 2019.

## Formato de arquivo DTSX

A movimentação de dados entre servidores de banco de dados requer regras e etapas de processamento para garantir a integridade dos dados durante essa operação. O SSIS garante que todas essas atividades, para mover e conformar dados de diferentes fontes em uma empresa, ocorram convenientemente. É aí que entra o DTSX que define as estruturas a serem utilizadas pelo SSIS para estabelecer as etapas onde os dados podem ser processados conforme segue por essas etapas.

O fluxo de dados descrito pelo DTSX é conforme mostrado na imagem a seguir.

{{< figure src="../DataFlowDTSX.png" alt="Fluxo de dados DTSX" >}}

DTSX é baseado em [XML](/pt/web/xml/) e está documentado em [MS-DTSX](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). A refatoração aprimorada do DTSX XML é o DTSX 2.0 que inclui novos atributos para as estruturas, substituição de propriedades nomeadas como atributos XML pai, especifica padrões para a maioria dos valores de atributo e colocação de elementos repetidos dentro de um elemento pai. As estruturas DTSX são descritas usando estes [XML Schemas](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) e o formato estrutural é celar-text XML.

## Referências

* [Formato DTSX - Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Formato DTSX 2 - Por Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

