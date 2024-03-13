{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTX Faylı - HTML Genişləndirilməsi Fayl Format",
  "description": "HTX faylının və HTX faylını yarada və aça bilən API-lərin nə olduğunu öyrənmək üçün fayl formatı bələdçisi.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-azx"
}
},
  "lastmod": "2019-09-10"
}

## HTX faylı nədir?

HTX faylı əslində verilənlər bazası sorğusunun nəticələrini veb səhifə kimi göstərmək üçün verilənlər dəyişənlərini ehtiva edən HTML faylıdır. Əsasən Microsoft FrontPage Veb inkişaf proqramı ilə yaradılan HTX faylları müvafiq Internet Database Connector (.IDC) faylı ilə eyni qovluqda saxlanılmaq üçün saxlanılır.

HTX faylları Microsoft FrontPage kimi proqramlar və Notepad, TextEdit və ya Atom kimi istənilən mətn redaktoru ilə açıla bilər.

## HTX fayl formatı

HTX faylları verilənlər bazasından məlumatların alınması və ekran üçün dəyişənlərdə saxlanması kodu ilə düz mətn faylı kimi saxlanılır.


### HTX fayl nümunəsi

HTX faylının nümunəsi sorğu məhdudiyyətini və istifadəçiyə göstərmək üçün səhifədə göstərilən sənədləri göstərmək üçün səhifə başlığını təyin edən aşağıdakı kimidir.

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

Bu nümunə kodunun çıxışı aşağıdakı kimidir.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Göründüyü kimi, HTX faylı nəticələrin necə qaytarıldığını və son istifadəçilərə göstərilməsini formatlayan şablondur. Bəzi IIS uzantıları və İndeksləmə Xidməti ilə HTML formatında yazılmışdır. Bu uzantılara dəyişən adları və nəticələrin işlənməsi üçün digər kodlar daxildir.

## İstinadlar

* [.Htx Faylında Nəticələrin Formatlanması](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


