{
  "date" : "2021-08-24",
  "keywords" :[ "arquivo trc", "formato de arquivo trc", "o que é um arquivo trc", "arquivo", "exemplo trc", "extensão de arquivo trc", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo TRC e APIs que podem criar e abrir arquivos TRC.",
  "title" :"TRC - Arquivo de rastreamento do SQL Server",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## O que é um arquivo TRC?
Um arquivo com extensão .trc contém os resultados de rastreamento da atividade de um banco de dados do servidor SQL da Miscrosoft. Esses arquivos são criados por um software SQL Server Profiler; geralmente empacotado com o software Microsoft SQL Server. Os administradores de banco de dados podem analisar uma sequência de instruções do banco de dados e podem revisar o log de rastreamento se houver suspeita de algum tipo de erro ou aviso. Esses arquivos geralmente estão localizados na pasta LOG típica do MSSQL dentro do diretório Program Files em um sistema operacional Windows.

## Formato de arquivo TRC
O formato de arquivo TRC é usado pelo SQL Server Profiler para gerar automaticamente um novo rastreamento das instruções executadas recentemente pelo servidor MS SQL. O SQL Server Profiler usa o modelo padrão para qualquer novo rastreamento. No entanto, o software inclui vários modelos predefinidos para monitorar determinados tipos de eventos. Além disso, o SQL Server Profiler pode ser usado para criar modelos que definem as classes de eventos e as colunas de dados a serem incluídas nos rastreamentos.

### Modelos predefinidos
Aqui está a lista de alguns modelos predefinidos incluídos no SQL Server Profiler:
- **SP_Counts**: captura o comportamento de execução do procedimento armazenado ao longo do tempo.
- **Padrão**: ponto de partida genérico para a criação de um rastreamento.
- **TSQL**: Captura todas as instruções Transact-SQL que são enviadas ao SQL Server pelos clientes e a hora de emissão.
- **TSQL_Duration**: captura todas as instruções Transact-SQL enviadas ao SQL Server por clientes, seu tempo de execução e as agrupa por duração.
- **TSQL_Grouped**: Use para investigar consultas de um determinado cliente ou usuário.
- **TSQL_Locks**: use para solucionar problemas de deadlocks, bloquear o tempo limite e bloquear eventos de escalação.
- **TSQL_Replay**: use para realizar ajustes iterativos, como testes de benchmark.
- **TSQL_SPs**: Use para analisar as etapas do componente de procedimentos armazenados.
- **Ajuste**: use para produzir saída de rastreamento que o Orientador de Otimização do Mecanismo de Banco de Dados pode usar como uma carga de trabalho para ajustar bancos de dados.
### Correlacione um rastreamento com os dados do log de desempenho do Windows
O SQL Server Profiler pode ser usado para abrir um log de desempenho do Microsoft Windows, escolher os contadores para correlacionar com um rastreamento e exibir os contadores de desempenho selecionados ao lado do rastreamento na GUI do MS SQL Server Profiler. Para indicar os dados do log de desempenho que se correlacionam com o evento de rastreamento selecionado, uma barra vertical vermelha no painel da janela de dados do Monitor do Sistema do SQL Server Profiler.


## Referências ##

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)

