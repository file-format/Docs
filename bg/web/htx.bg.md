{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX файл – файлов формат с разширение HTML",
  "description" :"Вашето ръководство за файлов формат, за да научите какво е HTX файл и API, които могат да създават и отварят HTX файл.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е HTX файл?

HTX файл всъщност е HTML файл, който съдържа променливи с данни за показване на резултатите от заявката към базата данни като уеб страница. Предимно създадени със софтуера за уеб разработка на Microsoft FrontPage, HTX файловете се записват, за да бъдат записани в същата папка като съответния файл на конектора за интернет база данни (.IDC).

HTX файловете могат да се отварят с приложения като Microsoft FrontPage и всеки текстов редактор като Notepad, TextEdit или Atom.

## HTX файлов формат

HTX файловете се записват като обикновен текстов файл с код за извличане на данни от база данни и записване в променливи за показване.


### Пример за HTX файл

Пример за HTX файл е както следва, който дефинира заглавка на страница за показване на ограничението на заявката и документите, показани на страницата за показване на потребителя.

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

Резултатът от този примерен код е както следва.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Както може да се види, HTX файлът е шаблон, който форматира как резултатите се връщат и показват на крайните потребители. Написан е в HTML формат с някои IIS разширения и услуга за индексиране. Тези разширения включват имена на променливи и други кодове за обработка на резултатите.

## Препратки

* [Форматиране на резултатите в .Htx файл](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

