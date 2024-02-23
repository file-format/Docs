{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aprenda sobre o formato de arquivo ABCDDB e APIs que podem criar e abrir arquivos ABCDDB.",
  "title" : "Formato de arquivo ABCDDB - Arquivo de banco de dados da lista de contatos do catálogo de endereços da Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-pt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## O que é um arquivo .ABCDDB?

O arquivo com extensão **.ABCDDB** significa Banco de dados da lista de contatos do catálogo de endereços da Apple. Ele pertence ao aplicativo **Catálogo de Endereços**, também comumente conhecido como **Contatos**. É um aplicativo integrado e incluído nos sistemas operacionais iOS e macOS. O aplicativo Contatos permite aos usuários salvar e organizar informações relacionadas aos seus contatos, incluindo indivíduos, empresas e organizações. Este aplicativo permite aos usuários acompanhar detalhes como nomes, endereços, números de telefone e endereços de e-mail, bem como categorizar seus contatos em grupos.

## Relação com SQLite e caminho típico

O AddressBook da Apple (também conhecido como Contatos) armazena informações de contato como vCards na pasta de metadados. **O arquivo _ABCDDB_ é na verdade _SQLite 3 datafile_**.

SQLite é um sistema popular de gerenciamento de banco de dados projetado para ser leve e independente. É usado em muitos tipos diferentes de software e dispositivos. SQLite é um tipo de RDBMS, o que significa que armazena dados em tabelas relacionadas entre si por meio de chaves. Ele pode lidar com uma variedade de tipos de dados, incluindo números inteiros, números de ponto flutuante, strings e dados binários. Além disso, o SQLite suporta transações, que permitem aos usuários realizar múltiplas operações de banco de dados juntas como uma única unidade de trabalho.

O arquivo com extensão ABCDDB normalmente é armazenado aqui

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Consertando banco de dados de contatos corrompido

Primeiro faça o backup antes de tentar fazer isso. Então navegue até

`~/Library/Application Support/AddressBook`

Nesse diretório, você encontrará três arquivos, incluindo aquele com extensão .abcddb

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

Exclua todos esses arquivos e reabra os Contatos, ele começará a funcionar novamente.

## Restaurar banco de dados AddressBook do Backup

Suponha que os contatos do seu banco de dados AddressBook estejam armazenados em `addressbook-v22.abcddb`

- Primeiro faça backup dos dados do seu AddressBook e feche todos os aplicativos.
- Mova seu arquivo de banco de dados para o subdiretório `~/Library/Application Support/AddressBook`
- Inicie **Address Book.app**.

## Exportar dados do arquivo ABCDDB para o Microsoft Access

Como o arquivo é um arquivo de dados SQLite 3, você pode exportar os dados dentro do arquivo abcddb para o Microsoft Access usando o conector ODBC.

O conector SQLite ODBC é uma biblioteca de software e driver que permite que aplicativos que suportam a interface ODBC se conectem a um banco de dados SQLite. Inclui uma biblioteca que define a interface ODBC e um driver que traduz essa interface em chamadas para a API SQLite. Para utilizar o conector SQLite ODBC, você deve primeiro instalá-lo e depois configurar uma fonte de dados ODBC em seu computador. Após concluir essas etapas, qualquer aplicativo equipado com suporte ODBC poderá se conectar à fonte de dados e recuperar dados do banco de dados SQLite.

## Referências
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Banco de dados de contatos para Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Como posso abrir ou exportar um arquivo abcddb no Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

