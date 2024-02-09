{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo MDF e APIs que podem criar e abrir arquivos MDF.",
  "title" :"Formato de arquivo MDF - Arquivo de banco de dados mestre do SQL Server",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo MDF?

Um arquivo com extensão .mdf é um arquivo de banco de dados mestre usado pelo [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) para armazenar dados do usuário. É de primordial importância, pois todos os dados são armazenados neste arquivo. O arquivo MDF armazena dados de usuários em bancos de dados relacionais nas colunas de formulário, linhas, campos, índices, exibições e tabelas. O SQL Server permite definir configurações de autogrow e autoshrink para ter um impacto positivo no desempenho do banco de dados. Os arquivos MDF podem ser carregados e anexados a um banco de dados usando o Microsoft SQL Server. Os arquivos MDF têm o tipo mime Application/octet-stream.

## Formato de arquivo MDF

A unidade fundamental de armazenamento de dados no SQL Server é uma página. Uma página de armazenamento atribuída ao banco de dados é dividida em páginas lógicas numeradas de 0 a n. Uma única página começa com um cabeçalho de 96 bytes que inclui ID da página, tipo de estrutura à qual a página pertence, número de registros na página e ponteiros para as páginas anterior e seguinte.

### Estrutura do arquivo

Um arquivo MDF tem a seguinte estrutura de dados.

* Página 0: Cabeçalho
* Página 1: Primeiro PFS
* Página 2: Primeiro GAM
* Página 3: Primeiro SGAM
* Página 4: Não utilizado
* Página 5: Não utilizado
* Página 6: Primeiro DCM
* Página 7: Primeiro BCM

#### Cabeçalho do arquivo

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

## Referências

* [Arquivos de banco de dados e grupos de arquivos](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Anexar e desanexar banco de dados - SQL Server](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server-ver15)
* [Analisando a anatomia do arquivo de dados do SQL Server](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

