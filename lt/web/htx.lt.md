{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTX failas – HTML plėtinio failo formatas",
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra HTX failas ir API, kurios gali sukurti ir atidaryti HTX failą.",
  "linktitle": "HTX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-ltx"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra HTX failas?

HTX failas iš tikrųjų yra HTML failas, kuriame yra duomenų kintamieji, skirti duomenų bazės užklausos rezultatams rodyti kaip tinklalapį. Dažniausiai kuriami naudojant Microsoft FrontPage žiniatinklio kūrimo programinę įrangą, HTX failai išsaugomi, kad būtų išsaugoti tame pačiame aplanke kaip ir atitinkamas interneto duomenų bazės jungties (.IDC) failas.

HTX failus galima atidaryti naudojant tokias programas kaip Microsoft FrontPage ir bet kurią teksto rengyklę, pvz., Notepad, TextEdit arba Atom.

## HTX failo formatas

HTX failai išsaugomi kaip paprasto teksto failai su kodu, skirtu duomenims iš duomenų bazės nuskaityti ir išsaugoti kintamuosiuose rodymui.


### HTX failo pavyzdys

Toliau pateikiamas HTX failo pavyzdys, kuriame apibrėžiama puslapio antraštė, skirta užklausos apribojimui ir puslapyje rodomiems dokumentams rodyti vartotojui.

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

Šio pavyzdinio kodo išvestis yra tokia.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Kaip matyti, HTX failas yra šablonas, kuris formatuoja, kaip rezultatai grąžinami ir rodomi galutiniams vartotojams. Jis parašytas HTML formatu su kai kuriais IIS plėtiniais ir indeksavimo paslauga. Šie plėtiniai apima kintamųjų pavadinimus ir kitus rezultatams apdoroti skirtus kodus.

## Nuorodos

* [Rezultatų formatavimas .Htx faile](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)


