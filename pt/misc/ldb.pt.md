{
"data": "20/04/2023",
  "keywords": [
"arquivo ldb",
"o que é um arquivo ldb",
"quais informações o ldb contém",
"qual é a finalidade do arquivo ldb",
"extensão LDB",
"arquivo",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo LDB - Arquivo de bloqueio do Microsoft Access",
  "description":"Aprenda sobre o formato LDB e quais informações ele contém.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent": "misc"
}
},
"último mod": "2023/04/20"
}

## O que é um arquivo .LDB?

Um arquivo LDB é um arquivo de bloqueio usado pelo Microsoft Access para evitar que vários usuários editem o mesmo banco de dados simultaneamente. Quando o usuário abre um banco de dados do Access, o Access cria um arquivo LDB correspondente no mesmo diretório do banco de dados. Este arquivo contém informações sobre quem está usando o banco de dados no momento e quais registros estão editando.

O arquivo LDB é criado automaticamente pelo Microsoft Access quando o banco de dados é aberto e é excluído quando o banco de dados é fechado. É importante observar que o arquivo LDB nunca deve ser excluído manualmente, pois isso pode causar problemas no banco de dados.

Se você encontrar problemas com o banco de dados Microsoft Access, uma solução potencial é tentar excluir o arquivo LDB associado a esse banco de dados. Isso liberará quaisquer bloqueios que possam estar impedindo você de acessar o banco de dados. No entanto, certifique-se de fazer um backup do banco de dados antes de tentar isso, pois a exclusão do arquivo LDB pode causar perda ou corrupção de dados se for feita incorretamente.

## Formato de arquivo LDB – Mais informações

Um arquivo LDB no Microsoft Access contém informações sobre os usuários que estão acessando o banco de dados, como nome de usuário, nome do computador e horário de login. O arquivo LDB também contém informações sobre quaisquer bloqueios que foram colocados no banco de dados, como quais registros estão sendo editados por qual usuário.

Aqui está uma lista mais detalhada dos tipos de informações que podem ser encontradas em um arquivo LDB:

- **Nome de usuário** - o nome do usuário que está acessando o banco de dados no momento
- **Nome do computador** - o nome do computador de onde o usuário está acessando o banco de dados
- **Hora de login** - a hora em que o usuário abriu o banco de dados pela primeira vez
- **Bloqueios de registro** - informações sobre quais registros estão sendo editados por qual usuário
- **Bloqueios de objetos** - informações sobre quais objetos de banco de dados (como tabelas, formulários ou relatórios) estão sendo editados atualmente por qual usuário
- **Informações de conexão** - informações sobre como o usuário está conectado ao banco de dados (por exemplo, se ele está usando conexão local ou de rede)

As informações no arquivo LDB são usadas pelo Microsoft Access para evitar que vários usuários façam alterações conflitantes no mesmo banco de dados ao mesmo tempo. Quando um usuário tenta editar um registro ou objeto que já está bloqueado por outro usuário, o Microsoft Access exibirá uma mensagem indicando que o objeto já está em uso. O arquivo LDB é atualizado conforme os usuários abrem e fecham o banco de dados e fazem alterações nos objetos bloqueados.

## Referências
* [O que é um arquivo LDB?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

