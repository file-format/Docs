{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Formato de arquivo de páginas de servidor Java",
  "description":"Aprenda sobre o formato de arquivo JSP com exemplo de JSP e APIs que podem criar e abrir arquivos JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## O que é um arquivo JSP?
Os arquivos JSP são realizados como páginas dinâmicas e orientadas por dados para seus aplicativos da Web Java. O JSP significa Java Server Pages; pode ser realizado como uma extensão do Servlet porque permite mais funcionalidades do que o servlet, como linguagem de expressão. O JSP e o Servlet fazem o mesmo trabalho juntos em aplicativos da web Java mais antigos. De uma perspectiva de programação, a diferença mais clara entre eles é que, com servlets, você escreve programa Java e, em seguida, incorpora marcação estática (como HTML) nesse código, enquanto JSP começa com o script ou marcação do lado do cliente e, em seguida, incorpora tags JSP para conecte sua página ao backend Java.

## Formato de arquivo JSP
Um arquivo salvo com **extensão de arquivo jsp** contém as seguintes seções na ordem em que estão listadas:

1. Abrindo comentários
2. Diretiva(s) de página JSP
3. Diretivas de biblioteca de tags opcionais
4. Declaração(ões) JSP opcional(is)
5. Código HTML e JSP

### Comentários de abertura
Um arquivo JSP ou arquivo de fragmento começa com um comentário no estilo do lado do servidor:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
O comentário acima é exibido apenas no lado do servidor porque é removido durante a renderização da página no navegador. O comentário pode conter as informações sobre o(s) autor(es), a data e o aviso de copyright da revisão, um identificador e uma descrição sobre a página JSP para desenvolvedores. Combinar os caracteres " @(#)" é reconhecido por certos programas como indicando o início de um identificador.

### Diretiva(s) de página JSP
Uma diretiva de página JSP define atributos associados à página JSPF no momento da tradução. A especificação JSP não impõe uma restrição sobre quantas diretivas de página JSP podem ser gravadas em uma única página. Veja o seguinte exemplo:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Se uma diretiva de página exceder a largura normal de uma página JSP, a diretiva será dividida em várias linhas:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Diretivas de biblioteca de tags opcionais
Na página JSP, uma diretiva de biblioteca de tags declara bibliotecas de tags personalizadas. Uma diretiva curta pode ser declarada em uma única linha. Várias diretivas de biblioteca de tags são empilhadas juntas no mesmo local no corpo da página JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Declaração(ões) JSP opcional(is)
  


Os métodos e variáveis declarados em um arquivo JSPF devem existir nas declarações JSP. Esses métodos e variáveis são semelhantes a declarações na linguagem de programação Java, e é por isso que as convenções de código relevantes devem ser seguidas. As declarações geralmente são escritas em um único < %! ... %> Bloco de declaração JSP, para centralizar as declarações dentro de uma área do corpo da página JSP. veja os exemplos a seguir:

#### Blocos de declaração diferentes:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Bloco de declaração preferido:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Código HTML e JSP
Esta seção de uma página JSP contém o corpo HTML da página JSP e o código JSPF, como expressões JSP, scriptlets e instruções JavaBeans.

## Ciclo de vida de uma página JSP

O fluxo de página JSP em fase é fornecido aqui:

- Tradução da página JSP
- Compilação da página JSP
- Classloading (o classloader carrega o arquivo de classe)
- Instanciação (Objeto do Servlet Gerado é criado).
- Inicialização (o container invoca o método jspInit()).
- Processamento de solicitação (o contêiner invoca o método _jspService()).
- Destroy (o contêiner invoca o método jspDestroy()).

{{< figure src="../jsp.jpg" alt="Formato de arquivo JSP" >}}

## Exemplo JSP

Aprender sobre as tecnologias JSP é muito fácil hoje em dia porque muitos tutoriais JSP estão disponíveis na Internet. O exemplo de JSP a seguir é para processar o pedido, atualizando os registros apropriados no banco de dados.
```
<html>
<head>
  <title>Order Book</title>
</head>
 

<body>
  <h1>Another E-Bookstore</h1>
  <h2>Thank you for ordering...</h2>
 

  <%
    String[] ids = request.getParameterValues("id");
    if (ids != null) {
  %>
  <%@ page import = "java.sql.*" %>
  <%
      Connection conn = DriverManager.getConnection(
          "jdbc:mysql://localhost:8888/ebookshop", "myuser", "xxxx"); // <== Check!
      // Connection conn =
      //    DriverManager.getConnection("jdbc:odbc:eshopODBC");  // Access
      Statement stmt = conn.createStatement();
      String sqlStr;
      int recordUpdated;
      ResultSet rset;
  %>
      <table border=1 cellpadding=3 cellspacing=0>
        <tr>
          <th>Author</th>
          <th>Title</th>
          <th>Price</th>
          <th>Qty In Stock</th>
        </tr>
  <%
      for (int i = 0; i < ids.length; ++i) {
        // Subtract the QtyAvailable by one
        sqlStr = "UPDATE books SET qty = qty - 1 WHERE id = " + ids[i];
        recordUpdated = stmt.executeUpdate(sqlStr);
        // carry out a query to confirm
        sqlStr = "SELECT * FROM books WHERE id =" + ids[i];
        rset = stmt.executeQuery(sqlStr);
        while (rset.next()) {
  %>
          <tr>
            <td><%= rset.getString("author") %></td>
            <td><%= rset.getString("title") %></td>
            <td>$<%= rset.getInt("price") %></td>
            <td><%= rset.getInt("qty") %></td>
          </tr>
  <%}
        rset.close();
  }
      stmt.close();
      conn.close();
}
  %>
  </table>
  <a href="query.jsp"><h3>BACK</h3></a>
</body>
</html>
```


 


## Referências

* [Convenções de código para as páginas JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Tutorial JSP](https://www.javatpoint.com/jsp-tutorial)

