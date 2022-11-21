{
  "date" : "2020-11-11",
  "keywords" :[ "DDL", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DDL e APIs que podem criar e abrir arquivos DDL.",
  "title" :"Formato de arquivo DDL - Um arquivo de linguagem de definição de dados",
  "linktitle" : "DDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## O que é um arquivo DDL?

Um arquivo com extensão .ddl é um arquivo de linguagem de definição de dados usado para definir o esquema de um banco de dados. Ele contém instruções/comandos para trabalhar com estruturas de banco de dados, como tabelas, colunas, registros e outros campos. Os comandos em um arquivo DDL são escritos em [SQL](/pt/database/sql/) e podem realizar operações como criar tabela no banco de dados, descartar e atualizar. Um esquema de banco de dados é de propriedade de seu criado e todas as operações CRUD podem ser executadas nele. Aplicativos populares que podem criar e abrir arquivos DDL são Windows Text Editor, Jetbrains Intellij Idea e EclipseLink.

## Comandos DDL

Um único arquivo DDL pode conter vários comandos que, devido à sintaxe correta, serão executados em sequência e farão alterações no esquema, como criar conjuntos de caracteres e tabelas, descartar tabelas, renomear e alterar tabelas. Os comandos DDL a seguir são comumente usados ao trabalhar com o esquema de banco de dados.

`CREATE` - Usado para criar o banco de dados ou seus objetos (como tabela, índice, função, visualizações, procedimento de armazenamento e gatilhos).

`DROP` – Usado para excluir objetos do banco de dados.

`ALTER` - Usado para alterar a estrutura do banco de dados.

`TRUNCATE` – Usado para remover todos os registros de uma tabela, inclusive todos os espaços alocados para que os registros sejam removidos.

`COMMENT` – Adiciona comentários ao dicionário de dados.

`RENAME` – Renomeia um objeto existente no banco de dados.

## Exemplo DDL

O exemplo a seguir mostra a instrução DDL para o comando CREATE que cria uma tabela e define seus campos.

```
CREATE TABLE employees (
    id            INTEGER       PRIMARY KEY,
    first_name    VARCHAR(50)   not null,
    last_name     VARCHAR(75)   not null,
    fname         VARCHAR(50)   not null,
    dateofbirth   DATE          not null
);
```

## Referências ##

* [DDL pela Wikipedia](https://en.wikipedia.org/wiki/Data_definition_language)

