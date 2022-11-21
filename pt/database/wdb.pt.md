{
  "date" : "2021-08-24",
  "keywords" :[ "arquivo wdb", "formato de arquivo wdb", "o que é um arquivo wdb", "arquivo", "exemplo wdb", "extensão de arquivo wdb", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo WDB e APIs que podem criar e abrir arquivos WDB.",
  "title" :"WDB - Arquivo de rastreamento do SQL Server",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## O que é um arquivo WDB?
Um arquivo com extensão .wdb é na verdade um arquivo de banco de dados criado pelo Microsoft Works que foi usado para executar funções como um sistema de gerenciamento de banco de dados. O arquivo WDB é semelhante ao arquivo Access Database ([MDB](/pt/database/mdb/)), mas menos eficiente e com maiores limitações. Os arquivos WDB não podem ser abertos usando o Microsoft Access. No entanto, você pode abrir o arquivo WDB no Microsoft Works e exportá-lo para o arquivo MDB, para abrir um arquivo WDB no MS Access.

## Formato de arquivo WDB
O Banco de Dados do Microsoft Works é o formato de banco de dados nativo do pacote de escritório do Microsoft Works. Devido à natureza proprietária do formato e algumas limitações. Os arquivos WDB não podem ser abertos em nenhum outro software que não seja o Microsoft Works. No formato de arquivo, um cabeçalho recorrente de 10 bytes pode ser encontrado antes de cada uma das cadeias de texto ASCII que representam os valores dos campos que foram terminados por um valor NULL. O cabeçalho geralmente começa com um byte **\x0f** e NULL, seguido por 4 bytes de dados alternados com NULLs.

### Estrutura do arquivo

A estrutura do arquivo WDB é dada abaixo:
- **1º cabeçalho**: do início do arquivo, terminando com \x25\x00\xf2 e 244 bytes NULL
- **2º cabeçalho**: começando com \xffT - ou seja, \xff\x54 e estendendo-se por 4096 bytes, que contém nomes de colunas/campos e outras coisas, e parece começar na posição de byte 6144.
- **Campo**: valor tem um cabeçalho de 10 bytes, com o seguinte formato: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , parte 2} {db 4} \x00. o byte de dados 2 é o número do campo, o byte de dados 3 é o número do registro (adicionando o byte de dados 3, parte 2 quando ultrapassar 256 registros).


## Referências ##

* [User:JesseW/formato wdb](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

