{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Saiba mais sobre o formato de arquivo DSN e APIs que podem criar e abrir arquivos DSN.",
  "title" : "Formato de arquivo DSN - arquivo de nome de origem do banco de dados",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-pt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## O que é um arquivo .DSN?

DSN significa Nome da fonte de dados” e é um formato de arquivo usado para armazenar informações de conexão com o banco de dados. Os arquivos DSN são normalmente usados em conjunto com ODBC (Open Database Connectivity) e permitem fácil acesso a um banco de dados específico, fornecendo as informações necessárias para conectar-se a ele, como nome do servidor, nome de usuário e senha. O arquivo geralmente está em texto simples e pode ser criado e editado usando um editor de texto. Ele pode ser usado em vários sistemas operacionais como Windows, Linux e Mac.

## Como criar arquivo DSN?

O método para criar um arquivo DSN pode variar de acordo com o sistema operacional e as ferramentas disponíveis. As etapas a seguir fornecem uma visão geral do processo de criação de um arquivo DSN em um sistema Windows.

1. Abra o Administrador de fonte de dados ODBC procurando por Fontes de dados ODBC no menu Iniciar.
2. Selecione a guia DSN do sistema” e clique no botão Adicionar”.
3. Selecione o driver apropriado para o banco de dados ao qual deseja se conectar e clique em Concluir”.
4. Preencha as informações necessárias para se conectar ao banco de dados, como nome do servidor, nome de usuário e senha.
5. Clique em OK” para salvar o arquivo DSN.

Alternativamente, você pode criar um arquivo DSN manualmente criando um arquivo de texto simples com a extensão .dsn e inserindo as informações de conexão necessárias no formato:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Você pode então usar o caminho deste arquivo como o DSN em seu código/script para se conectar ao banco de dados.

## Programas que abrem o arquivo DSN

Um arquivo DSN é um arquivo de texto simples que armazena informações usadas para conectar-se a um banco de dados, como nome do servidor, nome de usuário e senha. Normalmente é usado em conjunto com ODBC (Open Database Connectivity) para fornecer acesso fácil a um banco de dados específico.

Para abrir e visualizar o conteúdo de um arquivo DSN, você pode usar qualquer editor de texto, como Notepad, Sublime Text, Atom, etc. Esses programas permitirão que você abra o arquivo DSN e visualize as informações de conexão armazenadas nele.

No entanto, para usar o arquivo DSN para conectar-se a um banco de dados e executar operações como SELECT, INSERT, UPDATE, DELETE etc, um programa com suporte ODBC, como uma linguagem de programação como Python, Java, C# ou uma ferramenta de gerenciamento de banco de dados como Microsoft Access , o SQL Server Management Studio é obrigatório. Esses programas podem usar as informações do arquivo DSN para se conectar ao banco de dados e realizar a operação desejada.

## Referências

* [O que é um DSN (nome da fonte de dados)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



