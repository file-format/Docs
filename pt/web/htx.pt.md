{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo HTX - Formato de arquivo de extensão HTML",
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo HTX e APIs que podem criar e abrir um arquivo HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo HTX?

Um arquivo HTX é na verdade um arquivo HTML que contém variáveis de dados para exibir os resultados da consulta do banco de dados como uma página da web. Principalmente criados com o software de desenvolvimento da Web Microsoft FrontPage, os arquivos HTX são salvos para serem salvos na mesma pasta que o arquivo correspondente do Internet Database Connector (.IDC).

Os arquivos HTX podem ser abertos com aplicativos como o Microsoft FrontPage e qualquer editor de texto como o Bloco de Notas, TextEdit ou Atom.

## Formato de arquivo HTX

Os arquivos HTX são salvos como arquivo de texto simples com código para recuperar dados de um banco de dados e salvar em variáveis para exibição.


### Exemplo de arquivo HTX

Um exemplo de arquivo HTX é o seguinte que define um cabeçalho de página para exibir a restrição de consulta e os documentos exibidos na página para exibição ao usuário.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

A saída deste código de exemplo é a seguinte.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Como pode ser visto, o arquivo HTX é um modelo que formata como os resultados são retornados e exibidos para os usuários finais. Está escrito no formato HTML com algumas extensões do IIS e Serviço de Indexação. Essas extensões incluem nomes de variáveis e outros códigos para processar resultados.

## Referências

* [Formatando os resultados no arquivo .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

