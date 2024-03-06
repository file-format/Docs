{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTX fails — HTML paplašinājuma faila formāts",
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir HTX fails un API, kas var izveidot un atvērt HTX failu.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-lvx"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir HTX fails?

HTX fails faktiski ir HTML fails, kas satur datu mainīgos datu bāzes vaicājuma rezultātu parādīšanai kā tīmekļa lapai. Pārsvarā izveidoti ar Microsoft FrontPage Web izstrādes programmatūru, HTX faili tiek saglabāti, lai tos saglabātu tajā pašā mapē, kurā atrodas atbilstošs interneta datu bāzes savienotāja (.IDC) fails.

HTX failus var atvērt, izmantojot tādas lietojumprogrammas kā Microsoft FrontPage un jebkuru teksta redaktoru, piemēram, Notepad, TextEdit vai Atom.

## HTX faila formāts

HTX faili tiek saglabāti kā vienkārša teksta fails ar kodu datu izgūšanai no datu bāzes un saglabāšanai mainīgajos rādītājos.


### HTX faila piemērs

HTX faila piemērs ir šāds, kas definē lapas galveni vaicājuma ierobežojuma parādīšanai un lapā parādītos dokumentus, lai parādītu lietotājam.

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

Šī parauga koda izvade ir šāda.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Kā redzams, HTX fails ir veidne, kas formatē, kā rezultāti tiek atgriezti un parādīti galalietotājiem. Tas ir rakstīts HTML formātā ar dažiem IIS paplašinājumiem un indeksēšanas pakalpojumu. Šie paplašinājumi ietver mainīgo nosaukumus un citus kodus rezultātu apstrādei.

## Atsauces

* [Rezultātu formatēšana .Htx failā](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


