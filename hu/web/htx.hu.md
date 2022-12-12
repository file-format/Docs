{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX fájl – HTML kiterjesztés fájlformátum",
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az a HTX fájl és API-k, amelyek HTX fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a HTX fájl?

A HTX-fájl valójában egy HTML-fájl, amely adatváltozókat tartalmaz az adatbázis-lekérdezés eredményeinek weboldalként történő megjelenítéséhez. A legtöbbször a Microsoft FrontPage webfejlesztő szoftverrel létrehozott HTX fájlok ugyanabba a mappába kerülnek mentésre, mint a megfelelő Internet Database Connector (.IDC) fájl.

A HTX fájlok megnyithatók olyan alkalmazásokkal, mint a Microsoft FrontPage, és bármilyen szövegszerkesztővel, mint például a Jegyzettömb, TextEdit vagy Atom.

## HTX fájlformátum

A HTX fájlok egyszerű szöveges fájlként kerülnek mentésre olyan kóddal, amely lehetővé teszi az adatok adatbázisból való lekérését és a változókba való mentést a megjelenítéshez.


### HTX fájl példa

A következő példa a HTX fájlra, amely egy oldalfejlécet határoz meg a lekérdezési korlátozás és az oldalon megjelenített dokumentumok megjelenítéséhez a felhasználó számára.

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

Ennek a mintakódnak a kimenete a következő.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Mint látható, a HTX fájl egy sablon, amely formázza az eredmények visszaadását és megjelenítését a végfelhasználók számára. HTML formátumban íródott, néhány IIS-kiterjesztéssel és indexelő szolgáltatással. Ezek a kiterjesztések változóneveket és egyéb kódokat tartalmaznak az eredmények feldolgozásához.

## Hivatkozások

* [Az eredmények formázása .Htx fájlban](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

