{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Report Definition Language Client-side",
  "keywords" :[ "rdlc", "linguagem de definição de relatório", "formato mkv", "XSD", "lado do cliente da linguagem de definição de relatório"],
  "description":"Saiba mais sobre o formato de arquivo RDLC, que é uma representação XML de uma definição de relatório do SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## O que é um arquivo RDLC? ##

O RDLC significa lado do cliente da linguagem de definição de relatório. Na verdade, é uma extensão do arquivo de relatório criado usando a tecnologia de relatórios da Microsoft. A versão SQL Server 2005 do Report Designer é usada para criar esses arquivos. O controle **ReportViewer** no lado do cliente pode executar diretamente os relatórios RDLC.

## Arquivos RDL VS RDLC
|Arquivos .rdl |Arquivos .rdlc|
---|---|
|Os arquivos RDL são criados pela versão SQL Server 2005 do Report Designer|Os arquivos RDLC são criados pela versão Visual Studio 2005 do Report Designer|
|É usado no SQL Server Reporting Services|É usado no Visual Studio|
|É um relatório remoto|É um relatório local|
|Precisa de uma instância do Reporting Services para executá-lo|Não precisa de uma instância do Reporting Services|

## Criando arquivos de definição de relatório de cliente (.rdlc)
O controle ReportViewer é usado para executar arquivos de definição de relatório de cliente (.rdlc) usando o recurso de processamento interno do controle. Os relatórios do cliente executados no modo de processamento local podem ser criados facilmente em seu projeto de aplicativo. A seguir estão as abordagens para criar o relatório:

- Use o **Assistente de relatórios** para criar uma nova definição de relatório de cliente (.rdlc).

- Crie um novo arquivo de definição de relatório de cliente (.rdlc) usando o Visual Studio.

- Gere uma definição de relatório programaticamente.


Você só pode visualizar um relatório executando-o em um controle **ReportViewer**. Observe que você pode abrir e editar a definição do relatório a qualquer momento e, em seguida, criar ou implantar o aplicativo para verificar os resultados.

## Referências ##

- [Criando arquivos de definição de relatório de cliente (.rdlc)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

