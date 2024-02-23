{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Saiba mais sobre o formato de arquivo DB-WAL e APIs que podem criar e abrir arquivos DB-WAL.",
  "title" : "Formato de arquivo DB-WAL - Arquivo de log write-ahead do banco de dados SQLite",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-pt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## O que é um arquivo .DB-WAL?

A extensão de arquivo .db-wal está associada ao SQLite, um popular sistema de gerenciamento de banco de dados relacional de código aberto. O formato de arquivo WAL (abreviação de Write-Ahead Log) é uma alternativa ao diário de reversão tradicional usado pelo SQLite. Ele fornece mais controle de simultaneidade, permitindo que vários processos leiam o banco de dados ao mesmo tempo, ao mesmo tempo em que fornece recursos de recuperação de falhas. O arquivo .db-wal é usado para armazenar alterações feitas no banco de dados que ainda não foram confirmadas no arquivo do banco de dados principal (com extensão .db).

## Formato WAL geral

No formato de arquivo WAL (Write-Ahead Log), as alterações feitas no banco de dados são primeiro gravadas no arquivo WAL antes de serem confirmadas no arquivo de banco de dados principal. Isso permite um acesso mais simultâneo ao banco de dados, pois vários processos podem ler o banco de dados enquanto as alterações estão sendo feitas. Além disso, o formato de arquivo WAL fornece recursos de recuperação de falhas, permitindo que o banco de dados seja revertido para um estado anterior no caso de um desligamento inesperado.

## Diferença entre o formato DB-WAL e WAL

Os formatos de arquivo .db-wal e WAL estão associados ao SQLite, um popular sistema de gerenciamento de banco de dados relacional de código aberto. No entanto, há uma diferença sutil entre os dois.

O arquivo .db-wal é essencialmente um arquivo WAL, mas com uma extensão de arquivo diferente. O arquivo .db-wal é usado para armazenar alterações feitas no banco de dados que ainda não foram confirmadas no arquivo de banco de dados principal (com extensão .db), enquanto o formato de arquivo WAL é usado para armazenar o log write-ahead das alterações do banco de dados .

Em outras palavras, um arquivo .db-wal é um tipo específico de arquivo WAL usado por bancos de dados SQLite para armazenar alterações feitas no banco de dados que ainda não foram confirmadas no arquivo de banco de dados principal. O formato de arquivo WAL é o termo geral para este tipo de formato de arquivo.

Portanto, WAL é o termo geral para o formato de arquivo, .db-wal é uma implementação específica do formato de arquivo WAL usado por bancos de dados SQLite.

## Referências
* [Formato de arquivo no modo WAL](https://www.sqlite.org/walformat.html)

* [Registro Write-Ahead](https://www.sqlite.org/wal.html)


