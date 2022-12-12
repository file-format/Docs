{
  "date" : "2021-04-21",
  "keywords": [ "what is a jsp file", "tutorials on jsp","jsp means","jsp", "jsp files", "extension", "format", "jsp tutorial", ".jsp", "jsp example","jsp file extension" ,"how to open a jsp file"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSP - формат файлу сторінок сервера Java",
  "description":"Дізнайтеся про формат файлу JSP із прикладом JSP та API, які можуть створювати та відкривати файли JSP.",
  "linktitle" : "JSP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Що таке файл JSP?
Файли JSP реалізовані як динамічні, керовані даними сторінки для ваших веб-додатків Java. JSP означає сторінки сервера Java; може бути реалізований як розширення Servlet, оскільки він забезпечує більше функціональних можливостей, ніж сервлет, наприклад мова виразів. JSP і Servlet виконують однакову роботу разом у старих веб-додатках Java. З точки зору програмування, найбільш чітка різниця між ними полягає в тому, що для сервлетів ви пишете програму на Java, а потім вставляєте статичну розмітку (наприклад, HTML) у цей код, тоді як JSP починається зі сценарію або розмітки на стороні клієнта, а потім вставляєте теги JSP, щоб підключіть свою сторінку до серверної частини Java.

## Формат файлу JSP
Файл, збережений із **розширенням файлу jsp**, містить такі розділи в порядку їх переліку:

1. Вступні коментарі
2. Директива(и) сторінки JSP
3. Необов'язкова директива бібліотеки тегів
4. Додаткова декларація JSP
5. Код HTML і JSP

### Вступні коментарі
Файл JSP або файл фрагмента починається з коментаря в стилі сервера:

```
<%-- 

  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 

  --%>
```
Наведений вище коментар з’являється лише на стороні сервера, оскільки він видаляється під час візуалізації сторінки в браузері. Коментар може містити інформацію про автора (авторів), дату та повідомлення про авторські права щодо редакції, ідентифікатор та опис сторінки JSP для розробників. Поєднання символів " @(#)" розпізнається деякими програмами як позначення початку ідентифікатора.

### Директива JSP-сторінки
Директива сторінки JSP визначає атрибути, пов’язані зі сторінкою JSPF під час перекладу. Специфікація JSP не накладає обмежень на те, скільки директив сторінки JSP можна записати на одній сторінці. Перегляньте наступний приклад:

```
<%@ page session="false" %>
<%@ page import="java.util.*" %>
<%@ page errorPage="/common/errorPage.jsp" %>
```
Якщо директива сторінки перевищує нормальну ширину сторінки JSP, директива розбивається на кілька рядків:

```
<%@ page    session="false" 

            import="java.util.*"
            errorPage="/common/errorPage.jsp" 

%>
```
### Додаткова директива бібліотеки тегів
На сторінці JSP директива бібліотеки тегів оголошує власні бібліотеки тегів. Коротку директиву можна оголосити в одному рядку. Кілька директив бібліотеки тегів зібрані разом в одному місці в тілі сторінки JSP:

```
<%@ taglib uri="URI1" prefix="tagPrefix1" %>
<%@ taglib uri="URI2" prefix="tagPrefix2" %>
...
```
### Додаткова декларація JSP
  


Методи та змінні, оголошені у файлі JSPF, повинні існувати в оголошеннях JSP. Ці методи та змінні подібні до декларацій у мові програмування Java, тому слід дотримуватися відповідних умов коду. Оголошення зазвичай пишуться в одному < %! ... %> Блок оголошень JSP, щоб централізувати оголошення в одній області тіла сторінки JSP. подивіться на наступні приклади:

#### Розрізнені блоки декларацій:

```
<%! private int hitCount; %>
    <%! private Date today; %>
    ...
    <%! public int getHitCount() {
            return hitCount;
    }
    %>
```
#### Бажаний блок декларації:
```
<%! 

        private int hitCount;
        private Date today; 

    


        public int getHitCount() {
            return hitCount;
    }
    %>
```
### Код HTML і JSP
Цей розділ сторінки JSP містить тіло HTML сторінки JSP і код JSPF, такі як вирази JSP, скриптлети та інструкції JavaBeans.

## Життєвий цикл сторінки JSP

Пофазовий потік сторінки JSP наведено тут:

- Переклад сторінки JSP
- Компіляція сторінки JSP
- Завантаження класів (завантажувач класів завантажує файл класу)
- Створення екземпляра (створюється об'єкт згенерованого сервлета).
- Ініціалізація (контейнер викликає метод jspInit().
- Обробка запиту (контейнер викликає метод _jspService()).
- Destroy (контейнер викликає метод jspDestroy()).

{{< figure src="../jsp.jpg" alt="Формат файлу JSP" >}}

## Приклад JSP

Зараз дуже легко вивчити технології JSP, оскільки в Інтернеті доступно багато посібників з JSP. Наступний приклад JSP призначений для обробки замовлення шляхом оновлення відповідних записів у базі даних.
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


 


## Список літератури

* [Положення про код для сторінок JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)
* [Посібник JSP](https://www.javatpoint.com/jsp-tutorial)

