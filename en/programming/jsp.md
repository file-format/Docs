{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JSP - Java Server Pages File Format",
  "description":"Learn about JSP file format with JSP example and APIs that can create and open JSP files.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-21"
}

## What is a JSP file?
The JSP files are realized as the dynamic, data-driven pages for your Java web applications. The JSP means Java server Pages; can be thought of as an extension to Servlet because it enables more functionality than servlet such as expression language. The JSP and Servlet particularly work together in older Java web applications. From a programming perspective, the most clear difference between them is that with servlets you write Java program and then embed static markup (like HTML) into that code, whereas, JSP starts with the client-side script or markup, then embed JSP tags to connect your page to the Java backend. Learning about the JSP technologies are very easy now a days because a lot of JSP tutorials are available over the internet

## JSP File Organization
A JSP file contains the following sections in the order they are listed:

1. Opening comments
2. JSP page directive(s)
3. Optional tag library directive(s)
4. Optional JSP declaration(s)
5. HTML and JSP code

### Opening Comments
A JSP file or fragment file begins with a server side style comment:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Above comment is appeared only on the server side because it is removed while rendering the page in browser. The comment may contain the information about the author(s), the date, and the copyright notice of the revision, an identifier and a description about the JSP page for developers. Combining the characters " @(#)" is recognized by certain programs as indicating the start of an identifier.

### JSP Page Directive(s)
A JSP page directive defines attributes associated with the JSPF page at translation time. The JSP specification does not impose a constraint on how many JSP page directives can be written in a single page. See the following example:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
If a page directive, exceeds the normal width of a JSP page, the directive is broken into several lines:

```
<%@ page    session="false" 
            import="java.util.*"
            errorPage="/common/errorPage.jsp" 
%>
```
### Optional Tag Library Directive(s)
In JSP page, a tag library directive declares custom tag libraries. A short directive can be declared in a single line. Multiple tag library directives are stacked together in the same location within the JSP page's body:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Optional JSP declaration(s)
  
The methods and variables declared in a JSPF file should be existed in JSP declarations. These methods and variables are similar as declarations in the Java programming language, and that's why the relevant code conventions should be followed. Declarations are usually written in a single < %! ... %> JSP declaration block, to centralize declarations within one area of the JSP page's body. look at the following examples:

#### Disparate declaration blocks:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
        }
    %>
```
#### Preferred declaration block:
```
<%! 
        private int hitCount;
        private Date today; 
    
        public int getHitCount() {
            return hitCount;
        }
    %>
```
### HTML and JSP Code
This section of a JSP page holds the HTML body of the JSP page and the JSPF code, such JSP expressions, scriptlets, and JavaBeans instructions.

## Lifecycle of a JSP Page

The phase wise JSP page flow is given here:

- Translation of JSP Page
- Compilation of JSP Page
- Classloading (the classloader loads class file)
- Instantiation (Object of the Generated Servlet is created).
- Initialization ( the container invokes jspInit() method).
- Request processing ( the container invokes _jspService() method).
- Destroy ( the container invokes jspDestroy() method).

{{< figure src="../jsp.jpg" alt="JSP File Format" >}}

## JSP Example

The following JSP example is for processing the order, by updating the appropriate records in the database.
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
  <%    }
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



## References

 * [Code Conventions for the JavaServer Pages](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
 * [JSP Tutorial](https://www.javatpoint.com/jsp-tutorial)
