{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo LDF e APIs que podem criar e abrir arquivos LDF.",
  "title" :"LDF - Formato de arquivo de banco de dados mestre do SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo LDF?

Um arquivo com extensão .ldf é um arquivo de log mantido pelo Microsoft SQL Server, que é um sistema de gerenciamento de banco de dados relacional (RDBMS). Todas as transações realizadas em arquivos de banco de dados primários ([MDF](/pt/database/mdf/))(como inserção, atualização, exclusão) são registradas no arquivo LDF. Os arquivos LDF são componentes críticos de qualquer banco de dados. Em caso de falha do sistema, o arquivo de log é usado para restaurar o banco de dados para um estado consistente. O arquivo de log de transações pode aumentar de tamanho se as transações não forem totalmente confirmadas. Os arquivos LDF podem ser abertos com o aplicativo de software Microsoft SQL Server.

## Operações Registradas em Arquivo LDF

Um arquivo de log SQL registra as seguintes operações:

* O início e o fim de cada transação.

* Cada modificação de dados de dados (inserir, atualizar ou excluir). Isso também inclui alterações por procedimentos armazenados do sistema ou instruções de linguagem de definição de dados (DDL) em qualquer tabela, incluindo tabelas de sistema.

* Cada extensão e alocação de página ou desalocação.

* Criando ou descartando uma tabela ou índice.

## Formato de arquivo LDF

O arquivo LDF consiste em registros de transação do SQL Server que são organizados como sequência de registros de log. Cada registro de log tem um número de sequência de log (LSN) maior que o LSN do registro anterior. As strings são concatenadas uma após a outra no arquivo. Devido aos computadores modernos de alta velocidade, os registros podem ser inseridos onde o LSN2 existe no arquivo de log antes do LSN1. Como as operações são registradas em série, a alteração descrita por LSN2 foi realizada após o registro de log LSN1. Os registros de uma transação específica são vinculados para trás usando ponteiros que são usados e aceleram a reversão da transação.
 

## Referências

* [Arquivos de banco de dados e grupos de arquivos](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Guia de arquitetura e gerenciamento de log de transações](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

