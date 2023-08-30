{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo MDF e APIs que podem criar e abrir arquivos NDF.",
  "title" :"Formato de arquivo NDF - Arquivo de banco de dados mestre do SQL Server",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo NDF?

Um arquivo com extensão .ndf é um arquivo de banco de dados secundário usado pelo [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) para armazenar dados do usuário. NDF é um arquivo de armazenamento secundário porque o SQL Server armazena dados especificados pelo usuário em um arquivo de armazenamento primário conhecido como [MDF](/pt/database/mdf/). O arquivo de dados NDF é opcional e é definido pelo usuário para gerenciar o armazenamento de dados caso o arquivo MDF primário use todo o espaço alocado. Geralmente é armazenado em disco separado e pode se espalhar para vários dispositivos de armazenamento. A presença de arquivos MDF é necessária para abrir arquivos NDF.

## Formato de arquivo NDF

O formato de arquivo NDF não é diferente de [MDF](/pt/database/mdf/) e usa páginas como a unidade fundamental de armazenamento de dados. cada página começa com um cabeçalho de 96 bytes que inclui:

* ID da página
* Tipo de Estrutura
* Número de registros nas páginas
* Ponteiros para páginas anteriores e seguintes

### Estrutura do arquivo NDF

Um arquivo MDF tem a seguinte estrutura de dados.

* Página 0: Cabeçalho
* Página 1: Primeiro PFS
* Página 2: Primeiro GAM
* Página 3: Primeiro SGAM
* Página 4: Não utilizado
* Página 5: Não utilizado
* Página 6: Primeiro DCM
* Página 7: Primeiro BCM

#### Cabeçalho do arquivo NDF

O número de página 0 de todos os arquivos contém um cabeçalho que armazena metadados sobre o arquivo.

#### Espaço livre na página (PFS)
O PFS identifica o status de alocação e determina a quantidade de espaço livre.

* Bit 1: Indica se a página está alocada ou não.
* Bit 2: Indica se a página é de uma extensão mista.
* Bit 3: Indica que esta página é uma página do IAM.
* Bit 4: Indica que esta página contém registros fantasmas
* Bits 5 a 7: Um valor combinado de três bits, que indica o preenchimento da página da seguinte forma:
* 0: A página está vazia
* 1: A página está 1–50% cheia
* 2: A página está 51–80% cheia
* 3: A página está 81–95% cheia
* 4: A página está 96–100% cheia

## Página do arquivo de dados

As páginas em um arquivo de dados do SQL Server começam do zero (0) e são incrementadas sequencialmente. Cada arquivo é reconhecido por um número de identificação de arquivo exclusivo. O par de ID de arquivo e número de página identifica exclusivamente uma página em um banco de dados. Um exemplo mostrando números de página em um banco de dados, é como na imagem a seguir.

{{< figure src="../ndf.png" alt="Formato de arquivo de banco de dados NDF" >}}

Este exemplo mostra números de página em um banco de dados que possui um arquivo de dados primário de 4 MB e um arquivo de dados secundário de 1 MB.

## Referências

* [Arquivos de banco de dados e grupos de arquivos](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
* [Anexar e desanexar banco de dados - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Analisando a anatomia do arquivo de dados do SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

