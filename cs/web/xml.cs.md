{
  "date" : "2019-10-11",
  "keywords" :["xml", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "rozšiřitelný značkovací jazyk"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru XML",
  "description":"Další informace o formátu souboru XML a rozhraních API, která mohou vytvářet a otevírat soubory XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor XML?

XML je zkratka pro Extensible Markup Language, která je podobná **[HTML](/cs/web/html/)**, ale liší se v používání značek pro definování objektů. Celá myšlenka za vytvořením formátu souboru XML byla ukládat a přenášet data bez závislosti na softwarových nebo hardwarových nástrojích. Jeho popularita je způsobena tím, že je čitelný člověkem i strojově. To umožňuje vytvářet společné datové protokoly ve formě objektů, které mají být uloženy a sdíleny po síti, jako je World Wide Web (WWW). "X" v XML je pro rozšiřitelnost, což znamená, že jazyk lze rozšířit na libovolný počet symbolů podle požadavků uživatele. Právě pro tyto funkce jej využívá mnoho standardních formátů souborů, jako je Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/cs/web/xhtml/)** a **[SVG](/cs/page-description-language /svg/)**.

## Formát souboru XML

Formát souboru XML je založen na XML Document Object Model (DOM), což je programovací API pro HTML a XML dokumenty. XML DOM definuje standardní metodu pro přístup a manipulaci s prvky dokumentu XML. Vytváří stromový pohled na dokument XML, který lze použít pro přístup ke všem prvkům prostřednictvím stromu DOM. Existující prvky lze upravovat/mazat, stejně jako vytvářet nové prvky ve stromu XML. Každý prvek dokumentu XML se nazývá uzel. XML DOM je znázorněn na následujícím obrázku.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Univerzální přístup k XML

Síla XML z něj dělá univerzální jazyk pro datovou komunikaci po síti tím, že zjednodušuje přenos dat a změny platformy. To také zajišťuje možnost výměny dat mezi nekompatibilními systémy ukládáním dat ve formátu prostého textu. HTML je pro reprezentaci dat na webu, zatímco XML je pro výměnu dat. Páry značek značek používané uvnitř XML definují klíčové prvky struktury, které mají být využívány aplikacemi pro čtení.

## Příklad XML

Následuje zjednodušený příklad katalogu CD, kde každý záznam obsahuje informace o CD, jako je interpret, země, společnost, cena a rok výroby.

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

## Reference

* [XML – z Wikipedie](https://en.wikipedia.org/wiki/XML)

