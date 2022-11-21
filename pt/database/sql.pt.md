{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo SQL e APIs que podem criar e abrir arquivos SQL.",
  "title" :"Formato de arquivo SQL - um arquivo de dados de linguagem de consulta estruturada",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## O que é um arquivo SQL?

Um arquivo com extensão .sql é um arquivo SQL (Structured Query Language) que contém código para trabalhar com bancos de dados relacionais. Ele é usado para escrever instruções SQL para operações CRUD (Criar, Ler, Atualizar e Excluir) em bancos de dados. Arquivos SQL são comuns ao trabalhar com bancos de dados desktop e baseados na web. Existem várias alternativas ao SQL, como Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL e várias outras. Os arquivos SQL podem ser abertos por editores de consulta do Microsoft SQL Server, MySQL e outros editores de texto simples, como o Bloco de Notas no sistema operacional Windows.

## Breve história

* Desenvolvido e introduzido por Donal D. Chamberlin e Raymond F. Boyce na IBM no início dos anos 1970
* Usado para armazenar e recuperar dados do sistema de gerenciamento de banco de dados quase relacional original da IBM, System R
* Começou a ser usado em produtos comerciais baseados em seu protótipo do System R, incluindo System/38, SQL/DS e DB2, que estavam disponíveis comercialmente em 1979, 1981 e 1983, respectivamente.
* Oficialmente adotado pelos grupos de padrões ANSI e ISO como padrão "Database Language SQL" para sistemas de gerenciamento de banco de dados relacional (RDBMS) em 1986

## Formato de arquivo SQL

Os arquivos SQL estão em formato de texto simples e podem incluir vários elementos de linguagem. Várias instruções podem ser adicionadas a um único arquivo SQL se sua execução for possível sem depender uma da outra. Esses comandos SQL podem ser executados por editores de consulta para realizar operações CRUD.

### Elementos da linguagem SQL

Os elementos da linguagem SQL estão listados abaixo.

|Elemento|Descrição|
---|---|
|Cláusulas| Componentes constituintes de declarações e consultas.|
|Expressões| Pode produzir valores escalares ou tabelas que consistem em colunas e linhas de dados|
|Predicados| Especifique as condições que podem ser avaliadas para lógica de três valores SQL (3VL) (verdadeiro/falso/desconhecido) ou valores de verdade booleanos e são usados para limitar os efeitos de instruções e consultas ou para alterar o fluxo do programa.|
|Consultas| Recupere os dados com base em critérios específicos. Este é um elemento importante do SQL.|
|Declarações| Pode ter um efeito persistente em esquemas e dados ou pode controlar transações, fluxo de programa, conexões, sessões ou diagnósticos.|

### Exemplo SQL
A instrução SQL a seguir cria uma tabela chamada **DATA**, seguida por comandos adicionais `INSERT` para inserir registros nesta tabela.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referências ##

* [SQL da Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Sintaxe SQL](https://en.wikipedia.org/wiki/SQL_syntax)

