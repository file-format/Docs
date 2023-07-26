{
  "date" : "2021-05-24",
  "keywords" :["zul", "Fil", "Tillägg", "Filformat", "Filtillägg", "öppen"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK användargränssnittsfil",
  "description":"Lär dig om ZUL-filformat och API:er som kan skapa och öppna ZUL-filer.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Vad är ZUL fil?

En fil med filändelsen .zul är en webbfil skapad med User Interface Markup Language (ZUML) och innehåller definitioner för användargränssnittselement. Ajax- och Java-klasser stöder användning av den [XML](/sv/web/xml/)-baserade ZUML för att utveckla serversidefiler. ZUL-filformatet har utvecklats av ZK, ett UI-ramverk som gör att du kan bygga webb- och mobilapplikationer utan kunskap om JavaScript eller AJAX.

## ZUL filformat

ZUL-filer är XML-baserade och består av olika element för att skapa användargränssnitt. ZK-lastaren använder varje XML-element för att skapa en komponent. Den övergripande behandlingen av sidelementen såsom sidtitel, beskrivning etc. beskrivs av varje XML-bearbetningsinstruktion för ZUML.

### ZUL Exempel

I följande exempel på ZUML-kod anger den första raden sidtiteln, den andra raden skapar en rotkomponent med titel och ram, och den tredje raden skapar en knapp med etikett och en händelseavlyssnare.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
ZUL-schemat kan laddas ner från https://www.zkoss.org/2005/zul/zul.xsd.
## Referenser

* [ZUL - Av ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL Schema](https://www.zkoss.org/2005/zul/zul.xsd)

