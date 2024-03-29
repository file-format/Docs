{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo MDB e APIs que podem criar e abrir arquivos MDB.",
  "title" :"Formato de arquivo MDB - um arquivo de banco de dados do Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## O que é um arquivo MDB?

Um arquivo com extensão .mdb é um arquivo de banco de dados do Microsoft Access que é um RDBMS (Relational Database Management System). Ele armazena dados em tabelas de banco de dados que são vinculadas entre si por meio de chaves primárias e estrangeiras. O arquivo MDB contém a estrutura completa das tabelas do banco de dados, consultas, procedimentos armazenados. MDB é o formato de arquivo padrão para o Microsoft Access 2003. As versões laterais do Microsoft Access usam os formatos de arquivo [ACCDB](/pt/database/accdb/), que é o formato de arquivo mais recente até o momento. Os arquivos MDB podem ser abertos com aplicativos como Microsoft Access, MDB Viewer, MDBopener e podem ser convertidos para ACCDB, [CSV](/pt/spreadsheet/csv/), formatos Excel, etc.

## Formato de arquivo MDB

Existem especificações públicas disponíveis para o formato MDB e continua sendo o formato de arquivo proprietário da Microsoft. A Microsoft, no entanto, fornece acesso de conectividade ao arquivo MDB usando o padrão Open Database Connectivity (ODBC) e o Visual Basic for Applications (VBA). O guia não oficial do MDB fornece uma breve descrição informal do formato MDB com base na engenharia reversa e pode ser consultado para conhecer as especificações.

### Páginas

De acordo com o guia não oficial do MDB, um arquivo MDB consiste em páginas de tamanho fixo (2048 bytes para Jeb DB3 e 4096 bytes para Jet DB 4). O primeiro byte indica o tipo de página. A seguir estão os principais tipos de página:

`Primeira página:` Contém informações do cabeçalho do banco de dados que também inclui a identificação da versão do Jet DB com a qual o arquivo é compatível. Além disso, também inclui informações de segurança de arquivos e um mapa de uso da página.

`Página de definição de tabela:` Uma página de definição de tabela especifica colunas, tipos de dados, índice e outras informações. Ele usa páginas adicionais, se necessário, e inclui um mapa de páginas que contém os dados de linha para esta tabela.

`Páginas de dados:` As páginas de dados são os contêineres de dados reais onde os dados são armazenados por linhas. Ele usa páginas subsidiárias para armazenar valores de dados longos.

Um único banco de dados do Microsoft Access pode ser composto por vários arquivos que permitem exceder as limitações de tamanho de arquivo e tabela. Isso facilita a colocação de formulários e código em um arquivo MDB de front-end na área de trabalho do usuário e dados em outros arquivos MDB de back-end em servidores conectados à rede.

## Referências ##

* [Especificações de acesso](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
