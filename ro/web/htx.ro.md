{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier HTX - Format fișier de extensie HTML",
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier HTX și API-urile care pot crea și deschide fișierul HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier HTX?

Un fișier HTX este de fapt un fișier HTML care conține variabile de date pentru afișarea rezultatelor interogării bazei de date ca pagină web. Create în mare parte cu software-ul de dezvoltare Web Microsoft FrontPage, fișierele HTX sunt salvate pentru a fi salvate în același folder cu fișierul corespunzător Internet Database Connector (.IDC).

Fișierele HTX pot fi deschise cu aplicații precum Microsoft FrontPage și orice editor de text, cum ar fi Notepad, TextEdit sau Atom.

## Format de fișier HTX

Fișierele HTX sunt salvate ca fișier text simplu cu cod pentru preluarea datelor dintr-o bază de date și salvarea în variabile pentru afișare.


### Exemplu de fișier HTX

Un exemplu de fișier HTX este după cum urmează, care definește un antet de pagină pentru afișarea restricției de interogare și documentele afișate pe pagină pentru a fi afișate utilizatorului.

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

Rezultatul acestui exemplu de cod este după cum urmează.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

După cum se poate vedea, fișierul HTX este un șablon care formatează modul în care rezultatele sunt returnate și afișate utilizatorilor finali. Este scris în format HTML cu unele extensii IIS și Serviciul de indexare. Aceste extensii includ nume de variabile și alte coduri pentru procesarea rezultatelor.

## Referințe

* [Formatarea rezultatelor în fișierul .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

