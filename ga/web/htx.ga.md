{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad HTX - Formáid Chomhaid Shínte HTML",
  "description": "Do threoir formáid comhaid chun a fháil amach cad is comhad HTX agus APIs ann ar féidir comhad HTX a chruthú agus a oscailt.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad HDX ann?

I ndáiríre is comhad HTML é comhad HTX ina bhfuil athróga sonraí chun torthaí na gceisteanna bunachar sonraí a thaispeáint mar leathanach gréasáin. Cruthaítear den chuid is mó le bogearraí forbartha Gréasáin Microsoft FrontPage, déantar comhaid HTX a shábháil chun iad a shábháil san fhillteán céanna leis an gcomhad Nascóir Bunachar Sonraí Idirlín (.IDC) comhfhreagrach.

Is féidir comhaid HTX a oscailt le feidhmchláir ar nós Microsoft FrontPage agus aon eagarthóir téacs ar nós Notepad, TextEdit, nó Atom.

## Formáid Comhaid HTC

Déantar comhaid HTX a shábháil mar chomhad gnáth-théacs le cód chun sonraí a aisghabháil ó bhunachar sonraí agus a shábháil in athróga le taispeáint.


### Sampla Comhad HTC

Seo a leanas sampla de chomhad HTX a shainíonn ceanntásc leathanaigh chun srianadh na gceisteanna a thaispeáint agus na doiciméid a thaispeánfar ar an leathanach le taispeáint don úsáideoir.

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

Seo a leanas aschur an chóid shamplach seo.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Mar is léir, is teimpléad é an comhad HTX a fhormáidíonn conas a chuirtear torthaí ar ais agus a thaispeántar do na húsáideoirí deiridh. Tá sé scríofa i bhformáid HTML le roinnt síntí IIS agus Seirbhís Innéacsaithe. Áirítear leis na síntí seo ainmneacha athraitheacha agus cóid eile chun torthaí a phróiseáil.

## Tagairtí

* [Formáidiú na dTorthaí i gComhad .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


