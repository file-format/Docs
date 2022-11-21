{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo SQLITE e APIs que podem criar e abrir arquivos SQLITE.",
  "title" :"Formato de arquivo SQLite",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## O que é um arquivo SQLite?

Um arquivo com extensão .sqlite é um arquivo de banco de dados SQL leve criado com o software [SQLite](https://www.sqlite.org/index.html). É um banco de dados em um arquivo próprio e implementa um mecanismo de banco de dados [SQL](/pt/database/sql/) autocontido, completo e altamente confiável. Os arquivos de banco de dados SQLite podem ser usados para compartilhar conteúdo rico entre sistemas simplesmente trocando esses arquivos pela rede. Quase todos os celulares e computadores usam SQLite para armazenamento e compartilhamento de dados, e é a escolha do formato de arquivo para aplicativos multiplataforma. Devido ao seu uso compacto e fácil usabilidade, vem empacotado dentro de outros aplicativos. As ligações SQLite existem para linguagens de programação como C, [C#](/pt/programming/cs), [C++](/pt/programming/cpp), [Java](/pt/programming/java/), [PHP](/pt/programming/php/ ), e muitos outros.

## Formato de arquivo SQLite

SQLite na realidade é uma biblioteca C-Language que implementa o SQLite RDBMS usando o formato de arquivo SQLite. Com a evolução de novos dispositivos todos os dias, seu formato de arquivo foi mantido compatível com versões anteriores para acomodar dispositivos mais antigos. O formato de arquivo SQLite é visto como um formato de arquivamento de longo prazo para os dados.

### O arquivo de banco de dados

Um banco de dados SQLite é totalmente mantido por meio de dois arquivos.
* Arquivo de banco de dados principal - Contém o estado completo do banco de dados SQLite
* Rollback Journal - Armazena informações adicionais em um segundo arquivo e é usado durante a realização de transações. Caso o SQLite esteja no modo WAL, um arquivo de log de gravação é mantido.

#### Arquivo de diário

Este arquivo destina-se a manter todas as informações mantidas caso a última transação não possa ser concluída em casos como uma pane no computador. Este arquivo é usado para restaurar o arquivo de banco de dados para um estado consistente.

#### Páginas

O arquivo principal do banco de dados SQLite é composto por uma ou mais páginas. A qualquer momento, cada página no banco de dados principal tem um único uso, que é um dos seguintes:

* A página de bytes de bloqueio
* Uma página de lista livre
* Uma página de tronco de lista livre
* Uma página de folha de lista livre
* Uma página b-tree
* Uma página interior da tabela b-tree
* Uma página de folha de árvore b da tabela
* Uma página interna do índice b-tree
* Uma página de folha de árvore b de índice
* Uma página de estouro de carga útil
* Uma página de mapa de ponteiro

O tamanho dos arquivos de banco de dados SQLite pode variar de alguns kilobytes a alguns gigabytes.

### Cabeçalho SQLite

O cabeçalho do banco de dados SQLite está localizado nos primeiros 100 bytes do arquivo de banco de dados. Todo arquivo de banco de dados SQLite válido começa com 16 bytes (em hexadecimal):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Os detalhes dos campos de cabeçalho são como na tabela a seguir.

|Deslocamento|Tamanho|Descrição|
---|---|---|
|0|16|A string do cabeçalho: "formato SQLite 3\000"|
|16|2|O tamanho da página do banco de dados em bytes. Deve ser uma potência de dois entre 512 e 32768 inclusive, ou o valor 1 representando um tamanho de página de 65536.|
|18|1|Versão de gravação do formato de arquivo. 1 para legado; 2 para WAL.|
|19|1|Versão de leitura do formato do arquivo. 1 para legado; 2 para WAL.|
|20|1|Bytes de espaço "reservado" não utilizado no final de cada página. Normalmente 0.|
|21|1|Fração máxima de carga útil incorporada. Deve ser 64.|
|22|1|Fração de carga útil incorporada mínima. Deve ser 32.|
|23|1|Fração de carga útil da folha. Deve ser 32.|
|24|4|Contador de alteração de arquivo.|
|28|4|Tamanho do arquivo de banco de dados em páginas. O "tamanho do banco de dados no cabeçalho".|
|32|4|Número da primeira página de tronco da lista livre.|
|36|4|Número total de páginas de lista livre.|
|40|4|O cookie do esquema.|
|44|4|O número do formato do esquema. Os formatos de esquema com suporte são 1, 2, 3 e 4.|
|48|4|Tamanho de cache de página padrão.|
|52|4|O número da página da maior página de árvore b raiz quando em modos de vácuo automático ou de vácuo incremental, ou zero caso contrário.|
|56|4|A codificação de texto do banco de dados. Um valor de 1 significa UTF-8. Um valor de 2 significa UTF-16le. Um valor de 3 significa UTF-16be.|
|60|4|A "versão do usuário" conforme lida e definida pelo pragma user_version.|
|64|4|True (diferente de zero) para o modo de vácuo incremental. Falso (zero) caso contrário.|
|68|4|O "ID do aplicativo" definido pelo PRAGMA application_id.|
|72|20|Reservado para expansão. Deve ser zero.|
|92|4|O número da versão válida para.|
|96|4|SQLITE_VERSION_NUMBER|

## Referências ##

* [Formato de arquivo SQLite - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - Especificações da linguagem C](https://www.sqlite.org/c3ref/intro.html)

