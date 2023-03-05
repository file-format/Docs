{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл HTX — формат файла расширения HTML",
  "description" :"Ваше руководство по формату файла, чтобы узнать, что такое файл HTX и API, которые могут создавать и открывать файл HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .HTX вариант №

Файл HTX на самом деле представляет собой файл HTML, который содержит переменные данных для отображения результатов запроса к базе данных в виде веб-страницы. Файлы HTX, которые в основном создаются с помощью программного обеспечения для веб-разработки Microsoft FrontPage, сохраняются в той же папке, что и соответствующий файл Internet Database Connector (.IDC).

Файлы HTX можно открывать с помощью таких приложений, как Microsoft FrontPage, и любого текстового редактора, такого как Блокнот, TextEdit или Atom.

## Формат файла HTX

Файлы HTX сохраняются как обычный текстовый файл с кодом для извлечения данных из базы данных и сохранения в переменных для отображения.


### Пример файла HTX

Ниже приведен пример файла HTX, который определяет заголовок страницы для отображения ограничения запроса и документы, отображаемые на странице для отображения пользователю.

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

Вывод этого примера кода выглядит следующим образом.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Как видно, файл HTX представляет собой шаблон, который форматирует то, как результаты возвращаются и отображаются для конечных пользователей. Он написан в формате HTML с некоторыми расширениями IIS и службой индексирования. Эти расширения включают имена переменных и другие коды для обработки результатов.

## использованная литература

* [Форматирование результатов в файле .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

