{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - Java 服务器页面文件格式",
  "description":"通过 JSP 示例和可以创建和打开 JSP 文件的 API 了解 JSP 文件格式。",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## 什么是一 .jsp 文件？
JSP 文件被实现为 Java Web 应用程序的动态、数据驱动的页面。 JSP 表示 Java 服务器页面；可以作为 Servlet 的扩展来实现，因为它比 Servlet 提供了更多的功能，例如表达式语言。 JSP 和 Servlet 在较旧的 Java Web 应用程序中一起完成相同的工作。从编程的角度来看，它们之间最明显的区别在于，使用 servlet，您编写 Java 程序，然后将静态标记（如 HTML）嵌入到该代码中，而 JSP 从客户端脚本或标记开始，然后将 JSP 标记嵌入到代码中。将您的页面连接到 Java 后端。

## JSP 文件格式
使用 **jsp 文件扩展名** 保存的文件按列出的顺序包含以下部分：

1. 开场评论
2. JSP 页面指令
3. 可选标签库指令
4. 可选的 JSP 声明
5. HTML和JSP代码

### 打开评论
JSP 文件或片段文件以服务器端样式注释开头：

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
上面的评论只出现在服务器端，因为它在浏览器中呈现页面时被删除。评论可能包含关于作者的信息、日期和修订的版权声明、标识符和关于开发人员的 JSP 页面的描述。组合字符“@(#)"被某些程序识别为指示标识符的开始。

### JSP 页面指令
JSP 页面指令定义了在转换时与 JSPF 页面关联的属性。 JSP 规范没有限制在一个页面中可以写入多少个 JSP 页面指令。请参见以下示例：

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
如果页面指令超过了 JSP 页面的正常宽度，则该指令被分成几行：

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### 可选标签库指令
在 JSP 页面中，标签库指令声明自定义标签库。短指令可以在一行中声明。多个标签库指令在 JSP 页面主体内的同一位置堆叠在一起：

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### 可选 JSP 声明
  


JSPF 文件中声明的方法和变量应该存在于 JSP 声明中。这些方法和变量类似于 Java 编程语言中的声明，这就是为什么应该遵循相关的代码约定。声明通常以单个 < %! ... %> JSP 声明块，将声明集中在 JSP 页面主体的一个区域内。请看以下示例：

#### 不同的声明块：

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### 首选声明块：
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### HTML 和 JSP 代码
JSP 页面的这一部分包含 JSP 页面的 HTML 主体和 JSPF 代码，例如 JSP 表达式、scriptlet 和 JavaBeans 指令。

## JSP 页面的生命周期

分阶段的 JSP 页面流程如下所示：

- JSP页面的翻译
- JSP页面的编译
- 类加载（类加载器加载类文件）
- 实例化（创建生成的 Servlet 的对象）。
- 初始化（容器调用 jspInit() 方法）。
- 请求处理（容器调用 _jspService() 方法）。
- 销毁（容器调用 jspDestroy() 方法）。

{{< figure src="../jsp.jpg" alt="JSP 文件格式" >}}

## JSP 示例

现在学习 JSP 技术非常容易，因为互联网上有很多 JSP 教程。以下 JSP 示例用于通过更新数据库中的相应记录来处理订单。
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


 


## 参考

* [JavaServer 页面的代码约定](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [JSP 教程](https://www.javatpoint.com/jsp-tutorial)

