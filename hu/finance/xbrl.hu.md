{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "xbrl fájl", "xbrl fájlformátum", "xbrl fájltípus", "fájl", "típus", "mi az xbrl fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL – üzleti és pénzügyi jelentési fájlformátum",
  "description":"További információ az XBRL fájlformátumról és az API-król, amelyek XBRL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Mi az XBRL fájl?

Az .xbrl (eXtensible Business Reporting Language) kiterjesztésű fájl egy ingyenesen elérhető és globális keretrendszer az üzleti információk cseréjéhez. Manapság széles körben használják egyik szabványos formátumként, amely a régebbi papíralapú jelentéseket felváltotta hasznosabb és pontosabb digitális nyilvántartásokkal. Az XBRL-fájlok használatával kicserélt adatok főkönyveket, pénzügyi részleteket és mérlegeket tartalmaznak. Támogatja az adatcímkéket, amelyek lehetővé teszik mindenféle üzleti információ adatfeldolgozását az előkészítéstől az elemzési szakaszig. Az XBRL-fájlok olyan szoftverekkel nyithatók meg, mint a Rivet Software Dragon View XBRL Viewer, és olyan API-k segítségével, mint az [Aspose.Finance](https://products.aspose.com/finance/).

## XBRL fájlformátum

Az XBRL a digitális üzleti jelentéskészítés nyílt nemzetközi szabványa, amelyet világszerte széles körben használnak. Ez egy [XML](/hu/web/xml/) alapú nyelv, amely XBRL-elemeket, más néven címkéket használ az egyes üzleti adatok leírására a jelentések rendezéséhez és elemzéséhez szükséges adatok megfogalmazásához. Az XBRL fájlformátum specifikációit az XBRL International, Inc fejlesztette ki és tette közzé, jelenleg az [XBRL 2.1-es verziója](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) a felhasználók számára elérhető.

### XBRL-dokumentumstruktúra

Teljes információ az [XBRL 2.1 címkékről](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata- 2013-02-20.html) a programozók arra hivatkozhatnak, hogy írjanak alkalmazásokat ennek a fájlformátumnak a használatához. Az XBRL egy XBRL-példányból és taxonómiák gyűjteményéből áll.

**`XBRL-példány`** – Az XBRL-példány a következővel kezdődik<xbrl> gyökérelem. Egy nagy XML-dokumentum egynél több XBRL-példányt is tartalmazhat beágyazva.

**`XBRL taxonómia`** – Az [XBRL taxonómia](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31 A +corrected-errata-2013-02-20.html#_5) XML-sémaszerkezetként és közvetlenül hivatkozott külső hivatkozáselemek halmazaként van definiálva. A linkbázis hivatkozásokat bemutató méretezhető taxonómiai séma a következő.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Referenciák ##

* [XBRL – a Wikipedia által](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected- errata-2013-02-20.html)

