{
"data": "12/06/2023",
  "keywords": [
"bak",
"arquivo bak",
"Backup de banco de dados Microsoft SQL Server",
"o que é um arquivo bak",
"como abrir arquivo bak",
"arquivo",
"extensão de arquivo bak",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo BAK - Backup de banco de dados Microsoft SQL Server",
  "description":"Aprenda sobre o formato de backup BAK SQL Server e APIs que podem criar e abrir arquivos BAK.",
"linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent" : "database"
}
},
"último mod": "12/06/2023"
}

## O que é um arquivo .BAK?

Um arquivo “.bak”, no contexto do Microsoft SQL Server, é um formato de arquivo de backup usado para armazenar cópias de um banco de dados SQL Server. Esses arquivos contêm um instantâneo do banco de dados em um momento específico, incluindo seu esquema, dados e outras informações relacionadas. Eles são gerados usando a funcionalidade interna de backup e restauração do SQL Server e atendem a vários propósitos cruciais:

1. **Recuperação de dados:** arquivos .bak fornecem um meio de recuperar um banco de dados em caso de perda de dados, corrupção ou outros problemas. Ao restaurar um banco de dados a partir de um arquivo .bak, você pode revertê-lo para um estado anterior, minimizando o tempo de inatividade e a perda de dados.

2. **Migração e clonagem:** Os arquivos de backup são frequentemente usados para migrar bancos de dados entre servidores ou criar cópias de bancos de dados para fins de teste, desenvolvimento ou geração de relatórios. Eles oferecem uma maneira consistente e eficiente de mover bancos de dados entre ambientes.

3. **Recuperação pontual:** O SQL Server permite executar recuperação pontual usando arquivos .bak. Isso significa que você pode restaurar um banco de dados para um momento específico, o que pode ser crucial para conformidade regulatória ou auditoria de dados.

4. **Recuperação de desastres:** arquivos .bak são uma parte crítica do planejamento de recuperação de desastres. Eles garantem que seus dados estejam seguros e possam ser restaurados rapidamente em caso de falhas de hardware, desastres naturais ou outros eventos catastróficos.

## Crie um arquivo .BAK no SQL Server

Para criar um arquivo .bak no SQL Server, você normalmente usa comandos SQL Server Management Studio (SSMS) ou Transact-SQL (T-SQL), como BACKUP DATABASE ou BACKUP LOG. Aqui está um exemplo simplificado de como você pode criar um backup de banco de dados usando T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Restaurar um arquivo .BAK no SQL Server

Para restaurar um banco de dados a partir de um arquivo .bak, você pode usar o comando RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Como abrir o arquivo BAK no SQL Server?

Para abrir e acessar os dados armazenados em um arquivo ".bak", normalmente você precisa restaurá-lo em uma instância do Microsoft SQL Server. Aqui estão as etapas gerais para abrir um arquivo “.bak” usando o SQL Server Management Studio (SSMS):

1. **Inicie o SQL Server Management Studio**: Abra o SSMS em seu computador. Geralmente você pode encontrá-lo no menu Iniciar ou pesquisando por “SQL Server Management Studio”.

2. **Conectar-se a uma instância do SQL Server**: No SSMS, conecte-se à instância do SQL Server na qual deseja restaurar o banco de dados. Você precisará das permissões necessárias para realizar esta operação.

3. **Restaurar banco de dados**:

a. No painel Object Explorer no lado esquerdo, expanda a instância do SQL Server.

b. Expanda o nó "Bancos de dados".

c. Clique com o botão direito em “Bancos de dados” e selecione “Restaurar banco de dados”.

4. **Especifique a origem e o destino**:

a. Na página “Geral” da caixa de diálogo “Restaurar banco de dados”, insira um nome para o novo banco de dados no campo “Para banco de dados”. Este será o nome do banco de dados restaurado.

b. Na seção “Fonte”, escolha “Dispositivo” como tipo de mídia de backup.

c. Clique no botão “…” próximo ao campo “Dispositivo” para procurar o arquivo “.bak” que deseja restaurar.

d. Selecione o arquivo “.bak” que deseja abrir e clique em “OK”.

5. **Opções de restauração**: revise e configure as opções de restauração conforme necessário. Você pode especificar se deseja substituir um banco de dados existente, definir opções de recuperação e muito mais. Certifique-se de definir essas opções de acordo com suas necessidades.

6. **Iniciar a restauração**: Depois de configurar as opções de restauração, clique no botão "OK" na caixa de diálogo "Restaurar banco de dados". O SQL Server iniciará o processo de restauração.

7. **Acessar banco de dados restaurado**: após uma restauração bem-sucedida, você poderá acessar o banco de dados restaurado no SQL Server Management Studio como qualquer outro banco de dados. Você pode executar consultas, visualizar tabelas e trabalhar com os dados do banco de dados.

## Outros arquivos BAK

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.bak**.

**Base de dados**
- [BAK - Arquivo de backup do banco de dados](/pt/database/bak/)
- [BAK - Lei Swiftpage! Backup de banco de dados](/pt/database/bak-act/)

**Jogo**
- [BAK - Terraria World ou Backup do Jogador](/pt/game/bak-terraria/)

**Diversos**
- [BAK - Arquivo de backup](/pt/misc/bak-backup/)
- [BAK - Backup de favoritos do Chromium](/pt/misc/bak-chromium/)
- [BAK - Backup da pontuação final de 2012](/pt/misc/bak-finale/)
- [BAK - Backup do MobileTrans](/pt/misc/bak-mobiletrans/)
- [BAK - Backup do projeto de vídeo VEGAS](/pt/misc/bak-vegas/)

**Configurações**
- [BAK - Backup do Holo Launcher](/pt/settings/bak-holo/)

## Referências
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
