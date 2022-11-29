{
  "date" : "2019-10-11",
  "keywords" :["xml", "Fil", "Tillägg", "Filformat", "Filtillägg", "Utökningsbart märkningsspråk"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML-filformat",
  "description":"Läs mer om XML-filformat och API:er som kan skapa och öppna XML-filer.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en XML-fil?

XML står för Extensible Markup Language som liknar **[HTML](/sv/web/html/)** men skiljer sig från att använda taggar för att definiera objekt. Hela idén bakom skapandet av XML-filformat var att lagra och transportera data utan att vara beroende av mjukvara eller hårdvaruverktyg. Dess popularitet beror på att den är både mänsklig och maskinläsbar. Detta gör det möjligt för den att skapa gemensamma dataprotokoll i form av objekt som ska lagras och delas över nätverk som World Wide Web (WWW). "X" i XML är för extensible vilket innebär att språket kan utökas till valfritt antal symboler enligt användarens krav. Det är för dessa funktioner som många standardfilformat använder det som Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/sv/web/xhtml/)** och **[SVG](/sv/page-description-language /svg/)**.

## XML-filformat

XML-filformatet är baserat på XML Document Object Model (DOM) som är ett programmerings-API för HTML- och XML-dokument. XML DOM definierar en standardmetod för att komma åt och manipulera XML-dokumentelementen. Det gör en trädstrukturvy av ett XML-dokument som kan användas för att komma åt alla element via DOM-trädet. Befintliga element kan ändras/ta bort liksom nya element kan skapas i XML-trädet. Varje element i ett XML-dokument kallas en nod. XML DOM är som visas i följande bild.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Universell metod för XML

Kraften i XML gör det till ett universellt språk för datakommunikation över nätverket genom att göra datatransport och plattformsändringar förenklade. Detta säkerställer också utbyte av data mellan inkompatibla system genom att lagra data i vanlig textformat. HTML är för datarepresentation över webben, medan XML är för utbyte av data. Markup-taggparen som används i XML definierar nyckelelementen i strukturen som ska användas för att läsa applikationer.

## XML-exempel

Följande är ett förenklat exempel på en CD-katalog där varje skiva innehåller information om CD-skivor som artist, land, företag, pris och tillverkningsår.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referenser

* [XML - av Wikipedia](https://en.wikipedia.org/wiki/XML)

