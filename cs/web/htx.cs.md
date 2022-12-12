{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX File - HTML Extension File Format",
  "description" :"Váš průvodce formátem souboru, kde se dozvíte, co je soubor HTX a rozhraní API, která mohou vytvořit a otevřít soubor HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor HTX?

Soubor HTX je ve skutečnosti soubor HTML, který obsahuje datové proměnné pro zobrazení výsledků databázového dotazu jako webové stránky. Soubory HTX, většinou vytvořené pomocí webového vývojového softwaru Microsoft FrontPage, se ukládají do stejné složky jako odpovídající soubor Internet Database Connector (.IDC).

Soubory HTX lze otevřít pomocí aplikací, jako je Microsoft FrontPage a libovolného textového editoru, jako je Poznámkový blok, TextEdit nebo Atom.

## Formát souboru HTX

Soubory HTX se ukládají jako prostý textový soubor s kódem pro načítání dat z databáze a ukládání do proměnných pro zobrazení.


### Příklad souboru HTX

Příklad souboru HTX je následující, který definuje záhlaví stránky pro zobrazení omezení dotazu a dokumenty zobrazené na stránce pro zobrazení uživateli.

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

Výstup tohoto ukázkového kódu je následující.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Jak je vidět, soubor HTX je šablona, která formátuje, jak se výsledky vrací a zobrazují koncovým uživatelům. Je napsán ve formátu HTML s některými rozšířeními IIS a Indexing Service. Tato rozšíření zahrnují názvy proměnných a další kódy pro zpracování výsledků.

## Reference

* [Formátování výsledků v souboru .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

