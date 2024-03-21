{
  "date" : "2019-10-11",
  "keywords" :["xml", "File", "Extension", "File Format", "File Extension", "extensible markup language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XML fájlformátum",
  "description":"További információ az XML fájlformátumról és az XML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az XML fájl?

Az XML az Extensible Markup Language rövidítése, amely hasonló a **[HTML](/hu/web/html/)**-hoz, de különbözik az objektumok meghatározására szolgáló címkék használatában. Az XML fájlformátum létrehozásának teljes ötlete az volt, hogy az adatokat tárolják és szállítsák anélkül, hogy szoftver- vagy hardvereszközöktől függnének. Népszerűsége annak köszönhető, hogy emberi és géppel is olvasható. Ez lehetővé teszi, hogy közös adatprotokollokat hozzon létre objektumok formájában, amelyeket tárolni és megosztani a hálózaton, például a World Wide Web-en (WWW). Az XML-ben az "X" a bővíthető, ami azt jelenti, hogy a nyelv tetszőleges számú szimbólumra kiterjeszthető a felhasználói igényeknek megfelelően. Sok szabványos fájlformátum ezekhez a szolgáltatásokhoz használja, például a Microsoft Open XML, a LibreOffice OpenDocument, a **[XHTML](/hu/web/xhtml/)** és a **[SVG](/hu/page-description-language/svg/)**.

## XML fájl formátum

Az XML fájlformátum az XML Document Object Model (DOM)-on alapul, amely egy programozási API HTML és XML dokumentumokhoz. Az XML DOM szabványos módszert határoz meg az XML dokumentumelemek eléréséhez és kezeléséhez. Egy XML-dokumentum faszerkezetű nézetét készíti, amely felhasználható az összes elem eléréséhez a DOM-fán keresztül. A meglévő elemek módosíthatók/törölhetők, valamint új elemek hozhatók létre az XML fában. Az XML-dokumentum minden elemét csomópontnak nevezzük. Az XML DOM a következő képen látható.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Az XML univerzális megközelítése

Az XML ereje univerzális nyelvvé teszi a hálózaton keresztüli adatkommunikációhoz azáltal, hogy leegyszerűsíti az adatátvitelt és a platformmódosításokat. Ez az adatok egyszerű szöveges formátumban történő tárolásával is lehetővé teszi az inkompatibilis rendszerek közötti adatcserét. A HTML az adatok webes megjelenítésére szolgál, míg az XML az adatcserére. Az XML-ben használt jelölő címkepárok határozzák meg a struktúra kulcsfontosságú elemeit, amelyeket az alkalmazások olvasásakor kell használni.

## XML példa

Az alábbiakban egy egyszerűsített példa egy CD-katalógusra, ahol minden lemez információt tartalmaz a CD-kről, például előadó, ország, cég, ár és gyártási év.

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

## Hivatkozások

* [XML – a Wikipedia által](https://en.wikipedia.org/wiki/XML)

