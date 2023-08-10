{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Pacote de aplicação de camada de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DACPAC e APIs que podem criar e abrir arquivos DACPAC.",
  "title" :"DACPAC - Data Tier AppliCation Package",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## O que é um arquivo DACPAC?

Um arquivo com extensão .dacpac (significa Data Tier AppliCation Package) é um arquivo de banco de dados, criado com o aplicativo de camada de dados do Microsoft SQL Server, que contém o modelo de banco de dados para representação de objetos de banco de dados. Por conter o modelo completo do banco de dados, é utilizado para restaurar um banco de dados a partir dos detalhes disponíveis no modelo. Os arquivos DACPAC geralmente são entregues às equipes de implantação para instalação nas instalações do cliente para restaurar o banco de dados. Estes podem ser abertos com
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## Formato de arquivo DACPAC - Mais informações

Os arquivos do pacote de dados DACPAC são, na verdade, arquivos ZIP compactados que contêm vários arquivos [XML](/pt/web/xml/) contendo informações sobre o modelo de banco de dados, como tabelas e visualizações, usadas para restaurar um banco de dados. Para visualizar o conteúdo dos arquivos DACPAC, renomeie os arquivos de .dacpac para [.zip](/pt/compression/zip/) e extraia o arquivo zip usando qualquer utilitário de descompactação.

A seguir estão alguns arquivos que são encontrados dentro de um arquivo DACPAC.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origem.xml

*model.xml

Deve-se notar que o DACPAC não contém DATA e outros objetos de nível de servidor. O arquivo pode conter todos os tipos de objetos que podem ser mantidos no projeto SSDT.

## Referências

* [Aplicativos de camada de dados - Benefícios](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Implantando um aplicativo de camada de dados - Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Como criar um arquivo DACPAC?](https://sqlplayer.net/2018/10/how-to-create-dacpac-file/)

