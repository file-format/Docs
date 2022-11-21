{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Formato de arquivo de fragmento JSP",
  "description":"Saiba mais sobre o formato de arquivo JSPF e APIs que podem criar e abrir arquivos JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## O que é um arquivo JSPF?
O arquivo com extensão .jspf é chamado de fragmento JSP; um arquivo estático incluído em outro arquivo JSP. Os arquivos JSPF não são compilados por conta própria, no entanto, são compilados ao lado da página em que foram incluídos. Sua sintaxe é semelhante ao código Java Server Pages (JSP). Ele contém apenas um fragmento de JSP; não incluiu todo o documento JSP.

## Formato de arquivo JSP
O termo "segmento JSP" é usado em vez disso, pois o termo "fragmento JSP" está sobrecarregado na Especificação JSP 2.0. Os fragmentos JSP podem usar extensões .jsp ou .jspf e devem ser colocados em **/WEB-INF/jspf** ou com o restante dos arquivos estáticos. Os fragmentos JSP que não são páginas completas devem usar a extensão .jspf e devem ser colocados em **/WEB-INF/jspf**

### Organização do arquivo de fragmento JSP ou JSP
Um arquivo JSP contém as seguintes seções na ordem em que são listadas:

1. Abrindo comentários
2. Diretiva(s) de página JSP
3. Diretivas de biblioteca de tags opcionais
4. Declaração(ões) JSP opcional(is)
5. Código HTML e JSP

Um arquivo JSP ou JSPF começa com um comentário no estilo do lado do servidor chamado **Comentário de abertura**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Este comentário pode ser visível apenas no lado do servidor porque é removido durante a renderização da página JSP.

## Quando usar o arquivo de fragmento JSP?
Quando uma página JSP requer uma certa mas complexa estrutura que também pode ser reutilizada em outras páginas JSP, uma maneira de lidar com isso é dividi-la em partes, usando o padrão Composite View (a seção Patterns de Java Blueprints). Por exemplo, uma página JSP às vezes tem o seguinte layout lógico em sua estrutura de apresentação:

{{< figure src="../jspf.png" alt="Formato de arquivo JSPF" >}}

Nesta situação, esta página JSP composta pode ser convertida em vários módulos, cada um será chamado de fragmento JSP separado. Os fragmentos JSP podem então ser colocados em locais apropriados na página JSP composta. Portanto, o arquivo JSPF é usado quando as diretivas de inclusão estática são usadas para incluir uma página que não seria chamada sozinha, os arquivos com extensão .jspf devem ser colocados no diretório /WEB-INF/jspf/ do arquivo da aplicação Web ( guerra).

## Exemplo de JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Referências

* [Convenções de código para as páginas JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

