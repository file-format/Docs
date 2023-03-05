{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP — формат файла страниц сервера Java",
  "description":"Узнайте о формате файла JSP с примером JSP и API, которые могут создавать и открывать файлы JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## .JSP вариант №
Файлы JSP реализованы как динамические, управляемые данными страницы для ваших веб-приложений Java. JSP означает страницы сервера Java; может быть реализован как расширение сервлета, потому что он обеспечивает больше функциональных возможностей, чем сервлет, например язык выражений. JSP и Servlet вместе выполняют одну и ту же работу в старых веб-приложениях Java. С точки зрения программирования наиболее очевидная разница между ними заключается в том, что с сервлетами вы пишете программу на Java, а затем встраиваете в этот код статическую разметку (например, HTML), тогда как JSP начинается со сценария или разметки на стороне клиента, а затем встраивает теги JSP в код. подключите свою страницу к серверной части Java.

## Формат JSP-файла
Файл, сохраненный с расширением **jsp**, содержит следующие разделы в том порядке, в котором они перечислены:

1. Вступительные комментарии
2. Директива(ы) страницы JSP
3. Дополнительные директивы библиотеки тегов
4. Необязательные декларации JSP
5. Код HTML и JSP

### Вступительные комментарии
Файл JSP или файл фрагмента начинается с комментария в стиле серверной части:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Комментарий выше появляется только на стороне сервера, потому что он удаляется при рендеринге страницы в браузере. Комментарий может содержать информацию об авторе (авторах), дату и уведомление об авторских правах редакции, идентификатор и описание JSP-страницы для разработчиков. Сочетание символов "@(#)" распознается некоторыми программами как указание на начало идентификатора.

### Директива(ы) страницы JSP
Директива страницы JSP определяет атрибуты, связанные со страницей JSPF во время перевода. Спецификация JSP не накладывает ограничений на количество директив страниц JSP, которые могут быть записаны на одной странице. См. следующий пример:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Если директива страницы превышает нормальную ширину страницы JSP, директива разбивается на несколько строк:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Необязательные директивы библиотеки тегов
На странице JSP директива библиотеки тегов объявляет пользовательские библиотеки тегов. Короткая директива может быть объявлена в одной строке. Директивы нескольких библиотек тегов собраны вместе в одном и том же месте в теле страницы JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Необязательные декларации JSP
  


Методы и переменные, объявленные в файле JSPF, должны существовать в объявлениях JSP. Эти методы и переменные аналогичны объявлениям в языке программирования Java, поэтому необходимо соблюдать соответствующие соглашения по коду. Объявления обычно записываются одним < %! ... %> Блок объявлений JSP для централизации объявлений в одной области тела страницы JSP. посмотрите на следующие примеры:

#### Разрозненные блоки объявлений:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Предпочтительный блок объявлений:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Код HTML и JSP
Этот раздел страницы JSP содержит тело HTML страницы JSP и код JSPF, такие как выражения JSP, скриптлеты и инструкции JavaBeans.

## Жизненный цикл страницы JSP

Поэтапный поток страницы JSP приведен здесь:

- Перевод страницы JSP
- Компиляция JSP-страницы
- Загрузка классов (загрузчик классов загружает файл класса)
- Создание экземпляра (создается объект сгенерированного сервлета).
- Инициализация (контейнер вызывает метод jspInit()).
- Обработка запроса (контейнер вызывает метод _jspService()).
- Уничтожить (контейнер вызывает метод jspDestroy()).

{{< figure src="../jsp.jpg" alt="Формат JSP-файла" >}}

## Пример JSP

Изучить технологии JSP в наши дни очень просто, потому что в Интернете доступно множество учебных пособий по JSP. Следующий пример JSP предназначен для обработки заказа путем обновления соответствующих записей в базе данных.
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


 


## использованная литература

* [Соглашения кодов для страниц JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Учебное пособие по JSP](https://www.javatpoint.com/jsp-tutorial)

