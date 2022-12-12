{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл HTX - формат файлу розширення HTML",
  "description" :"Посібник із формату вашого файлу, щоб дізнатися, що таке файл HTX та API, які можуть створювати та відкривати файл HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл HTX?

Файл HTX насправді є файлом HTML, який містить змінні даних для відображення результатів запиту до бази даних у вигляді веб-сторінки. Здебільшого створені за допомогою програмного забезпечення для веб-розробки Microsoft FrontPage, файли HTX зберігаються для збереження в тій же папці, що й відповідний файл Internet Database Connector (.IDC).

Файли HTX можна відкривати за допомогою таких програм, як Microsoft FrontPage, і будь-якого текстового редактора, наприклад Notepad, TextEdit або Atom.

## Формат файлу HTX

Файли HTX зберігаються як звичайний текстовий файл із кодом для отримання даних із бази даних і збереження у змінних для відображення.


### Приклад файлу HTX

Нижче наведено приклад файлу HTX, який визначає заголовок сторінки для відображення обмеження запиту та документів, які відображаються на сторінці для відображення користувачеві.

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

Вихід цього прикладу коду виглядає наступним чином.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Як видно, файл HTX є шаблоном, який форматує, як результати повертаються та відображаються кінцевим користувачам. Він написаний у форматі HTML з деякими розширеннями IIS і службою індексування. Ці розширення містять імена змінних та інші коди для обробки результатів.

## Список літератури

* [Форматування результатів у файлі .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

